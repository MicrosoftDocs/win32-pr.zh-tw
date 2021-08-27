---
description: 執行 IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: 執行 IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de0ab694b2e2b8868717b6b4c11b2124ecc4042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982201"
---
# <a name="implementing-iamerrorlog"></a>執行 IAMErrorLog

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

[**IAMErrorLog**](iamerrorlog.md)介面包含單一方法 [**LogError**](iamerrorlog-logerror.md)。 方法的參數包含所發生錯誤的相關資訊。


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



錯誤碼和錯誤字串是由 DirectShow 編輯服務所定義。 如需錯誤清單，請參閱轉譯 [錯誤](rendering-errors.md)。

*PExtraInfo* 參數包含變數類型的指標，該類型會保存錯誤的其他相關資訊。 變數的資料類型和內容取決於發生的特定錯誤。 例如，如果錯誤是由不正確的檔案名所造成，則 VARIANT 是具有錯誤檔案名的字串。 有些錯誤沒有額外的資訊，所以 *pExtraInfo* 可能是 **Null**。 下列程式碼示範如何測試變異的 **vt** 成員（指出資料類型），並據以格式化訊息。


```C++
if( pExtraInfo )    // Report extra information, if any. 
{                           
    printf("\tExtra info: ");
    if( pExtraInfo->vt == VT_BSTR )      // Extra info is a BSTR.
    {
        UINT len = SysStringLen(pExtraInfo->bstrVal);
        char *szExtra = new char[len];
        if (szExtra != NULL)
        {
            // Note - If the BSTR contains embedded NULL characters, this
            // will only pick up the first sub-string.
            WideCharToMultiByte(CP_ACP, 0, pExtraInfo->bstrVal, -1, 
                szExtra, len, 0, 0);
            printf("%s\n", szExtra);
            delete [] szExtra;
        }
    } 
    else if( pExtraInfo->vt == VT_I4 )   // Extra info is an integer.
        printf("%d\n", pExtraInfo->lVal);

    else if( pExtraInfo->vt == VT_R8 )   // Extra info is floating-point.
        printf("%f\n", pExtraInfo->dblVal);
}
```



> [!Note]  
> 請勿釋出所指向的變異
>
> 
>
> 
| 標籤 | 值 |
|--------|-------|
| <pre><code>pExtraInfo</code></pre> | 

>
> 
>
> . 此外，此變數會在方法傳回之後變成無效，因此請勿稍後再參考。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[記錄錯誤](logging-errors.md)
</dt> </dl>

 

 



