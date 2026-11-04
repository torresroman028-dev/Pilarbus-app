# PilarBus - App de Gestión de Transporte

Repositorio oficial para el desarrollo y despliegue de la plataforma PilarBus.

## Control de versiones y CI/CD en GitHub

- **Pull Requests:** nadie sube código directo a main. Cada cambio se desarrolla en una rama, se abre un Pull Request y otro integrante lo revisa (code review) antes de fusionarlo.
- **Integración Continua (CI):** en cada Pull Request, GitHub Actions ejecuta automáticamente el Build y los Test. Si alguno falla, el PR queda bloqueado.
- **Entrega/Despliegue Continuo (CD):** al fusionar a main, un tercer paso Deploy publica la nueva versión en la nube mediante una estrategia sin interrupción del servicio (blue-green / rolling), de modo que los pasajeros no pierden la app durante la actualización.
- **Resultado:** el código que llega a producción siempre pasó revisión, compilación y pruebas, lo que reduce errores y permite desplegar varias veces por semana con bajo riesgo.
