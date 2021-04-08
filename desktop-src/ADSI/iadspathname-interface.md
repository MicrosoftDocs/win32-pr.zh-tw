---
title: IADsPathname 介面
description: 剖析和修改 ADsPath 的各種元素。
ms.assetid: 1f820488-2e75-4257-90c7-9ec67aac4fe4
ms.tgt_platform: multiple
keywords:
- IADsPathname 介面 ADSI
- 使用 IADsPathname ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 IADsPathname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5cbc5901c8f9dcebebde485decc49fc5bcf312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839176"
---
# <a name="iadspathname-interface"></a><span data-ttu-id="56191-106">IADsPathname 介面</span><span class="sxs-lookup"><span data-stu-id="56191-106">IADsPathname Interface</span></span>

<span data-ttu-id="56191-107">[**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)介面會剖析和修改 ADsPath 的各種元素。</span><span class="sxs-lookup"><span data-stu-id="56191-107">The [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface parses and modifies various elements of an ADsPath.</span></span> <span data-ttu-id="56191-108">它也會在不同的顯示格式之間轉換 ADsPaths。</span><span class="sxs-lookup"><span data-stu-id="56191-108">It also converts ADsPaths between various display formats.</span></span>

<span data-ttu-id="56191-109">下列程式碼範例會從有效的 ADsPath 解壓縮並傳回伺服器名稱，以便在維護公用程式中顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="56191-109">The following code example extracts and returns the server name from a valid ADsPath for display to the user in a maintenance utility.</span></span>


```C++
HRESULT GetServerName(BSTR adsPath, BSTR *adsServer)
{
    HRESULT hr = S_OK;
    IADsPathname *pIADsPathname = NULL;
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
 
    // Set the path.
    hr = pIADsPathname->Set(adsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
        // Extract and return the server name.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_SERVER, adsServer);
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
}
```



<span data-ttu-id="56191-110">下列程式碼範例會藉由從本身的 ADsPath 設定物件的 **辨別名稱** 屬性，協助初始化新建立的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="56191-110">The following code example helps to initialize a newly created ADSI object by setting the object's **Distinguished Name** property from its own ADsPath.</span></span> <span data-ttu-id="56191-111">請注意，呼叫常式必須叫用 **SetInfo** 方法，以認可基礎目錄存放區的任何變更。</span><span class="sxs-lookup"><span data-stu-id="56191-111">Be aware that the calling routine must commit any changes to the underlying directory store by invoking the **SetInfo** method.</span></span>


```C++
HRESULT SetDistinguishedName(IADs *pIADs)
{
    HRESULT hr = S_OK;
    CComBSTR sbstrADsPath;
    IADsPathname *pIADsPathname = NULL;
 
    // Get the ADsPath for this object.
    hr = pIADs->get_ADsPath(&sbstrADsPath);
    if (FAILED(hr))
        return (hr);
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
     // Set the path.
    hr = pIADsPathname->Set(sbstrADsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
    {
        CComBSTR sbstrDNPath;

        // Convert the path to Distinguished Name format.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,
                                     &sbstrDNPath);
 
        if (SUCCEEDED(hr))
        {
            // Set the distinguished name property.
            VARIANT var;
            VariantInit(&var);
            V_BSTR(&var) = sbstrDNPath;
            V_VT(&var) = VT_BSTR;
            hr = pIADs->Put(CComBSTR("distinguishedName"), var);
            VariantClear(&var);
        }
    }
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
 
}
```



 

 




