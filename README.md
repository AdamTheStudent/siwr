
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
Projekt próbował stworzyć algorytm do odczytu danych z czujników odometrii i IMU.

Algorytm składał się z kilku kluczowych kroków:
1. Subskrybowanie tematów ROS dotyczących odometrii i IMU.
2. Przetwarzanie danych z tych czujników w celu oszacowania pozycji i orientacji robota.
3. Implementacja filtrów i algorytmów do estymacji stanu robota na podstawie odczytów z czujników.
4. Integracja danych z odometrii i IMU w celu poprawy dokładności lokalizacji.

#### TODO
- Implementacja algorytmu subskrybowania tematów i reagowania na wartości z czujników.

> Podjęto wiele prób zaimplementowania tego algorytmu, ale niestety każda zakończyła się niepowodzeniem. Wielodniowe prace nad projektem nie przyniosły finalnie oczekiwanych rezultatów, ale mimo tego nauczyły nas wielu przydatnych umiejętności, takich jak stosowanie sieci Bayesowskich, używanie grafów czynników, warunkowych pól losowych oraz wykorzystania procesów decyzyjnych Markova.

### Literatura
- [Wprowadzenie do Robotyki](https://www.roboticsbook.org/intro.html)
- [Tutoriale GTSAM](https://gtsam.org/tutorials/intro.html)
- [Graph MSF](https://github.com/leggedrobotics/graph_msf)
- [Lokalizacja Robota przy użyciu Skanera Laserowego i Optymalizacji Grafu Pozycji](https://medium.com/@k3083518729/robot-localization-using-laser-scanner-and-pose-graph-optimization-fc40605bf5bc)

## Podsumowanie
Pomimo wyzwań i braku pełnej implementacji zamierzonego algorytmu, projekt dostarczył znaczących możliwości nauki w dziedzinie robotyki i AI. Doświadczenie zdobyte w trakcie pracy będzie wartościowe dla przyszłych projektów i zastosowań w tej dziedzinie.
