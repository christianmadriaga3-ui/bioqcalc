# BioqCalc
Más de 80 calculadoras clínicas para bioquímicos — sin backend, sin cookies, 100% offline

Herramienta web de apoyo profesional para bioquímicos y profesionales de laboratorio clínico. Agrupa más de 80 calculadoras organizadas en 11 áreas clínicas, con desarrollo paso a paso de cada fórmula, interpretación contextualizada y bibliografía referenciada.

> **Versión actual:** v1.8  
> **Estado:** Archivo HTML único — sin dependencias externas, sin backend, sin cookies.

---

## Demo rápido

https://christianmadriaga3-ui.github.io/bioqcalc/bioquimica_clinica_v1_8.html

Descargá o cloná el repositorio y abrí `bioquimica_clinica_v1_8.html` en cualquier navegador moderno. No requiere instalación ni conexión a internet.

```bash
git clone https://github.com/christianmadriaga3-ui/bioquimica-clinica.git
cd bioquimica-clinica
# Abrí bioquimica_clinica_v1_8.html en tu navegador
```

---

## Áreas clínicas cubiertas

| Área | Calculadoras incluidas |
|------|------------------------|
| **Nefrología** | CKD-EPI 2021, MDRD-4, Schwartz, HUGE, EKFC 2021, FENa, FEUrea, FE Ca²⁺, FE K⁺, FE Mg²⁺, FE P + TRP, Índice P/Cr, Índice A/Cr, KDIGO ERC, AKI KDIGO 2012, orientación etiológica AKI |
| **Lípidos** | Friedewald, Martin-Hopkins, Sampson 2020, Castelli I y II, TG/HDL, No-HDL, VLDL estimado, Perfil completo |
| **Función hepática** | Child-Pugh, MELD, MELD 3.0, NFS, FIB-4, De Ritis, GGT/FAL, Índice R (DILI), perfil AST/ALT/FAL, fracciones de bilirrubina |
| **Diabetes / Glucemia** | Glucemia en ayunas ADA 2024, HbA1c → eAG, HOMA-IR, HOMA-β, QUICKI, TyG, PTOG 75 g (ADA, IADPSG/OMS, ALAD) |
| **Equilibrio ácido-base** | Gasometría arterial completa, Henderson-Hasselbalch inverso, compensaciones (6 variantes), Anión gap + corrección por albúmina, Delta-delta, SID Stewart simplificado |
| **Hematología** | 7 índices de cribado para microcitosis (Mentzer, England-Fraser, Green-King, Shine-Lal, Srivastava, RDW-I, Ricerca), reticulocitos corregidos, IPR, diferencial absoluto, N/L, P/L, L/M, SII, desviación a la izquierda |
| **Electrolitos / Osmolaridad** | Osmolaridad plasmática (3 fórmulas + brecha osmolar), Na corregido por glucemia (Katz y Hillier), déficit de agua libre, déficit de Na⁺, K corrregido por pH, aldosterona/ARP, osmolaridad y brecha osmolar urinaria |
| **Calcio y fósforo** | Ca corregido por albúmina (Payne), Ca iónico estimado (Siggaard-Andersen), perfil completo de calcio, producto Ca×P, clasificación de fosfatemia |
| **Nutrición clínica** | NRI (Buzby), GNRI (Bouillanne), perfil combinado NRI + GNRI |
| **Inflamación / Sepsis** | SOFA (Sepsis-3), qSOFA, ratio PCR/Albúmina |
| **Coagulación** | INR con ISI (OMS), ratio TP, prueba de mezcla KPTT, Score CID ISTH 2001, índice D-dímero/Fibrinógeno |

---

## Características

- **Sin dependencias**: un único archivo `.html` con CSS y JS embebidos.  
- **Sin servidor**: funciona localmente o desde cualquier hosting estático (GitHub Pages, Netlify, etc.).  
- **Modo oscuro automático**: responde a `prefers-color-scheme` del sistema operativo.  
- **Bibliografía referenciada**: cada calculadora muestra sus referencias con enlace a DOI.  
- **Desarrollo paso a paso**: los resultados muestran cada paso del cálculo, no solo el número final.  
- **Interpretación clínica contextualizada**: los rangos de referencia incluyen su fuente y las variables que los modifican.

---


## Limitaciones conocidas

- La prueba de mezcla KPTT muestra el resultado a tiempo 0. La incubación a 37 °C (para detectar inhibidores tiempo-dependientes como el anti-VIII adquirido) debe interpretarse de forma manual.  
- El Ca iónico es una **estimación por fórmula**. Para decisiones clínicas críticas (UCI, neonatología, transfusión masiva) se requiere medición directa por electrodo ión-selectivo (ISE).  
- Los índices de cribado de microcitosis (Mentzer, England-Fraser, etc.) son herramientas orientativas. No reemplazan el ferrugrama ni la electroforesis/HPLC de hemoglobina.  
- El SOFA requiere datos clínicos (Glasgow, PAM, vasopresores) que no provienen del laboratorio; la calculadora los solicita explícitamente.

---

## Bibliografía principal

Las referencias completas se muestran al pie de cada calculadora. Las guías y trabajos originales más citados son:

- KDIGO CKD Work Group (2022). *Kidney International*, 102(3S).
- Inker LA et al. (2021). CKD-EPI 2021. *NEJM*, 385(19).
- Singer M et al. (2016). Sepsis-3. *JAMA*, 315(8).
- Kim WR et al. (2021). MELD 3.0. *Gastroenterology*, 161(6).
- ADA Professional Practice Committee (2024). *Diabetes Care*, 47(Suppl 1).
- Grundy SM et al. (2019). AHA/ACC lipids. *JACC*, 73(24).
- Taylor FB Jr et al. (2001). Score CID ISTH. *Thromb Haemost*, 86(5).
- EASL-EASD-EASO (2024). MASLD guidelines. *J Hepatol*, 82(6).

---

## Historial de versiones

| Versión | Cambios principales |
|---------|---------------------|
| v1.8 | Implementación de handlers faltantes (Child-Pugh, MELD clásico, NFS, GGT/FAL). Corrección de divisiones por cero en Delta-delta y prueba de mezcla KPTT. |
| v1.7 | Adición de módulos Coagulación, Inflamación/Sepsis, Calcio/Fósforo, Electrolitos, Nutrición clínica, Hematología y Equilibrio ácido-base. |
| v1.0 | Versión inicial con Nefrología, Lípidos, Función hepática y Diabetes. |

---

## Aviso profesional

Esta herramienta es de **apoyo profesional** para uso por bioquímicos y profesionales de laboratorio.  
**No reemplaza el criterio clínico del bioquímico ni del médico tratante.**  
Los resultados deben interpretarse siempre en el contexto clínico completo del paciente.

---

## Licencia

MIT License — libre para uso, modificación y distribución con atribución.

```
Copyright (c) 2025
```
