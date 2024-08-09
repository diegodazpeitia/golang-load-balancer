# Golang Load Balancer

## Overview

This project implements a load balancer in Go (Golang). A load balancer is a crucial component for distributing network traffic across multiple servers, thereby enhancing the reliability and scalability of modern applications.

This project demonstrates a basic load balancer written in Go, which supports flexible traffic distribution strategies and configuration options.

## Configuration

The load balancer’s behavior is controlled through a configuration file named `config.yaml`. Below is an example of the configuration file format:

```yaml
# Port on which the load balancer will listen
lb_port: 3333

# Maximum number of retries for a backend server
retry_limit: 3

# List of backend servers
backends:
  - "http://localhost:100"
  - "http://localhost:101"
```

## Supported Load Balancing Strategies

The load balancer supports two key traffic distribution strategies:

1. **Round Robin:** Distributes incoming traffic evenly across all available servers.
2. **Least Connections:** Directs traffic to the server with the fewest active connections.

You can specify the desired load balancing strategy in the configuration file:

```yaml
# Port on which the load balancer will listen
lb_port: 3333

# Load Balancing strategy (defaults to round-robin)
strategy: least-connections

# Maximum number of retries for a backend server
retry_limit: 3

# List of backend servers
backends:
  - "http://localhost:100"
  - "http://localhost:101"
```

## Getting Started

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/diegodazpeitia/golang-load-balancer.git
   ```

2. **Navigate to the Project Directory:**

   ```bash
   cd golang-load-balancer
   ```

3. **Build the Project:**

   ```bash
   go build -o loadbalancer
   ```

4. **Run the Load Balancer:**

   ```bash
   ./loadbalancer
   ```

5. **Configure the Load Balancer:**

   Edit the `config.yaml` file to set the desired port, retry limits, backend servers, and load balancing strategy.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributions

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.
