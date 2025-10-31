# 제어공학 과제 
**학번:** 2023732001  
**이름:** 임동현 

#  5주차 1차시 강의 요약  
### 주제: 상태변수(State Variables)와 상태공간방정식(State Space Equation)

##  1. 상태변수의 개념 (The Concept of State Variables)
- **상태변수(State Variable)** : 시스템의 현재 상태를 완전히 나타내는 최소 개수의 변수  
- 시스템은 **입력(Input)** → **상태(State)** → **출력(Output)** 으로 구성됨  
- 입력이 상태에 영향을 주고, 상태는 다시 출력으로 반영됨  
- 시스템의 동적 특성을 수학적으로 표현할 때 상태변수가 핵심 역할을 함  

## 예제 1 : 질량-스프링-댐퍼 시스템 (Spring-Mass-Damper System)

**구성요소**  
- 질량 M, 스프링 상수 k, 감쇠 계수 b, 외력 r(t)

**운동방정식**  
> M·(d²y/dt²) + b·(dy/dt) + k·y(t) = r(t)

**상태변수 정의**  
> x₁(t) = y(t)  
> x₂(t) = dy(t)/dt

**상태방정식**
> dx₁/dt = x₂  
> dx₂/dt = -(b/M)x₂ - (k/M)x₁ + (1/M)r(t)  
> 출력: y(t) = x₁(t)

 **해석:**  
2차 미분방정식을 1차 미분방정식 두 개로 분리하여 상태공간 형태로 표현.

---

## 예제 2 : R–L–C 회로 (RLC Circuit System)

**구성요소**  
전류원 u(t), 인덕터 L, 저항 R, 커패시터 C  

**상태변수 정의**  
> x₁(t) = 커패시터 전압 v_c(t)  
> x₂(t) = 인덕터 전류 i_L(t)

**KCL (전류법칙)**  
> u(t) = C·(dx₁/dt) + x₂  
> → dx₁/dt = (1/C)[-x₂ + u(t)]

**KVL (전압법칙)**  
> L·(dx₂/dt) + R·x₂ - x₁ = 0  
> → dx₂/dt = (1/L)[x₁ - R·x₂]

**출력식**  
> y(t) = R·x₂(t)

 **해석:**  
RLC 회로의 동적 관계를 KCL과 KVL로부터 유도하여 상태방정식으로 표현.

---

##  4. 1차 상태미분방정식 (1st Order State Differential Equation)

**기본 형태**  
> dx/dt = a·x(t) + b·u(t)

**라플라스 변환**  
> X(s) = (1 / (s - a))x(0) + (1 / (s - a))bU(s)

**시간 영역 해**  
> x(t) = e^(a·t)x(0) + ∫[e^(a(t-τ))b·u(τ)dτ]

- 첫 번째 항 → 초기 상태의 영향  
- 두 번째 항 → 입력의 영향  

---

## 상태공간방정식의 일반형 (State Space Representation)

**상태벡터**
> x(t) = [x₁(t), x₂(t), ..., xₙ(t)]ᵀ

**일반형**
> dx/dt = A·x(t) + B·u(t)  
> y(t) = C·x(t) + D·u(t)


