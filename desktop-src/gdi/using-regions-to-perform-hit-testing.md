---
description: 筆刷中的範例會使用區域來模擬 &\# 0034; 縮放&\# 0034; 查看 8 x 8 圖元的單色點陣圖。
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: 使用區域來執行點擊測試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d553eeaf37b954d0ec9d0b8897df98cf1a513d7ca7212ca82bc376afe1fc7163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558118"
---
# <a name="using-regions-to-perform-hit-testing"></a>使用區域來執行點擊測試

[筆刷](brushes.md)中的範例會使用區域來模擬 8 x 8 圖元單色點陣圖的「縮放」視圖。 藉由按一下此點陣圖中的圖元，使用者會建立適合繪圖作業的自訂筆刷。 此範例示範如何使用 [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) 函式來執行點擊測試，並使用 [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) 函數來反轉區域中的色彩。

 

 



