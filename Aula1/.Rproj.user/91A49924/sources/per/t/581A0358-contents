#Instale o pacote ggplot2 caso não tenha instalado executando: 
  # install.packages("ggplot2")
  
  # Carregar a biblioteca
  library(ggplot2)

# Recriando o dataframe (caso não esteja salvo na sessão)
dados <- data.frame(
  Planta = c(1, 2, 3, 4, 5, 6, 7, 8),
  Tratamento = c("Controle", "Controle", "Controle", "Controle", 
                 "Fungicida", "Fungicida", "Fungicida", "Fungicida"),
  Severidade_doenca = c(42, 38, 45, 40, 12, 18, 15, 10)
)

# Criar o gráfico
grafico <- ggplot(dados, aes(x = Tratamento, y = Severidade_doenca, fill = Tratamento)) +
  geom_boxplot(alpha = 0.7) + # Adiciona o boxplot
  geom_jitter(width = 0.2, size = 3, color = "black") + # Adiciona os pontos de cada planta
  labs(
    title = "Efeito do Fungicida na Severidade da Doença",
    x = "Tratamento",
    y = "Severidade da doença (%)"
  ) +
  theme_classic() + # Deixa o visual mais limpo
  scale_fill_manual(values = c("Controle" = "#e74c3c", "Fungicida" = "#2ecc71")) + # Cores personalizadas
  theme(
    legend.position = "none", # Remove a legenda pois os nomes já estão no eixo X
    plot.title = element_text(hjust = 0.5, face = "bold", size = 14),
    axis.title = element_text(face = "bold")
  )

# Visualizar o gráfico
print(grafico)
