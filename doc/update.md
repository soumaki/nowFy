# Nowfy Plugin v1.0.5 - Complete Feature Documentation

## English

### What is Nowfy?

Nowfy is an advanced plugin for exteraGram that allows you to display and control currently playing music with stylized and customizable cards. This version 1.0.5 has been completely refactored, offering better performance, maintainability, and new features.

### Total Features: 85+ Functionalities

#### **Backup & Restore System (6 features)** ⭐ **NEW**
- **Automatic settings backup** - Intelligent backup of all plugin configurations with timestamp
- **Export/Import functionality** - `.export` and `.import` commands for settings management
- **Backup listing** - `.backups` command to view all available backups with file details
- **Version compatibility** - Backup system tracks plugin versions (v1.0.5) for compatibility
- **Progress tracking** - Real-time progress indicators during backup operations (10 stages)
- **Safe restoration** - Verification system ensures settings are applied correctly with confirmation dialogs

**Technical Details:**
- **Storage Location**: `/storage/emulated/0/Android/media/com.exteragram.messenger/nowfy_backups`
- **File Format**: JSON with metadata (version, timestamp, plugin_name, settings)
- **Backup Scope**: All credentials (Spotify, Last.fm, YouTube), cache settings, bio automation, performance modes
- **Automatic Directory Creation**: Creates backup directory if it doesn't exist
- **File Naming**: `nowfy_backup_YYYYMMDD_HHMMSS.json` format
- **Validation System**: Validates backup structure and plugin compatibility before restore
- **Progress Stages**: Directory check → File listing → Selection → Reading → Validation → Current backup → Apply → Verify → Cleanup → Complete
- **Fallback Protection**: Automatically backs up current settings before importing new ones
- **Error Handling**: Comprehensive error logging and user-friendly error messages

#### **Apple UI Advanced Options (4 features)** ⭐ **NEW**
- **Enhanced Apple theme customization** - Advanced options for Apple Light, Dark, and Red themes
- **Refined visual elements** - Improved spacing, typography, and visual hierarchy
- **Adaptive design** - Smart layout adjustments based on content and screen size
- **Premium integration** - Seamless integration with Telegram Premium features

#### **Vinify UI System (7 features)** ⭐ **NEW**
- **ViniBar Settings** - Dedicated configuration panel for ViniBar customization
- **Color management** - Independent control of progress bar and background colors
- **Gradient controls** - Toggle and customize gradient effects with album cover integration
- **Real-time preview** - Live preview of ViniBar appearance during configuration
- **Theme integration** - Seamless integration with existing theme system
- **Album/Playlist Display** ⭐ **NEW** - Show current album or playlist name below artist with bold formatting
- **Device Information** ⭐ **NEW** - Display current playback device above ViniBar with "Device: NAME" format

#### **Custom Caption System (4 features)** ⭐ **NEW**
- **Personalized card captions** - Custom text for music card footers
- **Artist and song integration** - Dynamic insertion of current track information
- **Multi-language support** - Caption customization available in all supported languages
- **Template system** - Predefined caption templates with variable support

#### **Main Commands (24 commands)**
- `.now` - Show current Spotify track
- `.fm` - Show current Last.fm/Stats.fm track
- `.help` - List all available commands
- `.guide` - Setup instructions
- `.connect` - Connect Spotify account
- `.search [term]` - Search Spotify tracks
- `.play [ID]` - Play specific track
- `.pause` - Pause playback
- `.skip` - Next track
- `.back` - Previous track
- `.vol [0-100]` - Control volume
- `.repeat [mode]` - Toggle repeat mode
- `.like now` - Like current track
- `.like [ID]` - Like specific track
- `.list` - Show recently played tracks
- `.bio` - Restore default bio
- `.export` ⭐ **NEW** - Export all settings to backup
- `.import` ⭐ **NEW** - Import settings from backup
- `.backups` ⭐ **NEW** - List all available backups
- `.setid [client_id]` - Set Spotify Client ID
- `.setsecret [client_secret]` - Set Spotify Client Secret
- `.code [authorization_code]` - Exchange authorization code for tokens
- `.check` - Validate Spotify credentials
- `.setuser [username]` - Set Last.fm username
- `.setkey [api_key]` - Set Last.fm API key

#### **Authentication & Credentials System (Multi-platform)**
- **Spotify API Integration**:
  - Client ID and Client Secret configuration
  - Automatic refresh token management
  - Real-time credential validation with `.check` command
  - Secure token exchange via `.code` command
  - Authorization link generation with `.connect`
- **Last.fm API Support**:
  - API Key configuration (create at last.fm/api)
  - Username-based authentication
  - Scrobbling data integration
- **YouTube API (Optional)**:
  - Enhanced music and video cover data
  - Optional API key for improved performance
- **Telegram Bot API**:
  - Bot Token and Channel ID for NowCast
  - Secure message posting and photo uploads
- **Stats.fm Integration**:
  - Username-based Spotify tracking
  - Alternative data source for music information

#### **Supported Services (6 platforms)**
- **Spotify** (via official API)
- **Last.fm** (scrobbling)
- **Stats.fm** (Spotify tracking)
- **YouTube/YouTube Music**
- **SoundCloud**
- **exteraGram/AyuGram** (scrobbling from etg and ayu)

#### **Theme System (8+ themes)**
- **Apple Light** - Clean light theme for Spotify
- **Apple Dark** - Dark theme for Spotify
- **Apple Red** - Red accent theme for Spotify
- **Minimal** - Minimalist design for all services
- **CustomFM** - Fully customizable theme with advanced options
- **External Themes** - Support for third-party themes
- **Random Theme Mode** - Automatic theme rotation
- **Custom Fonts** - Support for custom font selection

#### **ViniBar Progress System (8 features)** ⭐ **NEW**
- **Exclusive Spotify API integration** - Real-time progress tracking
- **Visual progress indicator** - Sleek seekbar overlay on album covers
- **Multiple theme support** - Available in Apple Light, Apple Dark, and Apple Red themes
- **Precise synchronization** - Synchronized with Spotify's current playback position
- **Smart positioning** - Automatically positioned above album artwork
- **ViniBar with Gradient** ⭐ **NEW** - Dynamic gradient progress bar that combines selected colors with album cover colors
- **Customizable colors** - Full control over progress bar and background colors
- **Advanced gradient rendering** - Pixel-perfect gradient implementation with rounded corners and fallback systems

#### **CustomFM Advanced Features (15+ options)**
- **High Resolution Support** ⭐ **NEW**:
  - **1920x1080 image generation** - Ultra-high quality cards for better visual experience
  - **Automatic proportional scaling** - All elements scale perfectly with resolution
  - **Optimized performance** - Smart processing to minimize generation time
  - **Intelligent cache system** - Generated images are cached for instant reuse
- **Background customization**:
  - Album cover background with blur control
  - Custom solid colors (hex support)
  - Custom overlay images via URL
  - Background darkening control
- **Layout options**:
  - Cover positioning (left/right)
  - Adaptive text positioning
- **Styling controls**:
  - Rounded corners (5 levels: Standard, Small, Medium, Large, Circle)
  - Text emphasis (bold text option)
  - Custom text colors (hex support)
  - Service icon colors (colored/monochromatic)
- **Performance Optimizations** ⭐ **NEW**:
  - **Smart image caching** - Cached artwork loading for faster generation
  - **Optimized blur processing** - Enhanced blur algorithms for high resolution
  - **Fallback system** - Multiple sources for album artwork with priority system

#### **Advanced Cache System (18+ options)**
- **Multi-layer cache** - Persistent cache between restarts
- **YouTube thumbnail cache** - Stores YouTube thumbnails for faster access
- **SoundCloud thumbnail cache** - SoundCloud-specific cache system
- **CustomFM image cache** ⭐ **NEW** - Intelligent caching of generated CustomFM cards
- **Multi-resolution cache** - Different quality levels
- **Adaptive compression** - Automatically adjusts quality based on connection speed
- **URL cache** - Cache of valid thumbnail URLs
- **Quality fallback** - Tries different qualities if main one fails
- **Performance modes** - Turbo, Balanced, Quality
- **TTL configuration** - Configurable cache lifetime (1 hour for CustomFM)
- **Enhanced cache optimizations** - Advanced cache system for better performance
- **Preloading** - Automatically loads next tracks from playlist
- **Image compression** - Compress images to save space
- **Cache management** - Manual cache control
- **Persistent storage** - Cache survives app restarts
- **Smart cleanup** - Automatic cache maintenance
- **Hash-based caching** ⭐ **NEW** - Unique cache keys based on track metadata
- **Automatic cache invalidation** ⭐ **NEW** - Smart cache expiration and cleanup

#### **Bio Automation (8 features)**
- **Automatic bio updates** - Updates bio with current track
- **Custom bio text** - Personalized bio text with variables
- **Variable support** - {track} and {artist} placeholders
- **Default bio restoration** - .bio command for manual restoration
- **Bio notifications** - Alerts for bio changes
- **Original bio capture** - Automatically saves original bio
- **70-character limit** - Telegram bio limit compliance
- **Smart bio management** - Intelligent bio handling

#### **Configuration Interface (4 main sections)**
- **Main Settings**: Credentials, themes, captions, exteraBar, fonts
- **Advanced Options**: Custom commands, bio automation, performance, chat integration
- **Last.fm/Stats.fm Settings**: Player detection, API configuration, theme customization
- **Premium Features**: Premium emoji support, enhanced UI elements

#### **Performance Features (8 optimizations)**
- **Smart player detection** - Automatic detection of active music player
- **Intelligent link generation** - Context-aware link creation
- **Robust fallback system** - Multiple backup options
- **Image compression** - Space-saving optimizations with adaptive quality:
  - **Quality Mode**: 95% compression for maximum visual fidelity
  - **Balanced Mode**: 85% compression for optimal balance
  - **Turbo Mode**: 75% compression for fastest processing
- **Optimized cache** - Enhanced responsiveness with multi-layer caching
- **Configurable timeouts** - API timeout management (3s-7s cache, 5s-15s requests)
- **Connection speed adaptation** - Quality adjustment based on connection speed
- **Resource management** - Efficient memory usage with 600s inactivity timeout

#### **Performance Modes (3 optimization levels)**
- **Turbo Mode** - Maximum speed with 2-second timeout, 75% image compression
- **Balanced Mode** - Optimal balance with 3-second timeout, 85% image compression  
- **Quality Mode** - Maximum quality with 4-second timeout, 95% image compression
- **Adaptive timeouts** - Dynamic timeout adjustment based on selected mode
- **Smart compression** - JPEG optimization with automatic quality adjustment
- **Connection-based adaptation** - Quality automatically adjusts to connection speed

#### **Premium Features (2 functionalities)**
- **Premium Emoji Support** - Synchronization of premium emojis (requires Telegram Premium subscription)
- **Enhanced UI Elements** - Advanced interface components and visual improvements

#### **Technical Specifications**
- **User-Agent Optimization** - Multiple Chrome User-Agents (4+ variations) to prevent blocking
- **Smart HTTP Headers** - Service-specific headers (NowfyPlugin/1.0, Nowfy/1.0)
- **Hash-based Caching** - Unique cache keys based on track metadata for optimal performance
- **Automatic Cache Invalidation** - Smart cache expiration and cleanup system
- **Multi-resolution Support** - Different quality levels with fallback system
- **Persistent Storage** - Cache survives app restarts with intelligent cleanup

#### **Multilingual Support (5 languages)**
- **Portuguese** - Complete translation with Brazilian Portuguese localization
- **English** - Full English support with US/UK compatibility
- **Spanish** - Comprehensive Spanish translation
- **French** - Complete French localization
- **Russian** - Full Russian language support
- **Dynamic Language Detection** - Automatic language detection based on Telegram settings
- **Contextual Translations** - Service-specific translations for better user experience

#### **Chat Integration (4 features)**
- **Configurable chat menu** - Show/hide in chat menu with dynamic visibility control
- **Customizable notifications** - Notification preferences with bio change alerts
- **Custom captions** - Personalized card captions with dynamic variables:
  - **Variable Support**: `{track}` and `{artist}` placeholders
  - **Template System**: Predefined caption templates
  - **Multi-language Support**: Caption customization in all supported languages
  - **Real-time Preview**: Instant preview of caption changes
- **Smart links** - Intelligent link generation with multiple fallback options

#### **Smart Link System (6 link types)**
- **Spotify** - Direct link to track with automatic URL generation
- **YouTube/YouTube Music** - Search based on title/artist with intelligent query formatting
- **SoundCloud** - SoundCloud search with optimized search parameters
- **song.link** - Universal music links for .fm players with cross-platform compatibility
- **Last.FM/Stats.FM** - Profile links with user-specific URLs
- **Custom links** - User-defined link preferences with template support

#### **NowCast Enhanced Integration (4 advanced features)** ⭐ **NEW**
- **Telegram Bot API Integration** - Automatic posting to Telegram channels with rate limiting
- **Interactive Buttons** - 4 button types (None, Button, Button & Profile, Profile Only)
- **Advanced Caption System** - Bot captions with dynamic placeholder processing (`{track}`, `{artist}`)
- **Connection Testing** - Built-in bot connectivity validation with multilingual feedback

#### **Vinify UI System (7 advanced features)** ⭐ **NEW**
- **ViniBar Configuration Panel** - Dedicated configuration panel for ViniBar customization
- **Independent Color Management** - Separate control for progress bar and background colors
- **Gradient Controls** - Toggle and customize gradient effects with album cover integration
- **Real-time Preview** - Live preview of ViniBar appearance during configuration
- **Theme Integration** - Seamless integration with existing theme system
- **Album/Playlist Display** - Show current album or playlist name below artist with bold formatting
- **Device Information Display** - Show current playback device above ViniBar in "Device: NAME" format

#### **Advanced Device Management (6+ features)** ⭐ **NEW**
- **Automatic Device Selection** - Automatically selects active Spotify device
- **Manual Device Override** - Choose specific playback device
- **Real-time Device Updates** - Live updates of device list
- **Device Type Detection** - Identifies computers, smartphones, speakers
- **Connection Status Monitoring** - Monitors device connectivity and availability
- **Smart Fallback** - Automatic fallback to available devices

#### **Bio Automation System (8+ features)** ⭐ **NEW**
- **Automatic Bio Updates** - Automatically updates Telegram bio with current track
- **Custom Bio Templates** - Personalized bio text with dynamic placeholders
- **Real-time Synchronization** - Bio updates synchronized with music changes
- **Smart Fallback Handling** - Intelligent fallback when no music is playing
- **Multi-service Support** - Works with Spotify, Last.fm, and Stats.fm
- **Template Variables** - Support for `{track}`, `{artist}`, `{album}` placeholders
- **Manual Bio Restoration** - Easy restoration to default bio
- **Error Handling** - Graceful error management with user feedback

---

## Português

### O que é o Nowfy?

O Nowfy é um plugin avançado para exteraGram que permite exibir e controlar a música que está tocando atualmente com cards estilizados e personalizáveis. Esta versão 1.0.5 foi completamente refatorada, oferecendo melhor performance, manutenibilidade e novos recursos.

### Total de Recursos: 85+ Funcionalidades

#### **Sistema de Backup e Restauração (6 recursos)** ⭐ **NOVO**
- **Backup automático de configurações** - Backup inteligente de todas as configurações do plugin
- **Funcionalidade de Exportar/Importar** - Comandos `.export` e `.import` para gerenciamento de configurações
- **Listagem de backups** - Comando `.backups` para visualizar todos os backups disponíveis
- **Compatibilidade de versão** - Sistema de backup rastreia versões do plugin para compatibilidade
- **Rastreamento de progresso** - Indicadores de progresso em tempo real durante operações de backup
- **Restauração segura** - Sistema de verificação garante que as configurações sejam aplicadas corretamente

#### **Opções Avançadas do Apple UI (4 recursos)** ⭐ **NOVO**
- **Personalização aprimorada do tema Apple** - Opções avançadas para temas Apple Light, Dark e Red
- **Elementos visuais refinados** - Espaçamento, tipografia e hierarquia visual aprimorados
- **Design adaptativo** - Ajustes inteligentes de layout baseados no conteúdo e tamanho da tela
- **Integração premium** - Integração perfeita com recursos do Telegram Premium

#### **Sistema Vinify UI (7 recursos)** ⭐ **NOVO**
- **Configurações da ViniBar** - Painel de configuração dedicado para personalização da ViniBar
- **Gerenciamento de cores** - Controle independente das cores da barra de progresso e fundo
- **Controles de gradiente** - Alternar e personalizar efeitos de gradiente com integração da capa do álbum
- **Visualização em tempo real** - Pré-visualização ao vivo da aparência da ViniBar durante a configuração
- **Integração de tema** - Integração perfeita com o sistema de temas existente
- **Exibição de Álbum/Playlist** ⭐ **NOVO** - Mostrar nome do álbum ou playlist atual abaixo do artista com formatação em negrito
- **Informações do Dispositivo** ⭐ **NOVO** - Exibir dispositivo de reprodução atual acima da ViniBar no formato "Device: NOME"

#### **Sistema de Legenda Personalizada (4 recursos)** ⭐ **NOVO**
- **Legendas de card personalizadas** - Texto personalizado para rodapés de cards de música
- **Integração de artista e música** - Inserção dinâmica de informações da faixa atual
- **Suporte multilíngue** - Personalização de legenda disponível em todos os idiomas suportados
- **Sistema de templates** - Templates de legenda predefinidos com suporte a variáveis

#### **Comandos Principais (24 comandos)**
- `.now` - Mostrar faixa atual do Spotify
- `.fm` - Mostrar faixa atual do Last.fm/Stats.fm
- `.help` - Listar todos os comandos disponíveis
- `.guide` - Instruções de configuração
- `.connect` - Conectar conta do Spotify
- `.search [termo]` - Buscar faixas no Spotify
- `.play [ID]` - Reproduzir faixa específica
- `.pause` - Pausar reprodução
- `.skip` - Próxima faixa
- `.back` - Faixa anterior
- `.vol [0-100]` - Controlar volume
- `.repeat [modo]` - Alternar modo de repetição
- `.like now` - Curtir faixa atual
- `.like [ID]` - Curtir música específica
- `.list` - Mostrar músicas tocadas recentemente
- `.bio` - Restaurar bio padrão
- `.export` ⭐ **NOVO** - Exportar todas as configurações para backup
- `.import` ⭐ **NOVO** - Importar configurações do backup
- `.backups` ⭐ **NOVO** - Listar todos os backups disponíveis
- `.setid [client_id]` - Definir Client ID do Spotify
- `.setsecret [client_secret]` - Definir Client Secret do Spotify
- `.code [codigo_autorizacao]` - Trocar código de autorização por tokens
- `.check` - Validar credenciais do Spotify
- `.setuser [usuario]` - Definir usuário do Last.fm
- `.setkey [api_key]` - Definir chave da API do Last.fm

#### **Sistema de Postagem Automática NowCast (15+ recursos)** ⭐ **NOVO**
- **Detecção automática de música** - Monitoramento em tempo real da reprodução do Spotify
- **Lógica inteligente de postagem** - Previne posts duplicados e gerencia intervalos de postagem
- **Integração com bot do Telegram** - Postagem direta em canais via API do bot
- **Integração com Link Options** - Suporte completo para Spotify e Song.link baseado nas configurações
- **Botões interativos** - 4 modos de botão: Nenhum, Botão, Botão & Perfil, Apenas Perfil
- **Legendas dinâmicas** - Legendas personalizadas com placeholders: `{track}`, `{artist}`
- **Automação de legendas** - Atualização automática de legendas com informações da faixa atual
- **Teste de conexão** - Validação integrada de conectividade do bot
- **Gerenciamento de histórico** - Limpar histórico de postagens para permitir reposts
- **Suporte multilíngue** - Mensagens e tratamento de erros localizados
- **Monitoramento de status beta** - Implementação beta segura sem afetar o plugin principal
- **Validação de configuração** - Validação automática do token do bot e ID do canal
- **Rate limiting inteligente** - Respeita limites da API do Telegram com intervalos mínimos de 60 segundos
- **Cooldown de posts** - Intervalo mínimo de 30 segundos entre posts do NowCast para evitar spam
- **Cache com limpeza automática** - Limpeza automática do cache a cada 3600 segundos (1 hora)
- **Auto-desligamento por inatividade** - Desliga automaticamente após 10 minutos sem atividade musical
- **Sistema de recuperação de erros** - Reset automático após 5 erros consecutivos com timeouts adaptativos:
  - **Timeouts progressivos**: 45s + (erros × 15s), máximo 90s entre tentativas
  - **Timeouts de erro**: 30s + (erros × 15s), máximo 2 minutos para recuperação
  - **Reset automático**: Contador de erros zerado após operação bem-sucedida
  - **Sleep intervals adaptativos**: 2s (Turbo), 3s (Balanceado), 4s (Qualidade) baseados no modo de performance

#### **Sistema de Automação de Bio (8+ recursos)** ⭐ **NOVO**
- **Atualização automática de bio** - Atualiza automaticamente a bio do Telegram com a faixa atual
- **Templates de bio personalizados** - Texto de bio personalizado com placeholders dinâmicos
- **Sincronização em tempo real** - Atualizações de bio sincronizadas com mudanças de música
- **Tratamento de fallback** - Fallback inteligente quando nenhuma música está tocando
- **Suporte multi-serviço** - Funciona com Spotify, Last.fm e Stats.fm
- **Variáveis de template** - Suporte para placeholders `{track}`, `{artist}`, `{album}`
- **Restauração manual de bio** - Restauração fácil para bio padrão
- **Tratamento de erros** - Gerenciamento gracioso de erros com feedback ao usuário

#### **Sistema de Gerenciamento de Dispositivos (6+ recursos)** ⭐ **NOVO**
- **Seleção automática de dispositivo** - Seleciona automaticamente o dispositivo ativo do Spotify
- **Substituição manual de dispositivo** - Escolha dispositivo específico de reprodução
- **Atualização de dispositivos** - Atualizações em tempo real da lista de dispositivos
- **Detecção de tipo de dispositivo** - Identifica computadores, smartphones, alto-falantes
- **Status de conexão** - Monitora conectividade e disponibilidade do dispositivo
- **Fallback inteligente** - Fallback automático para dispositivos disponíveis

#### **Serviços Suportados (6 plataformas)**
- **Spotify** (via API oficial)
- **Last.fm** (scrobbling)
- **Stats.fm** (tracking do Spotify)
- **YouTube/YouTube Music**
- **SoundCloud**
- **exteraGram/AyuGram** (scrobbling from etg and ayu)

#### **Sistema de Temas (8+ temas)**
- **Apple Light** - Tema claro limpo para Spotify
- **Apple Dark** - Tema escuro para Spotify
- **Apple Red** - Tema com destaque vermelho para Spotify
- **Minimal** - Design minimalista para todos os serviços
- **CustomFM** - Tema totalmente personalizável com opções avançadas
- **Temas Externos** - Suporte para temas de terceiros
- **Modo Tema Aleatório** - Rotação automática de temas
- **Fontes Personalizadas** - Suporte para seleção de fontes customizadas

#### **Sistema de Progresso ViniBar (8 recursos)** ⭐ **NOVO**
- **Integração exclusiva com API do Spotify** - Rastreamento de progresso em tempo real
- **Indicador visual de progresso** - Barra de busca elegante sobre as capas dos álbuns
- **Suporte a múltiplos temas** - Disponível nos temas Apple Light, Apple Dark e Apple Red
- **Sincronização precisa** - Sincronizado com a posição atual de reprodução do Spotify
- **Posicionamento inteligente** - Automaticamente posicionado acima da capa do álbum
- **ViniBar com Gradiente** ⭐ **NOVO** - Barra de progresso com gradiente dinâmico que combina cores selecionadas com cores da capa do álbum
- **Cores personalizáveis** - Controle total sobre as cores da barra de progresso e fundo
- **Renderização avançada de gradiente** - Implementação pixel-perfect de gradiente com cantos arredondados e sistemas de fallback

#### **Recursos Avançados do CustomFM (15+ opções)**
- **Suporte à Alta Resolução** ⭐ **NOVO**:
  - **Geração de imagens em 1920x1080** - Cards de ultra alta qualidade para melhor experiência visual
  - **Escalonamento proporcional automático** - Todos os elementos escalam perfeitamente com a resolução
  - **Performance otimizada** - Processamento inteligente para minimizar o tempo de geração
  - **Sistema de cache inteligente** - Imagens geradas são armazenadas em cache para reutilização instantânea
- **Personalização de fundo**:
  - Fundo da capa do álbum com controle de blur
  - Cores sólidas personalizadas (suporte hex)
  - Imagens de overlay personalizadas via URL
  - Controle de escurecimento do fundo
- **Opções de layout**:
  - Posicionamento da capa (esquerda/direita)
  - Posicionamento adaptativo do texto
- **Controles de estilo**:
  - Cantos arredondados (5 níveis: Padrão, Pequeno, Médio, Grande, Círculo)
  - Ênfase do texto (opção de texto em negrito)
  - Cores de texto personalizadas (suporte hex)
  - Cores dos ícones de serviço (colorido/monocromático)
- **Configurações avançadas de qualidade para temas Apple**:
  - **Qualidade de antialiasing** - 4 níveis (Padrão, Suave, Ultra Suave, Máxima Qualidade)
  - **Qualidade da mini capa** - 3 níveis (Padrão, Alta, Ultra)
  - **Sistema de fallback inteligente** - SoundCloud para YouTube, Last.FM como backup
- **Processamento avançado de imagens**:
  - **Redimensionamento automático de thumbnails** - Padronização para 450x450 pixels
  - **Aplicação de cantos arredondados** - Raio de 20px para mini capas nos temas Apple
  - **Renderização pixel-perfect** - Algoritmos otimizados para máxima qualidade visual
- **Otimizações de Performance** ⭐ **NOVO**:
  - **Cache inteligente de imagens** - Carregamento de capas em cache para geração mais rápida
  - **Processamento de blur otimizado** - Algoritmos de blur aprimorados para alta resolução
  - **Sistema de fallback** - Múltiplas fontes para capas de álbum com sistema de prioridade
  - **URLs de alta qualidade** - Conversão automática para resolução t500x500 (SoundCloud)
  - **Fallback de qualidade do YouTube** - 5 níveis de qualidade (maxres, sd, hq, mq, default)

#### **Sistema de Cache Avançado (22+ opções)**
- **Cache multicamadas** - Cache persistente entre reinicializações
- **Cache de thumbnails do YouTube** - Armazena thumbnails do YouTube para acesso mais rápido
- **Cache de thumbnails do SoundCloud** - Sistema de cache específico para SoundCloud
- **Cache de imagens CustomFM** ⭐ **NOVO** - Cache inteligente de cards CustomFM gerados
- **Cache multi-resolução** - Diferentes níveis de qualidade
- **Compressão adaptativa** - Ajusta qualidade automaticamente baseada na velocidade de conexão
- **Cache de URLs** - Cache de URLs de thumbnails válidas
- **Fallback de qualidade** - Tenta diferentes qualidades se a principal falhar
- **Modos de performance** - Turbo (2s), Balanceado (3s), Qualidade (4s) com timeouts adaptativos
- **Configuração TTL** - Tempo de vida do cache configurável (padrão: 5 minutos, URLs válidas: 10 minutos)
- **Tamanho máximo de cache** - Limite configurável de itens no cache (padrão: 10 itens)
- **Limpeza automática de cache** - Limpeza preventiva a cada hora (3600 segundos)
- **Otimizações de cache avançadas** - Sistema de cache avançado para melhor performance
- **Pré-carregamento** - Carrega automaticamente as próximas faixas da playlist
- **Compressão de imagens** - Comprimir imagens para economizar espaço com qualidade adaptativa:
  - **Qualidade baseada no modo de performance**: 95% (Qualidade), 85% (Balanceado), 75% (Turbo)
  - **Compressão JPEG otimizada** com algoritmos de otimização automática
  - **Compressão adaptativa baseada na conexão** - Ajusta qualidade automaticamente
- **Gerenciamento de cache** - Controle manual do cache
- **Armazenamento persistente** - Cache sobrevive a reinicializações do app
- **Limpeza inteligente** - Manutenção automática do cache
- **Cache baseado em hash** ⭐ **NOVO** - Chaves de cache únicas baseadas em metadados da faixa
- **Invalidação automática de cache** ⭐ **NOVO** - Expiração e limpeza inteligente do cache
- **Cache otimizado por performance** - Timeouts adaptativos baseados no modo de performance selecionado
- **Sistema de fallback de cache** - URLs válidas permanecem em cache por período estendido

#### **Automação de Bio (10 recursos)**
- **Atualização automática da bio** - Atualiza a bio com a faixa atual
- **Texto de bio personalizado** - Texto de bio personalizado com variáveis
- **Suporte a variáveis** - Placeholders {track} e {artist}
- **Restauração de bio padrão** - Comando .bio para restauração manual
- **Notificações de bio** - Alertas para mudanças na bio
- **Captura da bio original** - Salva automaticamente a bio original
- **Limite de 70 caracteres** - Conformidade com limite de bio do Telegram
- **Gerenciamento inteligente de bio** - Manipulação inteligente da bio
- **Rate limiting do Telegram** - Proteção contra bloqueio temporário por mudanças frequentes na bio
- **Timeouts configuráveis** - Timeouts adaptativos para evitar travamentos na API do Telegram
- **Limite de caracteres rigoroso** - Conformidade com limite de 70 caracteres do Telegram
- **Detecção de bloqueio temporário** - Sistema inteligente que detecta e evita rate limiting

#### **Interface de Configuração (4 seções principais)**
- **Configurações Principais**: Credenciais, temas, legendas, exteraBar, fontes
- **Opções Avançadas**: Comandos personalizados, automação de bio, performance, integração de chat
- **Configurações Last.fm/Stats.fm**: Detecção de player, configuração de API, personalização de tema
- **Recursos Premium**: Suporte a emoji premium, elementos de UI aprimorados

#### **Recursos de Performance (10 otimizações)**
- **Detecção inteligente de player** - Detecção automática do player de música ativo
- **Geração inteligente de links** - Criação de links com base no contexto
- **Sistema de fallback robusto** - Múltiplas opções de fallback
- **Compressão de imagens** - Otimizações para economizar espaço
- **Cache otimizado** - Responsividade aprimorada
- **Timeouts configuráveis** - Controle de timeout da API (3s-7s para cache, 5s-15s para requisições)
- **Intervalos de inatividade** - Timeout de inatividade de 600 segundos (10 minutos) para otimização de recursos
- **Adaptação à velocidade de conexão** - Ajuste de qualidade baseado na conexão
- **Gerenciamento de recursos** - Uso eficiente de memória
- **User-Agents otimizados** - Múltiplos User-Agents Chrome para evitar bloqueios (4+ variações)
- **Headers HTTP inteligentes** - Headers customizados por serviço (NowfyPlugin/1.0, Nowfy/1.0)

#### **Recursos Premium (2 funcionalidades)**
- **Suporte a Emoji Premium** - Sincronização de emojis premium (requer assinatura Telegram Premium)
- **Elementos de UI Aprimorados** - Componentes de interface avançados e melhorias visuais

#### **Suporte Multilíngue (5 idiomas)**
- Português
- Inglês
- Espanhol
- Francês
- Russo

#### **Integração com Chat (4 recursos)**
- **Menu do chat configurável** - Mostrar/ocultar no menu do chat
- **Notificações personalizáveis** - Preferências de notificação
- **Legendas personalizadas** - Legendas de card personalizadas
- **Links inteligentes** - Links do Spotify/faixas

#### **Sistema de Links Inteligentes (6 tipos de links)**
- **Spotify** - Link direto para a faixa
- **YouTube/YouTube Music** - Busca baseada em título/artista
- **SoundCloud** - Busca no SoundCloud
- **song.link** - Links universais de música para players .fm
- **Last.FM/Stats.FM** - Links de perfil
- **Links personalizados** - Preferências de link definidas pelo usuário

---

## Español

### ¿Qué es Nowfy?

Nowfy es un plugin avanzado para exteraGram que permite mostrar y controlar la música que se está reproduciendo actualmente con tarjetas estilizadas y personalizables. Esta versión 1.0.5 ha sido completamente refactorizada, ofreciendo mejor rendimiento, mantenibilidad y nuevas características.

### Total de Características: 85+ Funcionalidades

#### **Sistema de Backup y Restauración (6 características)** ⭐ **NUEVO**
- **Backup automático de configuraciones** - Backup inteligente de todas las configuraciones del plugin
- **Funcionalidad de Exportar/Importar** - Comandos `.export` e `.import` para gestión de configuraciones
- **Listado de backups** - Comando `.backups` para visualizar todos los backups disponibles
- **Compatibilidad de versión** - Sistema de backup rastrea versiones del plugin para compatibilidad
- **Seguimiento de progreso** - Indicadores de progreso en tiempo real durante operaciones de backup
- **Restauración segura** - Sistema de verificación garantiza que las configuraciones se apliquen correctamente

#### **Opciones Avanzadas de Apple UI (4 características)** ⭐ **NUEVO**
- **Personalización mejorada del tema Apple** - Opciones avanzadas para temas Apple Light, Dark y Red
- **Elementos visuales refinados** - Espaciado, tipografía y jerarquía visual mejorados
- **Diseño adaptativo** - Ajustes inteligentes de diseño basados en contenido y tamaño de pantalla
- **Integración premium** - Integración perfecta con características de Telegram Premium

#### **Sistema Vinify UI (7 características)** ⭐ **NUEVO**
- **Configuraciones de ViniBar** - Panel de configuración dedicado para personalización de ViniBar
- **Gestión de colores** - Control independiente de colores de barra de progreso y fondo
- **Controles de gradiente** - Alternar y personalizar efectos de gradiente con integración de portada de álbum
- **Vista previa en tiempo real** - Vista previa en vivo de la apariencia de ViniBar durante configuración
- **Integración de tema** - Integración perfecta con sistema de temas existente
- **Visualización de Álbum/Playlist** ⭐ **NUEVO** - Mostrar nombre del álbum o playlist actual debajo del artista con formato en negrita
- **Información del Dispositivo** ⭐ **NUEVO** - Mostrar dispositivo de reproducción actual arriba de ViniBar en formato "Device: NOMBRE"

#### **Sistema de Leyenda Personalizada (4 características)** ⭐ **NUEVO**
- **Leyendas de tarjeta personalizadas** - Texto personalizado para pies de tarjetas de música
- **Integración de artista y canción** - Inserción dinámica de información de la pista actual
- **Soporte multiidioma** - Personalización de leyenda disponible en todos los idiomas soportados
- **Sistema de plantillas** - Plantillas de leyenda predefinidas con soporte de variables

#### **Comandos Principales (24 comandos)**
- `.now` - Mostrar pista actual de Spotify
- `.fm` - Mostrar pista actual de Last.fm/Stats.fm
- `.help` - Listar todos los comandos disponibles
- `.guide` - Instrucciones de configuración
- `.connect` - Conectar cuenta de Spotify
- `.search [término]` - Buscar pistas en Spotify
- `.play [ID]` - Reproducir pista específica
- `.pause` - Pausar reproducción
- `.skip` - Siguiente pista
- `.back` - Pista anterior
- `.vol [0-100]` - Controlar volumen
- `.repeat [modo]` - Alternar modo de repetición
- `.like now` - Me gusta a la pista actual
- `.like [ID]` - Me gusta a pista específica
- `.list` - Mostrar pistas reproducidas recientemente
- `.bio` - Restaurar biografía predeterminada
- `.export` ⭐ **NUEVO** - Exportar todas las configuraciones a backup
- `.import` ⭐ **NUEVO** - Importar configuraciones desde backup
- `.backups` ⭐ **NUEVO** - Listar todos los backups disponibles
- `.setid [client_id]` - Definir Client ID de Spotify
- `.setsecret [client_secret]` - Definir Client Secret de Spotify
- `.code [codigo_autorizacion]` - Intercambiar código de autorización por tokens
- `.check` - Validar credenciales de Spotify
- `.setuser [usuario]` - Definir usuario de Last.fm
- `.setkey [api_key]` - Definir clave API de Last.fm

#### **Servicios Soportados (6 plataformas)**
- **Spotify** (vía API oficial)
- **Last.fm** (scrobbling)
- **Stats.fm** (seguimiento de Spotify)
- **YouTube/YouTube Music**
- **SoundCloud**
- **exteraGram/AyuGram** (scrobbling from etg and ayu)

#### **Sistema de Temas (8+ temas)**
- **Apple Light** - Tema claro limpio para Spotify
- **Apple Dark** - Tema oscuro para Spotify
- **Apple Red** - Tema con acento rojo para Spotify
- **Minimal** - Diseño minimalista para todos los servicios
- **CustomFM** - Tema completamente personalizable con opciones avanzadas
- **Temas Externos** - Soporte para temas de terceros
- **Modo Tema Aleatorio** - Rotación automática de temas
- **Fuentes Personalizadas** - Soporte para selección de fuentes personalizadas

#### **Sistema de Progreso ViniBar (8 características)** ⭐ **NUEVO**
- **Integración exclusiva con API de Spotify** - Seguimiento de progreso en tiempo real
- **Indicador visual de progreso** - Barra de búsqueda elegante sobre las portadas de álbumes
- **Soporte para múltiples temas** - Disponible en temas Apple Light, Apple Dark y Apple Red
- **Sincronización precisa** - Sincronizado con la posición actual de reproducción de Spotify
- **Posicionamiento inteligente** - Automáticamente posicionado sobre la portada del álbum
- **ViniBar con Gradiente** ⭐ **NUEVO** - Barra de progreso con gradiente dinámico que combina colores seleccionados con colores de portada de álbum
- **Colores personalizables** - Control total sobre colores de barra de progreso y fondo
- **Renderizado avanzado de gradiente** - Implementación pixel-perfect de gradiente con esquinas redondeadas y sistemas de respaldo

#### **Características Avanzadas de CustomFM (15+ opciones)**
- **Soporte de Alta Resolución** ⭐ **NUEVO**:
  - **Generación de imágenes en 1920x1080** - Tarjetas de ultra alta calidad para mejor experiencia visual
  - **Escalado proporcional automático** - Todos los elementos escalan perfectamente con la resolución
  - **Rendimiento optimizado** - Procesamiento inteligente para minimizar el tiempo de generación
  - **Sistema de caché inteligente** - Las imágenes generadas se almacenan en caché para reutilización instantánea
- **Personalización de fondo**:
  - Fondo de portada de álbum con control de desenfoque
  - Colores sólidos personalizados (soporte hex)
  - Imágenes de superposición personalizadas vía URL
  - Control de oscurecimiento del fondo
- **Opciones de diseño**:
  - Posicionamiento de portada (izquierda/derecha)
  - Posicionamiento adaptativo del texto
- **Controles de estilo**:
  - Esquinas redondeadas (5 niveles: Estándar, Pequeño, Mediano, Grande, Círculo)
  - Énfasis del texto (opción de texto en negrita)
  - Colores de texto personalizados (soporte hex)
  - Colores de iconos de servicio (colorido/monocromático)
- **Optimizaciones de Rendimiento** ⭐ **NUEVO**:
  - **Caché inteligente de imágenes** - Carga de portadas en caché para generación más rápida
  - **Procesamiento de desenfoque optimizado** - Algoritmos de desenfoque mejorados para alta resolución
  - **Sistema de respaldo** - Múltiples fuentes para portadas de álbum con sistema de prioridad

#### **Sistema de Caché Avanzado (18+ opciones)**
- **Caché multicapa** - Caché persistente entre reinicios
- **Caché de miniaturas de YouTube** - Almacena miniaturas de YouTube para acceso más rápido
- **Caché de miniaturas de SoundCloud** - Sistema de caché específico para SoundCloud
- **Caché de imágenes CustomFM** ⭐ **NUEVO** - Caché inteligente de tarjetas CustomFM generadas
- **Caché multi-resolución** - Diferentes niveles de calidad
- **Compresión adaptativa** - Ajusta automáticamente la calidad según la velocidad de conexión
- **Caché de URLs** - Caché de URLs de miniaturas válidas
- **Respaldo de calidad** - Intenta diferentes calidades si la principal falla
- **Modos de rendimiento** - Turbo, Equilibrado, Calidad
- **Configuración TTL** - Tiempo de vida del caché configurable (1 hora para CustomFM)
- **Optimizaciones de caché avanzadas** - Sistema de caché avanzado para mejor rendimiento
- **Precarga** - Carga automáticamente las próximas pistas de la lista
- **Compresión de imágenes** - Comprimir imágenes para ahorrar espacio
- **Gestión de caché** - Control manual del caché
- **Almacenamiento persistente** - El caché sobrevive a reinicios de la app
- **Limpieza inteligente** - Mantenimiento automático del caché
- **Caché basado en hash** ⭐ **NUEVO** - Claves de caché únicas basadas en metadatos de la pista
- **Invalidación automática de caché** ⭐ **NUEVO** - Expiración y limpieza inteligente del caché

#### **Automatización de Bio (8 características)**
- **Actualizaciones automáticas de bio** - Actualiza la bio con la pista actual
- **Texto de bio personalizado** - Texto de bio personalizado con variables
- **Soporte de variables** - Marcadores {track} y {artist}
- **Restauración de bio predeterminada** - Comando .bio para restauración manual
- **Notificaciones de bio** - Alertas para cambios en la bio
- **Captura de bio original** - Guarda automáticamente la bio original
- **Límite de 70 caracteres** - Cumplimiento con límite de bio de Telegram
- **Gestión inteligente de bio** - Manejo inteligente de la bio

#### **Interfaz de Configuración (4 secciones principales)**
- **Configuraciones Principales**: Credenciales, temas, leyendas, exteraBar, fuentes
- **Opciones Avanzadas**: Comandos personalizados, automatización de bio, rendimiento, integración de chat
- **Configuraciones Last.fm/Stats.fm**: Detección de reproductor, configuración de API, personalización de tema
- **Características Premium**: Soporte de emoji premium, elementos de UI mejorados

#### **Características de Rendimiento (8 optimizaciones)**
- **Detección inteligente de reproductor** - Detección automática del reproductor de música activo
- **Generación inteligente de enlaces** - Creación de enlaces consciente del contexto
- **Sistema de respaldo robusto** - Múltiples opciones de respaldo
- **Compresión de imágenes** - Optimizaciones para ahorrar espacio
- **Caché optimizado** - Capacidad de respuesta mejorada
- **Timeouts configurables** - Gestión de timeout de API
- **Adaptación a velocidad de conexión** - Ajuste de calidad basado en la conexión
- **Gestión de recursos** - Uso eficiente de memoria

#### **Características Premium (2 funcionalidades)**
- **Soporte de Emoji Premium** - Sincronización de emojis premium (requiere suscripción Telegram Premium)
- **Elementos de UI Mejorados** - Componentes de interfaz avanzados y mejoras visuales

#### **Soporte Multiidioma (5 idiomas)**
- Portugués
- Inglés
- Español
- Francés
- Ruso

#### **Integración de Chat (4 características)**
- **Menú de chat configurable** - Mostrar/ocultar en el menú de chat
- **Notificaciones personalizables** - Preferencias de notificación
- **Leyendas personalizadas** - Leyendas de tarjeta personalizadas
- **Enlaces inteligentes** - Enlaces de Spotify/pistas

#### **Sistema de Enlaces Inteligentes (6 tipos de enlaces)**
- **Spotify** - Enlace directo a la pista
- **YouTube/YouTube Music** - Búsqueda basada en título/artista
- **SoundCloud** - Búsqueda en SoundCloud
- **song.link** - Enlaces universales de música para reproductores .fm
- **Last.FM/Stats.FM** - Enlaces de perfil
- **Enlaces personalizados** - Preferencias de enlace definidas por el usuario

---

## Français

### Qu'est-ce que Nowfy?

Nowfy est un plugin avancé pour exteraGram qui permet d'afficher et de contrôler la musique en cours de lecture avec des cartes stylisées et personnalisables. Cette version 1.0.5 a été complètement refactorisée, offrant de meilleures performances, une meilleure maintenabilité et de nouvelles fonctionnalités.

### Total des Fonctionnalités: 85+ Fonctionnalités

#### **Commandes Principales (24 commandes)**
- `.now` - Afficher la piste Spotify actuelle
- `.fm` - Afficher la piste Last.fm/Stats.fm actuelle
- `.help` - Lister toutes les commandes disponibles
- `.guide` - Instructions de configuration
- `.connect` - Connecter le compte Spotify
- `.search [terme]` - Rechercher des pistes sur Spotify
- `.play [ID]` - Lire une piste spécifique
- `.pause` - Mettre en pause la lecture
- `.skip` - Piste suivante
- `.back` - Piste précédente
- `.vol [0-100]` - Contrôler le volume
- `.repeat [mode]` - Basculer le mode de répétition
- `.like now` - Aimer la piste actuelle
- `.like [ID]` - Aimer une piste spécifique
- `.list` - Afficher les pistes récemment lues
- `.bio` - Restaurer la biographie par défaut
- `.export` ⭐ **NOUVEAU** - Exporter toutes les configurations vers backup
- `.import` ⭐ **NOUVEAU** - Importer les configurations depuis backup
- `.backups` ⭐ **NOUVEAU** - Lister tous les backups disponibles
- `.setid [client_id]` - Définir le Client ID de Spotify
- `.setsecret [client_secret]` - Définir le Client Secret de Spotify
- `.code [code_autorisation]` - Échanger le code d'autorisation contre des tokens
- `.check` - Valider les identifiants Spotify
- `.setuser [utilisateur]` - Définir l'utilisateur Last.fm
- `.setkey [api_key]` - Définir la clé API Last.fm

#### **Services Supportés (6 plateformes)**
- **Spotify** (via API officielle)
- **Last.fm** (scrobbling)
- **Stats.fm** (suivi Spotify)
- **YouTube/YouTube Music**
- **SoundCloud**
- **exteraGram/AyuGram** (scrobbling from etg and ayu)

#### **Système de Thèmes (8+ thèmes)**
- **Apple Light** - Thème clair propre pour Spotify
- **Apple Dark** - Thème sombre pour Spotify
- **Apple Red** - Thème avec accent rouge pour Spotify
- **Minimal** - Design minimaliste pour tous les services
- **CustomFM** - Thème entièrement personnalisable avec options avancées
- **Thèmes Externes** - Support pour thèmes tiers
- **Mode Thème Aléatoire** - Rotation automatique des thèmes
- **Polices Personnalisées** - Support pour sélection de polices personnalisées

#### **Système de Progrès ViniBar (8 fonctionnalités)**
- **Intégration exclusive avec l'API Spotify** - Suivi du progrès en temps réel
- **Indicateur visuel de progression** - Barre de recherche élégante sur les pochettes d'albums
- **Support de thèmes multiples** - Disponible dans les thèmes Apple Light, Apple Dark et Apple Red
- **Synchronisation précise** - Synchronisé avec la position de lecture actuelle de Spotify
- **Positionnement intelligent** - Automatiquement positionné au-dessus de la pochette d'album
- **Gradients dynamiques** ⭐ **NOUVEAU** - Gradients colorés qui s'adaptent à la couleur de la pochette d'album
- **Rendu avancé** ⭐ **NOUVEAU** - Système de rendu pixel par pixel pour une qualité optimale
- **Masquage intelligent** ⭐ **NOUVEAU** - Application de masques avec coins arrondis pour un look professionnel

#### **Système de Sauvegarde et Restauration (6 fonctionnalités)** ⭐ **NOUVEAU**
- **Export de paramètres** - Sauvegarde complète de toutes les configurations actuelles
- **Import de paramètres** - Restauration rapide des configurations sauvegardées
- **Validation de sauvegarde** - Vérification de l'intégrité des fichiers de sauvegarde
- **Sauvegarde automatique** - Création automatique de points de restauration
- **Gestion de versions** - Support pour multiples versions de sauvegarde
- **Interface intuitive** - Commandes simples `.export` et `.import`

#### **Options Avancées Apple UI (4 fonctionnalités)** ⭐ **NOUVEAU**
- **Mode Apple authentique** - Interface fidèle au design Apple Music
- **Optimisations visuelles** - Rendu optimisé pour l'esthétique Apple
- **Compatibilité étendue** - Support amélioré pour différentes résolutions
- **Personnalisation avancée** - Options de configuration spécifiques à Apple UI

#### **Système Vinify UI (7 fonctionnalités)** ⭐ **NOUVEAU**
- **Interface Vinify native** - Design spécialement conçu pour l'écosystème Vinify
- **Intégration transparente** - Compatibilité parfaite avec les thèmes Vinify
- **Optimisations de performance** - Rendu optimisé pour l'interface Vinify
- **Personnalisation étendue** - Options de configuration spécifiques à Vinify
- **Support multi-plateforme** - Fonctionnement optimal sur tous les appareils
- **Affichage Album/Playlist** ⭐ **NOUVEAU** - Afficher le nom de l'album ou playlist actuel sous l'artiste avec formatage en gras
- **Informations du Périphérique** ⭐ **NOUVEAU** - Afficher le périphérique de lecture actuel au-dessus de ViniBar au format "Device: NOM"

#### **Système de Légende Personnalisée (4 fonctionnalités)** ⭐ **NOUVEAU**
- **Variables dynamiques** - Support pour `{track}` et `{artist}` dans les légendes
- **Texte personnalisé** - Création de légendes entièrement personnalisées
- **Formatage intelligent** - Adaptation automatique du texte selon le contenu
- **Prévisualisation en temps réel** - Aperçu instantané des modifications de légende

#### **Fonctionnalités Avancées de CustomFM (15+ options)**
- **Support Haute Résolution** ⭐ **NOUVEAU**:
  - **Génération d'images en 1920x1080** - Cartes ultra haute qualité pour une meilleure expérience visuelle
  - **Mise à l'échelle proportionnelle automatique** - Tous les éléments s'adaptent parfaitement à la résolution
  - **Performance optimisée** - Traitement intelligent pour minimiser le temps de génération
  - **Système de cache intelligent** - Les images générées sont mises en cache pour une réutilisation instantanée
- **Personnalisation d'arrière-plan**:
  - Arrière-plan de pochette d'album avec contrôle de flou
  - Couleurs solides personnalisées (support hex)
  - Images de superposition personnalisées via URL
  - Contrôle d'assombrissement de l'arrière-plan
- **Options de mise en page**:
  - Positionnement de pochette (gauche/droite)
  - Positionnement adaptatif du texte
- **Contrôles de style**:
  - Coins arrondis (5 niveaux: Standard, Petit, Moyen, Grand, Cercle)
  - Emphase du texte (option de texte en gras)
  - Couleurs de texte personnalisées (support hex)
  - Couleurs d'icônes de service (coloré/monochromatique)
- **Optimisations de Performance** ⭐ **NOUVEAU**:
  - **Cache intelligent d'images** - Chargement de pochettes en cache pour génération plus rapide
  - **Traitement de flou optimisé** - Algorithmes de flou améliorés pour haute résolution
  - **Système de basculement** - Sources multiples pour pochettes d'album avec système de priorité

#### **Système de Cache Avancé (18+ options)**
- **Cache multicouche** - Cache persistant entre les redémarrages
- **Cache de vignettes YouTube** - Stocke les vignettes YouTube pour un accès plus rapide
- **Cache de vignettes SoundCloud** - Système de cache spécifique à SoundCloud
- **Cache d'images CustomFM** ⭐ **NOUVEAU** - Cache intelligent des cartes CustomFM générées
- **Cache multi-résolution** - Différents niveaux de qualité
- **Compression adaptative** - Ajuste automatiquement la qualité selon la vitesse de connexion
- **Cache d'URLs** - Cache des URLs de vignettes valides
- **Basculement de qualité** - Essaie différentes qualités si la principale échoue
- **Modes de performance** - Turbo, Équilibré, Qualité
- **Configuration TTL** - Durée de vie du cache configurable (1 heure pour CustomFM)
- **Optimisations de cache avancées** - Système de cache avancé pour de meilleures performances
- **Préchargement** - Charge automatiquement les pistes suivantes de la playlist
- **Compression d'images** - Compresser les images pour économiser de l'espace
- **Gestion du cache** - Contrôle manuel du cache
- **Stockage persistant** - Le cache survit aux redémarrages de l'app
- **Nettoyage intelligent** - Maintenance automatique du cache
- **Cache basé sur hash** ⭐ **NOUVEAU** - Clés de cache uniques basées sur les métadonnées de la piste
- **Invalidation automatique du cache** ⭐ **NOUVEAU** - Expiration et nettoyage intelligent du cache

#### **Automatisation Bio (8 fonctionnalités)**
- **Mises à jour automatiques de bio** - Met à jour la bio avec la piste actuelle
- **Texte de bio personnalisé** - Texte de bio personnalisé avec variables
- **Support de variables** - Marqueurs {track} et {artist}
- **Restauration de bio par défaut** - Commande .bio pour restauration manuelle
- **Notifications de bio** - Alertes pour changements de bio
- **Capture de bio originale** - Sauvegarde automatiquement la bio originale
- **Limite de 70 caractères** - Conformité avec limite de bio Telegram
- **Gestion intelligente de bio** - Manipulation intelligente de la bio

#### **Interface de Configuration (4 sections principales)**
- **Paramètres Principaux**: Identifiants, thèmes, légendes, exteraBar, polices
- **Options Avancées**: Commandes personnalisées, automatisation bio, performance, intégration chat
- **Paramètres Last.fm/Stats.fm**: Détection de lecteur, configuration API, personnalisation de thème
- **Fonctionnalités Premium**: Support d'emoji premium, éléments UI améliorés

#### **Fonctionnalités de Performance (8 optimisations)**
- **Détection intelligente de lecteur** - Détection automatique du lecteur de musique actif
- **Génération intelligente de liens** - Création de liens consciente du contexte
- **Système de basculement robuste** - Multiples options de sauvegarde
- **Compression d'images** - Optimisations pour économiser l'espace
- **Cache optimisé** - Réactivité améliorée
- **Timeouts configurables** - Gestion de timeout d'API
- **Adaptation à la vitesse de connexion** - Ajustement de qualité basé sur la connexion
- **Gestion des ressources** - Utilisation efficace de la mémoire

#### **Fonctionnalités Premium (2 fonctionnalités)**
- **Support d'Emoji Premium** - Synchronisation d'emojis premium (nécessite un abonnement Telegram Premium)
- **Éléments UI Améliorés** - Composants d'interface avancés et améliorations visuelles

#### **Support Multilingue (5 langues)**
- Portugais
- Anglais
- Espagnol
- Français
- Russe

#### **Intégration Chat (4 fonctionnalités)**
- **Menu de chat configurable** - Afficher/masquer dans le menu de chat
- **Notifications personnalisables** - Préférences de notification
- **Légendes personnalisées** - Légendes de carte personnalisées
- **Liens intelligents** - Liens Spotify/pistes

#### **Système de Liens Intelligents (6 types de liens)**
- **Spotify** - Lien direct vers la piste
- **YouTube/YouTube Music** - Recherche basée sur titre/artiste
- **SoundCloud** - Recherche SoundCloud
- **song.link** - Liens musicaux universels pour lecteurs .fm
- **Last.FM/Stats.FM** - Liens de profil
- **Liens personnalisés** - Préférences de lien définies par l'utilisateur

---

## Русский

### Что такое Nowfy?

Nowfy - это продвинутый плагин для exteraGram, который позволяет отображать и управлять текущей воспроизводимой музыкой с помощью стилизованных и настраиваемых карточек. Эта версия 1.0.5 была полностью переработана, предлагая лучшую производительность, удобство сопровождения и новые функции.

### Общее количество функций: 85+ Функциональностей

#### **Основные команды (24 команды)**
- `.now` - Показать текущий трек Spotify
- `.fm` - Показать текущий трек Last.fm/Stats.fm
- `.help` - Список всех доступных команд
- `.guide` - Инструкции по настройке
- `.connect` - Подключить аккаунт Spotify
- `.search [термин]` - Поиск треков в Spotify
- `.play [ID]` - Воспроизвести конкретный трек
- `.pause` - Приостановить воспроизведение
- `.skip` - Следующий трек
- `.back` - Предыдущий трек
- `.vol [0-100]` - Управление громкостью
- `.repeat [режим]` - Переключить режим повтора
- `.like now` - Лайкнуть текущий трек
- `.like [ID]` - Лайкнуть конкретный трек
- `.list` - Показать недавно воспроизведенные треки
- `.bio` - Восстановить стандартную биографию
- `.export` ⭐ **НОВОЕ** - Экспорт всех конфигураций в backup
- `.import` ⭐ **НОВОЕ** - Импорт конфигураций из backup
- `.backups` ⭐ **НОВОЕ** - Список всех доступных backup'ов
- `.setid [client_id]` - Установить Client ID Spotify
- `.setsecret [client_secret]` - Установить Client Secret Spotify
- `.code [код_авторизации]` - Обменять код авторизации на токены
- `.check` - Проверить учетные данные Spotify
- `.setuser [пользователь]` - Установить пользователя Last.fm
- `.setkey [api_key]` - Установить API ключ Last.fm

#### **Поддерживаемые сервисы (6 платформ)**
- **Spotify** (через официальный API)
- **Last.fm** (скробблинг)
- **Stats.fm** (отслеживание Spotify)
- **YouTube/YouTube Music**
- **SoundCloud**
- **exteraGram/AyuGram** (скробблинг из etg и ayu)

#### **Система тем (8+ тем)**
- **Apple Light** - Чистая светлая тема для Spotify
- **Apple Dark** - Темная тема для Spotify
- **Apple Red** - Тема с красным акцентом для Spotify
- **Minimal** - Минималистичный дизайн для всех сервисов
- **CustomFM** - Полностью настраиваемая тема с расширенными опциями
- **Внешние темы** - Поддержка сторонних тем
- **Режим случайной темы** - Автоматическая ротация тем
- **Пользовательские шрифты** - Поддержка выбора пользовательских шрифтов

#### **Система прогресса ViniBar (8 функций)**
- **Эксклюзивная интеграция с API Spotify** - Отслеживание прогресса в реальном времени
- **Визуальный индикатор прогресса** - Элегантная полоса поиска поверх обложек альбомов
- **Поддержка нескольких тем** - Доступно в темах Apple Light, Apple Dark и Apple Red
- **Точная синхронизация** - Синхронизировано с текущей позицией воспроизведения Spotify
- **Умное позиционирование** - Автоматически размещается над обложкой альбома
- **Динамические градиенты** ⭐ **НОВОЕ** - Цветные градиенты, адаптирующиеся к цвету обложки альбома
- **Продвинутый рендеринг** ⭐ **НОВОЕ** - Система рендеринга пиксель за пикселем для оптимального качества
- **Умное маскирование** ⭐ **НОВОЕ** - Применение масок с закругленными углами для профессионального вида

#### **Система резервного копирования и восстановления (6 функций)** ⭐ **НОВОЕ**
- **Экспорт настроек** - Полное резервное копирование всех текущих конфигураций
- **Импорт настроек** - Быстрое восстановление сохраненных конфигураций
- **Проверка резервных копий** - Проверка целостности файлов резервных копий
- **Автоматическое резервное копирование** - Автоматическое создание точек восстановления
- **Управление версиями** - Поддержка нескольких версий резервных копий
- **Интуитивный интерфейс** - Простые команды `.export` и `.import`

#### **Расширенные опции Apple UI (4 функции)** ⭐ **НОВОЕ**
- **Аутентичный режим Apple** - Интерфейс, верный дизайну Apple Music
- **Визуальные оптимизации** - Оптимизированный рендеринг для эстетики Apple
- **Расширенная совместимость** - Улучшенная поддержка различных разрешений
- **Продвинутая персонализация** - Специальные опции конфигурации для Apple UI

#### **Система Vinify UI (7 функций)** ⭐ **НОВОЕ**
- **Нативный интерфейс Vinify** - Дизайн, специально созданный для экосистемы Vinify
- **Бесшовная интеграция** - Идеальная совместимость с темами Vinify
- **Оптимизации производительности** - Оптимизированный рендеринг для интерфейса Vinify
- **Расширенная персонализация** - Специальные опции конфигурации для Vinify
- **Мультиплатформенная поддержка** - Оптимальная работа на всех устройствах
- **Отображение Альбома/Плейлиста** ⭐ **НОВОЕ** - Показать название текущего альбома или плейлиста под артистом с жирным форматированием
- **Информация об Устройстве** ⭐ **НОВОЕ** - Отображать текущее устройство воспроизведения над ViniBar в формате "Device: ИМЯ"

#### **Система пользовательских подписей (4 функции)** ⭐ **НОВОЕ**
- **Динамические переменные** - Поддержка `{track}` и `{artist}` в подписях
- **Пользовательский текст** - Создание полностью персонализированных подписей
- **Умное форматирование** - Автоматическая адаптация текста в зависимости от содержимого
- **Предварительный просмотр в реальном времени** - Мгновенный предварительный просмотр изменений подписи

#### **Расширенные функции CustomFM (15+ опций)**
- **Поддержка высокого разрешения** ⭐ **НОВОЕ**:
  - **Генерация изображений в 1920x1080** - Карточки ультра высокого качества для лучшего визуального опыта
  - **Автоматическое пропорциональное масштабирование** - Все элементы идеально масштабируются с разрешением
  - **Оптимизированная производительность** - Интеллектуальная обработка для минимизации времени генерации
  - **Интеллектуальная система кэша** - Сгенерированные изображения кэшируются для мгновенного повторного использования
- **Настройка фона**:
  - Фон обложки альбома с контролем размытия
  - Пользовательские сплошные цвета (поддержка hex)
  - Пользовательские изображения наложения через URL
  - Контроль затемнения фона
- **Опции макета**:
  - Позиционирование обложки (слева/справа)
  - Адаптивное позиционирование текста
- **Элементы управления стилем**:
  - Закругленные углы (5 уровней: Стандарт, Маленький, Средний, Большой, Круг)
  - Выделение текста (опция жирного текста)
  - Пользовательские цвета текста (поддержка hex)
  - Цвета иконок сервиса (цветные/монохромные)
- **Оптимизации производительности** ⭐ **НОВОЕ**:
  - **Интеллектуальное кэширование изображений** - Загрузка обложек из кэша для более быстрой генерации
  - **Оптимизированная обработка размытия** - Улучшенные алгоритмы размытия для высокого разрешения
  - **Система резервирования** - Множественные источники для обложек альбомов с системой приоритетов

#### **Расширенная система кэша (18+ опций)**
- **Многослойный кэш** - Постоянный кэш между перезапусками
- **Кэш миниатюр YouTube** - Сохраняет миниатюры YouTube для быстрого доступа
- **Кэш миниатюр SoundCloud** - Специальная система кэша для SoundCloud
- **Кэш изображений CustomFM** ⭐ **НОВОЕ** - Интеллектуальное кэширование сгенерированных карточек CustomFM
- **Мульти-разрешение кэш** - Разные уровни качества
- **Адаптивное сжатие** - Автоматически настраивает качество в зависимости от скорости соединения
- **Кэш URL** - Кэш действительных URL миниатюр
- **Переключение качества** - Пробует разные качества, если основное не работает
- **Режимы производительности** - Турбо, Сбалансированный, Качество
- **Конфигурация TTL** - Настраиваемое время жизни кэша (1 час для CustomFM)
- **Расширенные оптимизации кэша** - Продвинутая система кэша для лучшей производительности
- **Предзагрузка** - Автоматически загружает следующие треки из плейлиста
- **Сжатие изображений** - Сжимать изображения для экономии места
- **Управление кэшем** - Ручное управление кэшем
- **Постоянное хранение** - Кэш переживает перезапуски приложения
- **Умная очистка** - Автоматическое обслуживание кэша
- **Кэш на основе хэша** ⭐ **НОВОЕ** - Уникальные ключи кэша на основе метаданных трека
- **Автоматическая инвалидация кэша** ⭐ **НОВОЕ** - Умное истечение срока действия и очистка кэша

#### **Автоматизация биографии (8 функций)**
- **Автоматические обновления биографии** - Обновляет биографию с текущим треком
- **Пользовательский текст биографии** - Персонализированный текст биографии с переменными
- **Поддержка переменных** - Заполнители {track} и {artist}
- **Восстановление биографии по умолчанию** - Команда .bio для ручного восстановления
- **Уведомления биографии** - Оповещения об изменениях биографии
- **Захват оригинальной биографии** - Автоматически сохраняет оригинальную биографию
- **Ограничение в 70 символов** - Соответствие ограничению биографии Telegram
- **Умное управление биографией** - Интеллектуальная обработка биографии

#### **Интерфейс конфигурации (4 основные секции)**
- **Основные настройки**: Учетные данные, темы, подписи, exteraBar, шрифты
- **Расширенные опции**: Пользовательские команды, автоматизация биографии, производительность, интеграция чата
- **Настройки Last.fm/Stats.fm**: Обнаружение плеера, конфигурация API, настройка темы
- **Премиум функции**: Поддержка премиум эмодзи, улучшенные элементы UI

#### **Функции производительности (8 оптимизаций)**
- **Умное обнаружение плеера** - Автоматическое обнаружение активного музыкального плеера
- **Интеллектуальная генерация ссылок** - Создание ссылок с учетом контекста
- **Надежная система резервирования** - Множественные варианты резервного копирования
- **Сжатие изображений** - Оптимизации для экономии места
- **Оптимизированный кэш** - Улучшенная отзывчивость
- **Настраиваемые тайм-ауты** - Управление тайм-аутом API
- **Адаптация к скорости соединения** - Настройка качества на основе соединения
- **Управление ресурсами** - Эффективное использование памяти

#### **Премиум функции (2 функциональности)**
- **Поддержка премиум эмодзи** - Синхронизация премиум эмодзи (требуется подписка Telegram Premium)
- **Улучшенные элементы UI** - Продвинутые компоненты интерфейса и визуальные улучшения

#### **Многоязычная поддержка (5 языков)**
- Португальский
- Английский
- Испанский
- Французский
- Русский

#### **Интеграция чата (4 функции)**
- **Настраиваемое меню чата** - Показать/скрыть в меню чата
- **Настраиваемые уведомления** - Предпочтения уведомлений
- **Пользовательские подписи** - Персонализированные подписи карточек
- **Умные ссылки** - Ссылки Spotify/треков

#### **Система умных ссылок (6 типов ссылок)**
- **Spotify** - Прямая ссылка на трек
- **YouTube/YouTube Music** - Поиск на основе названия/исполнителя
- **SoundCloud** - Поиск SoundCloud
- **song.link** - Универсальные музыкальные ссылки для .fm плееров
- **Last.FM/Stats.FM** - Ссылки профиля
- **Пользовательские ссылки** - Пользовательские предпочтения ссылок

---

## Installation & Setup

### Spotify
1. Access [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create a new app
3. Configure Client ID and Client Secret in plugin
4. Use `.connect` to authorize

### Last.fm
1. Get an API Key from [Last.fm API](https://www.last.fm/api)
2. Configure username and API key
3. Use `.fm` to show scrobbles

### Stats.fm
1. Configure your Stats.fm username
2. Use `.fm` with Stats.fm selected

---

## What's New in v1.0.5

- **Complete refactoring** of code for better maintainability
- **New multi-layer cache** system with 15+ optimization options
- **Enhanced CustomFM** with 12 advanced customization options
- **exteraBar integration** with real-time Spotify progress tracking
- **External themes** support via additional plugins
- **Reorganized configuration** interface with expandable panels
- **Optimized performance** with Turbo/Balanced/Quality modes
- **More robust fallback** system for all services
- **Improved player** detection across 6 platforms
- **Adaptive image** compression based on connection speed
- **Persistent cache** between sessions with smart cleanup
- **Premium emoji** support for Telegram Premium users
- **Enhanced bio automation** with 8 advanced features
- **Smart link generation** for 6 different link types
- **Multilingual support** for 5 languages

---

## Requirements

- exteraGram v11.12.0 or higher
- Internet connection for API calls
- Spotify Developer App (for Spotify features)
- Last.fm API Key (for Last.fm features)
- Telegram Premium (for premium emoji features)

---

## Links

- **Developer**: @AGeekApple, @exteraDevPlugins
- **Support**: @nowfyDOCS
- **Version**: 1.0.5
- **Total Features**: 60+ functionalities across 16 main commands, 8+ themes, 6 service integrations, advanced cache system, intelligent automation, and organized configuration interface.

The Nowfy plugin offers a complete ecosystem for music control and display in Telegram, with over 60 functionalities distributed across multiple categories, providing users with the most comprehensive music integration experience available for exteraGram.
