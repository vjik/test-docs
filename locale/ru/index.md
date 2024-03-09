# Test Header2

```php
final class Engine
{
    public function __construct(
        private string $name,
    ) {}
}

final class Car
{
    public function __construct(
        private string $name,
        private Engine $engine,
    ) {}
}

// вложенный массив
$object = $hydrator->create(Car::class, [
    'name' => 'Ferrari',
    'engine' => [
        'name' => 'V8',
    ]
]);

// или dot-нотация
$object = $hydrator->create(Car::class, [
    'name' => 'Ferrari',
    'engine.name' => 'V8',
]);
```
