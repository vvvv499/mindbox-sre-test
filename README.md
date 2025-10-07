# mindbox-sre-test
# Mindbox SRE Test — Deployment Example

## 📄 Описание
Kubernetes-манифест для веб-приложения, оптимизированного под:
- мультизональный кластер (3 зоны, 5 нод),
- медленный старт (5–10 секунд),
- дневной цикл нагрузки,
- минимальное ночное потребление,
- высокую отказоустойчивость.

## ⚙️ Как проверить в песочнице (без установки)
Можно протестировать прямо в браузере с помощью **Play with Kubernetes**.

### 🔹 Шаги
1. Перейти на 👉 [https://labs.play-with-k8s.com](https://labs.play-with-k8s.com)
2. Нажать **Start** → появится терминал.
3. Выполнить команды:
   ```bash
   kubectl apply -f https://raw.githubusercontent.com/<ТВОЙ_GITHUB_НИК>/mindbox-sre-test/main/myapp.yaml
   kubectl get pods -n mindbox-sre-test -w
   kubectl get svc -n mindbox-sre-test
   kubectl get hpa -n mindbox-sre-test
