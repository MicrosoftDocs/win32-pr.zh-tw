---
description: 設定認證管理員
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: 設定認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983372"
---
# <a name="setting-a-credential-manager"></a><span data-ttu-id="40ec6-103">設定認證管理員</span><span class="sxs-lookup"><span data-stu-id="40ec6-103">Setting a Credential Manager</span></span>

<span data-ttu-id="40ec6-104">提供網路來源認證的應用程式必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="40ec6-104">An application that provides credentials to the network source must do the following:</span></span>

1.  <span data-ttu-id="40ec6-105">執行公開 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的認證管理員物件。</span><span class="sxs-lookup"><span data-stu-id="40ec6-105">Implement a credential manager object that exposes the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
2.  <span data-ttu-id="40ec6-106">建立網路來源之前，請先建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="40ec6-106">Before you create the network source, create a new property store.</span></span>
3.  <span data-ttu-id="40ec6-107">在屬性存放區上設定 [**MFNETSOURCE \_ CREDENTIAL \_ MANAGER**](mfnetsource-credential-manager-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="40ec6-107">Set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the property store.</span></span> <span data-ttu-id="40ec6-108">屬性的值是 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="40ec6-108">The value of the property is a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
4.  <span data-ttu-id="40ec6-109">將指向屬性存放區的指標傳遞至來源解析程式，如設定 [媒體來源](configuring-a-media-source.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="40ec6-109">Pass a pointer to the property store to the source resolver, as described in [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="40ec6-110">網路來源會使用認證管理員來取得使用者認證。</span><span class="sxs-lookup"><span data-stu-id="40ec6-110">The network sources uses the credential manager to get user credentials.</span></span> <span data-ttu-id="40ec6-111">如果網路來源需要認證才能存取網路資源，則會呼叫應用程式的 [**IMFNetCredentialManager：： BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) 方法。</span><span class="sxs-lookup"><span data-stu-id="40ec6-111">If the network source requires credentials to access a network resource, it calls the application's [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span> <span data-ttu-id="40ec6-112">此呼叫會啟動非同步要求以取得使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="40ec6-112">This call starts an asynchronous request to gets the user's credentials.</span></span> <span data-ttu-id="40ec6-113">**BeginGetCredentials** 方法可以從認證快取或使用者取得認證。</span><span class="sxs-lookup"><span data-stu-id="40ec6-113">The **BeginGetCredentials** method can get the credentials either from the credential cache or from the user.</span></span> <span data-ttu-id="40ec6-114">認證會儲存在 *credential 物件* 中。</span><span class="sxs-lookup"><span data-stu-id="40ec6-114">Credentials are stored in a *credential object*.</span></span> <span data-ttu-id="40ec6-115">當作業完成時，應用程式會叫用回呼介面來通知網路來源。</span><span class="sxs-lookup"><span data-stu-id="40ec6-115">When the operation is complete, the application invokes the callback interface to notify the network source.</span></span> <span data-ttu-id="40ec6-116">網路來源會呼叫 [**IMFNetCredentialManager：： EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) 來完成非同步作業。</span><span class="sxs-lookup"><span data-stu-id="40ec6-116">The network source calls [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) to complete the asynchronous operation.</span></span>

<span data-ttu-id="40ec6-117">由於這是非同步作業，因此應用程式必須在作業結束時分派回呼。</span><span class="sxs-lookup"><span data-stu-id="40ec6-117">Because this is an asynchronous operation, the application must dispatch the callback at the end of the operation.</span></span> <span data-ttu-id="40ec6-118">如需撰寫非同步方法的逐步指示，請參閱 [撰寫非同步方法](writing-an-asynchronous-method.md)。</span><span class="sxs-lookup"><span data-stu-id="40ec6-118">For step-by-step instructions about writing an asynchronous method, see [Writing an Asynchronous Method](writing-an-asynchronous-method.md).</span></span>

<span data-ttu-id="40ec6-119">下列範例顯示如何在網路來源上設定 [**MFNETSOURCE \_ CREDENTIAL \_ MANAGER**](mfnetsource-credential-manager-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="40ec6-119">The following example shows how to set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="40ec6-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="40ec6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ec6-121">網路來源驗證</span><span class="sxs-lookup"><span data-stu-id="40ec6-121">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



