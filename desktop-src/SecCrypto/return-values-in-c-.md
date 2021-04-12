---
description: 在 c + + 中，傳回值的類型通常是 HRESULT。
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: C + + 中的傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192739"
---
# <a name="return-values-in-c"></a>C + + 中的傳回值

在 c + + 中，傳回值的類型通常是 **HRESULT**。 這是來自此傳回值，可以判斷方法是否成功，如果不是，則錯誤是什麼。 \_當方法成功完成時，憑證服務通常會傳回 **HRESULT** 的「確定」。 需要傳回的程式設計值會透過方法中的 "out" 參數傳回。 下列範例顯示 c + + 方法呼叫，以抓取要求屬性：


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



在上述的程式碼片段中，成功或失敗會傳回給 **HRESULT** 變數 *hr*。 在程式碼中檢查 **HRESULT** 變數是否成功， \[ 條件 (S \_ OK！ = hr) \] 。 如果方法順利完成，就會在 **VARIANT** *varProp* 參數中傳回 request 屬性值。

 

 



