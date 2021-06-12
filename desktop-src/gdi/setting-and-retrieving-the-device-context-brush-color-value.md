---
description: 下列範例顯示應用程式如何使用 SetDCBrushColor 和 GetDCBrushColor 函式，來取得目前的 DC 筆刷色彩。
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: 設定和取出裝置內容筆刷色彩值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0bfc918f5882baa46208d27973e14b9446909e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010631"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a>設定和取出裝置內容筆刷色彩值

下列範例顯示應用程式如何使用 [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) 和 [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) 函式，來取得目前的 DC 筆刷色彩。


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc,RGB(00,0xff,00));
PatBlt(hdc,0,0,200,200,PATCOPY);
SetDCBrushColor(hdc,RGB(00,00,0xff));
PatBlt(hdc,0,0,200,200,PATCOPY);
```



 

 



