# Code

```html {*}{maxHeight:'400px'}
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <title>Dashboard de Monitoreo - Pozo #12</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.2/dist/chart.umd.min.js"></script>
</head>

<body class="bg-light">

    <nav class="navbar navbar-dark bg-dark">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">
                ⚙️ Monitor de Producción | Pozo CA-12
            </a>
        </div>
    </nav>

    <div class="container mt-4">

        <h3 class="mb-4">Indicadores Clave de Desempeño (KPIs)</h3>

        <div class="row">
            <div class="col-4">
                <div class="card bg-success text-white mb-3">
                    <div class="card-body">
                        <div class="h5">Producción Actual (BPD)</div>
                        <div class="display-4">2,850</div>
                        <small>Objetivo: 3,000 BPD</small>
                    </div>
                </div>
            </div>
            <div class="col-4">
                <div class="card bg-warning text-dark mb-3">
                    <div class="card-body">
                        <div class="h5">Corte de Agua (%)</div>
                        <div class="display-4">34%</div>
                        <small>Tendencia: Aumento moderado</small>
                    </div>
                </div>
            </div>
            <div class="col-4">
                <div class="card bg-danger text-white mb-3">
                    <div class="card-body">
                        <div class="h5">Presión Cabezal (PSI)</div>
                        <div class="display-4">1,250</div>
                        <small>Alerta Baja: 1,200 PSI</small>
                    </div>
                </div>
            </div>
        </div>

        <hr>

        <h3 class="mt-4 mb-3">Histórico de Variables Clave (Últimos 7 Días)</h3>

        <div class="row">

            <div class="col-4">
                <div class="card mb-3">
                    <div class="card-header bg-success text-white">
                        1. Producción de Crudo (BPD)
                    </div>
                    <div class="card-body">
                        <canvas id="produccionChart"></canvas>
                    </div>
                </div>
            </div>

            <div class="col-4">
                <div class="card mb-3">
                    <div class="card-header bg-warning text-dark">
                        2. Corte de Agua (%)
                    </div>
                    <div class="card-body">
                        <canvas id="waterCutChart"></canvas>
                    </div>
                </div>
            </div>

            <div class="col-4">
                <div class="card mb-3">
                    <div class="card-header bg-danger text-white">
                        3. Presión de Fondo (BHP - PSI)
                    </div>
                    <div class="card-body">
                        <canvas id="bhpChart"></canvas>
                    </div>
                </div>
            </div>

        </div>
        <div class="row">
            <div class="col-12">
                <h3 class="mt-4 mb-3">Alertas Operacionales</h3>
                <div class="card">
                    <div class="card-header">
                        Alertas y Novedades del Sistema
                    </div>
                    <ul class="list-group list-group-flush">
                        <li class="list-group-item text-danger">⚠️ ALERTA CRÍTICA: Presión Cabezal acercándose al límite
                            (1,250 PSI). Revisar válvula V-03.</li>
                        <li class="list-group-item text-danger">⚠️ AVISO: El Corte de Agua aumentó 2% en las últimas 24
                            horas. Monitoreo en curso.</li>
                        <li class="list-group-item">🟢 ESTADO: Bomba de fondo operando al 85%.</li>
                        <li class="list-group-item">🗓️ MANTENIMIENTO: Próxima inspección de válvulas: Mañana 8:00 AM.
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <script>
        const dias = ['Día -6', 'Día -5', 'Día -4', 'Día -3', 'Día -2', 'Ayer', 'Hoy'];

        // DATOS 1: Producción de Crudo
        const datosProduccion = [2950, 3010, 3000, 2900, 2800, 2870, 2850];
        new Chart(document.getElementById('produccionChart'), {
            type: 'line',
            data: {
                labels: dias,
                datasets: [{
                    label: 'Barriles (BPD)',
                    data: datosProduccion,
                    borderColor: 'rgba(25, 135, 84, 1)',
                    borderWidth: 2,
                    tension: 0.4,
                    fill: false
                }]
            }
        });

        // DATOS 2: Corte de Agua (Water Cut)
        const datosWaterCut = [30, 30, 31, 32, 33, 33, 34]; // Valores en porcentaje
        new Chart(document.getElementById('waterCutChart'), {
            type: 'line',
            data: {
                labels: dias,
                datasets: [{
                    label: 'Water Cut (%)',
                    data: datosWaterCut,
                    borderColor: 'rgba(255, 193, 7, 1)', // Color amarillo de Bootstrap
                    backgroundColor: 'rgba(255, 193, 7, 0.2)',
                    borderWidth: 2,
                    tension: 0.4,
                    fill: true
                }]
            }
        });

        // DATOS 3: Presión de Fondo (BHP)
        const datosBHP = [3500, 3450, 3400, 3350, 3300, 3250, 3200]; // Valores en PSI
        new Chart(document.getElementById('bhpChart'), {
            type: 'bar', // Usamos barras para variar
            data: {
                labels: dias,
                datasets: [{
                    label: 'Presión de Fondo (PSI)',
                    data: datosBHP,
                    backgroundColor: 'rgba(220, 53, 69, 0.8)', // Color rojo de Bootstrap
                    borderColor: 'rgba(220, 53, 69, 1)',
                    borderWidth: 1
                }]
            }
        });
    </script>

</body>

</html>
```