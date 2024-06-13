# Projekt SIWR (2024)

## Opis Projektu

Ten projekt został wykonany w ramach kursu Sztuczna Inteligencja w Robotyce (SIWR). Głównym celem było stworzenie systemu estymacji stanu dla robota dwukołowego z wykorzystaniem probabilistycznych modeli grafowych. System miał za zadanie lokalizować robota w znanej mapie na podstawie danych z wielu czujników.

Projekt polega na stworzeniu systemu estymacji stanu robota z wykorzystaniem probabilistycznych modeli grafowych. System ma za zadanie lokalizować robota dwukołowego w znanej mapie na podstawie informacji z wielu czujników.

Dane wejściowe mogą pochodzić z symulacji (np. ROS GAZEBO) lub z gotowego pliku ROSBAG.

## Szczegóły Implementacji

### Wykorzystane Czujniki
- **LIDAR**: Używany do mapowania i wykrywania przeszkód.
- **Odometria i IMU**: Używane do śledzenia pozycji i ruchu robota.

### Implementacja Świata
Robot działa w świecie przypominającym labirynt. Środowisko jest zaprojektowane tak, aby stanowić wyzwanie dla nawigacji robota i jego systemu estymacji stanu. Labirynt zawiera różnorodne przeszkody i ścieżki, które robot musi rozpoznać i unikać, co wymaga zaawansowanej analizy danych z czujników. Docelowo robot ma za zadanie odnaleźć swoją drogę przez labirynt, wykorzystując estymację stanu i lokalizację opartą na danych z LIDARu oraz IMU.

### Algorytm
Stworzono algorytm do odczytu danych z czujników odometrii i IMU.

Algorytm składa się z kilku kluczowych kroków:
1. Subskrybowanie tematów ROS dotyczących odometrii i IMU.
2. Przetwarzanie danych z tych czujników w celu oszacowania pozycji i orientacji robota.
3. Implementacja filtrów i algorytmów do estymacji stanu robota na podstawie odczytów z czujników.
4. Integracja danych z odometrii i IMU w celu poprawy dokładności lokalizacji.

### Implementacja
W projekcie zostały użyte czujniki IMU i Odom. Został zaimplementowany labirynt i uruchomiony robot, który odczytuje wartości z czujników. Robot próbuje się odnaleźć w labiryncie i wydostać się z niego. W celu realizacji projektu:
- Stworzono symulację w środowisku ROS2 oraz Gazebo.
- Zaimplementowano algorytmy fuzji danych z czujników IMU i odometrii.
- Wykorzystano algorytmy SLAM (Simultaneous Localization and Mapping) do jednoczesnego mapowania i lokalizowania robota w labiryncie.
- Przeprowadzono wielokrotne testy i kalibrację czujników w celu uzyskania jak najlepszej dokładności estymacji pozycji robota.

### Literatura
- [Wprowadzenie do Robotyki](https://www.roboticsbook.org/intro.html)
- [Tutoriale GTSAM](https://gtsam.org/tutorials/intro.html)
- [Graph MSF](https://github.com/leggedrobotics/graph_msf)
- [Lokalizacja Robota przy użyciu Skanera Laserowego i Optymalizacji Grafu Pozycji](https://medium.com/@k3083518729/robot-localization-using-laser-scanner-and-pose-graph-optimization-fc40605bf5bc)

## Podsumowanie
Robot wyszukuje odpowiedniej drogi w labiryncie i na podstawie odczytu z czujników próbuje się z niego wydostać. Projekt dostarczył znaczących możliwości nauki w dziedzinie robotyki i AI. Doświadczenie zdobyte w trakcie pracy obejmuje:
- Korzystanie z różnych typów czujników i integracja ich danych.
- Implementację zaawansowanych algorytmów AI do sterowania robotem.
- Praktyczne zastosowanie teorii probabilistycznych modeli grafowych w robotyce.
- Rozwój umiejętności w zakresie symulacji robotów i środowisk w ROS2 i Gazebo.
- Analizę i optymalizację algorytmów w celu poprawy dokładności i efektywności działania systemów robotycznych.