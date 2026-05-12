# 📚 Banco de Preguntas: Tema Criptoseguridad

## Pregunta 1
Encuentre el inverso multiplicativo de 29 en $\mathbb{Z}/97\mathbb{Z}$  

- [ ] 45
- [ ] 1/29
- [ ] 37
- [x] **87**

**Explicación:** Necesitamos $x$ tal que $29x \equiv 1 \pmod{97}$. En [[Criptografía]], usando el Algoritmo de Euclides Extendido encontramos que $29 \times (-10) = -290 = 3(-97) + 1$, por lo que el inverso es $-10$. Al pasarlo a formato positivo usando el módulo obtenemos $-10 + 97 = 87$. Comprobación: $29 \times 87 = 2523 \equiv 1 \pmod{97}$.

---

## Pregunta 2
Alicia y Beto desean crear un numero secreto compartido utilizando el protocolo Diffie-Hellman. Supongamos que Alicia y Beto acuerdan, de manera pública en utilizar $p=23$ para el módulo y $g=5$ para la base. Encontrar el secreto compartido $s$, si el número secreto de Alice es $a=4$ y el número secreto de Bob es $b=3$.

- [ ] 21
- [x] **18**
- [ ] 7
- [ ] 5

**Explicación:** En el intercambio de llaves [[Diffie-Hellman]], el secreto es $s = g^{ab} \pmod p$. Reemplazando: $s = 5^{4 \times 3} \pmod{23} = 5^{12} \pmod{23}$. Podemos calcular $5^3 = 125 \equiv 10 \pmod{23}$. Luego, $10^4 = 100^2 \equiv 8^2 = 64 \equiv 18 \pmod{23}$. El secreto es 18.

---

## Pregunta 3
Alicia desea mandarle a Beto un mensaje encriptado utilizando el protocolo ElGamal. Beto elige como parametros $q=17$ como orden del grupo, $g=3$ como generador y $b=15$ como número secreto. La llave pública para la encriptación de mensajes está dada por $(q,g,e)$ donde $e=6$. Alicia le manda a Beto el mensaje cifrado $(c_1,c_2)=(5,8)$. ¿Cúal es el valor del mensaje original $m$?

- [ ] 5
- [ ] 10
- [ ] 8
- [x] **6**

**Explicación:** Para desencriptar en [[ElGamal]], usamos $m = c_2 \cdot (c_1^b)^{-1} \pmod q$. Sabemos que $c_1 = 5$ y $b = 15$. 
$c_1^{15} = 5^{15} \pmod{17} \equiv 5^{-1} \pmod{17} \equiv 7 \pmod{17}$.
Necesitamos el inverso de $c_1^b$ que es el inverso de $7 \pmod{17}$, el cual es 5 (ya que $7 \times 5 = 35 \equiv 1 \pmod{17}$). 
Multiplicamos: $m = 8 \times 5 = 40 \equiv 6 \pmod{17}$.

---

## Pregunta 4
Supongamos que trabajamos sobre el campo finito con orden $p=5$ y consideramos la curva elíptica $y^{2}= x^{3} +x +1$. Dado $P=(3,1)$, encontrar $Q=3P$.

- [ ] $Q=(3,1)$
- [ ] $Q=O$ (La identidad en la curva elíptica)
- [ ] $Q=(3,4)$
- [x] **$Q=(2,4)$**

**Explicación:** La adición en una [[Curva elíptica]] se hace sumando puntos. Primero obtenemos $2P$: calculamos la pendiente $\lambda$ derivando ($x_1=3, y_1=1$); $\lambda = (3(3)^2+1)/(2(1)) = 28/2 \equiv 3/2 \equiv 3 \times 3 = 9 \equiv 4 \pmod 5$. Con $\lambda=4$, $x_{2P} = 16-3-3 \equiv 0 \pmod 5$ y $y_{2P} = 4(3-0)-1 = 11 \equiv 1 \pmod 5$. Tenemos $2P = (0,1)$. Ahora $3P = 2P + P = (0,1) + (3,1)$. Como son puntos diferentes, $\lambda = (1-1)/(3-0) = 0$. Al calcular obtenemos $x_{3P} = 0 - 0 - 3 \equiv 2 \pmod 5$ y $y_{3P} = 0(0-2) - 1 = -1 \equiv 4 \pmod 5$. Por lo tanto, $Q = (2,4)$.

---

