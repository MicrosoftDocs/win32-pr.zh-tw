---
description: 當應用程式執行這類工作時，必須抓取字元寬度的資料，以將文字的字串調整為頁面或資料行寬度。
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: 字元寬度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fbb7e6ad1e5f4ef12f2abd9e528ce3158a869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848575"
---
# <a name="character-widths"></a>字元寬度

當應用程式執行這類工作時，必須抓取字元寬度的資料，以將文字的字串調整為頁面或資料行寬度。 應用程式可以使用四個函式來取出字元寬度的資料。 其中兩個函式會抓取字元前進寬度，而其中兩個函式會取出實際的字元寬度資料。

應用程式可以使用 [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) 和 [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) 函式，在文字字串中取得個別字元或符號的前進寬度。 [前進寬度] 是影片顯示器上的游標或印表機上的列印頭必須先前進，然後才能列印文字字串中的下一個字元。 [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a)函式會將前進寬度傳回為整數值。 如果需要更高的精確度，則應用程式可以使用 [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) 函式來取出小數預付寬度值。

應用程式可以使用 [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) 和 [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) 函數來取得實際的字元寬度資料。 **GetCharABCWidthsFloat** 函數適用于所有字型。 [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa)函式僅適用于 TrueType 和 OpenType 字型。 如需有關 TrueType 和 OpenType 字型的詳細資訊，請參閱 [點陣、向量、TrueType 和 opentype](raster--vector--truetype--and-opentype-fonts.md)字型。

下圖顯示字元寬度的三個元件：

![顯示兩個相鄰字元的間距、b 間距和 c 間距的圖例](images/csftx-02.png)

間距是在放置字元之前，要加入至目前位置的寬度。 B 間距是字元本身的寬度。 C 間距是字元右邊的空白字元。 總進寬度是藉由計算 + B + C 的總和來決定。 字元資料格是以字型括住每個字元或符號的虛數矩形。 因為字元可能會超出或 underhang 字元資料格，所以 A 和 C 的每個增量都可以是負數。

 

 
