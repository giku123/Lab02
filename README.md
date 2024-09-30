
SnakeGame este o implementare a jocului clasic "Snake", în care jucătorul controlează un șarpe care se mișcă pe o tablă, având scopul de a mânca mere. Pe măsură ce șarpele consumă mere, acesta crește în lungime, iar provocarea devine mai mare, evitând coliziunile cu pereții sau cu propriul corp. Jocul se încheie atunci când jucătorul comite o greșeală.

Componentele Proiectului
1. point.hpp
Funcționalitate: Definește structura Point, care reprezintă coordonatele x și y ale unui punct pe tablă. Aceasta este esențială pentru poziționarea șarpelui, a merelor și a altor obiecte.

Structură:

Constructor implicit: Inițializează coordonatele la 0.
Constructor cu parametri: Permite setarea coordonatelor x și y la valori specificate.
2. snake.hpp
Funcționalitate: Reprezintă șarpele, gestionând poziția și comportamentul acestuia.

Elemente principale:

segments[100]: Un array ce stochează până la 100 de segmente ale șarpelui.
length: Reține lungimea actuală a șarpelui.
Funcții cheie:

Move(Point direction): Mută șarpele într-o direcție dată.
Grow(): Adaugă un segment la coadă, crescând astfel lungimea.
GetHeadPosition(): Returnează poziția capului șarpelui.
3. board.hpp
Funcționalitate: Reprezintă tabla de joc, gestionând dimensiunile și desenarea elementelor pe tablă.

Elemente principale:

width și height: Dimensiunile tablei.
Funcții cheie:

GetWidth(): Returnează lățimea tablei.
GetHeight(): Returnează înălțimea tablei.
4. .gitignore
Definiții: Specifică setările pentru compilare.

CXX: Compilatorul utilizat (g++).
CXXFLAGS: Opțiunile de compilare, ***** ar fi -Wall și -std=c++17.
EXEC: Numele fișierului executabil.
SRC: Fișierele sursă care trebuie compilate, inclusiv main.cpp.
OBJ: Fișierele obiect generate.
Implementarea Funcțiilor
5. board.cpp
Constructorul Board(int w, int h): Inițializează tabla de joc cu dimensiunile specificate.

Funcții:

GetWidth() și GetHeight(): Returnează dimensiunile tablei, asigurând limitele de mișcare ale șarpelui.
6. snake.cpp
Constructorul Snake(): Setează poziția inițială a șarpelui și lungimea acestuia la 1.

Funcții:

Move(): Actualizează pozițiile segmentelor șarpelui.
Grow(): Crește lungimea șarpelui adăugând un nou segment.
GetHeadPosition(): Obține poziția capului șarpelui.
Concluzie
SnakeGame este o implementare simplă, dar captivantă a unui joc clasic, având o structură clară și modulară. Fiecare componentă joacă un rol esențial în funcționarea jocului, permițând jucătorilor să se bucure de o experiență retro autentică.