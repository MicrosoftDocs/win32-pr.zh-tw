---
description: 在 c + + 中，每個憑證服務方法都會直接傳回 HRESULT 值，指出方法呼叫成功或失敗。 如果呼叫失敗，傳回值會指出失敗的原因。
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: 在 c + + 中檢查錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e374c6f0bd933c2e4de7a477fea02b4e1538a7a1fa9b4de78e45fd896b192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874068"
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



 

 



