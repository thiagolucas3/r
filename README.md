vetor<-c( "dim", "em", "fim", "go", "high", "image", "jam", "king", "low", "magic")
x<-c(1,3,9,27,81,243,729,2187)
x[2]
x[4]
paste(x,x)
rep(x[1:8], times=3)
paste(x, x, sep = "+") # sep é um argumento da função paste
mean(x)    # média
median(x)  # mediana
sd(x)      # desvio padrão
var(x)     # variância
min(x)     # mínimo
max(x)     # máximo
summary(x)
x<-c(1, 3, 9, 27, 81, 243, 729, 2187)
summary(x) # summary, no R, não inclui desvio padrão e variância
matr1<-matrix(1:10, nrow = 2, ncol = 5)
matr1
print(matr1)
media<-mean(x)
x<-c(1, 3, 9, 27, 81, 243, 729, 2187)
media<-mean(x)          # Agora 'media' aparece no Environment
resumo<-summary(x)      # 'resumo' também
plot(x)                   # Um gráfico aparecerá na aba Plots
print(matr1)
plot(matr1)
matr1[1,2]
matr1[2,5]
vetor3<-c(1,3,9,27,81)
vetor9<-c(243,729,2187,6561,19683)
matr3<-matrix(c(1, 3, 9, 27, 81, 243), nrow=3,ncol=2)
matr9<-matrix(c(243,729,2187,6561,19683,59049),nrow=2,ncol=3)
plot(matr3)
plot(matr9)
print(matr9)
listaelemen<-list(v1=vetor3,v2=vetor9,m1=matr3,m2=matr9)
print(listaelemen)
print(listaelemen$m2)
print(listaelemen$m2[2,3])
vetor3+vetor9
vetor3+vetor9[1:5]
vetor3 * vetor9[1:5]
plot(vetor3 * vetor9[1:5])
print(vetor3 * vetor9[1:5])
matr3 + matr3
matr3 * matr3
listaelemen$v1 + listaelemen$v2[1:5]    # Soma de vetores dentro da lista
listaelemen$m1 * 2                      # Multiplicando uma matriz da lista por 2
plot(listaelemen$v1 + listaelemen$v2[1:5])
sum(vetor3,vetor9)
sum(1,3,9,27,81,243,729,2187,6561,19683) # isso mostra que funciona mesmo o somatório com vetores RxR
listaelemen$m2       # Acessa a matriz m2 dentro da lista
listaelemen$v1       # Acessa o vetor v1 dentro da lista

# Vetor com potências de 3 para as linhas
linhas <- 3^(0:4)  # 1, 3, 9, 27, 81

# Vetor com múltiplos de 3 para as colunas
colunas <- c(3, 6, 9)

# Criar data frame com multiplicações
df <- data.frame(
  mult_3 = linhas * 3,
  mult_6 = linhas * 6,
  mult_9 = linhas * 9
)

# Adicionar os valores das potências como nomes das linhas
row.names(df) <- linhas

# Visualizar
print(df)
# Criar o data frame novamente (caso precise)
linhas <- 3^(0:4)  # 1, 3, 9, 27, 81
colunas <- c(3, 6, 9)

df <- data.frame(
  mult_3 = linhas * 3,
  mult_6 = linhas * 6,
  mult_9 = linhas * 9
)
row.names(df) <- linhas

# 1. Gráfico de barras
barplot(as.matrix(df), beside = TRUE, col = c("blue", "red", "green"),
        legend.text = colnames(df), args.legend = list(title = "Múltiplos de 3"),
        main = "Gráfico de Barras: Múltiplos de 3",
        ylab = "Valores")

# 2. Gráfico de linha
matplot(df, type = "b", col = c("blue", "red", "green"), pch = 19,
        main = "Gráfico de Linha: Múltiplos de 3", ylab = "Valores", xlab = "Potências de 3")
legend("topright", legend = colnames(df), col = c("blue", "red", "green"), pch = 19)

# 3. Gráfico de dispersão
plot(df$mult_3, df$mult_6, main = "Gráfico de Dispersão", 
     xlab = "Multiplicação por 3", ylab = "Multiplicação por 6", col = "blue", pch = 19)
points(df$mult_3, df$mult_9, col = "red", pch = 19)
legend("topright", legend = c("Multiplicação por 6", "Multiplicação por 9"), 
       col = c("blue", "red"), pch = 19)
library(ggplot2)
# Criar o data frame com potências de 3
dados <- data.frame(
  nome = c("a", "b", "c", "d", "e", "f", "g", "h", "i", "j"),
  pot3 = 3^(0:9),
  dobro = 2 * 3^(0:9)
)
# Gráfico de barras para potências de 3
ggplot(dados, aes(x = nome, y = pot3, fill = nome)) +
  geom_bar(stat = "identity") +
  labs(title = "Gráfico de Barras: Potências de 3", x = "Nome", y = "Potência de 3") +
  theme_minimal()
# Gráfico de barras para os nomes
ggplot(dados, aes(x = nome, y = dobro, fill = nome)) +
  geom_bar(stat = "identity") +
  labs(title = "Gráfico de Barras: Dobro das Potências de 3", x = "Nome", y = "Dobro") +
  theme_minimal()

print(vetorn)
