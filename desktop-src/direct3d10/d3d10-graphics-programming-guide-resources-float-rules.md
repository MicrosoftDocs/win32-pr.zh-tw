---
description: Direct3D 10 支援數個不同的浮點數標記法。 所有浮點數運算都是在定義的 IEEE 754 32 位單一精確度浮點數行為的子集下運作。
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: " (Direct3D 10) 的 FFloating 點規則"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966634"
---
# <a name="floating-point-rules-direct3d-10"></a> (Direct3D 10) 的浮點規則

Direct3D 10 支援數個不同的浮點數標記法。 所有浮點數運算都是在定義的 IEEE 754 32 位單一精確度浮點數行為的子集下運作。

-   [32位 Floating-Point 規則](#32-bit-floating-point-rules)
    -   [接受 IEEE-754 規則](#honored-ieee-754-rules)
    -   [IEEE-754 規則的偏差或其他需求](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [16位 Floating-Point 規則](#16-bit-floating-point-rules)
-   [11位和10位 Floating-Point 規則](#11-bit-and-10-bit-floating-point-rules)
-   [相關主題](#related-topics)

## <a name="32-bit-floating-point-rules"></a>32位 Floating-Point 規則

有兩組規則：符合 IEEE-754 的規則，以及偏離標準的規則。

### <a name="honored-ieee-754-rules"></a>接受 IEEE-754 規則

有些規則是單一選項，由 IEEE-754 提供選擇。

-   除以 0 會產生 +/- INF，除了 0/0 得到 NaN 的結果。
-   (+/-) 0 的對數會產生 -INF。 負值 (-0 除外) 的對數會產生 NaN。
-   負數的反平方根 (rsq) 或平方根 (sqrt) 會產生 NaN。 例外是 -0；sqrt(-0) 會產生 -0，而 rsq(-0) 會產生 -INF。
-   INF - INF = NaN
-   (+/-)INF / (+/-)INF = NaN
-    (+/-) INF \* 0 = NaN
-   NaN (任意 OP) 任意值 = NaN
-   比較 EQ、GT、GE、LT 和 LE，若任一個或兩個運算元皆為 NaN，則傳回 **FALSE**。
-   比較會忽略 0 的正負號 (因此 +0 等於 -0)。
-   比較 NE，若任一個或兩個運算元皆為 NaN，則傳回 **TRUE**。
-   任何非 NaN 值與 +/- INF 比較會傳回正確的結果。

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>IEEE-754 規則的偏差或其他需求

-   IEEE-754 需要浮點運算產生結果，此結果為最接近無限精確結果的可表示值，也稱為 round-to-nearest-even。 但是，Direct3D 10 定義了較鬆散需求：32位的浮點運算會產生一個單位-最後一個單元中的結果， (1 ULP) 的無限精確度結果。 這表示，例如硬體允許截斷結果至 32 位元，而不是執行 round-to-nearest-even，因為這樣會讓最多一個 ULP 產生錯誤。
-   不支援浮點例外、狀態位元或設陷。
-   Denorm 會在任何浮點數學運算的輸入和輸出上，排清至保留正負號的零。 不會運算元據的任何 i/o 或資料移動作業都會發生例外狀況。
-   包含浮點值的狀態（例如，MinDepth/MaxDepth、邊框型值等）可提供為 denorm 值，而且可能會在硬體使用之前或可能不會被清除。
-   最小值或最大值作業會針對比較排清 denorm，但結果不一定會是排清 denorm。
-   對作業的 NaN 輸入一律會在輸出上產生 NaN，不過，不需要 NaN 的確切位模式來維持相同的 (除非作業是原始的移動指令，而這完全不會改變數據。 ) 
-   只有一個運算元為 NaN 的最小或最大作業會傳回另一個運算元作為結果， (與上述) 的比較規則相反。 這是在 Direct3D 10 中所需 (IEEE 754R) 的新 IEEE 規則。
-   另一個新的 IEEE 754R 規則是 min (-0、+ 0) = = min (+ 0、-0) = =-0 和 max (-0、+ 0) = = max (+ 0、-0) = = + 0 （相較于上述 (所述的帶正負號零) 的比較規則）。 Direct3D 10 在此建議 IEEE 754R 行為，但不會強制執行;您可以使用忽略符號的比較，讓比較零的結果相依于參數的順序。
-   \*除了 denorm 排清) 之外，x 1.0 f 一律會產生 x (。
-   x/1.0f 一律產生 x (除了會排清 denorm)。
-   x +/- 0.0f 一律產生 x (除了會排清 denorm)。 但是 -0 + 0 = +0。
-   合併運算 (例如 mad、dp3) 產生的結果肯定比非合併擴展運算可能最差的序列評估順序精確。 請注意，最差可能順序的定義（基於容錯目的）不是指定之融合作業的固定定義;這取決於輸入的特定值。 Unfused 擴充中的個別步驟分別允許1個 ULP 容忍 (或針對任何 Direct3D 10 呼叫的指示，其中具有比 1 ULP 更寬鬆的容錯能力，) 允許較寬鬆的容錯。
-   合併運算遵循與非合併運算相同的 NaN 規則。
-   將每個在32位浮點精確度層級的作業相乘和相除 (精確度為 1 ULP) 。

## <a name="16-bit-floating-point-rules"></a>16位 Floating-Point 規則

Direct3D 10 也支援以16位表示的浮點數。

格式：

-   在 MSB 位元位置 1 帶正負號位元 (s)
-   5 位元偏置指数 (e)
-   10 位元分數 (f)，含一個額外的隱藏位元

 (v) 的 float16 值會遵循下列規則：

-   若 e == 31 且 f != 0，則 v 為 NaN，不考慮 s
-   如果 e = = 31 且 f = = 0，則 v = (-1) \* 無限大 (帶正負號的無限大) 
-   如果 e 介於0和31之間，則 v = (-1) s \* 2 (e-15) \* (1. f) 
-   如果 e = = 0 和 f！ = 0，則 v = (-1) s \* 2 (e-14) \* (0 f)  (反正規化數位) 
-   如果 e = = 0 且 f = = 0，則 v = (-1) s \* 0 (帶正負號的零) 

32位浮點規則也會保存16位浮點數，並針對上面所述的位配置進行調整。 例外狀況包括：

-   精確度︰16 位元浮點數的未合併運算產生的結果為最接近無限精確結果的可表示值 (進位置最接近偶數，依照 IEEE-754，適用於 16 位元值)。 32 位元浮點規則遵循 1 ULP 誤差，16 位元浮點規則針對非合併運算遵循 0.5 ULP，合併運算則為 0.6 ULP。
-   16 位元浮點數保留 denorm。

## <a name="11-bit-and-10-bit-floating-point-rules"></a>11位和10位 Floating-Point 規則

Direct3D 10 也支援11位和10位浮點數格式。

格式：

-   不帶正負號的位元
-   5 位元偏置指数 (e)
-   11 位元格式為 6 位元分數 (f)，10 位元格式為 5 位元分數 (f)，兩者皆有一個額外的隱藏位元。

float11/float10 值 (v) 遵循下列規則：

-   若 e == 31 且 f != 0，則 v 為 NaN
-   若 e == 31 且 f == 0，則 v = +infinity
-   如果 e 介於0和31之間，則 v = 2 (e-15) \* (1. f) 
-   如果 e = = 0 和 f！ = 0，則 v = \* 2 (e-14) \* (0. f)  (反正規化數位) 
-   若 e == 0 且 f == 0，則 v = 0 (零)

32位浮點規則也會保留11位和10位浮點數，並針對上面所述的位配置進行調整。 例外狀況包括：

-   精確度︰32 位元浮點規則遵循 0.5 ULP。
-   10/11 位元浮點數保留 denorm。
-   任何會產生小於零之數位的作業都會壓制為零。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



