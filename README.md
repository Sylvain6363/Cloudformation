# Cloudformation Infrastructure Web et Intranet via VPN

## Description

Créer une infrastructure sur le Cloud d'AWS
Cette infrastructure comprendra :
     la partie web hautement disponible, disposant d'un elastic load balancer, de 2 instances ec2 incluant docker et wordpress, et d'une instance RDS multiAZ
     la seconde partie, un réseau privé contenant un intranet et une passerelle VPN accessible uniquement depuis un site local via un serveur VPN

![image](https://github.com/Sylvain6363/Cloudformation/blob/main/Infrastructurecloud.png)

### Prerequis

Avoir un compte AWS

## Installation

- Créer un serveur VPN local avec la solution OpenVPN d'installée, et y insérer le fichier server.conf dans le répertoire /etc/openvpn/server/
- Créer sur le serveur VPN, une liste de révocation, le certificat d'autorité, la clé tls-crypt, la clé publique, la clé privée, la clé diffie-hellman et la clé secrète du serveur
- Remplacer les clés de la configuration client dans la stack"4_Template_Systeme.yaml" avec les votres
- Insérer les 4 stacks, l'un après l'autre depuis Cloudformation sur AWS


## Auteur

* **Sylvain VIGIER** - [Sylvain6363](https://github.com/Sylvain6363)

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/Sylvain6363/Cloudformation/LICENSE) file for details

