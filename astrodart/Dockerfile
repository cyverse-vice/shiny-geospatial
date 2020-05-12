FROM cyversevice/shiny-geospatial:latest

RUN R -e "install.packages(c('rgl','leaflet','leaflet.extras','shinythemes','shinyWidgets','shinyBS','shinyjs','sf','geosphere','jsonlite', 'dplyr', 'DT', 'crul'))"

RUN cd /srv/shiny-server && git clone https://github.com/archidart/astrodart

# change permission of the shiny folder where the app resides
RUN chmod -R 777 /srv/shiny-server

WORKDIR /srv/shiny-server/astrodart/

# Start the server
CMD ["/usr/bin/shiny-server.sh"]
