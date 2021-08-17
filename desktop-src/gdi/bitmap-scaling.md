---
description: StretchBlt 函式會藉由在來源裝置內容中的矩形執行位區塊傳輸，來調整點陣圖，以轉換成目的地裝置內容中的矩形。
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: 點陣圖縮放比例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14975f884906fb95bf07fbf3ab5277b89c5cbfd2612864202eb64eedc5df646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699895"
---
# <a name="bitmap-scaling"></a>點陣圖縮放比例

[**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)函式會藉由在來源裝置內容中的矩形執行位區塊傳輸，來調整點陣圖，以轉換成目的地裝置內容中的矩形。 但是，與 [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) 函式不同的是，它會在目的矩形中複製來源矩形的維度，而 **StretchBlt** 可讓應用程式指定來源和目的地矩形的維度。 當目的點陣圖小於來源點陣圖時，系統會將色彩資料的資料列或資料行 (或點陣圖中) 的資料行，然後在顯示裝置上呈現對應的影像。 系統會根據指定的延展模式（由應用程式透過呼叫 [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) 函式來定義）來合併色彩資料。 當目的點陣圖大於來源點陣圖時，系統會據以調整或放大結果影像中的每個圖元。

 

 



