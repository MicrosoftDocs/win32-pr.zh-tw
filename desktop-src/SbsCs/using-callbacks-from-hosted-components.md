---
description: 託管元件的回呼是讓裝載成為可能的。 不過，您所裝載的元件可能已啟用另一個用來存取本身外掛程式或元件的啟用內容。
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: 使用託管元件的回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb13e61b83ba52f0f8dd5265b11585e8366c0e8558d45c5738f179d43df2eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884598"
---
# <a name="using-callbacks-from-hosted-components"></a>使用託管元件的回呼

託管元件的回呼是讓裝載成為可能的。 不過，您所裝載的元件可能已啟用另一個用來存取本身外掛程式或元件的啟用內容。 在此情況下，如果裝載的元件在參考其本身 COM 物件的堆疊上保留啟用內容，則裝載應用程式可能會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來取得它所預期的物件，而改為接收主控元件的物件。 為了避免這項啟用內容繼承，良好的裝載應用程式應該在回呼期間先啟用自己的知名啟用內容。

請考慮下列保護主控應用程式程式碼的範例：

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

這可確保在將要求傳遞至 **Funct** 的內部實執行之前，會先設定適當的啟用內容。 您自己的實電腦可以內嵌實際的實值，但先前的方法可透過建立委派的包裝函式，來確保互通性更容易。 當公開一般 (非 COM) 回呼時，建議使用類似的方法。

 

 
