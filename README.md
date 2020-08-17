# Larasocket, Tailwind, Alpine, Livewire 및 Laravel을 사용하여 실시간 채팅방 구축

https://medium.com/@zachvv11/real-time-chat-room-with-larasocket-tailwind-alpine-livewire-and-laravel-406a8c5e680d


```php
Schema::create('messages', function (Blueprint $table) {
    $table->id();
    $table->text('body');
    $table->foreignId('user_id')->constrained()->cascadeOnDelete();
    $table->timestamps();
});
```

```php
$message = Auth::user()->messages()->create(['body'=>'test1'])->load('user');
```


