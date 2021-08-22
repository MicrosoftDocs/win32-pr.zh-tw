---
title: 轉換字串
description: 轉換字串
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- mciSendString 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efeb5801c46d89686ed3fe9fcf25b311d57d4d553c220902907ac0e70a5b7e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144791"
---
# <a name="converting-strings"></a>轉換字串

當您使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式時，以命令和所有傳回值傳遞的所有值都是文字字串，因此您的應用程式需要轉換常式，以將變數轉換成字串或傳回。 下列範例會捕獲來源矩形，並將傳回的字串轉換成矩形座標。


```C++
BOOL GetSourceRect(LPTSTR lpstrAlias, LPRECT lprc) 
{ 
    TCHAR achRetBuff[128]; 
    TCHAR achCommandBuff[128]; 

    int result;
    MCIERROR err;
 
    // Build the command string. 
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("where %s source"), 
        lpstrAlias); 

    if (result == -1)
    {
        return FALSE;
    }
    
    // Clear the RECT.
    SetRectEmpty(lprc);
 
    // Send the MCI command. 
    err = mciSendString(
        achCommandBuff, 
        achRetBuff, 
        sizeof(achRetBuff), 
        NULL);

    if (err != 0)
    {
        return FALSE;
    }
        
    // The rectangle is returned as "x y dx dy". 
    // Translate the string into the RECT structure. 

    // Warning: This example omits error checking
    // for the _tcstok_s and _tstoi functions.
    TCHAR *p; 
    TCHAR *context;

    // Left.
    p = _tcstok_s(achRetBuff, TEXT(" "), &context);
    lprc->left = _tstoi(p);

    // Top.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->top = _tstoi(p);

    // Right.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->right = _tstoi(p);
    
    // Bottom.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->bottom = _tstoi(p);

    return TRUE;
}
 
```



> [!Note]  
> 除了 Windows 的其他部分，以不同的方式處理在 MCI 中的 **矩形** 結構。在 MCI 中，**右邊** 的成員包含矩形的寬度，而 **底部** 的成員則包含其高度。 在字串介面中，矩形會指定為 *X1*、 *Y1*、 *X2* 和 *Y2*。 座標 *X1* 和 *Y1* 指定矩形的左上角，而座標 *X2* 和 *Y2* 則指定寬度和高度。

 

 

 