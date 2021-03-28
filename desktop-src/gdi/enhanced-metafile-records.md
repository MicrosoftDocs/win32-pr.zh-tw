---
description: 增強的中繼檔是一組記錄。
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: 增強的中繼檔記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972681"
---
# <a name="enhanced-metafile-records"></a>增強的中繼檔記錄

增強的中繼檔是一組記錄。 中繼檔記錄是可變長度的 [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) 結構。 每個增強型中繼檔記錄的開頭都是 [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) 結構，其中包含兩個成員。 第一個成員 iType 會識別記錄類型，也就是其參數包含在記錄中的 GDI 函數。 因為結構的長度是變數，所以另一個成員 nSize 包含記錄的大小。 緊接在 nSize 成員後面的是 GDI 函數的其餘參數（如果有的話）。 結構的其餘部分包含相依于記錄類型的其他資料。

增強中繼檔中的第一筆記錄一律是 [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) 結構，也就是增強型中繼檔的標頭。 標頭會指定下列資訊：

-   中繼檔的大小（以位元組為單位）
-   圖片框架的尺寸（以裝置單位）
-   圖片框架的維度，以 01-毫米單位為單位
-   中繼檔中的記錄數目
-   選擇性文字描述的位移
-   選用區的大小
-   原始裝置的解析度（以圖元為單位）
-   原始裝置的解析度（以毫米為單位）

選擇性的文字描述可在標頭記錄之後。 文字描述描述圖片和作者的名稱。 選擇性調色板會指定用來建立增強型中繼檔的色彩。 其餘記錄會識別用來建立圖片的 GDI 函數。 下列十六進位輸出對應至針對 [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) 函式的呼叫所產生的記錄。


```C++
00000011 0000000C 00000004 
```



值0x00000011 會指定記錄類型 (對應至檔案 \_ Wingdi 中定義的 EMR SETMAPMODE 常數) 。 0x0000000C 值會指定記錄的長度（以位元組為單位）。 值0x00000004 會識別對應模式 (對應至 \_ [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) 函數中定義的 MM LOENGLISH 常數) 。

如需其他記錄類型的清單，請參閱 [中繼檔結構](metafile-structures.md)。

 

 



