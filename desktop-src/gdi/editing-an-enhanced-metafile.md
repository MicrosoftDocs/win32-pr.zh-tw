---
description: 若要編輯儲存在增強型中繼檔中的圖片，應用程式必須執行下列程式中所述的工作。
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: 編輯增強的中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114668"
---
# <a name="editing-an-enhanced-metafile"></a>編輯增強的中繼檔

若要編輯儲存在增強型中繼檔中的圖片，應用程式必須執行下列程式中所述的工作。

**編輯儲存在增強型中繼檔中的圖片**

1.  使用點擊測試來捕捉游標座標，並取出物件 (行、弧線、矩形、橢圓形、多邊形或不規則圖形) 的位置，讓使用者想要改變。
2.  將這些座標轉換為邏輯 (或全球) 單位。
3.  呼叫 [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) 函數，並檢查每個中繼檔記錄。
4.  判斷指定的記錄是否對應至 GDI 繪圖函數。
5.  如果有的話，請判斷儲存在記錄中的座標是否對應至與使用者指定之座標相交的線條、弧線、橢圓形或其他圖形元素。
6.  尋找對應至使用者想要變更之輸出的記錄時，請清除畫面上對應至原始記錄的物件。
7.  從中繼檔中刪除對應的記錄，並將指標儲存到其位置。
8.  允許使用者重繪或取代物件。
9.  將用來繪製新物件的 GDI 函數轉換成一或多個增強中繼檔記錄。
10. 將這些記錄儲存在增強的中繼檔中。

 

 



