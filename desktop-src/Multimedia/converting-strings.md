---
title: 轉換字串
description: 轉換字串
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- mciSendString 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1db4cb4b3d02a93adecc82d6ce95de436fb2e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933110"
---
# <a name="converting-strings"></a><span data-ttu-id="a0fc8-104">轉換字串</span><span class="sxs-lookup"><span data-stu-id="a0fc8-104">Converting Strings</span></span>

<span data-ttu-id="a0fc8-105">當您使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式時，以命令和所有傳回值傳遞的所有值都是文字字串，因此您的應用程式需要轉換常式，以將變數轉換成字串或傳回。</span><span class="sxs-lookup"><span data-stu-id="a0fc8-105">When you use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, all values passed with the command and all return values are text strings, so your application needs conversion routines to translate from variables to strings or back again.</span></span> <span data-ttu-id="a0fc8-106">下列範例會捕獲來源矩形，並將傳回的字串轉換成矩形座標。</span><span class="sxs-lookup"><span data-stu-id="a0fc8-106">The following example retrieves the source rectangle and converts the returned string into rectangle coordinates.</span></span>


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
> <span data-ttu-id="a0fc8-107">在 MCI 中，**矩形** 結構的處理方式不同于 Windows 的其他部分;在 MCI 中，**右邊** 的成員包含矩形的寬度，而 **底部** 的成員則包含其高度。</span><span class="sxs-lookup"><span data-stu-id="a0fc8-107">**RECT** structures are handled differently in MCI than in other parts of Windows; in MCI, the **right** member contains the width of the rectangle and the **bottom** member contains its height.</span></span> <span data-ttu-id="a0fc8-108">在字串介面中，矩形會指定為 *X1*、 *Y1*、 *X2* 和 *Y2*。</span><span class="sxs-lookup"><span data-stu-id="a0fc8-108">In the string interface, a rectangle is specified as *X1*, *Y1*, *X2*, and *Y2*.</span></span> <span data-ttu-id="a0fc8-109">座標 *X1* 和 *Y1* 指定矩形的左上角，而座標 *X2* 和 *Y2* 則指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="a0fc8-109">The coordinates *X1* and *Y1* specify the upper-left corner of the rectangle, and the coordinates *X2* and *Y2* specify the width and height.</span></span>

 

 

 