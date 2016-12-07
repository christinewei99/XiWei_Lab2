import folium
import pandas as pd

PHILLY_COORDINATES = (39.9816, -75.1495)
crimedata = pd.read_csv(r'C:\Data\incident.csv')

#for speed purpose
MAX_RECORDS = 250

#create empty map zoomed in on Temple University 
map = folium.Map(location = PHILLY_COORDINATES, zoom_start = 12)

#add a marker for every record in the filtered data, use a clustered view
for each in crimedata[0:MAX_RECORDS].iterrows():
    map.simple_marker(
        location = [each[1]['Y'], each[1]['X']],
        clustered_marker = True)
        
map.create_map(path='Crimemap1.html')

#create a choropleth map using Folium

#definition of the boundaries in the map
district_geo = r'C:\Data\Boundaries_Division.geojson'

#calculating total number of incidents per district
crimedata2 = pd.DataFrame(crimedata['DC_DIST'].value_counts().astype(float))  
crimedata2.to_json('crimeagg.json')  
crimedata2 = crimedata2.reset_index()  
crimedata2.columns = ['District', 'Number']

#creation of the choropleth
cm= folium.Map(location=PHILLY_COORDINATES, zoom_start=12)  
cm.geo_json(geo_path = district_geo,  
              data_out = 'crimeagg.json', 
              data = crimedata2,
              columns = ['District', 'Number'],
              key_on = 'feature.properties.District',
              fill_color = 'YlOrRd', 
              fill_opacity = 0.7, 
              line_opacity = 0.2,
              legend_name = 'Number of incidents per district')

cm.create_map(path='cm.html')
