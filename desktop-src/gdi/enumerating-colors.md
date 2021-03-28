---
description: 您可以藉由抓取裝置的色彩計數和列舉純色的色彩，判斷裝置支援的色彩數量，以及這些色彩的色彩。
ms.assetid: cbaa3732-e55e-42af-93de-390450d38fc9
title: 列舉色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca39ec9817ecab07c2c2bc42b08fbee83333f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972680"
---
# <a name="enumerating-colors"></a>列舉色彩

您可以藉由抓取裝置的色彩計數和列舉純色的色彩，判斷裝置支援的色彩數量，以及這些色彩的色彩。 若要取出色彩數目，請使用 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函數搭配 NUMCOLORS 值。 若要列舉單色筆刷，請使用 [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) 函式和對應的回呼函式，以接收每個畫筆的相關資訊。


```C++
// GetTheColors - returns the count and color values of solid colors 
// Returns a pointer to the array containing colors 
// hdc - handle to device context 

COLORREF *GetTheColors(HDC hdc)
{
    int cColors;
    COLORREF *aColors;

    // Get the number of colors. 
    cColors = GetDeviceCaps(hdc, NUMCOLORS);

    // Allocate space for the array. 
    aColors = (COLORREF *)LocalAlloc(LPTR, sizeof(COLORREF) * 
        (cColors+1));

    // Save the count of colors in first element. 
    aColors[0] = (LONG)cColors;

    // Enumerate all pens and save solid colors in the array. 
    EnumObjects(hdc, OBJ_PEN, (GOBJENUMPROC)MyEnumProc, (LONG)aColors);

    // Refresh the count of colors. 
    aColors[0] = (LONG)cColors;

    return aColors;
}

int MyEnumProc(LPVOID lp, LPBYTE lpb)
{
    LPLOGPEN lopn;
    COLORREF *aColors;
    int iColor;

    lopn = (LPLOGPEN)lp;
    aColors = (COLORREF *)lpb;

    if (lopn->lopnStyle==PS_SOLID) 
    {
        // Check for too many colors. 
        if ((iColor = (int)aColors[0]) <= 0)
             return 0;
        aColors[iColor] = lopn->lopnColor;
        aColors[0]--;
    }
    return 1;
}
```



 

 



