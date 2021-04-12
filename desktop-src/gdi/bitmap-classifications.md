---
description: 點陣圖分類
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: 點陣圖分類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191964"
---
# <a name="bitmap-classifications"></a>點陣圖分類

點陣圖有兩種類別：

-   [與裝置無關的點陣圖](device-independent-bitmaps.md) (DIB) 。 DIB 檔案格式的設計目的，是要確保使用一個應用程式建立的點陣圖圖形可以載入並顯示在另一個應用程式中，並保留與原始相同的外觀。

-   [裝置相關點陣圖](device-dependent-bitmaps.md) (DDB) （也稱為 GDI 點陣圖）是舊版 3.0) 之前的16位 Microsoft Windows (中唯一可用的點陣圖。 不過，隨著顯示器技術的改善，以及隨著各種可用的顯示裝置增加，某些固有問題可能只會使用 Dib 來解決。 例如，沒有任何方法可儲存 (或抓取點陣圖建立所在的顯示類型解析度) ，因此繪圖應用程式無法快速判斷點陣圖是否適用于執行應用程式的影片顯示裝置類型。

    儘管有這些問題，DDBs (也稱為相容點陣圖) 仍適用于更好的 GDI 效能和其他情況。

 

 



