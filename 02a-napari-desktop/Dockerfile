FROM 01-jupyter-desktop:latest

USER root
WORKDIR /

# create a conda env called napari and install napari with pip
RUN source /opt/conda/etc/profile.d/conda.sh \
  && conda create --yes --name napari python=3.9 \
  &&  conda run --name napari python -m pip install napari[all] 


# CUSTOMIZATIONS

## replace desktop background
# Image credit
# By NASA - http://eol.jsc.nasa.gov/scripts/sseop/photo.pl?mission=ISS014&amp;roll=E&amp;frame=5365, 
# cropped, Public Domain, https://commons.wikimedia.org/w/index.php?curid=3070187
COPY ./background.png /usr/share/backgrounds/xfce/xfce-stripes.png
RUN chmod a+r /usr/share/backgrounds/xfce/xfce-stripes.png

## add menu shortcut
COPY ./Napari.desktop /usr/share/applications/Napari.desktop


WORKDIR /src/jupyterhub
USER $NB_UID
