# SLOBODA-01

## Infrastructure technique du serveur

### Prérequis

- [ ] Installer Docker
- [ ] Installer Docker-compose
- [ ] Installer Git
- [ ] Cloner le projet
- [ ] Ajouter le fichier .env

### Installation

1. Cloner le projet

```bash
git clone git@github.com:SlobodaFR/sloboda-01.git
```

2. Ajouter le fichier .env

```bash
echo "MYSQL_ROOT_PASSWORD=foobar" > .env
echo "MYSQL_DATABASE=foobar" >> .env
echo "MYSQL_PASSWORD=foobar" > .env
echo "POSTGRES_PASSWORD=foobar" > .env
echo "HIVE_PASSWORD=foobar" > .env
echo "SANDBOX_PASSWORD=foobar" > .env
```

3. Lancer les conteneurs

```bash
docker-compose up -d
```

4. Arrêter les conteneurs

```bash
docker-compose down
```

5. Supprimer les conteneurs

```bash
docker-compose down -v
```

6. Supprimer les images

```bash
docker rmi $(docker images -q)
```

7. Supprimer les volumes

```bash
docker volume rm $(docker volume ls -q)
```

8. Supprimer les réseaux

```bash
docker network rm $(docker network ls -q)
```

9. Supprimer les conteneurs, les images, les volumes et les réseaux

```bash
docker system prune -a
```

10. Se connecter à un conteneur

```bash
docker exec -it <container_name> bash
```
