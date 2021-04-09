---
title: IADsObjectOptions 介面
description: IADsObjectOptions 介面可讓您直接存取來設定和取得提供者特定的選項。
ms.assetid: b4ac114f-1a23-4be6-af02-0c0d34a8f78f
ms.tgt_platform: multiple
keywords:
- IADsObjectOptions 介面 ADSI
- 使用 IADsObjectOptions ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 IADsObjectOptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049d4dee7f6bf2e7ebb61f01f42ef9fc39271c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931837"
---
# <a name="iadsobjectoptions-interface"></a><span data-ttu-id="c0742-106">IADsObjectOptions 介面</span><span class="sxs-lookup"><span data-stu-id="c0742-106">IADsObjectOptions Interface</span></span>

<span data-ttu-id="c0742-107">[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)介面可讓您直接存取來設定和取得提供者特定的選項。</span><span class="sxs-lookup"><span data-stu-id="c0742-107">The [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) interface enables direct access to setting and retrieving provider-specific options.</span></span>

<span data-ttu-id="c0742-108">其中一個 Active Directory 物件選項是傳回伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="c0742-108">One of the Active Directory object options is to return the host name of a server.</span></span> <span data-ttu-id="c0742-109">下列程式碼範例會使用介面來取出通用類別目錄伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="c0742-109">The following code example uses the interface to retrieve the host name of the global catalog server.</span></span>


```C++
HRESULT GetGCServerName(VARIANT *vGCServer) 
{
    HRESULT hr = S_OK
    HRESULT hre = S_OK;
    IADsContainer *pContainer = NULL;
    IUnknown *pUnk = NULL;
    IEnumVARIANT *pEnum = NULL;
    IDispatch *pDisp = NULL;
    IADsObjectOptions *pOpt = NULL;
    VARIANT var;
    ULONG lFetch = 0;

    VariantInit(&var);
 
    // Bind to the global catalog using a serverless bind.
    hr = ADsOpenObject(L"GC:", NULL, NULL,
                       ADS_SECURE_AUTHENTICATION,
                       IID_IADsContainer, (void**) &pContainer );
    if (FAILED(hr))
        return (hr);
 
    hr = pContainer->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void**) &pEnum);
        if (SUCCEEDED(hr))
        {
            // Enumerate.
            hr = pEnum->Next(1, &var, &lFetch);
            if (SUCCEEDED(hr))
            {
                while (SUCCEEDED(hr))
                {
                    if (lFetch == 1)
                    {
                        pDisp = V_DISPATCH(&var);
                        hre = pDisp->QueryInterface(
                                          IID_IADsObjectOptions,
                                          (void**)&pOpt);
                        if (pDisp)
                            pDisp->Release();
                    }
                    VariantClear(&var);
                    hr = pEnum->Next(1, &var, &lFetch);
                }
                // S_FALSE indicates that the row was read properly.
                if (hr == S_FALSE)
                    hr = hre;
            }
 
            if (SUCCEEDED(hr))
            {
                // There is a valid pOpt, so request the server name.
                VariantInit(vGCServer);
                hr = pOpt->GetOption(ADS_OPTION_SERVERNAME,vGCServer);
            }
        }
    }
 
// Cleanup.
    VariantClear(&var);
    if (pOpt)
        pOpt->Release();
    if (pEnum)
        pEnum->Release();
    if (pUnk)
        pUnk->Release();
    if (pContainer)
        pContainer->Release();
    return (hr);
}
```



 

 




