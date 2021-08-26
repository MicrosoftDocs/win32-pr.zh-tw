---
description: 您可以使用 GetGlyphOutline 函數，從 TrueType 字型取出圖像的外框。
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: 正在抓取字元外框
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3db9b9200f665088096fdecbffc12866668d093c0c4d5ddb4a1612153873e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092648"
---
# <a name="retrieving-character-outlines"></a>正在抓取字元外框

您可以使用 [GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) 函數，從 TrueType 字型取出圖像的外框。 [**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea)函式所傳回的圖像大綱適用于格線擬合的圖像。  (格線擬合的字元已經過修改，因此其點陣圖影像會盡可能符合圖像的原始設計 ) 。若您的應用程式需要未修改的圖像大綱，請在大小等於字型單位的字型中，要求字元的字元外框。  (若要建立具有這個大小的字型，請將 [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfHeight** 成員設定為 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構的 **ntmSizeEM** 成員值的負值 ) 。

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) 會以點陣圖或一系列的線條和曲線來傳回大綱。 當應用程式將圖像大綱視為一連串的多線條和曲線時，會傳回 [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) 結構中的資訊，並在描述圖像時所需的 [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) 結構數目。 所有點都會以 [POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) 結構的形式傳回，並代表絕對位置，而不是相對移動。 [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader)結構的 **pfxStart** 成員所指定的起點是開始分佈的輪廓點。 接下來的 [**TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) 結構可以是聚合線條記錄或曲線記錄。

若要轉譯 TrueType 字元外框，您必須同時使用折線和曲線記錄。 系統可以輕鬆地轉譯折線和曲線。 每一個聚合線條和曲線記錄盡可能包含最多的連續點，以將傳回的記錄數目降至最低。

在 [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) 結構中指定的起始點一律位於圖像的外框上。 指定的點可作為輪廓的開始和結束點。

本節提供下列主題的相關資訊。

-   [聚合線條記錄](polyline-records.md)
-   [曲線記錄](spline-records.md)

 

 
