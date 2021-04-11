---
title: VML Eqn 屬性
description: VML Eqn 屬性
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da00084a825147c6f8a05f503e5ee2679f40e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316414"
---
# <a name="vml-eqn-attribute"></a>VML Eqn 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義公式所使用的方程式。 讀取/寫入 **字串**。

**適用於**

[公式](msdn-online-vml-formulas-element.md)) 的[F](msdn-online-vml-f-element.md) (子項目

**標記語法**

<v： *element* eqn = " *expression* " >

**指令碼語法**

 eqn = "*expression*"

*運算式* =** eqn

**備註**

方程式是藉由評估具有運算一般形式的文字運算式來定義，並在後面加上最多三個引數。 每個引數都可以是下列類型：

-   調整 (例如， \# 2) 
-   另一個公式 (例如， @2) 
-   固定數位 (例如，2) 
-   預先定義的值

下表定義可搭配選擇性引數使用的公式，指定名稱為 *v*、 *p1* 和 *p2*。公式模式為：

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| 作業 | Params | 精確  | 結果                    | 描述                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| 瓦爾       | 1      | 是    | v                         | 定義其他值的輔助線值。                                   |
| Sum       | 3      | 是    | v + p1-p2               | 用於加法和減法。                                             |
| product   | 3      | 輪 | v \* p1/p2              | 用於乘法和除法。                                          |
| mid       | 2      |  (c)     |  (v + p1) /2               | 平均。                                                                       |
| abs       | 1      | 是    | abs (v)                     | 絕對值。                                                                |
| 分鐘       | 2      | 是    | min (v，p1)                  | V 和 p1 的較小值。                                                  |
| max       | 2      | 是    | max (v，p1)                  | V 和 p1 的值愈大。                                                 |
| if        | 3      | 是    | v > 0？ p1： p2        | 條件式測試。                                                           |
| mod       | 3      | 不可以     | sqrt (v ^ 2 + p1 ^ 2 + p2 ^ 2)    | 模數值。                                                                 |
| atan2     | 2      | 不可以     | atan2 (p1，v)                | 以度為單位 \* 2 ^ 16 (fd 單位) 的極值。                                     |
| sin       | 2      | 不可以     | v \* sin (p1)               | Sin，以度數 \* 2 ^ 16 (fd [單位](msdn-online-vml-units.md) ) 的引數。     |
| cos       | 2      | 不可以     | v \* cos (p1)               | Cos，以度數 \* 2 ^ 16 (fd [單位](msdn-online-vml-units.md) ) 的引數。     |
| cosatan2  | 3      | 不可以     | v \* cos (atan2 (p2，p1) )     | 在中繼計算中保留完整的精確度。                           |
| sinatan2  | 3      | 不可以     | v \* sin (atan2 (p2，p1) )     | 在中繼計算中保留完整的精確度。                           |
| sqrt      | 1      | 不可以     | sqrt (v)                    | 結果為正向下四捨五入。                                            |
| sumangle  | 3      | 是    | v + p1 \* 2 ^ 16 + p2 \* 2 ^ 16 | 依 2 ^ 16 比例的 vp1 和 p2 是度。<br/>                            |
| ellipse   | 3      | 不可以     | p2 \* sqrt (1- (v/p1) ^ 2)     | 橢圓。                                                                       |
| tan       | 2      | 不可以     | v \* tan (p1)               | 正切函數，以度數 \* 2 ^ 16 (fd [單位](msdn-online-vml-units.md) ) 的引數。 |



 

請注意，方程式只包含作業和數位;會省略數學符號。 例如，方程式

eqn = "sum 5 9 3"

會產生對等的

5 + 9-3

傳回的值為11。 如果遺漏了運算元，就不會使用此值。 例如，

eqn = "sum 5 9"

會產生對等的

5 + 9

而且會忽略遺漏的運算元。

*VML 標準屬性*

**範例**

下列公式產生的結果為 6 (兩個數字的總和除以 2) ，如果這是第一個公式，則可以使用符號 "" 來抓取 @0 。


```HTML
    <v:f eqn="mid 5 7"/>
```



 

