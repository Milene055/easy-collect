<div align="center">
<img src="https://raw.githubusercontent.com/DP6/templates-centro-de-inovacoes/main/public/images/centro_de_inovacao_dp6.png" height="100px" />
</div>

<p align="center">
  <a href="#badge">
    <img alt="semantic-release" src="https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg">
  </a>
  <a href="https://codecov.io/gh/DP6/easy-collect">
    <img src="https://codecov.io/gh/DP6/easy-collect/branch/master/graph/badge.svg?token=GAQ88UQJQN"/>
  </a>
  <a href="#badge">
    <img alt="Test" src="https://github.com/dp6/easy-collect/actions/workflows/test.yml/badge.svg">
  </a>
  <a href="https://www.codacy.com/gh/DP6/easy-collect/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=DP6/easy-collect&amp;utm_campaign=Badge_Grade">
    <img src="https://app.codacy.com/project/badge/Grade/741dc3805af14444b9e6b4cb9b4269f4"/>
  </a>
</p>

### Idiomas disponíveis

- [Read this page in English](https://github.com/DP6/easy-collect/blob/master/documentations/docs/en/gtm-config-ga4.md)
- [Leia esta página em Português](https://github.com/DP6/easy-collect/blob/master/documentations/docs/pt/gtm-config-ga4.md)

---
# **Configuração do Google Tag Manager - Easy Collect + GA4**

Este documento descreve os passos para a utilização da biblioteca Easy-collect em conjunto com o Google Tag Manager, e as configurações necessárias para coleta de dados via GA4.

## **Indice**
  [1. Configuração do Easy Collect](#1.Configuração-do-Easy-Collect)  
   * [1.1 Tag Easy Collect](#1.1Tag-Easy-Collect)  
   * [1.2 Tag de Configuração GA4](#1.2-Tag-de-Configuração-GA4)  
   * [1.3 Tag coleta Event](#1.3-Tag-coleta-Event)  

      
  [2. Templates](#2.-Templates)  
   * [2.1. Template para coleta somente de *Eventos Recomendados*](###2.1.-Template-para-coleta-somente-de-*Eventos-Recomendados*)      
   * [2.2. Template para coleta somente de *Enhanced Ecommerce*](###2.2.-Template-para-coleta-somente-de-*Enhanced-Ecommerce*)    
   * [2.3. Template para coleta  de *Enhanced Ecommerce* e *Eventos Recomendados*](###-2.3.-Template-para-coleta-de-*Enhanced-Ecommerce*-e-*Eventos-Recomendados*)   

## **1. Configuração do Easy Collect** ⚙️

A seguir um breve tutorial da configuração do Easy Collect em seu Google Tag Manager, lembrando que a configuração pode ser manual ou via template disponivel no tópico (preencher depois).


## **1.1 Tag Easy Collect**       

  O arquivo há ser instalado está presente na pasta [build](https://github.com/DP6/easy-collect/blob/master/build/gtm/main.js), seja ele o arquivo de exemplo disponível neste repositório, ou uma versão personalizada gerada via Gulp, deverá ser copiado integralmente para uma Tag Custom HTML.
 
 - É necessario que as variaveis incorporadas *DebugMode* e *Container ID* estejam habilitadas para seu perfeito funcionamento. 

 - Em configurações avançadas, a opção de executar uma única vez por página deverá ser selecionada.


**Tag Modelo**

![Animação](https://user-images.githubusercontent.com/103647128/188479825-6de619dc-413a-47c2-8054-55bdc13ac0ce.gif)


## **1.2 Tag de Configuração GA4**


 O template utilizado será o padrão de configuração do GA4 , nele deverá ser inserido o id referente ao fluxo de dados/ data streams desejado .
  - Caso o site a ser taggueado seja SPA a opção de envio de evento de visualização de página pode ser ignorada, caso o site seja MPA o uso deste fica a criterio da estrategia de coleta.

**Tag Modelo**
![ga4Configuration](https://user-images.githubusercontent.com/103647128/188482596-6cad3a91-8953-413d-b9d8-1a7b68d32607.gif)


## **1.3 Tag coleta Event**


  Deve-se utilizar o template padrão de eventos do Google Tag Manager para coleta de eventos GA4 com as seguintes configurações:

  - A tag de configuração que contém o id do data streams 
  - Uma variavel de evento personalizado anexada, contendo: *{{event_name}}*
  - O acionador sera um evento personalizado contendo: *{{ga4_event}}*
  - É possivel fazer o envio de parametros para coleta de *enhanced ecommerce* e *eventos personalizados* ja nesta tag de event, exemplos destas configurações estão disponiveis em (colocar os links dos templates, e o link da doc do google de parametros obrigatorios)

  **Tag Modelo**

![ga4Event](https://user-images.githubusercontent.com/103647128/188487990-35e419f8-26c6-43ce-aaf0-2d18006b5a46.gif)

  
## 2. Templates  
  

### 2.1. Template para coleta somente de *Eventos Recomendados*



(descrever o que tem implementado no template e disponibilizar link)

### 2.2. Template para coleta somente de *Enhanced Ecommerce*

(descrever o que tem implementado no template e disponibilizar link)

<a href="https://raw.githubusercontent.com/Milene055/easy-collect/master/docs/pt/template_ecommerce.json" dowload="template_ecommerce.json" type="application/json"> Baixar Template</a>

### 2.3. Template para coleta  de *Enhanced Ecommerce* e *Eventos Recomendados*

