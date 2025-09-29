# Changelog - NowFy Plugin v1.0.6

## **Resumo das Alterações**
Esta versão inclui correções críticas de bugs, melhorias na interface do usuário e novos comandos para integração com serviços de música.

---

## **Correções de Bugs**

### **1. Erro "list index out of range"**
- **Problema**: Plugin crashava ao tentar acessar a skin "Red" que não existia
- **Solução**: 
  - Corrigida lista de skins disponíveis
  - Removida skin "Red" dos seletores para evitar crashes
  - Mantidas apenas as skins "Light" e "Dark" funcionais

### **2. Qualidade das Capas nos Temas Apple**
- **Problema**: Capas com baixa qualidade visual
- **Tentativa Inicial**: 
  - Ajustadas coordenadas de posicionamento 
- **Solução Final**:
  - Melhorada qualidade interna de processamento
  - Mantido design original com melhor resolução

---

## **Melhorias de Interface**

### **3. Novo Seletor de Efeitos de Fundo no Vinify UI**
- **Problema**: Switch "Dark Background" oferecia apenas liga/desliga
- **Solução**: Substituído por seletor com 4 opções avançadas

#### **Opções Disponíveis:**
1. **Nenhum** - Sem efeitos aplicados
2. **Blur** - Apenas desfoque na imagem de fundo
3. **Escuro** - Apenas escurecimento sutil
4. **Blur + Escuro** - Combinação de desfoque e escurecimento

#### **Melhorias:**
- Adicionadas traduções em múltiplos idiomas
- Interface mais intuitiva com seletor
- Maior controle sobre efeitos visuais
- Corrigida compatibilidade técnica do componente

---

## **Novos Comandos**

### **4. Comandos de Integração com Serviços**
- **Comando `.fm`** - Integração exclusiva com Last.fm
  - Permite acesso a dados e estatísticas do Last.fm
  - Funciona apenas quando conectado ao serviço Last.fm

- **Comando `.stats`** - Integração exclusiva com Stats.fm  
  - Acesso a estatísticas detalhadas do Stats.fm
  - Funciona apenas quando conectado ao serviço Stats.fm

---

## **Impacto das Mudanças**

### **Estabilidade:**
- Eliminados crashes relacionados a skins inexistentes
- Compatibilidade mantida com todas as plataformas
- Interface totalmente funcional

### **Experiência do Usuário:**
- Maior controle sobre efeitos visuais (4 opções vs 2)
- Melhor qualidade de imagem mantendo design original
- Novos comandos para integração com serviços externos
- Interface mais intuitiva e responsiva

### **Funcionalidades:**
- Integração aprimorada com Last.fm e Stats.fm
- Comandos específicos para cada serviço
- Processamento otimizado de imagens

---

## **Status Final**
- Todas as correções aplicadas e testadas
- Interface totalmente funcional e estável  
- Novos comandos implementados
- Plugin pronto para uso em produção


---

# Changelog - NowFy Plugin v1.0.6 (English)

## **Summary of Changes**
This version includes critical bug fixes, user interface improvements, and new commands for music service integration.

---

## **Bug Fixes**

### **1. "list index out of range"**
- **Problem**: Plugin crashed when trying to access the "Red" skin that didn't exist
- **Solution**: 
  - Fixed available skins list
  - Removed "Red" skin from selectors to prevent crashes
  - Kept only functional "Light" and "Dark" skins

### **2. Cover Quality in Apple Themes**
- **Problem**: Covers with low visual quality
- **Initial Attempt**: 
  - Increased cover size to 450x450 pixels
  - Adjusted positioning coordinates
- **Rollback**: 
  - Change caused design disproportion
  - Reverted to original size maintaining proportions
- **Final Solution**:
  - Improved internal processing quality
  - Maintained original design with better resolution

---

## **Interface Improvements**

### **3. New Background Effects Selector in Vinify UI**
- **Problem**: "Dark Background" switch offered only on/off
- **Solution**: Replaced with selector with 4 advanced options

#### **Available Options:**
1. **None** - No effects applied
2. **Blur** - Only background image blur
3. **Dark** - Only subtle darkening
4. **Blur + Dark** - Combination of blur and darkening

#### **Improvements:**
- Added translations in multiple languages
- More intuitive interface with selector
- Greater control over visual effects
- Fixed component technical compatibility

---

## **New Commands**

### **4. Service Integration Commands**
- **`.fm` Command** - Exclusive Last.fm integration
  - Allows access to Last.fm data and statistics
  - Works only when connected to Last.fm service

- **`.stats` Command** - Exclusive Stats.fm integration  
  - Access to detailed Stats.fm statistics
  - Works only when connected to Stats.fm service

---

## **Impact of Changes**

### **Stability:**
- Eliminated crashes related to non-existent skins
- Maintained compatibility with all platforms
- Fully functional interface

### **User Experience:**
- Greater control over visual effects (4 options vs 2)
- Better image quality maintaining original design
- New commands for external service integration
- More intuitive and responsive interface

### **Features:**
- Enhanced Last.fm and Stats.fm integration
- Service-specific commands
- Optimized image processing

---

## **Final Status**
- All fixes applied and tested
- Fully functional and stable interface
- New commands implemented
- Plugin ready for production use

---

# Changelog - NowFy Plugin v1.0.6 (Español)

## **Resumen de Cambios**
Esta versión incluye correcciones críticas de errores, mejoras en la interfaz de usuario y nuevos comandos para integración con servicios de música.

---

## **Correcciones de Errores**

### **1. Error "list index out of range"**
- **Problema**: El plugin se bloqueaba al intentar acceder a la skin "Red" que no existía
- **Solución**: 
  - Corregida lista de skins disponibles
  - Removida skin "Red" de los selectores para evitar bloqueos
  - Mantenidas solo las skins funcionales "Light" y "Dark"

### **2. Calidad de Carátulas en Temas Apple**
- **Problema**: Carátulas con baja calidad visual
- **Intento Inicial**: 
  - Aumentado tamaño de carátulas a 450x450 píxeles
  - Ajustadas coordenadas de posicionamiento
- **Reversión**: 
  - El cambio causó desproporción en el diseño
  - Revertido al tamaño original manteniendo proporciones
- **Solución Final**:
  - Mejorada calidad interna de procesamiento
  - Mantenido diseño original con mejor resolución

---

## **Mejoras de Interfaz**

### **3. Nuevo Selector de Efectos de Fondo en Vinify UI**
- **Problema**: El switch "Dark Background" ofrecía solo encendido/apagado
- **Solución**: Reemplazado por selector con 4 opciones avanzadas

#### **Opciones Disponibles:**
1. **Ninguno** - Sin efectos aplicados
2. **Blur** - Solo desenfoque de imagen de fondo
3. **Oscuro** - Solo oscurecimiento sutil
4. **Blur + Oscuro** - Combinación de desenfoque y oscurecimiento

#### **Mejoras:**
- Añadidas traducciones en múltiples idiomas
- Interfaz más intuitiva con selector
- Mayor control sobre efectos visuales
- Corregida compatibilidad técnica del componente

---

## **Nuevos Comandos**

### **4. Comandos de Integración con Servicios**
- **Comando `.fm`** - Integración exclusiva con Last.fm
  - Permite acceso a datos y estadísticas de Last.fm
  - Funciona solo cuando está conectado al servicio Last.fm

- **Comando `.stats`** - Integración exclusiva con Stats.fm  
  - Acceso a estadísticas detalladas de Stats.fm
  - Funciona solo cuando está conectado al servicio Stats.fm

---

## **Impacto de los Cambios**

### **Estabilidad:**
- Eliminados bloqueos relacionados con skins inexistentes
- Mantenida compatibilidad con todas las plataformas
- Interfaz completamente funcional

### **Experiencia del Usuario:**
- Mayor control sobre efectos visuales (4 opciones vs 2)
- Mejor calidad de imagen manteniendo diseño original
- Nuevos comandos para integración con servicios externos
- Interfaz más intuitiva y responsiva

### **Funcionalidades:**
- Integración mejorada con Last.fm y Stats.fm
- Comandos específicos para cada servicio
- Procesamiento optimizado de imágenes

---

## **Estado Final**
- Todas las correcciones aplicadas y probadas
- Interfaz completamente funcional y estable
- Nuevos comandos implementados
- Plugin listo para uso en producción

---

# Changelog - NowFy Plugin v1.0.6 (Français)

## **Résumé des Modifications**
Cette version inclut des corrections critiques de bugs, des améliorations de l'interface utilisateur et de nouvelles commandes pour l'intégration avec les services musicaux.

---

## **Corrections de Bugs**

### **1. Erreur "list index out of range"**
- **Problème**: Le plugin plantait en essayant d'accéder au skin "Red" qui n'existait pas
- **Solution**: 
  - Corrigé la liste des skins disponibles
  - Supprimé le skin "Red" des sélecteurs pour éviter les plantages
  - Gardé seulement les skins fonctionnels "Light" et "Dark"

### **2. Qualité des Pochettes dans les Thèmes Apple**
- **Problème**: Pochettes avec une qualité visuelle faible
- **Tentative Initiale**: 
  - Augmenté la taille des pochettes à 450x450 pixels
  - Ajusté les coordonnées de positionnement
- **Retour en Arrière**: 
  - Le changement a causé une disproportion dans le design
  - Revenu à la taille originale en maintenant les proportions
- **Solution Finale**:
  - Amélioré la qualité interne de traitement
  - Maintenu le design original avec une meilleure résolution

---

## **Améliorations de l'Interface**

### **3. Nouveau Sélecteur d'Effets d'Arrière-plan dans Vinify UI**
- **Problème**: Le switch "Dark Background" offrait seulement marche/arrêt
- **Solution**: Remplacé par un sélecteur avec 4 options avancées

#### **Options Disponibles:**
1. **Aucun** - Aucun effet appliqué
2. **Flou** - Seulement flou de l'image d'arrière-plan
3. **Sombre** - Seulement assombrissement subtil
4. **Flou + Sombre** - Combinaison de flou et d'assombrissement

#### **Améliorations:**
- Ajouté des traductions en plusieurs langues
- Interface plus intuitive avec sélecteur
- Plus grand contrôle sur les effets visuels
- Corrigé la compatibilité technique du composant

---

## **Nouvelles Commandes**

### **4. Commandes d'Intégration avec les Services**
- **Commande `.fm`** - Intégration exclusive avec Last.fm
  - Permet l'accès aux données et statistiques de Last.fm
  - Fonctionne seulement quand connecté au service Last.fm

- **Commande `.stats`** - Intégration exclusive avec Stats.fm  
  - Accès aux statistiques détaillées de Stats.fm
  - Fonctionne seulement quand connecté au service Stats.fm

---

## **Impact des Modifications**

### **Stabilité:**
- Éliminé les plantages liés aux skins inexistants
- Maintenu la compatibilité avec toutes les plateformes
- Interface entièrement fonctionnelle

### **Expérience Utilisateur:**
- Plus grand contrôle sur les effets visuels (4 options vs 2)
- Meilleure qualité d'image en maintenant le design original
- Nouvelles commandes pour l'intégration avec services externes
- Interface plus intuitive et responsive

### **Fonctionnalités:**
- Intégration améliorée avec Last.fm et Stats.fm
- Commandes spécifiques pour chaque service
- Traitement optimisé des images

---

## **État Final**
- Toutes les corrections appliquées et testées
- Interface entièrement fonctionnelle et stable
- Nouvelles commandes implémentées
- Plugin prêt pour utilisation en production

---

# Changelog - NowFy Plugin v1.0.6 (Русский)

## **Краткое Описание Изменений**
Эта версия включает критические исправления ошибок, улучшения пользовательского интерфейса и новые команды для интеграции с музыкальными сервисами.

---

## **Исправления Ошибок**

### **1. Ошибка "list index out of range"**
- **Проблема**: Плагин вылетал при попытке доступа к скину "Red", которого не существовало
- **Решение**: 
  - Исправлен список доступных скинов
  - Удален скин "Red" из селекторов для предотвращения вылетов
  - Оставлены только функциональные скины "Light" и "Dark"

### **2. Качество Обложек в Темах Apple**
- **Проблема**: Обложки с низким визуальным качеством
- **Первоначальная Попытка**: 
  - Увеличен размер обложек до 450x450 пикселей
  - Скорректированы координаты позиционирования
- **Откат**: 
  - Изменение вызвало диспропорцию в дизайне
  - Возвращен к оригинальному размеру с сохранением пропорций
- **Финальное Решение**:
  - Улучшено внутреннее качество обработки
  - Сохранен оригинальный дизайн с лучшим разрешением

---

## **Улучшения Интерфейса**

### **3. Новый Селектор Эффектов Фона в Vinify UI**
- **Проблема**: Переключатель "Dark Background" предлагал только вкл/выкл
- **Решение**: Заменен селектором с 4 расширенными опциями

#### **Доступные Опции:**
1. **Нет** - Без применения эффектов
2. **Размытие** - Только размытие фонового изображения
3. **Темный** - Только тонкое затемнение
4. **Размытие + Темный** - Комбинация размытия и затемнения

#### **Улучшения:**
- Добавлены переводы на несколько языков
- Более интуитивный интерфейс с селектором
- Больший контроль над визуальными эффектами
- Исправлена техническая совместимость компонента

---

## **Новые Команды**

### **4. Команды Интеграции с Сервисами**
- **Команда `.fm`** - Эксклюзивная интеграция с Last.fm
  - Позволяет доступ к данным и статистике Last.fm
  - Работает только при подключении к сервису Last.fm

- **Команда `.stats`** - Эксклюзивная интеграция с Stats.fm  
  - Доступ к детальной статистике Stats.fm
  - Работает только при подключении к сервису Stats.fm

---

## **Влияние Изменений**

### **Стабильность:**
- Устранены вылеты, связанные с несуществующими скинами
- Сохранена совместимость со всеми платформами
- Полностью функциональный интерфейс

### **Пользовательский Опыт:**
- Больший контроль над визуальными эффектами (4 опции против 2)
- Лучшее качество изображения с сохранением оригинального дизайна
- Новые команды для интеграции с внешними сервисами
- Более интуитивный и отзывчивый интерфейс

### **Функциональность:**
- Улучшенная интеграция с Last.fm и Stats.fm
- Специфичные команды для каждого сервиса
- Оптимизированная обработка изображений

---

## **Финальный Статус**
- Все исправления применены и протестированы
- Полностью функциональный и стабильный интерфейс
- Новые команды реализованы
- Плагин готов к использованию в продакшене
