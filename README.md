# minecraft-bedrock

## Fork of nguyer/bedrock-server

1. Clone
  
2. Build  
     `docker build -t minecraft_bedrock .`
  
3. Create container  
     ` docker run -d --name=minecraft_bedrock -v '/volume1/docker/_config/minecraft/worlds:/bedrock-server/worlds' -v '/volume1/docker/_config/minecraft/server.properties:/bedrock-server/server.properties' -v '/volume1/docker/_config/minecraft/whitelist.json:/bedrock-server/whitelist.json' -v '/volume1/docker/_config/minecraft/permissions.json:/bedrock-server/permissions.json' --network host --restart=always minecraft_bedrock`  
       
     1. Replace source paths with your local server locations
     2. I use `Permissions` and `Whitelist`, but they are optional.
  
4. Start  
  `docker start minecraft_bedrock`