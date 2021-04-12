---
title: 使用 COM 介面
description: 使用 COM 介面
ms.assetid: 44e1aeac-585c-4856-8c4d-1adb5b307b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b5d402079debf5e0a565c6b91136605cec50fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300199"
---
# <a name="using-a-com-interface"></a><span data-ttu-id="0acd0-103">使用 COM 介面</span><span class="sxs-lookup"><span data-stu-id="0acd0-103">Using a COM Interface</span></span>

<span data-ttu-id="0acd0-104">用戶端程式代碼是 COM 介面的使用者。</span><span class="sxs-lookup"><span data-stu-id="0acd0-104">The client code is the user of the COM interface.</span></span> <span data-ttu-id="0acd0-105">若要使用任何 COM 介面（自訂或標準），用戶端必須知道它的 IID。</span><span class="sxs-lookup"><span data-stu-id="0acd0-105">To use any COM interface, custom or standard, a client must know its IID.</span></span> <span data-ttu-id="0acd0-106">在下列範例中，呼叫 CustomRpt 的驅動程式會將轉換成寬字元格式的物件名稱傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="0acd0-106">In the following example, the driver that calls CustomRpt passes it the name of the object that is converted to a wide-character format.</span></span> <span data-ttu-id="0acd0-107">物件名稱會送至 [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) ，因此可以建立檔案的標記，而用戶端可以系結至執行中的物件。</span><span class="sxs-lookup"><span data-stu-id="0acd0-107">The object name is fed to [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) so that a file moniker can be created and the client can bind to the running object.</span></span> <span data-ttu-id="0acd0-108">在物件執行之後，CustomRpt 可以存取標準 proxy/stub 中的介面指標，例如 [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)，或存取自訂介面 ICustomInterface。</span><span class="sxs-lookup"><span data-stu-id="0acd0-108">After the object is running, CustomRpt can access a pointer to either an interface in the standard proxy/stub, such as [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile), or to the custom interface, ICustomInterface.</span></span>


```C++
void CustomRpt(char *pszObject) 
{ 
    HRESULT             hr; 
    WCHAR               wszObject[128]; 
    WCHAR               wszMsg[128] = {L"Your Message Here...\n"}; 
    IMoniker            *pmkObject = NULL; 
    IUnknown            *pIUnk = NULL; 
    IPersistFile        *pIPersistFile = NULL; 
    ICustomInterface    *pICustomInterface = NULL; 
 
    // Create a wide-character version of the object's file name. 
    StringCchPrintf(wszObject, 128, L"%hs", pszObject); 
 
    // Get a file moniker for the object (a *.smp file). 
    hr = CreateFileMoniker(wszObject, &pmkObject); 
 
    if(FAILED(hr)) 
    { 
        printf("Client: CreateFileMoniker for Object failed"); 
        return; 
    } 
 
    // BindMoniker is equivalent to calling CreateBindCtx() followed by 
    // a call to BindToObject(). It has the net result of binding the 
    // interface (specified by the IID) to the moniker. 
 
    hr = BindMoniker(pmkObject, 0, IID_IUnknown, (void **)&pIUnk); 
    if (FAILED(hr)) 
    { 
        printf("Client: BindMoniker failed (%x)\n", hr); 
        return; 
    } 
 
    // Try a couple QueryInterface calls into the object code; first a 
    // QueryInterface to IPersistFile... 
 
    hr = pIUnk->QueryInterface(IID_IPersistFile, (void **)&pIPersistFile); 
 
    if (FAILED(hr)) { 
        printf("Client: QueryInterface IPersistFile failed (%x)\n", hr); 
        pIUnk->Release(); 
        return; 
    } 
 
    // Followed by a QueryInterface to ICustomInterface. 
    hr = pIUnk->QueryInterface(IID_ICustomInterface, (void **)&pICustomInterface); 
 
    if (FAILED(hr)) { 
        printf("Client: QueryInterface failed (%x)\n", hr); 
        pIUnk->Release(); 
        pIPersistFile->Release(); 
        return; 
    } 
 
    // CustomReport() is the object function that displays the time and 
    // date information on the object. 
    hr = pICustomInterface->CustomReport(); 
 
    if (FAILED(hr)) 
    { 
        printf("Client: pICustomInterface->CustomReport failed (%x)\n", hr); 
        pIUnk->Release(); 
        pIPersistFile->Release(); 
        return; 
    } 
 
    // Clean up resources by calling release on each of the interfaces. 
    pIPersistFile->Release(); 
    pICustomInterface->Release(); 
    pIUnk->Release(); 
    return; 
} 
```



 

 




