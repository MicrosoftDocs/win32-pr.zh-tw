---
title: 處理 MCI 錯誤
description: 處理 MCI 錯誤
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967883"
---
# <a name="handling-mci-errors"></a>處理 MCI 錯誤

您應該一律檢查 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數的傳回值。 如果它指出錯誤，您可以使用 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) 來取得錯誤的文字描述。

下列範例會將 *dwError* 指定的 MCI 錯誤碼傳遞給 **mciGetErrorString**，然後使用 [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) 函式來顯示產生的文字錯誤描述。


```C++
// Use mciGetErrorString to get a textual description of an MCI error.
// Display the error description using MessageBox.

void showError(DWORD dwError)
{
    char szErrorBuf[MAXERRORLENGTH];
    MessageBeep(MB_ICONEXCLAMATION);
    if(mciGetErrorString(dwError, (LPSTR) szErrorBuf, MAXERRORLENGTH))
    {
        MessageBox(hMainWnd, szErrorBuf, "MCI Error",
        MB_ICONEXCLAMATION);
    }
    else
    {
        MessageBox(hMainWnd, "Unknown Error", "MCI Error",
            MB_ICONEXCLAMATION);
    }
}
 
```



> [!Note]  
> 若要自行解讀 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 錯誤的值，請將高序位字遮罩 (低序位單字包含錯誤碼) 。 但是，如果您將錯誤傳回值傳遞給 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))，則必須傳遞整個雙全雙全數值。

 

 

 