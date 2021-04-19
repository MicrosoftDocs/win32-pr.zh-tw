---
description: 執行 IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: 執行 IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65eb968eb370d06fab6aca13af3215bb3b650257
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970697"
---
# <a name="implementing-iamerrorlog"></a><span data-ttu-id="20958-103">執行 IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="20958-103">Implementing IAMErrorLog</span></span>

<span data-ttu-id="20958-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="20958-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="20958-105">[**IAMErrorLog**](iamerrorlog.md)介面包含單一方法 [**LogError**](iamerrorlog-logerror.md)。</span><span class="sxs-lookup"><span data-stu-id="20958-105">The [**IAMErrorLog**](iamerrorlog.md) interface contains a single method, [**LogError**](iamerrorlog-logerror.md).</span></span> <span data-ttu-id="20958-106">方法的參數包含所發生錯誤的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="20958-106">The parameters to the method contain information about the error that occurred.</span></span>


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



<span data-ttu-id="20958-107">錯誤碼和錯誤字串是由 DirectShow 編輯服務所定義。</span><span class="sxs-lookup"><span data-stu-id="20958-107">The error code and the error string are defined by DirectShow Editing Services.</span></span> <span data-ttu-id="20958-108">如需錯誤清單，請參閱轉譯 [錯誤](rendering-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="20958-108">For a list of errors, see [Rendering Errors](rendering-errors.md).</span></span>

<span data-ttu-id="20958-109">*PExtraInfo* 參數包含變數類型的指標，該類型會保存錯誤的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="20958-109">The *pExtraInfo* parameter contains a pointer to a VARIANT type that holds additional information about the error.</span></span> <span data-ttu-id="20958-110">變數的資料類型和內容取決於發生的特定錯誤。</span><span class="sxs-lookup"><span data-stu-id="20958-110">The data type and contents of the VARIANT depend on the specific error that occurred.</span></span> <span data-ttu-id="20958-111">例如，如果錯誤是由不正確的檔案名所造成，則 VARIANT 是具有錯誤檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="20958-111">For example, if the error was caused by an incorrect file name, the VARIANT is a string with the bad file name.</span></span> <span data-ttu-id="20958-112">有些錯誤沒有額外的資訊，所以 *pExtraInfo* 可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="20958-112">Some errors do not have extra information, so *pExtraInfo* might be **NULL**.</span></span> <span data-ttu-id="20958-113">下列程式碼示範如何測試變異的 **vt** 成員（指出資料類型），並據以格式化訊息。</span><span class="sxs-lookup"><span data-stu-id="20958-113">The following code shows how to test the **vt** member of the VARIANT, which indicates the data type, and format a message accordingly.</span></span>


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
> <span data-ttu-id="20958-114">請勿釋出所指向的變異</span><span class="sxs-lookup"><span data-stu-id="20958-114">Do not free the VARIANT pointed to by</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>pExtraInfo</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="20958-115">.</span><span class="sxs-lookup"><span data-stu-id="20958-115">.</span></span> <span data-ttu-id="20958-116">此外，此變數會在方法傳回之後變成無效，因此請勿稍後再參考。</span><span class="sxs-lookup"><span data-stu-id="20958-116">Also, the VARIANT becomes invalid after the method returns, so do not reference it later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="20958-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="20958-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20958-118">記錄錯誤</span><span class="sxs-lookup"><span data-stu-id="20958-118">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



