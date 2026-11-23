# 3D-модели

Файлы `.glb` из Higgsfield, уже сжатые: текстуры уменьшены до 1024 px и переведены в JPEG.
Игра подхватывает их по именам из таблицы. Если файла нет, показывается простая модель из примитивов.

| Файл | Что это | Higgsfield job |
|---|---|---|
| `mower-s100.glb` | Райдер S100 без логотипов, зелёно-жёлтый | a77db5af-813a-499d-812d-caea42370d02 |
| `hero.glb` | Герой, сидит (анимация sit) | 4a70748c-1b5f-4f7e-8366-02338c6c24e1 |
| `kowalski.glb` | Mrs. Kowalski | 53546a9b-6158-4276-849f-eb266d73e1cf |
| `hank.glb` | Big Hank | 9713f264-c4a4-4b57-9eb1-7826dbe3201c |
| `park-manager.glb` | Менеджер парка | 6a582ab4-1d8f-44f4-96c0-1b36506eff30 |
| `dale.glb` | Dale, гринкипер | 63e1dc87-4c77-4ee3-b6d9-f1ce753dda4d |
| `ashford.glb` | Lady Ashford | bc647cfc-4feb-49f5-b0c0-b11e2fbcd242 |
| `udc-driver.glb` | Водитель фургона UDC | 6e1a3c1f-3e52-48a8-9279-7c7468bff504 |
| `neighbor-woman.glb` | Спортивная соседка | be24aca3-4269-4b84-8854-c9d689e93612 |
| `rival.glb` | Конкурент Turf Kings | 010665ae-88e4-4770-a952-0b497ee60b69 |

Как сжать новый файл:
```
npx @gltf-transform/cli resize in.glb tmp.glb --width 1024 --height 1024
npx @gltf-transform/cli jpeg tmp.glb out.glb --formats png --slots "*" --quality 82
```

Где используются модели:
- `mower-s100`: стартовая косилка «John Deere 42″» (поле `model3d` в `MOWERS`)
- `hero`: водитель на любой косилке, анимация сидения
- клиенты: таблица `CLIENT_MODEL` по типу газона
- `rival`: появляется у заказов, где есть Turf Kings
- `udc-driver`: срочная доставка
