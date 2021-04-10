---
title: IADsExtension 使用方式
description: 本主題包含使用 IADsExtension 介面的 c + + 程式碼範例。
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- 延伸模組 ADSI、IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a844d320b28548e9e9998881fd2a09815d1882e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182988"
---
# <a name="iadsextension-usage"></a><span data-ttu-id="cd701-104">IADsExtension 使用方式</span><span class="sxs-lookup"><span data-stu-id="cd701-104">IADsExtension Usage</span></span>

<span data-ttu-id="cd701-105">當至少符合下列其中一個條件時， [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)是延伸模組寫入器所執行的選擇性介面：</span><span class="sxs-lookup"><span data-stu-id="cd701-105">[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) is an optional interface implemented by the extension writer when at least one of the following conditions are met:</span></span>

-   <span data-ttu-id="cd701-106">擴充元件需要由 [**操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate)方法中的 **ADSI \_ EXT \_ \* dwCode**\* 所定義的初始化通知。</span><span class="sxs-lookup"><span data-stu-id="cd701-106">The extension component requires an initialization notification as defined by **ADSI\_EXT\_\*dwCode**\* in the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span>
-   <span data-ttu-id="cd701-107">此延伸模組支援雙重或分派介面。</span><span class="sxs-lookup"><span data-stu-id="cd701-107">The extension supports a dual or dispatch interface.</span></span>

<span data-ttu-id="cd701-108">如果延伸模組元件因為第一個原因支援 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) 介面， [**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) 和 [**IADsExtension：:P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) 方法可以傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="cd701-108">If an extension component supports the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for the first reason, the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**IADsExtension::PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods can return **E\_NOTIMPL**.</span></span> <span data-ttu-id="cd701-109">或者，如果擴充元件支援雙重或分派介面，則 [**操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate)方法可以忽略資料並傳回 **E \_ >notimpl** 的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="cd701-109">Alternatively, if an extension component supports a dual or dispatch interface , the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method can ignore the data and return an **HRESULT** of **E\_NOTIMPL**.</span></span>

<span data-ttu-id="cd701-110">下列程式碼顯示執行 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="cd701-110">The following code shows an extension implementing [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




