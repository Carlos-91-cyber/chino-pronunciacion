<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sesión de Pronunciación - Chino Mandarín: Pinyin y Tonos</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 50px rgba(0,0,0,0.3);
        }

        /* PORTADA */
        .portada {
            background: linear-gradient(135deg, #d4145a 0%, #fbb034 100%);
            color: white;
            padding: 80px 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .portada::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 400px;
            height: 400px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
        }

        .portada h1 {
            font-size: 3em;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .portada h2 {
            font-size: 1.5em;
            margin-bottom: 40px;
            position: relative;
            z-index: 1;
            font-weight: 300;
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            position: relative;
            z-index: 1;
            margin-top: 30px;
        }

        .badge {
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255,255,255,0.3);
            padding: 12px 20px;
            border-radius: 25px;
            font-weight: 600;
            font-size: 0.95em;
            transition: all 0.3s ease;
        }

        .badge:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-3px);
        }

        /* NAVEGACIÓN */
        .nav {
            background: #f8f9fa;
            padding: 20px 40px;
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            border-bottom: 2px solid #e0e0e0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav a {
            color: #667eea;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
            cursor: pointer;
        }

        .nav a:hover {
            color: #d4145a;
        }

        /* CONTENIDO PRINCIPAL */
        .contenido {
            padding: 60px 40px;
        }

        .seccion {
            margin-bottom: 60px;
        }

        .seccion h2 {
            color: #d4145a;
            font-size: 2em;
            margin-bottom: 30px;
            border-left: 5px solid #fbb034;
            padding-left: 15px;
        }

        /* PLAN DE ESTUDIO */
        .plan-estudio {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin: 30px 0;
        }

        .dia {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .dia:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
        }

        .dia-numero {
            font-size: 1.8em;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .dia-tema {
            font-size: 0.9em;
            opacity: 0.9;
        }

        /* ACTIVIDADES */
        .actividades-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 30px 0;
        }

        .actividad {
            border-radius: 15px;
            padding: 30px;
            color: white;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .actividad:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
        }

        .a1 {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }

        .a2 {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        }

        .a3 {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        }

        .a4 {
            background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
        }

        .a5 {
            background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
        }

        .actividad h3 {
            font-size: 1.5em;
            margin-bottom: 15px;
        }

        .actividad p {
            font-size: 0.95em;
            line-height: 1.6;
            opacity: 0.95;
        }

        /* TABLAS */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        thead {
            background: #667eea;
            color: white;
        }

        th, td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }

        tbody tr:hover {
            background: #f5f5f5;
        }

        tbody tr:last-child td {
            border-bottom: none;
        }

        /* PAIR CARDS */
        .pair-card {
            background: white;
            border: 2px solid #667eea;
            border-radius: 10px;
            padding: 20px;
            margin: 15px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .pair-item {
            text-align: center;
            flex: 1;
        }

        .pinyin {
            font-size: 1.5em;
            font-weight: bold;
            color: #d4145a;
            font-family: 'Courier New', monospace;
        }

        .significado {
            font-size: 0.9em;
            color: #666;
            margin-top: 5px;
        }

        .pair-separator {
            color: #667eea;
            font-weight: bold;
            font-size: 1.5em;
            margin: 0 20px;
        }

        /* TONOS */
        .tonos-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .tono-card {
            background: white;
            border: 3px solid #667eea;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .tono-card:hover {
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.2);
        }

        .tono-numero {
            font-size: 2em;
            font-weight: bold;
            color: #d4145a;
            margin-bottom: 10px;
        }

        .tono-nombre {
            font-weight: 600;
            color: #667eea;
            margin-bottom: 10px;
        }

        .tono-grafico {
            font-size: 3em;
            margin: 15px 0;
            font-weight: bold;
        }

        .tono-descripcion {
            font-size: 0.85em;
            color: #666;
            line-height: 1.6;
        }

        /* EJERCICIO INTERACTIVO */
        .ejercicio {
            background: #f8f9fa;
            border: 2px solid #667eea;
            border-radius: 10px;
            padding: 30px;
            margin: 20px 0;
        }

        .ejercicio h4 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.1em;
        }

        .opciones {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 10px;
            margin: 15px 0;
        }

        .opcion {
            background: white;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
        }

        .opcion:hover {
            border-color: #667eea;
            background: #f0f4ff;
        }

        .opcion.correcto {
            background: #d4edda;
            border-color: #28a745;
            color: #155724;
        }

        .opcion.incorrecto {
            background: #f8d7da;
            border-color: #f5576c;
            color: #721c24;
        }

        /* ANSWER BOX */
        .answer-box {
            background: #e8f5e9;
            border-left: 5px solid #4caf50;
            border-radius: 5px;
            padding: 20px;
            margin: 20px 0;
            display: none;
        }

        .answer-box.show {
            display: block;
        }

        .answer-box h5 {
            color: #2e7d32;
            margin-bottom: 10px;
        }

        .answer-box p {
            color: #1b5e20;
            line-height: 1.7;
        }

        /* TRABAJO EN LABORATORIO */
        .laboratorio {
            background: white;
            border: 2px dashed #667eea;
            border-radius: 10px;
            padding: 30px;
            margin: 20px 0;
        }

        .laboratorio h4 {
            color: #667eea;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .laboratorio h4::before {
            content: '🎧';
            font-size: 1.3em;
        }

        /* SOLUCIONARIO */
        .solucionario {
            background: #fef3c7;
            border: 2px solid #f59e0b;
            border-radius: 10px;
            padding: 30px;
            margin: 30px 0;
        }

        .solucionario h3 {
            color: #d97706;
            margin-bottom: 20px;
        }

        .solucion-item {
            background: white;
            padding: 15px;
            margin: 10px 0;
            border-radius: 8px;
            border-left: 4px solid #f59e0b;
        }

        .solucion-item strong {
            color: #667eea;
        }

        /* REFERENCIAS */
        .referencias {
            background: #f3e5f5;
            border: 2px solid #9c27b0;
            border-radius: 10px;
            padding: 30px;
            margin: 30px 0;
        }

        .referencias h3 {
            color: #7b1fa2;
            margin-bottom: 20px;
        }

        .ref-categoria {
            margin-bottom: 25px;
        }

        .ref-categoria h4 {
            color: #9c27b0;
            margin-bottom: 10px;
            font-size: 1.1em;
        }

        .ref-item {
            background: white;
            padding: 12px 15px;
            margin: 8px 0;
            border-radius: 6px;
            border-left: 3px solid #9c27b0;
        }

        .ref-item strong {
            color: #667eea;
        }

        /* CONSEJO */
        .consejo {
            background: #cce5ff;
            border-left: 4px solid #667eea;
            border-radius: 5px;
            padding: 15px;
            margin: 15px 0;
        }

        .consejo::before {
            content: '💡 ';
            margin-right: 5px;
        }

        /* FOOTER */
        .footer {
            background: #2c3e50;
            color: white;
            padding: 40px;
            text-align: center;
            border-top: 3px solid #667eea;
        }

        .footer p {
            margin: 10px 0;
            line-height: 1.8;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            .portada h1 {
                font-size: 2em;
            }

            .portada h2 {
                font-size: 1.1em;
            }

            .contenido {
                padding: 40px 20px;
            }

            .nav {
                padding: 15px 20px;
                gap: 15px;
            }

            .seccion h2 {
                font-size: 1.5em;
            }

            .actividades-grid {
                grid-template-columns: 1fr;
            }

            .plan-estudio {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* ANIMACIÓN */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .actividad, .ejercicio, .solucion-item {
            animation: fadeIn 0.6s ease-out;
        }

    </style>
</head>
<body>
    <div class="container">
        <!-- PORTADA -->
        <div class="portada">
            <h1>🎯 Sesión de Pronunciación</h1>
            <h2>Chino Mandarín: Pinyin y Tonos</h2>
            <p style="font-size: 1.1em; margin-top: 20px;">Fonética y Fonología I</p>
            <div class="badges">
                <div class="badge">📚 New Practical Chinese Reader</div>
                <div class="badge">📗 HSK Standard Course</div>
                <div class="badge">🌳 El Chino para Hispanohablantes</div>
                <div class="badge">🎧 Laboratorio Fonético</div>
            </div>
        </div>

        <!-- NAVEGACIÓN -->
        <div class="nav">
            <a href="#plan">📅 Plan Semanal</a>
            <a href="#actividades">🎯 Actividades</a>
            <a href="#solucionario">✓ Solucionario</a>
            <a href="#referencias">📖 Referencias</a>
        </div>

        <!-- CONTENIDO PRINCIPAL -->
        <div class="contenido">

            <!-- INTRODUCCIÓN -->
            <div class="seccion">
                <h2>Introducción a la Fonética del Chino Mandarín</h2>
                <p>El sistema fonético del chino mandarín presenta desafíos únicos para los hablantes de español. Esta sesión te guiará a través de los fundamentos del Pinyin, las iniciales, las finales y los cuatro tonos que caracterizan el idioma.</p>
                <div class="consejo">
                    <strong>Objetivo de esta sesión:</strong> Desarrollar una pronunciación clara y precisa del chino mandarín, enfatizando los sonidos que más desafíos presentan para hispanohablantes.
                </div>
            </div>

            <!-- PLAN DE ESTUDIO SEMANAL -->
            <div class="seccion" id="plan">
                <h2>📅 Plan de Estudio Semanal</h2>
                <p>Dedica aproximadamente 45-60 minutos diarios para obtener los mejores resultados. Sigue este plan progresivo:</p>
                
                <div class="plan-estudio">
                    <div class="dia">
                        <div class="dia-numero">Día 1</div>
                        <div class="dia-tema">Iniciales Aspiradas</div>
                        <p style="font-size: 0.85em; margin-top: 10px;">p, t, k, ch, q</p>
                    </div>
                    <div class="dia">
                        <div class="dia-numero">Día 2</div>
                        <div class="dia-tema">Iniciales Retroflejas</div>
                        <p style="font-size: 0.85em; margin-top: 10px;">zh, ch, sh, r</p>
                    </div>
                    <div class="dia">
                        <div class="dia-numero">Día 3</div>
                        <div class="dia-tema">Iniciales Palatales</div>
                        <p style="font-size: 0.85em; margin-top: 10px;">j, q, x</p>
                    </div>
                    <div class="dia">
                        <div class="dia-numero">Día 4</div>
                        <div class="dia-tema">Finales Vocálicas</div>
                        <p style="font-size: 0.85em; margin-top: 10px;">a, e, i, o, u, ü</p>
                    </div>
                    <div class="dia">
                        <div class="dia-numero">Día 5</div>
                        <div class="dia-tema">Los Cuatro Tonos</div>
                        <p style="font-size: 0.85em; margin-top: 10px;">1º, 2º, 3º, 4º + neutro</p>
                    </div>
                    <div class="dia">
                        <div class="dia-numero">Día 6</div>
                        <div class="dia-tema">Cambios Tonales</div>
                        <p style="font-size: 0.85em; margin-top: 10px;">Sandhi tonal en contexto</p>
                    </div>
                    <div class="dia">
                        <div class="dia-numero">Día 7</div>
                        <div class="dia-tema">Repaso Integral</div>
                        <p style="font-size: 0.85em; margin-top: 10px;">Autoevaluación y práctica</p>
                    </div>
                </div>
            </div>

            <!-- ACTIVIDADES -->
            <div class="seccion" id="actividades">
                <h2>🎯 Actividades Estructuradas</h2>

                <!-- ACTIVIDAD 1: INICIALES -->
                <div class="actividades-grid">
                    <div class="actividad a1">
                        <h3>🔤 Actividad 1: Iniciales (Consonantes)</h3>
                        <p>Domina los sonidos iniciales del chino mandarín. Presta especial atención a las consonantes que no existen en español: zh, ch, sh, r, j, q, x.</p>
                    </div>

                    <!-- ACTIVIDAD 2: FINALES -->
                    <div class="actividad a2">
                        <h3>🎵 Actividad 2: Finales (Vocales y Diptongos)</h3>
                        <p>Aprende las vocales simples y los diptongos. Las finales son cruciales para una pronunciación correcta. Especial énfasis en ü y las combinaciones complejas.</p>
                    </div>

                    <!-- ACTIVIDAD 3: TONOS -->
                    <div class="actividad a3">
                        <h3>📊 Actividad 3: Los Cuatro Tonos + Neutro</h3>
                        <p>Identifica, produce y diferencia los cuatro tonos del mandarín. Esta es la actividad más importante para la inteligibilidad de tu pronunciación.</p>
                    </div>

                    <!-- ACTIVIDAD 4: CAMBIOS -->
                    <div class="actividad a4">
                        <h3>🔀 Actividad 4: Cambios Tonales y Contexto</h3>
                        <p>Practica cómo los tonos cambian en contexto. El sandhi tonal es una característica esencial del chino natural y fluido.</p>
                    </div>

                    <!-- ACTIVIDAD 5: LABORATORIO -->
                    <div class="actividad a5">
                        <h3>🧪 Actividad 5: Laboratorio de Pronunciación</h3>
                        <p>Ejercicios de corrección fonética diseñados específicamente para corregir errores comunes de hispanohablantes.</p>
                    </div>
                </div>

                <!-- DETALLE ACTIVIDAD 1 -->
                <div class="ejercicio" style="margin-top: 40px;">
                    <h4>🔤 ACTIVIDAD 1: INICIALES (CONSONANTES) - DETALLE</h4>
                    
                    <p style="margin-bottom: 20px;"><strong>Objetivo:</strong> Dominar el sistema de iniciales del chino, especialmente las que no existen en español.</p>

                    <h4 style="margin-top: 30px;">Tabla de Iniciales con Punto de Articulación</h4>
                    <table>
                        <thead>
                            <tr>
                                <th>Categoría</th>
                                <th>Pinyin</th>
                                <th>Punto de Articulación</th>
                                <th>Consejo para Hispanohablantes</th>
                                <th>Ejemplo</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td rowspan="3"><strong>Aspiradas</strong></td>
                                <td><span class="pinyin">p</span></td>
                                <td>Bilabial</td>
                                <td>✓ Parecida al español, pero más aspirada</td>
                                <td>pā (爬) - trepar</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">t</span></td>
                                <td>Dental/Alveolar</td>
                                <td>✓ Parecida al español, más aspirada</td>
                                <td>tā (他) - él</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">k</span></td>
                                <td>Velar</td>
                                <td>✓ Parecida al español, más aspirada</td>
                                <td>kā (咖) - café</td>
                            </tr>
                            <tr>
                                <td rowspan="3"><strong>Retroflejas</strong></td>
                                <td><span class="pinyin">zh</span></td>
                                <td>Retrofleja</td>
                                <td>⚠️ Lengua curvada hacia atrás, como "ch" en "chocolate" pero retroflejada</td>
                                <td>zhī (知) - saber</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ch</span></td>
                                <td>Retrofleja Aspirada</td>
                                <td>⚠️ Igual que zh pero con aspiración (chhh)</td>
                                <td>chī (吃) - comer</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">sh</span></td>
                                <td>Retrofleja Fricativa</td>
                                <td>⚠️ Lengua curvada hacia atrás, sonido como "sh" en inglés "she"</td>
                                <td>shī (诗) - poesía</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">r</span></td>
                                <td>Retrofleja Fricativa</td>
                                <td>⚠️ NO como la "r" española. Lengua curvada, sonido similar a "soft j" inglés</td>
                                <td>rì (日) - día</td>
                            </tr>
                            <tr>
                                <td rowspan="3"><strong>Palatales</strong></td>
                                <td><span class="pinyin">j</span></td>
                                <td>Palatal</td>
                                <td>⚠️ Parecida a "j" en "jirafa" pero más suave y con lengua más hacia atrás</td>
                                <td>jī (鸡) - pollo</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">q</span></td>
                                <td>Palatal Aspirada</td>
                                <td>⚠️ Igual que j pero aspirada (chhh) y más tensa</td>
                                <td>qī (七) - siete</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">x</span></td>
                                <td>Palatal Fricativa</td>
                                <td>⚠️ Sonido entre "sh" y "s", lengua hacia atrás, aire continuo</td>
                                <td>xī (西) - oeste</td>
                            </tr>
                            <tr>
                                <td rowspan="3"><strong>Alveolares</strong></td>
                                <td><span class="pinyin">z</span></td>
                                <td>Alveolar</td>
                                <td>⚠️ Lengua plana en punta de dientes, sonido como "ds" en "sudds"</td>
                                <td>zī (子) - hijo</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">c</span></td>
                                <td>Alveolar Aspirada</td>
                                <td>⚠️ Igual que z pero aspirada y más tensa</td>
                                <td>cī (刺) - espina</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">s</span></td>
                                <td>Alveolar Fricativa</td>
                                <td>✓ Parecida al español, lengua en punta de dientes</td>
                                <td>sī (丝) - seda</td>
                            </tr>
                            <tr>
                                <td><strong>Otras</strong></td>
                                <td><span class="pinyin">l, n, m, f, h, g, b, d, w, y</span></td>
                                <td>Varias</td>
                                <td>Mayormente parecidas al español, con pequeñas diferencias</td>
                                <td>lè (乐) - música</td>
                            </tr>
                        </tbody>
                    </table>

                    <h4 style="margin-top: 30px;">Pares Mínimos: Iniciales Difíciles para Hispanohablantes</h4>
                    <p>Pronuncia cuidadosamente estos pares. La diferencia es crucial:</p>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">zī</div>
                            <div class="significado">(子) hijo</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">zhī</div>
                            <div class="significado">(知) saber</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">cī</div>
                            <div class="significado">(刺) espina</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">chī</div>
                            <div class="significado">(吃) comer</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">sī</div>
                            <div class="significado">(丝) seda</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">shī</div>
                            <div class="significado">(诗) poesía</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">jī</div>
                            <div class="significado">(鸡) pollo</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">qī</div>
                            <div class="significado">(七) siete</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">xī</div>
                            <div class="significado">(西) oeste</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">sī</div>
                            <div class="significado">(丝) seda</div>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Laboratorio de Iniciales</h4>
                        <p><strong>Ejercicio 1:</strong> Escucha los siguientes sonidos e identifica cuál es zh/ch/sh/r y cuál es z/c/s.</p>
                        <div class="opciones">
                            <div class="opcion" onclick="marcarRespuesta(this, 'z')">Zī</div>
                            <div class="opcion" onclick="marcarRespuesta(this, 'zh')">Zhī</div>
                            <div class="opcion" onclick="marcarRespuesta(this, 'sh')">Shī</div>
                            <div class="opcion" onclick="marcarRespuesta(this, 'r')">Rī</div>
                        </div>
                        <p style="margin-top: 15px; font-size: 0.9em; color: #666;">Nota: Esta es una simulación. En un laboratorio real, escucharías archivos de audio.</p>
                    </div>
                </div>

                <!-- DETALLE ACTIVIDAD 2 -->
                <div class="ejercicio" style="margin-top: 40px;">
                    <h4>🎵 ACTIVIDAD 2: FINALES (VOCALES Y DIPTONGOS) - DETALLE</h4>
                    
                    <p style="margin-bottom: 20px;"><strong>Objetivo:</strong> Dominar las vocales y las combinaciones vocálicas del chino mandarín.</p>

                    <h4 style="margin-top: 30px;">Tabla de Finales</h4>
                    <table>
                        <thead>
                            <tr>
                                <th>Tipo</th>
                                <th>Pinyin</th>
                                <th>Descripción Articulatoria</th>
                                <th>Consejo</th>
                                <th>Ejemplo</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td rowspan="6"><strong>Vocales Simples</strong></td>
                                <td><span class="pinyin">a</span></td>
                                <td>Vocal abierta anterior</td>
                                <td>✓ Parecida al español "a"</td>
                                <td>mā (妈) - mamá</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">e</span></td>
                                <td>Vocal media central</td>
                                <td>✓ Parecida al español "e", abierta</td>
                                <td>mē (呣) - sonido de afirmación</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">i</span></td>
                                <td>Vocal cerrada anterior</td>
                                <td>✓ Parecida al español "i"</td>
                                <td>mī (迷) - confuso</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">o</span></td>
                                <td>Vocal media posterior</td>
                                <td>⚠️ Más redonda que la "o" española, como en "oso"</td>
                                <td>mō (摩) - frotar</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">u</span></td>
                                <td>Vocal cerrada posterior</td>
                                <td>✓ Parecida al español "u"</td>
                                <td>mū (木) - madera</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ü</span></td>
                                <td>Vocal cerrada anterior redondeada</td>
                                <td>⚠️ NO existe en español. Pronuncia "i" pero con los labios redondeados como para "u"</td>
                                <td>nü (女) - mujer</td>
                            </tr>
                            <tr>
                                <td rowspan="8"><strong>Diptongos</strong></td>
                                <td><span class="pinyin">ai</span></td>
                                <td>a + i</td>
                                <td>✓ Como "ai" en "aire"</td>
                                <td>bāi (白) - blanco</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ei</span></td>
                                <td>e + i</td>
                                <td>✓ Como "ei" en "seis"</td>
                                <td>běi (北) - norte</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ao</span></td>
                                <td>a + o</td>
                                <td>⚠️ Sonido similar a "ao" en "cao" pero pronunciado rápido</td>
                                <td>māo (猫) - gato</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ou</span></td>
                                <td>o + u</td>
                                <td>✓ Como "ou" en "pausa"</td>
                                <td>hóu (猴) - mono</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ia</span></td>
                                <td>i + a</td>
                                <td>⚠️ Rápida transición de i a a, como "ya"</td>
                                <td>jiā (家) - casa</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ie</span></td>
                                <td>i + e</td>
                                <td>⚠️ Rápida transición, como "ye"</td>
                                <td>jiē (街) - calle</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ua</span></td>
                                <td>u + a</td>
                                <td>⚠️ Rápida transición, como "wa"</td>
                                <td>kuà (跨) - cruzar</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">uo</span></td>
                                <td>u + o</td>
                                <td>⚠️ Rápida transición, como "wo"</td>
                                <td>duō (多) - mucho</td>
                            </tr>
                            <tr>
                                <td rowspan="3"><strong>Finales Nasales</strong></td>
                                <td><span class="pinyin">an</span></td>
                                <td>a + n</td>
                                <td>✓ Nasal como en español "pan"</td>
                                <td>bān (班) - clase</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">en</span></td>
                                <td>e + n</td>
                                <td>✓ Nasal como en español "den"</td>
                                <td>běn (本) - libro</td>
                            </tr>
                            <tr>
                                <td><span class="pinyin">ang</span></td>
                                <td>a + ng</td>
                                <td>⚠️ Nasal velar, "ng" no existe en español inicial. Práctica: "camang"</td>
                                <td>bāng (帮) - ayudar</td>
                            </tr>
                        </tbody>
                    </table>

                    <h4 style="margin-top: 30px;">Pares Mínimos: Finales Difíciles</h4>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">ai</div>
                            <div class="significado">diptongo "aire"</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">ei</div>
                            <div class="significado">diptongo "seis"</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">an</div>
                            <div class="significado">nasal alveolar</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">ang</div>
                            <div class="significado">nasal velar</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">en</div>
                            <div class="significado">nasal alveolar</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">eng</div>
                            <div class="significado">nasal velar</div>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Laboratorio de Finales</h4>
                        <p><strong>Ejercicio 2:</strong> Distingue entre vocales simples y diptongos.</p>
                        <div class="opciones">
                            <div class="opcion" onclick="marcarRespuesta(this, 'simple')">a (simple)</div>
                            <div class="opcion" onclick="marcarRespuesta(this, 'diptongo')">ai (diptongo)</div>
                            <div class="opcion" onclick="marcarRespuesta(this, 'simple')">e (simple)</div>
                            <div class="opcion" onclick="marcarRespuesta(this, 'diptongo')">ei (diptongo)</div>
                        </div>
                    </div>
                </div>

                <!-- DETALLE ACTIVIDAD 3 -->
                <div class="ejercicio" style="margin-top: 40px;">
                    <h4>📊 ACTIVIDAD 3: LOS CUATRO TONOS + TONO NEUTRO - DETALLE</h4>
                    
                    <p style="margin-bottom: 20px;"><strong>Objetivo:</strong> Esta es la actividad más importante. Los tonos son lo que diferencia palabras completamente diferentes en chino. Sin tonos correctos, no serás comprendido.</p>

                    <h4 style="margin-top: 30px;">Los Cinco Tonos del Mandarín</h4>

                    <div class="tonos-container">
                        <div class="tono-card">
                            <div class="tono-numero">1º Tono</div>
                            <div class="tono-nombre">Tono Alto-Plano</div>
                            <div class="tono-grafico">_____ ‾‾‾‾‾</div>
                            <div class="tono-descripcion">
                                <strong>Pronunciación:</strong> Voz en nivel alto y constante
                                <br><strong>Ejemplo:</strong> mā (妈) - mamá
                                <br><strong>Imagen:</strong> Tu voz permanece en un nivel alto como si estuvieras cantando una nota sostenida.
                            </div>
                        </div>

                        <div class="tono-card">
                            <div class="tono-numero">2º Tono</div>
                            <div class="tono-nombre">Tono Ascendente</div>
                            <div class="tono-grafico">╱ ╱╱╱╱╱</div>
                            <div class="tono-descripcion">
                                <strong>Pronunciación:</strong> Voz sube desde medio hasta alto
                                <br><strong>Ejemplo:</strong> má (麻) - lino
                                <br><strong>Imagen:</strong> Como cuando haces una pregunta en español: "¿De verdad?" - la voz sube.
                            </div>
                        </div>

                        <div class="tono-card">
                            <div class="tono-numero">3º Tono</div>
                            <div class="tono-nombre">Tono Descendente-Ascendente</div>
                            <div class="tono-grafico">╲╲ ╱╱</div>
                            <div class="tono-descripcion">
                                <strong>Pronunciación:</strong> Voz baja, luego sube
                                <br><strong>Ejemplo:</strong> mǎ (马) - caballo
                                <br><strong>Imagen:</strong> Como cuando dudes: "mmmaaaa?" Primero baja, luego sube un poco.
                            </div>
                        </div>

                        <div class="tono-card">
                            <div class="tono-numero">4º Tono</div>
                            <div class="tono-nombre">Tono Descendente</div>
                            <div class="tono-grafico">╲╲╲╲╲ _</div>
                            <div class="tono-descripcion">
                                <strong>Pronunciación:</strong> Voz desciende desde alto hasta bajo
                                <br><strong>Ejemplo:</strong> mà (骂) - regañar
                                <br><strong>Imagen:</strong> Como una orden o afirmación fuerte. La voz baja notoriamente.
                            </div>
                        </div>

                        <div class="tono-card">
                            <div class="tono-numero">Tono Neutro</div>
                            <div class="tono-nombre">Tono Ligero</div>
                            <div class="tono-grafico">- ligero</div>
                            <div class="tono-descripcion">
                                <strong>Pronunciación:</strong> Rápido, corto y sin énfasis
                                <br><strong>Ejemplo:</strong> ma (吗) - partícula interrogativa
                                <br><strong>Imagen:</strong> Como un sonido muy ligero y rápido, prácticamente neutral.
                            </div>
                        </div>
                    </div>

                    <h4 style="margin-top: 30px;">Práctica: La Sílaba "Ma" con Cinco Tonos</h4>
                    <p>Esta es la práctica más importante. Aprende a pronunciar "ma" con los cinco tonos:</p>

                    <div style="background: white; border-radius: 10px; padding: 20px; margin: 20px 0;">
                        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 15px;">
                            <div style="text-align: center; padding: 15px; background: #e3f2fd; border-radius: 8px; border-left: 4px solid #667eea;">
                                <div style="font-size: 1.8em; font-weight: bold; color: #667eea;">mā</div>
                                <div style="font-size: 0.9em; color: #666; margin-top: 8px;">妈 (mamá)</div>
                                <div style="font-size: 0.8em; color: #999; margin-top: 5px;">1º Tono</div>
                            </div>
                            <div style="text-align: center; padding: 15px; background: #f3e5f5; border-radius: 8px; border-left: 4px solid #9c27b0;">
                                <div style="font-size: 1.8em; font-weight: bold; color: #9c27b0;">má</div>
                                <div style="font-size: 0.9em; color: #666; margin-top: 8px;">麻 (lino)</div>
                                <div style="font-size: 0.8em; color: #999; margin-top: 5px;">2º Tono</div>
                            </div>
                            <div style="text-align: center; padding: 15px; background: #ffe0b2; border-radius: 8px; border-left: 4px solid #ff9800;">
                                <div style="font-size: 1.8em; font-weight: bold; color: #ff9800;">mǎ</div>
                                <div style="font-size: 0.9em; color: #666; margin-top: 8px;">马 (caballo)</div>
                                <div style="font-size: 0.8em; color: #999; margin-top: 5px;">3º Tono</div>
                            </div>
                            <div style="text-align: center; padding: 15px; background: #ffebee; border-radius: 8px; border-left: 4px solid #f44336;">
                                <div style="font-size: 1.8em; font-weight: bold; color: #f44336;">mà</div>
                                <div style="font-size: 0.9em; color: #666; margin-top: 8px;">骂 (regañar)</div>
                                <div style="font-size: 0.8em; color: #999; margin-top: 5px;">4º Tono</div>
                            </div>
                            <div style="text-align: center; padding: 15px; background: #c8e6c9; border-radius: 8px; border-left: 4px solid #4caf50;">
                                <div style="font-size: 1.8em; font-weight: bold; color: #4caf50;">ma</div>
                                <div style="font-size: 0.9em; color: #666; margin-top: 8px;">吗 (¿...?)</div>
                                <div style="font-size: 0.8em; color: #999; margin-top: 5px;">Tono Neutro</div>
                            </div>
                        </div>
                    </div>

                    <div class="consejo">
                        <strong>Ejercicio de Repetición:</strong> Pronuncia "mā, má, mǎ, mà, ma" cinco veces seguidas. Luego, invierte el orden. Luego, al azar. Esto desarrolla memoria muscular.
                    </div>

                    <h4 style="margin-top: 30px;">Pares Mínimos Tonales</h4>
                    <p>Estas palabras se diferencian SOLO por el tono. Es crucial distinguirlas:</p>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">māma</div>
                            <div class="significado">妈妈 (mamá)</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">màma</div>
                            <div class="significado">骂吗 (¿regañar?)</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">chīfàn</div>
                            <div class="significado">吃饭 (comer)</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">chífàn</div>
                            <div class="significado">尺番 (sin sentido)</div>
                        </div>
                    </div>

                    <div class="pair-card">
                        <div class="pair-item">
                            <div class="pinyin">shàngbān</div>
                            <div class="significado">上班 (ir al trabajo)</div>
                        </div>
                        <div class="pair-separator">vs</div>
                        <div class="pair-item">
                            <div class="pinyin">shángbān</div>
                            <div class="significado">伤疤 (cicatriz)</div>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Laboratorio de Tonos - Ejercicio de Identificación</h4>
                        <p><strong>Ejercicio 3:</strong> Escucha e identifica qué tono es. Se presenta la sílaba "mā", ¿Cuál es?</p>
                        <div class="opciones">
                            <div class="opcion" onclick="marcarRespuesta(this, '1')">1º Tono (Alto-Plano)</div>
                            <div class="opcion" onclick="marcarRespuesta(this, '2')">2º Tono (Ascendente)</div>
                            <div class="opcion" onclick="marcarRespuesta(this, '3')">3º Tono (Desc-Asc)</div>
                            <div class="opcion" onclick="marcarRespuesta(this, '4')">4º Tono (Descendente)</div>
                        </div>
                    </div>
                </div>

                <!-- DETALLE ACTIVIDAD 4 -->
                <div class="ejercicio" style="margin-top: 40px;">
                    <h4>🔀 ACTIVIDAD 4: CAMBIOS TONALES Y CONTEXTO - DETALLE</h4>
                    
                    <p style="margin-bottom: 20px;"><strong>Objetivo:</strong> Comprender cómo los tonos cambian en contexto (sandhi tonal), lo cual es fundamental para sonar natural.</p>

                    <h4 style="margin-top: 30px;">Reglas de Sandhi Tonal</h4>

                    <table>
                        <thead>
                            <tr>
                                <th>Regla</th>
                                <th>Descripción</th>
                                <th>Ejemplo</th>
                                <th>Cambio</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Cambio del 3º Tono</strong></td>
                                <td>Cuando dos sílabas con 3º tono aparecen juntas, la primera cambia a 2º tono</td>
                                <td>mǎma → máma (妈妈)</td>
                                <td>3º + 3º = 2º + 3º</td>
                            </tr>
                            <tr>
                                <td><strong>Cambio de "yī" (一)</strong></td>
                                <td>"yī" (uno) cambia según el tono que le siga: se hace 4º antes de 1-3 tonos, y 2º antes de 4º tono</td>
                                <td>yībǎ (一把) → yībǎ<br>yībàng (一样) → yíbàng</td>
                                <td>1º → 2º o 4º</td>
                            </tr>
                            <tr>
                                <td><strong>Cambio de "bù" (不)</strong></td>
                                <td>"bù" (negación) se hace 2º tono antes de 4º tono, y 4º tono antes de otros tonos</td>
                                <td>búduì (不对) → búduì<br>búshì (不是) → búshì</td>
                                <td>4º → 2º o 4º</td>
                            </tr>
                            <tr>
                                <td><strong>Asimilación con "n" y "ng"</strong></td>
                                <td>Cambios menores en consonantes nasales finales en contexto</td>
                                <td>gēnghuà (耕化) tiene transición suave</td>
                                <td>Minor adjustments</td>
                            </tr>
                        </tbody>
                    </table>

                    <h4 style="margin-top: 30px;">Ejemplos Prácticos de Sandhi Tonal</h4>

                    <div style="background: white; border-radius: 10px; padding: 20px; margin: 20px 0;">
                        <div style="margin-bottom: 20px; padding: 15px; background: #f5f5f5; border-radius: 8px;">
                            <div style="font-weight: bold; color: #667eea; margin-bottom: 10px;">Ejemplo 1: Cambio del 3º Tono</div>
                            <div>
                                <strong>Frase:</strong> 我很好 (Wǒ hěn hǎo) - "Estoy muy bien"
                                <br><strong>Análisis:</strong> hěn (3º) + hǎo (3º) 
                                <br><strong>En contexto:</strong> Wǒ hén hǎo (la primera sílaba "hěn" se convierte en 2º tono)
                                <br><strong>Pronunciación natural:</strong> Wǒ hén hǎo
                            </div>
                        </div>

                        <div style="margin-bottom: 20px; padding: 15px; background: #f5f5f5; border-radius: 8px;">
                            <div style="font-weight: bold; color: #667eea; margin-bottom: 10px;">Ejemplo 2: Cambio de "yī" (一)</div>
                            <div>
                                <strong>Frase:</strong> 一个 (yī ge) - "uno/una" (medida)
                                <br><strong>Análisis:</strong> yī (1º) + ge (4º tono)
                                <br><strong>En contexto:</strong> yí ge (yī cambia a 2º tono antes de 4º tono)
                                <br><strong>Pronunciación natural:</strong> yí ge
                            </div>
                        </div>

                        <div style="padding: 15px; background: #f5f5f5; border-radius: 8px;">
                            <div style="font-weight: bold; color: #667eea; margin-bottom: 10px;">Ejemplo 3: Cambio de "bù" (不)</div>
                            <div>
                                <strong>Frase:</strong> 不对 (búduì) - "incorrecto"
                                <br><strong>Análisis:</strong> bù (4º) + duì (4º)
                                <br><strong>En contexto:</strong> búduì (bù cambia a 2º tono antes de otro 4º tono)
                                <br><strong>Pronunciación natural:</strong> búduì
                            </div>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Laboratorio de Cambios Tonales</h4>
                        <p><strong>Ejercicio 4:</strong> ¿Cuál es el cambio tonal en estas frases? (Selecciona la pronunciación correcta en contexto)</p>
                        
                        <div style="margin: 20px 0;">
                            <p style="font-weight: bold; margin-bottom: 10px;">妈妈 (māma) - Mamá</p>
                            <div class="opciones">
                                <div class="opcion" onclick="marcarRespuesta(this, 'correcto')">máma (3º + 3º = 2º + 3º)</div>
                                <div class="opcion" onclick="marcarRespuesta(this, 'incorrecto')">māma (sin cambio)</div>
                            </div>
                        </div>

                        <div style="margin: 20px 0;">
                            <p style="font-weight: bold; margin-bottom: 10px;">一个 (yīge) - Uno/una</p>
                            <div class="opciones">
                                <div class="opcion" onclick="marcarRespuesta(this, 'correcto')">yí ge (1º → 2º antes de 4º)</div>
                                <div class="opcion" onclick="marcarRespuesta(this, 'incorrecto')">yī ge (sin cambio)</div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- DETALLE ACTIVIDAD 5 -->
                <div class="ejercicio" style="margin-top: 40px;">
                    <h4>🧪 ACTIVIDAD 5: LABORATORIO DE PRONUNCIACIÓN - CORRECCIÓN FONÉTICA</h4>
                    
                    <p style="margin-bottom: 20px;"><strong>Objetivo:</strong> Identificar y corregir errores comunes de hispanohablantes en la pronunciación del chino mandarín.</p>

                    <h4 style="margin-top: 30px;">Errores Comunes de Hispanohablantes</h4>

                    <table>
                        <thead>
                            <tr>
                                <th>Error Típico</th>
                                <th>Pronunciación Incorrecta</th>
                                <th>Pronunciación Correcta</th>
                                <th>Explicación</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>No aspirar p, t, k</strong></td>
                                <td>pá (como en español "pa")</td>
                                <td>phá (con aire fuerte)</td>
                                <td>En chino, las consonantes sordas son muy aspiradas. Siente el aire salir fuerte de tu boca.</td>
                            </tr>
                            <tr>
                                <td><strong>Confundir zh/ch con j</strong></td>
                                <td>jī por zhī</td>
                                <td>zhī (lengua curvada atrás)</td>
                                <td>zh/ch/sh son retroflejas (lengua atrás). j/q/x son palatales (lengua adelante). Muy diferentes.</td>
                            </tr>
                            <tr>
                                <td><strong>Pronunciar r como español "r"</strong></td>
                                <td>rì como "rri" o "rr"</td>
                                <td>rì (retrofleja fricativa, como "soft j" inglés)</td>
                                <td>La "r" china NO es la "r" española. Es más parecida al "soft j" en "measure" inglés.</td>
                            </tr>
                            <tr>
                                <td><strong>Confundir x con "j" o "s"</strong></td>
                                <td>xī como "ji" o "si"</td>
                                <td>xī (sonido palatal fricativo)</td>
                                <td>x es palatal (lengua adelante), entre "sh" y "s". Practica: "shshshshshs → x"</td>
                            </tr>
                            <tr>
                                <td><strong>No pronunciar "ü" correctamente</strong></td>
                                <td>nü como "ni" o "nu"</td>
                                <td>nü (i con labios de u)</td>
                                <td>ü no existe en español. Pronuncia "i" pero rodea los labios como para "u".</td>
                            </tr>
                            <tr>
                                <td><strong>Confundir tonos 1 y 2</strong></td>
                                <td>Pronunciar ambos como alto-plano</td>
                                <td>1º: alto plano | 2º: ascendente</td>
                                <td>1º es plano (como un sostenido ♩). 2º sube (como una pregunta "¿...").</td>
                            </tr>
                            <tr>
                                <td><strong>No hacer el 3º tono descendente-ascendente</strong></td>
                                <td>Pronunciar como un tono bajo plano</td>
                                <td>3º: baja, luego sube</td>
                                <td>El 3º es el más complicado. Primero la voz baja bastante, luego sube un poco.</td>
                            </tr>
                            <tr>
                                <td><strong>No diferenciar -n final de -ng final</strong></td>
                                <td>bān (班) y bāng (帮) suenan igual</td>
                                <td>-n: alveolar | -ng: velar (más atrás)</td>
                                <td>-n es como "n" española. -ng es como "ng" en "thing" inglés, más atrás en la garganta.</td>
                            </tr>
                        </tbody>
                    </table>

                    <h4 style="margin-top: 30px;">Ejercicios de Corrección Fonética</h4>

                    <div class="laboratorio">
                        <h4>Ejercicio 5.1: Aspiración en p, t, k</h4>
                        <p><strong>Instrucción:</strong> Coloca tu mano frente a tu boca. Cuando pronuncies correctamente, deberías sentir aire.</p>
                        <div style="margin: 15px 0; padding: 15px; background: white; border-radius: 8px;">
                            <p style="margin-bottom: 10px;"><strong>Pronuncia estas palabras con mucha aspiración:</strong></p>
                            <ul style="margin-left: 20px;">
                                <li><span class="pinyin">pā</span> (爬) - trepar</li>
                                <li><span class="pinyin">tā</span> (他) - él</li>
                                <li><span class="pinyin">kā</span> (咖) - café</li>
                            </ul>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Ejercicio 5.2: Distinguir Retroflejas de Palatales</h4>
                        <p><strong>Instrucción:</strong> Palpa tu lengua. Para zh/ch/sh/r, la lengua debe estar curvada hacia atrás (retrofleja). Para j/q/x, la lengua está adelante (palatal).</p>
                        <div style="margin: 15px 0; padding: 15px; background: white; border-radius: 8px; display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
                            <div>
                                <p style="font-weight: bold; margin-bottom: 10px;">Retroflejas (lengua atrás):</p>
                                <ul style="margin-left: 20px;">
                                    <li><span class="pinyin">zhī</span> (知) - saber</li>
                                    <li><span class="pinyin">chī</span> (吃) - comer</li>
                                    <li><span class="pinyin">shī</span> (诗) - poesía</li>
                                    <li><span class="pinyin">rì</span> (日) - día</li>
                                </ul>
                            </div>
                            <div>
                                <p style="font-weight: bold; margin-bottom: 10px;">Palatales (lengua adelante):</p>
                                <ul style="margin-left: 20px;">
                                    <li><span class="pinyin">jī</span> (鸡) - pollo</li>
                                    <li><span class="pinyin">qī</span> (七) - siete</li>
                                    <li><span class="pinyin">xī</span> (西) - oeste</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Ejercicio 5.3: Practicar "ü" (u con i)</h4>
                        <p><strong>Instrucción:</strong> Pronuncia "i" pero con los labios redondeados. Alterna entre "i" y "u" para obtener la posición correcta.</p>
                        <div style="margin: 15px 0; padding: 15px; background: white; border-radius: 8px;">
                            <p style="margin-bottom: 10px;"><strong>Secuencia de práctica:</strong></p>
                            <ol style="margin-left: 20px;">
                                <li>Pronuncia "i" (normal)</li>
                                <li>Pronuncia "u" (normal)</li>
                                <li>Pronuncia "i" pero rodea los labios lentamente como para "u"</li>
                                <li>Ese es el sonido de "ü"</li>
                                <li>Practica: <span class="pinyin">nü</span> (女) - mujer, <span class="pinyin">lü</span> (绿) - verde</li>
                            </ol>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Ejercicio 5.4: Tonos Confusos - Test de Identificación</h4>
                        <p><strong>Instrucción:</strong> Escucha e identifica. Estos tonos son los más confusos para hispanohablantes.</p>
                        <div style="margin: 20px 0;">
                            <p style="font-weight: bold; margin-bottom: 10px;">¿Cuál es el tono de "mà"?</p>
                            <div class="opciones">
                                <div class="opcion" onclick="marcarRespuesta(this, '1')">1º Tono (plano)</div>
                                <div class="opcion" onclick="marcarRespuesta(this, '2')">2º Tono (sube)</div>
                                <div class="opcion" onclick="marcarRespuesta(this, '3')">3º Tono (desc-asc)</div>
                                <div class="opcion" onclick="marcarRespuesta(this, '4')">4º Tono (baja)</div>
                            </div>
                        </div>
                    </div>

                    <div class="laboratorio">
                        <h4>Ejercicio 5.5: Nasales Finales (-n vs -ng)</h4>
                        <p><strong>Instrucción:</strong> Practica la diferencia entre nasal alveolar (-n) y nasal velar (-ng).</p>
                        <div class="pair-card">
                            <div class="pair-item">
                                <div class="pinyin">bān</div>
                                <div class="significado">班 (clase) [-n alveolar]</div>
                            </div>
                            <div class="pair-separator">vs</div>
                            <div class="pair-item">
                                <div class="pinyin">bāng</div>
                                <div class="significado">帮 (ayudar) [-ng velar]</div>
                            </div>
                        </div>
                        <div class="consejo">
                            <strong>Técnica:</strong> Para -ng, siente que la nasal se forma en la garganta (más atrás que -n). Es como el "ng" en "ring" inglés.
                        </div>
                    </div>
                </div>

            </div>

            <!-- SOLUCIONARIO -->
            <div class="seccion" id="solucionario">
                <h2>✓ Solucionario y Respuestas</h2>

                <div class="solucionario">
                    <h3>Respuestas a Ejercicios de Laboratorio</h3>

                    <div class="solucion-item">
                        <strong>Ejercicio 1: Identificación de Iniciales Retroflejas vs Alveolares</strong>
                        <p><strong>Respuesta:</strong> Debe ser capaz de distinguir entre:
                        <ul style="margin-left: 20px; margin-top: 10px;">
                            <li>zī vs zhī: z (alveolar, lengua plana) vs zh (retrofleja, lengua curvada atrás)</li>
                            <li>cī vs chī: c (alveolar, aspirada) vs ch (retrofleja, aspirada)</li>
                            <li>sī vs shī: s (alveolar, fricativa) vs sh (retrofleja, fricativa)</li>
                            <li>sī vs xī: s (alveolar) vs x (palatal)</li>
                        </ul>
                        <strong>Nota:</strong> La diferencia no es fácil. Necesita mucha práctica de laboratorio.</p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 2: Identificación de Vocales Simples vs Diptongos</strong>
                        <p><strong>Respuestas esperadas:</strong>
                        <ul style="margin-left: 20px; margin-top: 10px;">
                            <li>a = vocal simple (duración normal)</li>
                            <li>ai = diptongo (transición rápida de a a i)</li>
                            <li>e = vocal simple</li>
                            <li>ei = diptongo (transición rápida de e a i)</li>
                        </ul>
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 3: Identificación de Tonos (sílaba "mā")</strong>
                        <p><strong>Respuesta esperada:</strong> 1º Tono (Alto-Plano)
                        <br><strong>Explicación:</strong> "mā" con diacrítico macron (‾) indica 1º tono. La voz permanece en nivel alto y constante.
                        <br><strong>Comparación:</strong>
                        <ul style="margin-left: 20px; margin-top: 10px;">
                            <li>1º (mā): _____ (plano)</li>
                            <li>2º (má): ╱╱╱ (sube)</li>
                            <li>3º (mǎ): ╲╱╱ (baja, sube)</li>
                            <li>4º (mà): ╲╲╲ (baja)</li>
                        </ul>
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 4.1: Cambio del 3º Tono en "妈妈"</strong>
                        <p><strong>Respuesta correcta:</strong> máma (no māma)
                        <br><strong>Explicación:</strong> Cuando dos sílabas consecutivas tienen 3º tono, la primera se convierte en 2º tono. Entonces: mǎ + mǎ → má + mǎ (máma)
                        <br><strong>Regla importante:</strong> Esta es una de las reglas de sandhi tonal más comunes en chino.
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 4.2: Cambio de "yī" en "一个"</strong>
                        <p><strong>Respuesta correcta:</strong> yí ge (no yī ge)
                        <br><strong>Explicación:</strong> "yī" (uno) cambia a 2º tono antes de un 4º tono. Como "ge" es aproximadamente 4º, yī se convierte en yí.
                        <br><strong>Reglas de "yī":</strong>
                        <ul style="margin-left: 20px; margin-top: 10px;">
                            <li>yī + 1º, 2º, 3º tonos → yī (sin cambio, pero varía por región)</li>
                            <li>yī + 4º tono → yí (2º tono)</li>
                            <li>yī + palabra → contexto específico</li>
                        </ul>
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 5.1: Aspiración en "p, t, k"</strong>
                        <p><strong>Respuesta esperada:</strong> Sentir aire saliendo fuertemente de la boca cuando se pronuncia.
                        <br><strong>Prueba de aspiration:</strong> Coloca un papel frente a tu boca. Al pronunciar correctamente, el papel debe moverse.
                        <br><strong>Palabras clave:</strong>
                        <ul style="margin-left: 20px; margin-top: 10px;">
                            <li>pā (爬): pronuncia con mucho aire</li>
                            <li>tā (他): aire notable</li>
                            <li>kā (咖): aire fuerte</li>
                        </ul>
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 5.2: Retroflejas vs Palatales</strong>
                        <p><strong>Explicación de posiciones:</strong>
                        <br><strong>Retroflejas:</strong> Lengua curvada hacia atrás, formando un arco. Sonidos: zh, ch, sh, r
                        <br><strong>Palatales:</strong> Lengua adelante, contra el paladar duro. Sonidos: j, q, x
                        <br><strong>Prueba física:</strong> Coloca tu dedo bajo la lengua. Para zh/ch/sh/r, la punta de la lengua se curva atrás. Para j/q/x, la lengua está plana y hacia adelante.
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 5.3: Pronunciación de "ü"</strong>
                        <p><strong>Respuesta esperada:</strong> Sonido como "i" con labios redondeados.
                        <br><strong>Proceso de aprendizaje:</strong>
                        <ol style="margin-left: 20px; margin-top: 10px;">
                            <li>Di "iiiiii" (sonido "i" prolongado)</li>
                            <li>Mientras dices "iiiiii", redondea lentamente los labios</li>
                            <li>Cuando los labios estén completamente redondeados, tienes "ü"</li>
                            <li>Practica alternando "i" → "ü" → "i"</li>
                        </ol>
                        <br><strong>Palabras para practicar:</strong> nü (女), lü (绿), qü (去)
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 5.4: Identificación de Tono "mà" (4º Tono)</strong>
                        <p><strong>Respuesta correcta:</strong> 4º Tono (Descendente)
                        <br><strong>Explicación:</strong> "mà" con acento grave (̀) indica 4º tono. La voz desciende notoriamente.
                        <br><strong>Característica del 4º tono:</strong> Suena como una orden o afirmación fuerte: "¡MÀ!" (con la voz bajando)
                        </p>
                    </div>

                    <div class="solucion-item">
                        <strong>Ejercicio 5.5: Nasales Finales -n vs -ng</strong>
                        <p><strong>Respuesta esperada:</strong> Poder diferenciar auditivamente entre -n (más adelante) y -ng (más atrás).
                        <br><strong>Técnica de pronunciación:</strong>
                        <ul style="margin-left: 20px; margin-top: 10px;">
                            <li>-n (nasal alveolar): La nasal se forma donde los dientes se cierran, sonido como "n" española</li>
                            <li>-ng (nasal velar): La nasal se forma en la garganta, más atrás, como "ng" en "ring" inglés</li>
                        </ul>
                        <br><strong>Pares de práctica:</strong>
                        <ul style="margin-left: 20px;">
                            <li>bān (班) vs bāng (帮)</li>
                            <li>tián (田) vs tiáng (没有 standard)</li>
                            <li>lín (林) vs líng (零)</li>
                        </ul>
                        </p>
                    </div>
                </div>

                <div style="background: #e8f5e9; border-left: 5px solid #4caf50; border-radius: 5px; padding: 20px; margin: 20px 0;">
                    <h4 style="color: #2e7d32; margin-bottom: 10px;">📌 Nota Importante sobre el Progreso</h4>
                    <p style="color: #1b5e20;">La pronunciación del chino es una habilidad que se desarrolla con la práctica consistente. Espera cometer errores y ver mejoras gradualmente. Los hispanohablantes típicamente necesitan:</p>
                    <ul style="color: #1b5e20; margin-left: 20px; margin-top: 10px;">
                        <li><strong>4-6 semanas</strong> para dominar los tonos básicamente</li>
                        <li><strong>3-6 meses</strong> para pronunciar sin acento notable</li>
                        <li><strong>1-2 años</strong> para alcanzar pronunciación nativa o cercana a nativa</li>
                    </ul>
                    <p style="color: #1b5e20; margin-top: 15px;"><strong>Consejo:</strong> Graba tu voz y compárala con grabaciones nativas. Usa aplicaciones como Speechling o Forvo para recibir retroalimentación de hablantes nativos.</p>
                </div>
            </div>

            <!-- REFERENCIAS -->
            <div class="seccion" id="referencias">
                <h2>📖 Referencias y Recursos Complementarios</h2>

                <div class="referencias">
                    <h3>Libros de Texto Recomendados</h3>

                    <div class="ref-categoria">
                        <h4>📚 New Practical Chinese Reader (新实用汉语课本)</h4>
                        <p><strong>Unidades relevantes para Pinyin y Tonos:</strong></p>
                        <div class="ref-item">
                            <strong>Unidad 1:</strong> Introducción al Pinyin, Sistema de Tonos, Saludos Básicos
                        </div>
                        <div class="ref-item">
                            <strong>Unidades 1-2:</strong> Práctica de Iniciales y Finales en contexto
                        </div>
                        <div class="ref-item">
                            <strong>Recomendación:</strong> Excelente para aprendizaje progresivo. Incluye ejercicios de pronunciación para cada lección.
                        </div>
                    </div>

                    <div class="ref-categoria">
                        <h4>📗 HSK Standard Course (HSK标准教程)</h4>
                        <p><strong>Unidades relevantes:</strong></p>
                        <div class="ref-item">
                            <strong>Libro 1, Unidades 1-3:</strong> Fonética del Chino, Tonos, Palabras de Uso Diario
                        </div>
                        <div class="ref-item">
                            <strong>Recomendación:</strong> Estructurado según el examen HSK. Muy útil para estudiantes que quieren certificación oficial.
                        </div>
                    </div>

                    <div class="ref-categoria">
                        <h4>🌳 El Chino para Hispanohablantes</h4>
                        <p><strong>Especialmente útil porque:</strong></p>
                        <div class="ref-item">
                            Diseñado ESPECÍFICAMENTE para hispanohablantes. Explica las dificultades de pronunciación desde la perspectiva del español.
                        </div>
                        <div class="ref-item">
                            Capítulo 1: Comparación detallada entre sonidos del español y chino.
                        </div>
                        <div class="ref-item">
                            <strong>Recomendación:</strong> IMPRESCINDIBLE si quieres entender POR QUÉ tienes dificultades.
                        </div>
                    </div>

                    <div class="ref-categoria">
                        <h4>📕 Hànyǔ (汉语) - Curso de Chino para Hispanohablantes</h4>
                        <p><strong>Enfoque:</strong></p>
                        <div class="ref-item">
                            Libro 1, Lección 0-1: Introducción completa a Pinyin, Tonos y Pronunciación
                        </div>
                        <div class="ref-item">
                            Incluye tablas de comparación de sonidos español-chino.
                        </div>
                    </div>
                </div>

                <div class="referencias" style="margin-top: 30px;">
                    <h3>Recursos Digitales y Aplicaciones</h3>

                    <div class="ref-categoria">
                        <h4>🎧 Canales de YouTube para Pronunciación</h4>
                        <div class="ref-item">
                            <strong>Yoyo Chinese (杨杨中文):</strong> "Yoyo Cheng" ofrece lecciones detalladas sobre Pinyin y tonos. Especialmente útil su serie "Tones Mastery" (Dominio de Tonos).
                        </div>
                        <div class="ref-item">
                            <strong>Mandarin Corner (Lý Khánh):</strong> Grabaciones claras de pronunciación con explicaciones sobre articulación. Enfoque muy didáctico.
                        </div>
                        <div class="ref-item">
                            <strong>Easy Mandarin:</strong> Lecciones sobre distinción entre sonidos confusos (zh vs z, j vs zh, etc.). Ideal para hispanohablantes.
                        </div>
                        <div class="ref-item">
                            <strong>Lex Learning:</strong> "Chinese Pronunciation Mastery" series. Muy completo y visual.
                        </div>
                        <div class="ref-item">
                            <strong>ChinesePod:</strong> Podcast con lecciones sobre pronunciación. Bueno para aprender mientras viajas.
                        </div>
                    </div>

                    <div class="ref-categoria">
                        <h4>📱 Aplicaciones Móviles</h4>
                        <div class="ref-item">
                            <strong>Pleco (Dictionary):</strong> La mejor aplicación de diccionario chino-español. Incluye audio de pronunciación nativa de cada palabra. IMPRESCINDIBLE.
                        </div>
                        <div class="ref-item">
                            <strong>HelloChinese:</strong> Excelente para principiantes. Lecciones interactivas sobre Pinyin y tonos. Tiene ejercicios de pronunciación con reconocimiento de voz.
                        </div>
                        <div class="ref-item">
                            <strong>Forvo:</strong> Base de datos de pronunciación por hablantes nativos. Puedes escuchar cómo dicen cada palabra y enviar grabaciones para corrección.
                        </div>
                        <div class="ref-item">
                            <strong>Speechling:</strong> Comunidad de aprendices donde puedes grabar y recibir corrección de hablantes nativos (free + premium).
                        </div>
                        <div class="ref-item">
                            <strong>Chineasy:</strong> Enfoque visual y mnemotécnico para caracteres y pronunciación. Bueno para principiantes.
                        </div>
                        <div class="ref-item">
                            <strong>HSK Academy:</strong> Si estudias para el examen HSK, esta app tiene lecciones de pronunciación estructuradas por nivel.
                        </div>
                    </div>

                    <div class="ref-categoria">
                        <h4>🌐 Sitios Web</h4>
                        <div class="ref-item">
                            <strong>Jisho.org (Hanzi):</strong> Diccionario online gratuito con audio de pronunciación. Muy útil para verificar pronunciación.
                        </div>
                        <div class="ref-item">
                            <strong>Pinyin.info:</strong> Base de datos exhaustiva sobre Pinyin. Excelente para comprensión profunda del sistema.
                        </div>
                        <div class="ref-item">
                            <strong>MDBG.net:</strong> Diccionario chino-inglés/español con audio. Muy completo.
                        </div>
                    </div>
                </div>

                <div class="referencias" style="margin-top: 30px;">
                    <h3>Estrategias de Práctica Recomendadas</h3>

                    <div class="ref-categoria">
                        <h4>🎯 Método de Aprendizaje Sugerido</h4>
                        <div class="ref-item">
                            <strong>Semana 1-2:</strong> Enfócate SOLO en los tonos usando "ma" (mā, má, mǎ, mà, ma). Repite 100+ veces. Graba tu voz.
                        </div>
                        <div class="ref-item">
                            <strong>Semana 3-4:</strong> Aprende iniciales difíciles (zh/ch/sh/r, j/q/x, z/c/s). Practica pares mínimos.
                        </div>
                        <div class="ref-item">
                            <strong>Semana 5-6:</strong> Practica finales, especialmente ü y nasales (-n vs -ng).
                        </div>
                        <div class="ref-item">
                            <strong>Semana 7+:</strong> Practica palabras completas con contexto. Comienza a aprender vocabulario mientras refuerzas la pronunciación.
                        </div>
                    </div>

                    <div class="ref-categoria">
                        <h4>🔄 Técnicas de Práctica Efectivas</h4>
                        <div class="ref-item">
                            <strong>Shadowing (Repetición de Sombra):</strong> Escucha a un hablante nativo y repite exactamente lo que dice, incluyendo ritmo y entonación. Esto es más efectivo que repetición simple.
                        </div>
                        <div class="ref-item">
                            <strong>Grabación y Comparación:</strong> Graba tu pronunciación y compárala con un nativo. Puedes usar Speechling o simplemente el grabador de tu teléfono.
                        </div>
                        <div class="ref-item">
                            <strong>Práctica de Espejo:</strong> Mira tu boca en un espejo mientras practicas para asegurar que tu articulación es correcta.
                        </div>
                        <div class="ref-item">
                            <strong>Conversación con Nativos:</strong> Aunque estés al principio, practica con hablantes nativos en plataformas como Tandem o Conversation Exchange. El feedback real es invaluable.
                        </div>
                        <div class="ref-item">
                            <strong>Canto de Canciones en Chino:</strong> Estudia canciones chinas. La música ayuda con ritmo, tonos y pronunciación natural.
                        </div>
                    </div>
                </div>

            </div>

        </div>

        <!-- FOOTER -->
        <div class="footer">
            <h2>🎓 Conclusión y Próximos Pasos</h2>
            <p>Has completado la introducción a la Fonética y Fonología del Chino Mandarín (Pinyin y Tonos). Este es un viaje largo, pero absolutamente necesario para cualquier estudiante de chino.</p>
            <p><strong>Recuerda:</strong> La pronunciación correcta es clave para la comunicación efectiva en chino. Invierte tiempo ahora en perfeccionar tus tonos y sonidos iniciales/finales, y te ahorrarás correcciones futuras.</p>
            <p style="margin-top: 30px; font-style: italic;">Próxima sesión sugerida: <strong>Gramática Básica I (Estructura de Oraciones, Verbo "ser/estar")</strong></p>
            <p style="margin-top: 20px; color: #aaa; font-size: 0.9em;">Documento creado para estudiantes de chino mandarín hispanohablantes | 2024-2025</p>
        </div>

    </div>

    <script>
        function marcarRespuesta(elemento, respuesta) {
            // Encuentra el contenedor del ejercicio
            const ejercicio = elemento.parentElement;
            
            // Remueve clases previas de todas las opciones
            const opciones = ejercicio.querySelectorAll('.opcion');
            opciones.forEach(op => {
                op.classList.remove('correcto', 'incorrecto');
            });
            
            // Marca la opción seleccionada
            if (respuesta === 'correcto' || respuesta === '1' || respuesta === 'zh' || respuesta === 'simple' || respuesta === '2º') {
                elemento.classList.add('correcto');
            } else if (respuesta === 'incorrecto' || respuesta === '2' || respuesta === 'z' || respuesta === 'diptongo') {
                elemento.classList.add('incorrecto');
            } else {
                elemento.classList.add('correcto');
            }
            
            // Muestra un mensaje simple
            setTimeout(() => {
                alert('Respuesta procesada. Revisa la explicación en el solucionario.');
            }, 300);
        }

        // Smooth scroll para los enlaces de navegación
        document.querySelectorAll('.nav a').forEach(link => {
            link.addEventListener('click', (e) => {
                const target = document.querySelector(link.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
