---
description: 許多函式會使用目前選取的筆刷至裝置內容，以執行點陣圖作業。
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: 點陣圖作為筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191959"
---
# <a name="bitmaps-as-brushes"></a>點陣圖作為筆刷

許多函式會使用目前選取的筆刷至裝置內容，以執行點陣圖作業。 例如， [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) 函式會在視窗內的矩形區域中複寫筆刷，而 [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) 函式會將筆刷複寫到指定色彩所系結之視窗內的某個區域內， (不同于 **PatBlt**， **FloodFill** 會填滿非矩形圖形) 。

[**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)函式會在以指定的色彩所系結的區域內複寫筆刷。 但是，與 [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) 函式不同的是， **FloodFill** 不會將筆刷的色彩資料與顯示器上的圖元色彩資料結合在一起。它只會將顯示區域內的所有圖元色彩，設定為目前在裝置內容中選取之筆刷的色彩。

 

 



