# Spring4Shell Vulnerable Container Application
This is a dockerized application that is vulnerable to the Spring4Shell vulnerability (CVE-2022-22965). This container application is strictly for testing purpose only, not to be used for production application. 

# Requirement
1. Docker
2. Python with required library

# Instructions
1. Clone this repository
2. Build and run the container
   ```
   docker build . -t spring4shell && docker run -p 8080:8080 spring4shell
   ```
3. Application should be running on the host, and accessible via (http://localhost:8080/helloworld/greeting)[http://localhost:8080/helloworld/greeting]
4. To exploit the application ```python exploit.py --url "http://localhost:8080/helloworld/greeting"```
5. Visit the created webshell! Modify the cmd GET parameter for your commands. (http://localhost:8080/shell.jsp by default)
   ```
   http://localhost:8080/shell.jsp?cmd
   ```
