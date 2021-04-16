---
description: 在 c + + 中，每個憑證服務方法都會直接傳回 HRESULT 值，指出方法呼叫成功或失敗。 如果呼叫失敗，傳回值會指出失敗的原因。
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: 在 c + + 中檢查錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a56acd41269ece0f9a5c7de4a2dff1960bb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513140"
---
# <a name="error-checking-in-c"></a>在 c + + 中檢查錯誤

在 c + + 中，每個憑證服務方法都會直接傳回 **HRESULT** 值，指出方法呼叫成功或失敗。 如果呼叫失敗，傳回值會指出失敗的原因。

下列範例顯示如何使用傳回的 **HRESULT** 值進行錯誤檢查。 如需範例錯誤碼，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。


```C++
HRESULT hr;
BSTR strAttributeName;
BSTR strAttributeValue = NULL;

if(!(strAttributeName = SysAllocString(L"TheAttribute")))
{
     printf("Could not allocate memory for attribute name.\n");
     exit(1);
}

hr = pICertServerPolicy->GetRequestAttribute(
                                strAttributeName,
                                &strAttributeValue);
if(S_OK != hr)          // Check to determine whether method failed
{
    if (E_INVALIDARG == hr)
    {
        //... Do something to recover from errors and so on.
    }
}
// Free BSTRs when finished.
if (NULL != strAttributeName)
    SysFreeString(strAttributeName);
if (NULL != strAttributeValue)
    SysFreeString(strAttributeValue);
```



 

 



