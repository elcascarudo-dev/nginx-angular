# Nginx-Angular

La siguiente imagen permite ejecutar proyectos Angular en producción permitiendo acceder a las rutas deforma directa.

#### Dockerfile - Proyecto Angular

```dockerfile
FROM elcascarudodev/nginx-angular

COPY  {./dist} /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]
```
### docker-compose
```docker-compose
version: '3.1'

service:

	frontend:
		build: .
		restart: always
		ports:
			- 4200:80
```
