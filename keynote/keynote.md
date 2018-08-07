# [fit] Reinforcement 
# [fit] Learning
## [fit] **wprowadzenie**
## by **Tooploox AI**
Jeremi Kaczmarczyk
Rafał  Nowak
Piotr  Semberecki

^ Presenter notes

---

# Reinforcement Learning

> Reinforcement Learning - jest to uczenie co zrobić - jak dopasować sytuacje do akcji aby zmaksymalizować numeryczny sygnał nagrody
- Reinforcement Learning: An Introduction 2nd ed

^ Presenter notes

---

# State - **stan**

# [fit] $$\large{s}, \large{s^{\prime}}, \large{s_{t}}$$

Stan określamy symbolem $$\large{s}$$ i jest to obecna sytuacja w jakiej znajduje się środowisko. Jako $$\large{s^{\prime}}$$ oznaczamy stan będący rezultatem stanu $$\large{s}$$, natomiast $$\large{s_{t}}$$ jest to stan dla danego kroku.

^ Presenter notes

---

## Action - **akcja**

# [fit] $$\large{a}, \large{a_{t}}$$

Znajdując się w stanie $$\large{s}$$ możemy wykonać akcję $$\large{a}$$. Akcja powoduję zmianę stanu z $$\large{s}$$ do $$\large{s^{\prime}}$$.

^ Presenter notes

---

## Reward - **nagroda**

# [fit] $$\large{r}, \large{r_{t}}$$

Po wykonaniu akcji otrzymujemy nagrodę $$\large{r}$$ od środowiska. Nagrodę otrzymujemy po każdym kroku i niekoniecznie jest pozytywna. Projektowanie sygnału nagrody ma kluczowe znaczenie przy rozwiązywaniu problemów Reinforcement Learningiem.

^ 
- Przykłady, dlaczego nie projektujemy nagrody za stany cząstkowe, np. Szachy. Jeśli damy nagrodę za stany cząstkowe lub zbijanie figur przeciwnika, algorytm będzie optymalizował pod to nie pod wygrywanie, etc. 
- AlphaGo, nagroda za zwycięstwo, algorytm wpada na rozwiązania nie znane dotychczas.

---

# Policy - **polityka**

# [fit] $$\large{\pi}, \large{\pi(s)}, \large{\pi(a|s)}$$


Polityka definiuje zachowanie w danym momencie. Jest to funkcja parametryzowana zwykle stanem lub parą stan-akcja. W przypadku prostych problemów jest to zwykle słownik. Zwraca akcję którą agent powinien wykonać w danym stanie albo prawdopodobieństwa wykonania każdej z akcji.

^ Presenter notes

--- 

## Value - **wartość**

# [fit] $$\large{v_{\pi}(s)}, \large{q_{\pi}(s, a)}$$

Wartość określana jest w stosunku do danej polityki $$\large{\pi}$$. Określana jako $$\large{v}$$ jeśli jest to wartość dla stanu, albo $$\large{q}$$ jeśli dla pary stan-akcja.    Jest to numeryczna wartość określająca jak dobrze jest być w danym stanie albo inaczej jaka jest średnia skumulowana nagroda możliwa w danym stanie lub dla danej pary stan-akcja.

^ Presenter notes

---

# Agent - środowisko

![inline](figtmp7.png)

^ Presenter notes

---

# Taxi

*  `:` możemy przejść, przez `|` nie
*  `R`, `G`, `Y`, `B` miejsca podnoszenia / zostawienia pasażerów
* +20 nagrody za sukces
* -10 nagrody za nielegalne podniesienie / zostawienie
* -1 nagrody za każdy ruch

![fill right](taxi_random.gif)

^ Presenter notes

---

# Markov Decision Process - MDP

