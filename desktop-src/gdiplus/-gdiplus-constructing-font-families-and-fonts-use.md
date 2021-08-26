---
description: Windows GDI+ 將字型相同但樣式不同的字型組合成字型系列。
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: 建立字型系列和字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc405883eadd85b5b8018f75da270085197aed4792bf1c6848628cce02f457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015189"
---
# <a name="constructing-font-families-and-fonts"></a>建立字型系列和字型

Windows GDI+ 將字型相同但樣式不同的字型組合成字型系列。 例如，Arial 字型家族包含下列字型：

-   Arial 標準
-   Arial 粗體
-   Arial 斜體
-   Arial 粗體斜體

GDI+ 使用四種樣式來形成系列：標準、粗體、斜體和粗體斜體。 像 *窄* 和 *圓角* 的形容詞不會被視為樣式;它們是系列名稱的一部分。 例如，Arial 窄是一種字型家族，其成員如下所示：

-   Arial 窄的一般
-   Arial 窄粗體
-   Arial 窄斜體
-   Arial 窄粗體斜體

在您可以使用 GDI+ 繪製文字之前，您必須先建立 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件和 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)物件。 **FontFamily** 物件會指定字型 (例如，Arial) ，而 **字型** 物件則指定大小、樣式和單位。

下列範例會建立大小為16圖元的一般樣式 Arial 字型：


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



在上述程式碼中，傳遞至 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 函式的第一個引數是 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 物件的位址。 第二個引數會指定以第四個引數所識別的單位來測量的字型大小。 第三個引數會識別樣式。

[* * * * UnitPixel * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) * 是 **單位** 列舉的成員，而 [* * * * FontStyleRegular * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) * 是 **FontStyle** 列舉的成員。 這兩個列舉都是在 Gdiplusenums 中宣告。

 

 



