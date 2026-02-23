# U1_Post1_02230131020_Otalora_Luis
# Refactorización con Principios SOLID

## Violaciones detectadas en OrderManager

1. Violación SRP:
La clase maneja creación de pedidos, descuentos, persistencia,
notificaciones y reportes.

2. Violación OCP:
Para agregar un nuevo descuento se debe modificar el método createOrder.

3. Violación DIP:
Depende directamente de FileWriter.

4. Alto acoplamiento:
Todo está concentrado en una sola clase.

## Decisiones de diseño

- Se creó la clase Order para representar la entidad.
- Se implementó Strategy Pattern para descuentos.
- Se aplicó DIP usando interfaces:
  - OrderRepository
  - NotificationService
- Se utilizó inyección por constructor en OrderService.
