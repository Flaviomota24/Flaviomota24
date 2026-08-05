<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfólio & Currículo Profissional - Flávio Vinício Mota da Silva</title>
    <!-- Bootstrap 5 CSS -->
    <link href="https://jsdelivr.net" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cloudflare.com">
    <!-- Devicon Icons (Tecnologias nativas sem quebra de SVG) -->
    <link rel="stylesheet" href="https://jsdelivr.net">
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://googleapis.com">
    <link rel="preconnect" href="https://gstatic.com" crossorigin>
    <link href="https://googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <!-- AOS Animation CSS -->
    <link href="https://jsdelivr.net" rel="stylesheet">

    <style>
        :root {
            --bg-main: #060913;
            --card-background: rgba(13, 20, 38, 0.5);
            --border-color: rgba(255, 255, 255, 0.06);
            --cyan-accent: #00D2FF;
            --purple-accent: #8A2BE2;
            --text-primary: #F3F4F6;
            --text-muted: #94A3B8;
            --text-secondary: #CBD5E1;
            --font-mono: 'JetBrains+Mono', monospace;
        }

        body {
            background-color: var(--bg-main);
            color: var(--text-primary);
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-image: 
                radial-gradient(at 0% 0%, rgba(0, 210, 255, 0.04) 0px, transparent 50%),
                radial-gradient(at 100% 0%, rgba(138, 43, 226, 0.04) 0px, transparent 50%);
            background-attachment: fixed;
            overflow-x: hidden;
        }

        /* Modificadores Globais */
        .text-cyan { color: var(--cyan-accent); }
        .text-purple { color: var(--purple-accent); }
        .font-mono { font-family: var(--font-mono); }
        .fs-7 { font-size: 0.875rem; }
        .leading-relaxed { line-height: 1.6; }
        .tracking-tight { letter-spacing: -0.025em; }
        .tracking-wider { letter-spacing: 0.05em; }
        .uppercase { text-transform: uppercase; }

        /* Barra de Ações Superior */
        .action-bar {
            background: rgba(10, 15, 30, 0.7);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.2);
        }

        .btn-action {
            background: rgba(255, 255, 255, 0.03);
            color: var(--text-primary);
            border: 1px solid var(--border-color);
            padding: 10px 18px;
            border-radius: 10px;
            font-size: 0.85rem;
            font-weight: 500;
            transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-action:hover {
            background: rgba(255, 255, 255, 0.08);
            color: #ffffff;
            transform: translateY(-1px);
            border-color: rgba(0, 210, 255, 0.3);
        }

        /* Container do Currículo */
        .main-resume {
            background: rgba(10, 16, 32, 0.4);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border: 1px solid var(--border-color);
            border-radius: 24px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.4);
        }

        .avatar-frame {
            width: 100px;
            height: 100px;
            border-radius: 24px;
            background: rgba(0, 210, 255, 0.03);
            border: 1px solid rgba(0, 210, 255, 0.2);
            box-shadow: inset 0 0 12px rgba(0, 210, 255, 0.1);
        }

        .badge-tech-pill {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-color);
            color: var(--text-primary);
            padding: 8px 14px;
            border-radius: 8px;
            font-weight: 500;
            font-size: 0.8rem;
        }

        /* Cards com Design de Painel */
        .card-glass {
            background: var(--card-background);
            border: 1px solid var(--border-color);
            border-radius: 16px;
        }

        /* Linha do Tempo Customizada */
        .custom-timeline {
            border-left: 1px dashed rgba(255, 255, 255, 0.15);
        }

        .timeline-node {
            position: absolute;
            left: -20px;
            top: 5px;
            width: 9px;
            height: 9px;
            border-radius: 50%;
            box-shadow: 0 0 8px currentColor;
        }

        .education-card {
            background: rgba(255, 255, 255, 0.01);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 12px;
        }

        /* Sistema Progressivo de Skills */
        .progress-bar-bg {
            background: rgba(255, 255, 255, 0.02);
            height: 5px;
            border-radius: 3px;
            overflow: hidden;
        }

        .progress-bar-fill {
            height: 100%;
            border-radius: 3px;
        }

        .bg-cyan { background: var(--cyan-accent); }
        .bg-purple { background: var(--purple-accent); }

        /* Grid de Tecnologias Devicon */
        .tech-icon-grid i {
            font-size: 2rem;
            filter: grayscale(15%) opacity(85%);
            transition: all 0.2s ease;
        }

        .tech-icon-grid i:hover {
            filter: grayscale(0%) opacity(100%);
            transform: scale(1.1);
        }

        /* Seção Oculta para Renderização Exclusiva de Markdown do README */
        .readme-section {
            background: #0d1117;
            border: 1px solid #30363d;
            border-radius: 16px;
            color: #c9d1d9;
        }
        
        .readme-pre {
            background: #161b22;
            color: #e6edf3;
            padding: 16px;
            border-radius: 10px;
            font-family: var(--font-mono);
            font-size: 0.85rem;
            overflow-x: auto;
            border: 1px solid #30363d;
        }

        /* Otimização Estrita para Folha de Impressão */
        @media print {
            .no-print { display: none !important; }
            body { background: #ffffff !important; color: #000000 !important; }
            .main-resume { background: #ffffff !important; border: none !important; box-shadow: none !important; padding: 0 !important; }
            .card-glass, .education-card { background: #ffffff !important; border: 1px solid #e2e8f0 !important; color: #000000 !important; page-break-inside: avoid; }
            h1, h2, h3, h4, h5, .text-white { color: #000000 !important; }
            .text-cyan, .text-purple, .text-muted { color: #334155 !important; }
            .badge-tech-pill { border: 1px solid #cbd5e1 !important; color: #000000 !important; background: transparent !important; }
            .progress-bar-bg { background: #f1f5f9 !important; border: 1px solid #cbd5e1 !important; }
            .progress-bar-fill { background: #0f172a !important; }
        }
    </style>
</head>
<body>

    <!-- Bloco Superior de Ações Corporativas -->
    <div class="container my-4 no-print" data-aos="fade-down">
        <div class="action-bar d-flex flex-wrap justify-content-center gap-2 p-3">
            <button class="btn btn-action" onclick="window.print()">
                <i class="fa-solid fa-print"></i> Imprimir Currículo
            </button>
            <button class="btn btn-action" onclick="baixarPDF()">
                <i class="fa-solid fa-file-pdf"></i> Baixar PDF
            </button>
            <button class="btn btn-action" onclick="compartilharEmail()">
                <i class="fa-solid fa-envelope"></i> Enviar por E-mail
            </button>
            <button class="btn btn-action" onclick="compartilharWhatsapp()">
                <i class="fa-brands fa-whatsapp"></i> Compartilhar no WhatsApp
            </button>
            <button class="btn btn-action btn-copy-link" onclick="copiarLink()">
                <i class="fa-solid fa-copy"></i> Copiar Link
            </button>
            <a href="https://linkedin.com" target="_blank" class="btn btn-action">
                <i class="fa-brands fa-linkedin"></i> LinkedIn
            </a>
            <a href="#readme-box" class="btn btn-action text-cyan border-cyan-subtle">
                <i class="fa-brands fa-github"></i> Ver Código README.md
            </a>
        </div>
    </div>

    <!-- Container Principal do Currículo Online -->
    <main class="container main-resume p-4 p-md-5 mb-5" data-aos="fade-up" data-aos-delay="100">
        
        <!-- Header Técnico Corporativo -->
        <header class="row align-items-center header-section border-bottom border-secondary border-opacity-25 pb-4 mb-5">
            <div class="col-md-3 text-center mb-4 mb-md-0">
                <div class="avatar-frame mx-auto d-flex align-items-center justify-content-center">
                    <i class="fa-solid fa-user-shield text-cyan fa-3x"></i>
                </div>
            </div>
            <div class="col-md-9 text-center text-md-start">
                <h1 class="fw-bold tracking-tight text-white mb-2">Flávio Vinício Mota da Silva</h1>
                <p class="lead text-cyan mb-3 fw-medium">Analista e Desenvolvedor de Sistemas</p>
                <div class="d-flex flex-wrap justify-content-center justify-content-md-start gap-2 core-specialties">
                    <span class="badge badge-tech-pill"><i class="fa-solid fa-network-wired me-2 text-purple"></i>Engenharia de Redes</span>
