
Docker provides several commands for managing and working with networks. Here is a list of key commands related to Docker networking:

1. `docker network ls`  
   - Description: Lists all Docker networks.
   - Example:  
     ```
     docker network ls
     ```

2. `docker network inspect <network>`  
   - Description: Provides detailed information about a specific Docker network.
   - Example:  
     ```
     docker network inspect bridge
     ```

3. `docker network create <network_name>`  
   - Description: Creates a new Docker network.
   - Example:  
     ```
     docker network create my_network
     ```

4. `docker network rm <network_name>`  
   - Description: Removes one or more Docker networks.
   - Example:  
     ```
     docker network rm my_network
     ```

5. `docker network connect <network_name> <container_name_or_id>`  
   - Description: Connects a container to a network.
   - Example:  
     ```
     docker network connect my_network my_container
     ```

6. `docker network disconnect <network_name> <container_name_or_id>`  
   - Description: Disconnects a container from a network.
   - Example:  
     ```
     docker network disconnect my_network my_container
     ```

7. `docker network prune`  
   - Description: Removes all unused networks.
   - Example:  
     ```
     docker network prune
     ```

8. `docker network inspect <network_name> --format`  
   - Description: Use the `--format` flag to get a specific field from the network's details in a more concise output format (e.g., JSON).
   - Example:  
     ```
     docker network inspect my_network --format '{{.Id}}'
     ```

9. `docker network create --driver <driver_name> <network_name>`  
   - Description: Create a network with a specific driver (e.g., `bridge`, `host`, `overlay`).
   - Example:  
     ```
     docker network create --driver bridge my_bridge_network
     ```

10. `docker network create --subnet <subnet>`  
   - Description: Create a network with a specific subnet.
   - Example:  
     ```
     docker network create --subnet=192.168.1.0/24 my_network_with_subnet
     ```

11. `docker network create --gateway <gateway>`  
   - Description: Create a network with a specific gateway.
   - Example:  
     ```
     docker network create --gateway=192.168.1.1 my_network_with_gateway
     ```

12. `docker network create --ipv6`  
   - Description: Create a network that supports IPv6.
   - Example:  
     ```
     docker network create --ipv6 my_network_ipv6
     ```

13. `docker network ls --filter <key>=<value>`  
   - Description: Lists Docker networks with optional filters (e.g., by driver or name).
   - Example:  
     ```
     docker network ls --filter driver=bridge
     ```

These commands are essential for managing network configurations in Docker environments.
