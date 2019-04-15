# EdgeAuto-datastream
#### By Mitchell Parker

## Objective 
  The datastream handles the data collection from the carloop connected to the vehicle, all the way to the node. This will handle the direction of the output for the carloop to a specific node based on the carloop's GPS position. 

## Design Scheme
  The carloop performs a handshake with the mapping node with a TCP/IP connection. Once the mapping node receives the request, it creates a unique ID for the carloop and its current session. The carloop receives this information, then process to wait for the GPS module to begin data collection. After the GPS data has been ascertained, it is sent to the mapping server for evaluation. The mapping node will send back the IP address of the node the carloop should stream to. The connection is then ended and the carloop begins streaming data. 
  
  The regular nodes will receive data in the form of "arb_id,message,latitude,longitude,cantime,session_id;". This data will be picked up from the socket and will typically contain more than one message. The ";" delimiter will denote an entry message sent to the node, whereas the delimiter "," denotes the different values of a message. All of this is then stored into the mySQL database.
  
## Configuration
  The carloop should be preprogrammed to connect to the mapping node. On the node that will be hosting the mapping functionality, run `php mapping.php`.
  
## License

There is none. If for some unlikely reason you want to use anything here, you can do so without my permission. I grant thee the privilege.
