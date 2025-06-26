# TP-Optimizacion-Gianetti
Uso de Sprite Atlas por tipo de pantalla (Atlas_Gameplay, Atlas_Shop, Atlas_Settings, Atlas_UI_Common) para reducir draw calls.

Separación de elementos reutilizables en Atlas_UI_Common según criterio de uso compartido (ej: close button.png).

Evitar sprites duplicados en múltiples atlas para mantener coherencia y evitar duplicación de memoria.

Sprites con tamaño potencia de dos (1024) para compatibilidad.

Edición de imágenes para agregar padding visual real (ej: popup_safe.png) para prevenir overlapping con otro sprite del mismo atlas. al ver que esto no funcionó, decidí dejar afuera del atlas el sprite popup.png, ya que incluso con padding agregado seguia overlappeando con close button png.

Uso del RectTransform para escalado de UI, en lugar de Transform.Scale.

Uso de CanvasScaler con Scale With Screen Size, referencia 1920x1080, Match: 0.5 para UI responsiva.

Verificación en múltiples resoluciones y aspect ratios (16:9, 1920x1080, 1280x720) para asegurar adaptabilidad visual.

Canvas en Screen Space - Overlay, evitando el uso innecesario de cámara.

Evitar Raycast Target en elementos no interactivos (solo visuales).

Modularidad en la estructura de UI (paneles independientes): GameplayPanel, ShopPanel, SettingsPanel.
