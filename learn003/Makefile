.PHONY: setup
setup:
	docker-compose build

.PHONY: up
up:
	docker-compose up -d
	docker-compose logs -f

.PHONY: down
down:
	docker-compose down

.PHONY: register-task
register-task:
	curl http://localhost:5000/task?task_id=1

.PHONY: redis-cli
redis-cli:
	redis-cli -p 6379 -n 1

.PYONY: scale-up
scale-up:
	# >=v2.2
	docker-compose up --scale worker=3 -d
