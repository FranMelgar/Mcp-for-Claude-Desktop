🤖 Descripción

Este proyecto implementa un MCP (Model Context Protocol) Server utilizando n8n, permitiendo que Claude Desktop interactúe con herramientas externas y ejecute acciones reales.

El servidor expone múltiples herramientas productivas y un sistema RAG basado en vector store para consultas semánticas.

Convierte a Claude en un agente con capacidades operativas reales.

🧠 Arquitectura General

El workflow utiliza:

MCP Server Trigger

Tools conectadas como ai_tool

Vector Store con embeddings

Servicios Google integrados

Sistema RAG con Pinecone

Claude puede decidir dinámicamente qué herramienta utilizar según la intención del usuario.

🛠️ Herramientas Expuestas
📅 Google Calendar

Crear eventos

Consultar múltiples eventos por rango de fecha

Gestión automática de start/end mediante $fromAI()

📧 Gmail

Envío de emails dinámicos

Generación automática de:

Destinatario

Asunto

Contenido

📊 Google Sheets

Obtener filas existentes

Agregar nuevas filas

Gestión estructurada de columnas:

name

mail

telefon

🧮 Calculator Tool

Permite cálculos matemáticos dinámicos ejecutados directamente por el agente.

🔎 Pinecone Vector Store (RAG)

Recuperación semántica de información

Namespace: n8ndocs

Index: n8ncoursetsla

Embeddings generados con OpenAI

Permite que Claude consulte documentación interna usando búsqueda por similitud vectorial.

🧩 Conexiones Clave

Todas las tools están conectadas al MCP Server Trigger mediante ai_tool.

Pinecone utiliza Embeddings OpenAI para indexación y búsqueda.

Claude decide qué herramienta ejecutar según el contexto.

🚀 Capacidades del Sistema

Este MCP Server permite a Claude:

Crear eventos en calendario

Consultar agenda

Enviar emails

Gestionar hojas de cálculo

Realizar cálculos

Consultar documentación mediante RAG

Operar como agente autónomo con tools externas

🏗️ Tecnologías Utilizadas

n8n

MCP (Model Context Protocol)

Claude Desktop

OpenAI Embeddings

Pinecone

Google Calendar API

Gmail API

Google Sheets API

🔐 Requisitos

n8n (self-hosted recomendado)

Claude Desktop

API Keys:

Google OAuth2

Pinecone

OpenAI

MCP configurado en Claude Desktop

▶️ Instalación

Importar el workflow en n8n.

Configurar todas las credenciales necesarias.

Activar el workflow.

Conectar la URL MCP en Claude Desktop.

Probar ejecución desde Claude.

🧠 Conceptos Implementados

Tool-based AI Architecture

MCP Server Implementation

Retrieval-Augmented Generation (RAG)

Vector Search

AI-controlled external systems

Dynamic parameter injection con $fromAI()

📌 Nivel Técnico

Este proyecto demuestra:

Integración avanzada LLM + herramientas

Arquitectura modular basada en tools

Conexión entre modelos y sistemas reales

Implementación práctica de RAG

Orquestación de servicios externos mediante IA
