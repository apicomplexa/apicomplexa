# Зоболев Александр - биоинформатик, студент-медик

📍 Архангельск | Telegram: @apicomplexa | GitHub: [apicomplexa](https://github.com/apicomplexa)

Студент 5 курса лечебного факультета СГМУ, биоинформатик научной группы.
Строю воспроизводимые пайплайны для NGS-данных и анализирую их в R и Python.
Клиническая подготовка помогает формулировать биологически и медицински осмысленные
вопросы к данным. Сейчас осваиваю single-cell транскриптомику.

## Образование

[Северный государственный медицинский университет (СГМУ)](https://www.nsmu.ru/university/visit_card/), лечебный факультет - 5 курс, 2022 – н. в.

## Опыт

**Отдел цифровых технологий и инноваций СГМУ** - администратор, май 2026 – н. в.

**Научная группа Know Your Heart** - биоинформатик, июнь 2026 – н. в.
Анализ микробиоты кишечника в популяционной когорте Know Your Heart.

## Проекты

### Микробиота кишечника и депрессия — [kyh_microbio_depression](https://github.com/apicomplexa/kyh_microbio_depression)
16S rRNA (V3–V4), 685 образцов стула, когорта [Know Your Heart (Архангельск)](https://pubmed.ncbi.nlm.nih.gov/30123849/).
- Спроектировал и реализовал пайплайн на **Snakemake 9**: загрузка из SRA → обрезка праймеров
  (cutadapt) → **DADA2** (ASV) → таксономия (**IdTaxa / SILVA**) → функциональное предсказание
  (**PICRUSt2**) → α/β-разнообразие, **PERMANOVA / PERMDISP**.
- Воспроизводимость: зависимости закреплены через **pixi.lock**, отдельные conda-окружения на правило,
  профили запуска на разных платформах.

### Пол эмбриона и онкогенные сигнатуры трофобласта — [PlacentaCancer](https://github.com/apicomplexa/PlacentaCancer)
Реанализ bulk RNA-seq (PRJNA1215956, 12 образцов); доклад на студенческом научном кружке, 2025.
- Пайплайн на **Nextflow**: SRA → FastQC → псевдовыравнивание **kallisto** → MultiQC.
- **tximport + DESeq2** (дифэкспрессия), **GSEA** по онкогенным сигнатурам MSigDB C6;
  интеграция DE и leading-edge генов выявила кандидата **TNFRSF12A** (Fn14).

## Навыки

**Программирование.** Python (pandas, numpy, scipy, matplotlib, seaborn, biopython, gseapy),
R (tidyverse, data.table, ggplot2, Bioconductor: DESeq2, edgeR, phyloseq, DADA2), Bash.

**Биологические базы данных и веб-инструменты.** NCBI (Entrez, SRA, GEO), ENA, Zenodo, Ensembl,
UniProt, PDB, AlphaFold DB, GO, KEGG, Reactome, MSigDB, GTEx, TCGA, KM-plotter; программная загрузка
данных через API и SRA Toolkit.

**Анализ данных.**
- Bulk RNA-seq: kallisto, tximport, DESeq2, GSEA (PlacentaCancer).
- Микробиом 16S: cutadapt, DADA2, SILVA/IdTaxa, PICRUSt2, α/β-разнообразие, PERMANOVA/PERMDISP (vegan)
  на когорте из 685 участников с клиническими метаданными (kyh_microbio_depression).
- Статистика высокоразмерных данных: GLM для count-данных, нормализация (VST), множественные сравнения,
  перестановочные тесты.

**Биологическая интерпретация.** Медицинское образование (4 курса полных курса классического медицинского образования, клиническая практика в стационаре);
интерпретация DE/GSEA в контексте сигнальных путей и клинической онкологии (доклад по TNFRSF12A и
хориокарциноме).

**Машинное обучение.** Понимание статистических моделей, лежащих в основе биоинформатических
инструментов (EM-алгоритм, Dirichlet-multinomial mixtures); работа с AlphaFold и AlphaGenome;
планирую применить ESM / ESM Metagenomic Atlas в проекте по микробиому.

**Воспроизводимость и инфраструктура.** Snakemake, Nextflow, conda, pixi (lockfiles), Git;
Docker и Docker Compose (Dockerfile, compose.yml - в IT-проектах), Apptainer; Linux, HPC (SLURM), Google Colab.

**Сейчас изучаю:** single-cell RNA-seq (scanpy), deep learning для омиксных данных.

## Языки

Русский - родной; английский - свободно говорю и читаю (в том числе научную литературу).
