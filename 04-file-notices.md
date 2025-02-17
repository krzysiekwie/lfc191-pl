﻿# Oznakowanie w plikach

## Wprowadzenie

### Przegląd rozdziału

Oznakowanie w plikach to informacja załączona do pliku z kodem źródłowym obejmująca notę o prawach autorskich i licencję.

Forma not o prawach autorskich została omówiona w rozdziale 3. Forma informacji o licencji została omówiona w rozdziale 2. Nota copyright i określenie licencji tworzą łącznie oznakowanie w pliku.

### Założenia rozdziału

W tym rozdziale nauczysz się, jak:

* określać, co jest potrzebne do stworzenia typowego oznakowania w plikach,
* rozpoznawać niektóre typowe przykłady poprawnego oznakowaniach w plikach.

# Oznakowanie w plikach

### Czym jest poprawne oznakowanie w plikach?

Czym jest poprawne oznakowanie w plikach? Poprawne oznakowanie charakteryzuje się jasnym określeniem licencji, którą objęty jest plik, i może zawierać informacje lub odniesienia do właścicieli praw autorskich. Oznakowanie w pliku może również podawać dodatkowe informacje o autorstwie, kiedy autor nie jest właścicielem praw.

Jeżeli oznakowanie podaje takie informacje za pomocą jednoznacznego odniesienia do licencji, to mogą być one wykrywane automatycznie.

Pozwala to znacznie usprawnić obsługę zgodności. Ułatwia również użytkownikom otwartego oprogramowania zrozumienie warunków wykorzystywania go i informuje, gdzie kierować pytania w razie wątpliwości.

Zgodnie z konwencją oznakowanie umieszcza się na początku pliku.

### Przykład: Linux

![Linux](img/linux.jpg)

```plaintext
// SPDX-License-Identifier: GPL-2.0-only
/*
 *  ARM64 Specific Low-Level ACPI Boot Support
 *
 *  Copyright (C) 2013-2014, Linaro Ltd.
 *      Author: Al Stone <al.stone@linaro.org>
 *      Author: Graeme Gregory <graeme.gregory@linaro.org>
 *      Author: Hanjun Guo <hanjun.guo@linaro.org>
 *      Author: Tomasz Nowicki <tomasz.nowicki@linaro.org>
 *      Author: Naresh Bhat <naresh.bhat@linaro.org>
 */
 ```

Pierwszy [przykład](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/arch/arm64/kernel/acpi.c), któremu się przyjrzymy, pochodzi z systemu operacyjnego Linux. W pliku `acpi.c` oznaczonym właścicielem praw autorskich jest Linaro. Użycie słowa "Copyright" jednocześnie z odpowiadającym mu symbolem to przesada, ale nie stanowi poważnego problemu. Pierwotna data publikacji to 2013, ale w 2014 dodano wiele znaczących zmian. Oznaczono to, wykorzystując zakres dat. Określenie praw autorskich mieści się w jednej linii.

Wymienienie pełnych nazwisk i adresów mailowych pięciu autorów, którzy przyczynili się do powstania tego pliku i godzą się na kontakt w przypadku pytań, jest pomocne, ale nie należy do oficjalnej części informacji o prawach autorskich. W tym przypadku autorzy nie są właścicielami praw autorskich. Wykonywali swoją pracę na rzecz pracodawcy - Linaro - i dlatego to właśnie Linaro jest wskazane jako właściciel praw autorskich.

Użyta tu licencja to wersja 2 GPL. Oznaczono to przez umieszczenie w pierwszej linii pliku skróconego identyfikatora SPDX.

Co ciekawe, jeśli spojrzysz na [zapis historii git dla tego pliku](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/log/arch/arm64/kernel/acpi.c), to zobaczysz wiele zmian w pliku po roku 2014. Niektóre z nich to drobne usprawnienia, a nawet usunięcia (bez dodania treści), ale część miała znaczą długość (a kilka powyżej 100 linii kodu). Gdyby te dodane treści były przedmiotem praw autorskich, to podany zakres lat „2013-2014” byłby niekompletny. A gdyby którykolwiek z kolejnych współtwórców nie był zatrudniony przez Linaro, to informacja o prawach autorskich nie podawałaby prawidłowej listy właścicieli praw. Pokazuje to, dlaczego poleganie wyłącznie na nocie copyright może wprowadzać w błąd albo nie wystarczyć do pełnego zrozumienia własności praw autorskich w kontekście pliku lub całego projektu.

### Przykład: FOSSology

![FOSSology](img/fossology.png)

```plaintext
/**************************************************************
 Copyright (C) 2006-2013 Hewlett-Packard Development Company, L.P.

 This program is free software; you can redistribute it and/or
 modify it under the terms of the GNU General Public License
 version 2 as published by the Free Software Foundation.

 This program is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
 GNU General Public License for more details.

 You should have received a copy of the GNU General Public License along
 with this program; if not, write to the Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.

 ***************************************************************/
```

W kolejnym [przykładzie](https://github.com/fossology/fossology/blob/master/src/nomos/agent/list.c), zaczerpniętym z FOSSology, standardowy nagłówek wskazujący na wersję 2 licencji GPL jest umieszczony po określeniu praw autorskich.

W tym pliku użyto również pełnego oficjalnego tekstu standardowego nagłówka licencji. W innym przykładzie użyto identyfikatora SPDX, ale tak czy inaczej wiadomo, że obowiązującą licencją jest wersja 2 GPL, a to się liczy przede wszystkim.

### Przykład: gcc

![GNU](img/gnu.png)

```plaintext
/* Common hooks for AArch64.
    Copyright (C) 2012-2015 Free Software Foundation, Inc.
    Contributed by ARM Ltd.

    This file is part of GCC.

    GCC is free software; you can redistribute it and/or modify it
    under the terms of the GNU General Public License as published
    by the Free Software Foundation; either version 3, or (at your
    option) any later version.

    GCC is distributed in the hope that it will be useful, but WITHOUT
    ANY WARRANTY; without even the implied warranty of MERCHANTABILITY
    or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public
    License for more details.

    You should have received a copy of the GNU General Public License
    along with GCC; see the file COPYING3.  If not see
    <http://www.gnu.org/licenses/>.  */
```

W tym [przykładzie](https://github.com/gcc-mirror/gcc/blob/master/gcc/common/config/aarch64/aarch64-common.c), `aarch64-common.c`, projekt GNU wymaga przypisania praw autorskich w ramach warunków uznania autorstwa, więc prawa autorskie zostały przypisane do Free Software Foundation przez ARM Ltd. Sformułowanie "Contributed by ARM Ltd." nie jest określeniem praw autorskich, a jedynie dodatkową informacją o autorstwie.

Informacja o prawach autorskich znów niepotrzebnie używa zarówno słowa „Copyright”, jak i symbolu ©, ale to nic nie szkodzi.

Pierwsze treści zostały dodane do tego pliku w 2012 roku, a znaczące uaktualnienia następowały w 2103, 2014 i 2015 wraz z dodawaniem nowych informacji o architekturze ARM64. Wskazuje na to zakres dat 2012-2015.

Po informacji o prawach autorskich znajduje się standardowy nagłówek licencji GNU General Public License (znanej jako GPL) w wersji 3 lub nowszych. Zgodnie z GPL, jeśli licencjodawca nie określił numeru wersji, licencjobiorca ma prawo korzystać z dowolnej wersji GPL opublikowanej przez Free Software Foundation. Określanie numeru wersji licencji to dobra praktyka, ponieważ jasno komunikuje intencje. Różnice między licencjami GPL v2 i GPL v3 są znaczne i kod, którego wykorzystanie jest ograniczone tylko do wersji 2 (GPL-2.0-only), nie może być łączony z kodem na licencji GPL 3.0.

### Przykład: Nova

![OpenStack](img/openstack.png)

```plaintext
# Copyright 2010 United States Government as represented by the
# Administrator of the National Aeronautics and Space Administration.
# Copyright 2011 Justin Santa Barbara
# All Rights Reserved.
#
#    Licensed under the Apache License, Version 2.0 (the "License"); you may
#    not use this file except in compliance with the License. You may obtain
#    a copy of the License at
#
#         http://www.apache.org/licenses/LICENSE-2.0
#
#    Unless required by applicable law or agreed to in writing, software
#    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
#    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
#    License for the specific language governing permissions and limitations
#    under the License.
```

Inną popularną rodziną projektów otwartego oprogramowania jest [OpenStack](https://docs.openstack.org/keystone/10.0.2/10.0.2/_modules/keystone/common/authorization.html). Należy do niej projekt Nova.

Plik licencji dla tego projektu powstał w 2010 i jest objęty prawami autorskimi rządu USA. W 2011 Justin Barbara dokonał w projekcie istotnych zmian i jego prawa autorskie również są oznaczone.

Po informacjach o prawach autorskich umieszczono standardowy nagłówek Apache 2.0 License, aby określić licencję projektu. Standardowe nagłówki zawierają czasami URL prowadzący do tekstu licencji. Po jednoznacznym określeniu "Licensed under the Apache License, Version 2.0” dołączanie linku jest już niepotrzebne, ale skoro jest on częścią standardowego nagłówka Apache, to niech już tak zostanie.

Ogólnie rzecz biorąc, powielone informacje nie przeszkadzają, o ile są zgodne ze sobą.

Konkretnym i dość typowym przykładem niezgodności jest dodanie informacji o prawach autorskich jednocześnie z deklaracją, że materiały są w domenie publicznej. O ile nie jest to praca stworzona przez rząd USA, to przeznaczenie jej do domeny publicznej jest bardzo mało prawdopodobne. Informacja o prawach autorskich bez określenia licencji oznacza, że istnieje właściciel praw, ale - o ile nie zaznaczono inaczej w innym miejscu dotyczącym danego pliku - to nie ma żadnej przyznanej licencji.

Nie zalecamy zmieniania nagłówków w kodzie innych osób, nawet jeśli są tam powielone te same informacje. Najlepszą metodą jest kontaktowanie się z autorami i proszenie ich o dokonanie zmian. Podobnie, jeśli podane informacje są sprzeczne, skontaktuj się z autorami i poproś o wyjaśnienia i poprawki.

### Przykład: Das U-Boot

```plaintext
/* SPDX-License-Identifier: GPL-2.0+ */
/*
 * (C) Copyright 2002
 * Wolfgang Denk, DENX Software Engineering, wd@denx.de.
 *
 * (C) Copyright 2010
 * Michael Zaidman, Kodak, michael.zaidman@kodak.com
 * post_word_{load|store} cleanup.
 */
```

W ostatnich latach niektóre projekty zaczęły korzystać ze skróconych identyfikatorów SPDX, aby jasno określić, jaka licencja obowiązuje dla danego pliku.

W tym [przykładzie](https://github.com/u-boot/u-boot/blob/master/include/post.h) plik został utworzony w 2002 przez Wolfganga Denka, w ramach pracy dla DENX Software Engineering. Nie da się jasno stwierdzić, czy właścicielem praw autorskich jest on sam (Wolfgang Denk) czy organizacja (DENX Software Engineering), 

więc aby to wyjaśnić i dowiedzieć się, czy nie przestał później pracować dla DENX Software Engineering, należy się z nim skontaktować. W 2010 Michael Zaidman z Kodaka dodał znaczące zmiany i dołączył informację o prawach autorskich. W tym przypadku wydaje się, że właścicielem praw jest Kodak, ale w zależności od formy zatrudnienia może też nim być Michael Zaidman.

Następnie widzimy SPDX-License-Identifier wskazujący na "GPL-2.0+". Jest to skrócony format ujednolicony przez SPDX, powszechnie odnoszący się do licencji GPL w wersji 2 lub nowszych. Jak mówiliśmy wcześniej, w ciągu kilku ostatnich lat, we współpracy z Free Software Foundation, rodzina licencji GNU zmieniła skrócone oznaczenia na "GPL-2.0-only" lub "GPL-2.0-or-later" zamiast "GPL-2.0+", które - mimo że nadal poprawne - jest już przestarzałe. A zatem powyższy przykład można by uaktualnić do nowego formatu. Pełną listę skróconych identyfikatorów zawiera [strona internetowa SPDX](https://spdx.org/licenses/). Są tam również skopiowane pełne teksty licencji wraz z linkami do oryginalnych.

### Przykład: Zephyr

```plaintext
/*
 * Copyright (c) 2018 Intel Corporation
 *
 * SPDX-License-Identifier: Apache-2.0
 */
```

W tym [przykładzie](https://github.com/zephyrproject-rtos/zephyr/blob/master/kernel/sched.c) plik `sched.c` utworzył w 2018 ktoś pracujący dla Intela, więc pierwotna informacja o prawach autorskich wskazuje na Intel Corporation. Od czasu utworzenia pliku 30 osób dodawało do niego treści i niektóre z nich być może nie są pracownikami Intela.

Licencją pliku jest Apache 2, co określa użycie identyfikatora "Apache-2.0".

## Podsumowanie

### Konkluzje

Ten rozdział wyjaśnił, z czego składa się typowe oznaczenie w pliku, i podał kilka konkretnych przykładów przedstawiających poprawne oznaczenia.
