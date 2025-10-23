# spotify-brazil-lyrics-sentiment-2014-2023
Datasets created for a sentiment analysis study of song lyrics by the most listened artists on Spotify Brazil (2014–2023).

Datasets criados para o Trabalho de Conclusão de Curso (TCC) sobre análise de sentimento em letras de músicas, considerando os artistas mais ouvidos no Spotify Brasil entre 2014 e 2023.  
A análise de sentimento das letras foi realizada utilizando o modelo **BERTimbau**, pré-treinado para a língua portuguesa e ajustado a partir do dataset GoEmotions.

## Contexto e Objetivo
Este repositório reúne três bases de dados elaboradas a partir de informações do Spotify Brasil entre 2014 e 2023. O objetivo do trabalho é investigar como técnicas de análise de sentimento podem ser aplicadas às letras de músicas, observando padrões linguísticos e emocionais na produção dos artistas mais populares do período.  

A análise de sentimento das letras foi realizada com o modelo **BERTimbau** ajustado a partir do dataset GoEmotions, permitindo classificar emoções e gerar scores de sentimento em textos em português.

---

## Datasets
- **df_albuns.csv**  
  Contém informações sobre os álbuns dos artistas analisados.  
  Principais colunas:  
  `artist_id`, `album_id`, `album_name`, `album_type`, `album_group`, `release_date`, `release_date_precision`, `total_tracks`, `external_url`.

- **df_letras.csv**  
  Reúne as letras das músicas coletadas e suas análises de sentimento realizadas com **BERTimbau**.  
  Principais colunas:  
  `artist_id`, `ranking_spotify`, `nome_artista`, `track_name`, `track_name_limpo`, `musica_letra`, `idioma`, `letras_traduzidas`, `letras_lematizadas`, `letras_sem_stopwords`, `release_date`, `ano`, `explicit`, `track_release_count`, `genero_musical`, `emocoes_detectadas`, `score_emocao`, `emocao_label`.

- **df_tracks.csv**  
  Inclui detalhes de cada faixa disponível no Spotify.  
  Principais colunas:  
  `artist_name`, `track_artists`, `album_name`, `release_date`, `release_year`, `track_id`, `track_number`, `track_name`, `duration_ms`, `explicit`, `parceria`, `external_url`.

---

## Como usar
Exemplo em Python com pandas:

```python
import pandas as pd

df_albuns = pd.read_csv("df_albuns.csv")
df_letras = pd.read_csv("df_letras.csv")
df_tracks = pd.read_csv("df_tracks.csv")

print(df_letras.head())
