# Mis_componente_ha

![Icono del catálogo](icon.png)

Catálogo público de integraciones de Home Assistant Core para **Private Git Manager**.
No ejecuta los servidores de Headscale Gateway o PiVigia. Contiene varias
integraciones; para HACS/Marketplace utiliza sus repositorios individuales.

| Integración | Guía y archivos | Repositorio individual |
| --- | --- | --- |
| Headscale Gateway | [Componente](custom_components/headscale_gateway/) | [headscale_gateway_ha](https://github.com/Gente-del-Condado/headscale_gateway_ha) |
| PiVigia | [Componente](custom_components/pivigia/) | [pivigia_ha](https://github.com/Gente-del-Condado/pivigia_ha) |
| JackSignal | [Componente](custom_components/jacksignal/) | [jacksignal_ha](https://github.com/Gente-del-Condado/jacksignal_ha) |
| Private Git Manager · Forgejo Backup | [Componente](custom_components/pgm_forgejo_backup/) | [Fuentes y guía](https://github.com/Gente-del-Condado/HA-Private-Git-Manager/blob/main/FORGEJO_BACKUPS.md) |

## Instalar o actualizar

1. Añade este repositorio de GitHub en Private Git Manager y sincroniza `main`.
2. En **Componentes**, selecciona la integración, revisa el commit e instala o actualiza.
3. Reinicia Home Assistant Core cuando lo solicite. Añade la integración desde **Dispositivos y servicios**.

Elige una sola vía de actualización por integración. Forgejo Backup necesita un
repositorio privado propio para guardar sus copias cifradas: ese destino es
independiente de este catálogo público. Consulta la
[guía de copias](https://gente-del-condado.github.io/HA-Private-Git-Manager/#copias-forgejo).
Las aplicaciones del Supervisor se distribuyen en
[Mis_app_ha](https://github.com/Gente-del-Condado/Mis_app_ha).

## Origen y publicación

Cada proyecto se mantiene primero en Forgejo, se replica a GitHub y publica
solo su carpeta en este catálogo mediante GitHub Actions. No existe un derivado
de esta tienda en Forgejo y los publicadores no escriben en ese servidor.

| Proyecto | Origen Forgejo | Espejo GitHub | Carpeta publicada |
| --- | --- | --- | --- |
| Headscale Gateway | [Forgejo](https://gentedelcondado.es/forgejo/wolfbelmi88/headscale_gateway) | [GitHub](https://github.com/Gente-del-Condado/headscale_gateway) | `custom_components/headscale_gateway/` |
| PiVigia | [Forgejo](https://gentedelcondado.es/forgejo/wolfbelmi88/pivigia) | [GitHub](https://github.com/Gente-del-Condado/pivigia) | `custom_components/pivigia/` |
| JackSignal | [Forgejo](https://gentedelcondado.es/forgejo/wolfbelmi88/jacksignal) | [GitHub](https://github.com/Gente-del-Condado/jacksignal) | `custom_components/jacksignal/` |
| Private Git Manager | [Forgejo](https://gentedelcondado.es/forgejo/wolfbelmi88/HA-Private-Git-Manager) | [GitHub](https://github.com/Gente-del-Condado/HA-Private-Git-Manager) | `custom_components/pgm_forgejo_backup/` |

Headscale Gateway, PiVigia y JackSignal publican después de superar sus flujos
de calidad en el `main` vigente de GitHub. Private Git Manager tiene publicadores
propios por cambios en `main`. Los principales de los tres primeros son privados;
la distribución instalable es pública. Los commits de publicación identifican
la revisión de origen. Cada publicador conserva los demás proyectos.

No edites las carpetas generadas: corrige la fuente en el principal de Forgejo.
La publicación no instala automáticamente las actualizaciones en los equipos.
