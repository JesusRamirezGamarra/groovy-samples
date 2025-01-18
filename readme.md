https://github.com/jenkinsci/docker-agent/blob/master/README_inbound-agent.md
SECRET agente-1 : bca46ae60080ef32a3ab8a5d29682210b038ed22fac27101d2bbad7cac9b31ba 

docker run --network jenkins_default --init jenkins/inbound-agent -url http://172.18.0.2:8080/ -secret bca46ae60080ef32a3ab8a5d29682210b038ed22fac27101d2bbad7cac9b31ba -name agente-1

docker network inspect
docker network inspect jenkins_default
[
    {
        "Name": "jenkins_default",
        "Id": "cbecb596284f590a42b7719ef183e650bad10d4cac9ad3570e10c61b8a4aa786",
        "Created": "2025-01-08T02:23:55.35852814Z",
        "Scope": "local",
        "Driver": "bridge",
        "EnableIPv6": false,
        "IPAM": {
            "Driver": "default",
            "Options": null,
            "Config": [
                {
                    "Subnet": "172.18.0.0/16",
                    "Gateway": "172.18.0.1"
                }
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Containers": {
            "8ebdc50643449421c3bceb2ef50fc80daa10d18059493bb2855a33c6fa973930": {
                "Name": "jenkins-jenkins-1",
                "EndpointID": "933974b142ae8b758980c317f5fd53cdc17213b1a464157d3ee70ef501a9feb8",
                "MacAddress": "02:42:ac:12:00:02",
                "IPv4Address": "172.18.0.2/16",
                "IPv6Address": ""
            }
        },
        "Options": {},
        "Labels": {
            "com.docker.compose.network": "default",
            "com.docker.compose.project": "jenkins",
            "com.docker.compose.version": "2.29.2"
        }
    }
]