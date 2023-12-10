# K:02 (Fork)

## Сборка

1. Клонируем репозиторий:
```sh
git clone --recurse-submodules https://github.com/idefant/vial-qmk
```
2. Делаем нужные изменения в папках (опционально):
  - `keyboards/ergohaven/k02/keymaps/idefant`
  - `users/idefant`
3. Собираем прошивку с помощью Docker:
```sh
util/docker_build.sh ergohaven/k02:idefant
```
4. Перевод клавиатуры в режим загрузки прошивки (bootloader) с помощью bootmagic / кейкода RESET
5. Копируем файл с прошивкой `.build/ergohaven_k02_idefant.uf2` в открывшуюся папку (клавиатура подхватит файл и сама загрузится)
6. Прошить нужно обе половинки (переткнуть кабель и повторить 2 последний действия)

## Требования

### Hardware

- 3+ GB памяти на диске

### Software

- Git: https://git-scm.com/
- Docker Desktop: https://www.docker.com/products/docker-desktop/

## Благодарности

- ErgoHaven ([vial-qmk](https://github.com/ergohaven/vial-qmk))
- Никита Широков aka @braindefender ([Гайд по адаптированию раскладки](https://github.com/braindefender/wellum/blob/master/guides/%D0%BA%D0%B0%D0%BA-%D0%B0%D0%B4%D0%B0%D0%BF%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D1%82%D1%8C-%D1%80%D0%B0%D1%81%D0%BA%D0%BB%D0%B0%D0%B4%D0%BA%D1%83-%D0%BF%D0%BE%D0%B4-%D0%BC%D0%BE%D1%8E-%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D0%B0%D1%82%D1%83%D1%80%D1%83.md))
