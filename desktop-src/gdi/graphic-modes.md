---
description: Windows 支援五種圖形模式，可讓應用程式指定色彩的混合方式、顯示輸出的方式、如何調整輸出等等。 下表說明這些儲存在 DC 中的模式。
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: 圖形模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512889"
---
# <a name="graphic-modes"></a>圖形模式

Windows 支援五種圖形模式，可讓應用程式指定色彩的混合方式、顯示輸出的方式、如何調整輸出等等。 下表說明這些儲存在 DC 中的模式。



| 圖形模式 | Description                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| 背景    | 定義背景色彩如何與點陣圖和文字作業的現有視窗或螢幕色彩混合。              |
| 繪圖       | 定義如何使用畫筆、筆刷、點陣圖和文字作業的現有視窗或螢幕色彩來混合前景色彩。 |
| 對應       | 定義圖形輸出如何從邏輯 (或世界) 空間對應至視窗、螢幕或印表機紙張。             |
| 多邊形填滿  | 定義如何使用筆刷模式來填滿複雜區域的內部。                                             |
| 伸展    | 定義點陣圖壓縮 (或縮小) 時，如何使用現有的視窗或螢幕色彩來混合點陣圖色彩。  |



 

和繪圖物件一樣，系統會使用預設的圖形模式來初始化 DC。 應用程式可以藉由呼叫下列函式來取得和檢查這些預設模式。



| 圖形模式 | 函式                                       |
|---------------|------------------------------------------------|
| 背景    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| 繪圖       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| 對應       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| 多邊形填滿  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| 伸展    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

應用程式可以藉由呼叫下列其中一項功能來變更預設模式。



| 圖形模式 | 函式                                       |
|---------------|------------------------------------------------|
| 背景    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| 繪圖       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| 對應       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| 多邊形填滿  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| 伸展    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



