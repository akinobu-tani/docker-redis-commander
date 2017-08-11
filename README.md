[Redis Commander](https://github.com/joeferner/redis-commander)

## Usage

```yaml
version: "3"
services:
  redis:
    image: redis

  redis-commander:
    image: redis-commander
    depends_on:
      - redis
    ports:
      - "8081:8081"
    command: ["redis-commander", "--redis-host", "redis"]
```
