
# Projekt SIWR (2024)

## Opis Projektu

Ten projekt został wykonany w ramach kursu Sztuczna Inteligencja w Robotyce (SIWR). Głównym celem było stworzenie systemu estymacji stanu dla robota dwukołowego z wykorzystaniem probabilistycznych modeli grafowych. System miał za zadanie lokalizować robota w znanej mapie na podstawie danych z wielu czujników.

## Wymagania Projektu

- Projekt musi być wykonany samodzielnie.
- Praca będzie sprawdzana pod kątem plagiatu, a wykrycie plagiatu skutkuje oceną niedostateczną bez możliwości poprawy.
- Praca musi być oddana poprzez prywatne repozytorium na GitHubie. Proszę utworzyć prywatne repozytorium, nadać prowadzącemu dostęp (login na GitHubie: jpiasek) i przesłać link do repozytorium przez zadanie na stronie kursu.
- Raport opisujący algorytmy należy umieścić w pliku README.md.
- Raport powinien zawierać opis koncepcji i zasady działania projektu, natomiast objaśnienia kodu powinny znajdować się jako komentarze w kodzie.

## Opis

Projekt polega na stworzeniu systemu estymacji stanu robota z wykorzystaniem probabilistycznych modeli grafowych. System ma za zadanie lokalizować robota dwukołowego w znanej mapie na podstawie informacji z wielu czujników.

Dane wejściowe mogą pochodzić z symulacji (np. ROS GAZEBO) lub z gotowego pliku ROSBAG.

Projekt będzie oceniany na podstawie następujących elementów:
- Liczba wykorzystanych systemów pomiarowych (należy użyć min. 3 czujników, np. odometria, IMU, GPS itp.);
- Dokładność działania algorytmu;
- Tryb działania (wyżej oceniane będą projekty, w których publikowana jest wiadomość z estymowaną pozycją, niż takie, w których estymacja następuje offline);
- Czytelność kodu i sprawozdania.

## Szczegóły Implementacji

### Wykorzystane Czujniki
- **LIDAR**: Używany do mapowania i wykrywania przeszkód.
- **Kamery Głębi**: Używane do wykrywania głębokości i przeszkód w środowisku.
- **Odometria i IMU**: Używane do śledzenia pozycji i ruchu robota.

### Implementacja Świata
Robot działa w świecie przypominającym labirynt. Środowisko jest zaprojektowane tak, aby stanowić wyzwanie dla nawigacji robota i jego systemu estymacji stanu.

### Algorytm
Projekt próbował stworzyć algorytm do odczytu danych z czujników odometrii i IMU.

#### TODO
- Implementacja algorytmu subskrybowania tematów i reagowania na wartości z czujników.

> Podjęto wiele prób zaimplementowania tego algorytmu, ale niestety każda zakończyła się niepowodzeniem. Wielodniowe prace nad projektem nie przyniosły finalnie oczekiwanych rezultatów, ale mimo tego nauczyły nas wielu przydatnych umiejętności, takich jak stosowanie sieci Bayesowskich, używanie grafów czynników, warunkowych pól losowych oraz wykorzystania procesów decyzyjnych Markova.

### Przydatne Zasoby
- [Wprowadzenie do Robotyki](https://www.roboticsbook.org/intro.html)
- [Tutoriale GTSAM](https://gtsam.org/tutorials/intro.html)
- [Graph MSF](https://github.com/leggedrobotics/graph_msf)
- [Lokalizacja Robota przy użyciu Skanera Laserowego i Optymalizacji Grafu Pozycji](https://medium.com/@k3083518729/robot-localization-using-laser-scanner-and-pose-graph-optimization-fc40605bf5bc)

## Podsumowanie
Pomimo wyzwań i braku pełnej implementacji zamierzonego algorytmu, projekt dostarczył znaczących możliwości nauki w dziedzinie robotyki i AI. Doświadczenie zdobyte w trakcie pracy będzie wartościowe dla przyszłych projektów i zastosowań w tej dziedzinie.
