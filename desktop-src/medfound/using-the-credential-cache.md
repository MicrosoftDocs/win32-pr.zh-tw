---
description: 使用認證快取
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: 使用認證快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974349"
---
# <a name="using-the-credential-cache"></a><span data-ttu-id="0b93b-103">使用認證快取</span><span class="sxs-lookup"><span data-stu-id="0b93b-103">Using the Credential Cache</span></span>

<span data-ttu-id="0b93b-104">媒體基礎提供 [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) 介面的預設實作為。</span><span class="sxs-lookup"><span data-stu-id="0b93b-104">Media Foundation provides a default implementation of the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface.</span></span> <span data-ttu-id="0b93b-105">執行 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的應用程式可以使用預設的認證快取物件來儲存使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="0b93b-105">An application that implements the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface can use the default credential cache object to store the user's credentials.</span></span>

<span data-ttu-id="0b93b-106">若要建立預設的認證快取物件，請呼叫 [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) 函數。</span><span class="sxs-lookup"><span data-stu-id="0b93b-106">To create the default credential cache object, call the [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) function.</span></span>


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



<span data-ttu-id="0b93b-107">建立認證快取之後，應用程式可以使用下列方法來取得認證物件、設定使用者認證，以及指定快取選項。</span><span class="sxs-lookup"><span data-stu-id="0b93b-107">After the credential cache is created, the application can use the following methods to get a credential object, set user credentials, and specify the caching options.</span></span>

-   <span data-ttu-id="0b93b-108">若要取得 URL 的認證物件，請呼叫 [**IMFNetCredentialCache：： GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)。</span><span class="sxs-lookup"><span data-stu-id="0b93b-108">To get the credential object for a URL, call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span>

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    <span data-ttu-id="0b93b-109">如果指定之 URL 的認證不存在於認證快取中， [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 會建立一個新的認證物件，其中包含空的使用者名稱和密碼值。</span><span class="sxs-lookup"><span data-stu-id="0b93b-109">If the credentials for the specified URL do not exist in the credential cache, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) creates a new credential object with empty user name and password values.</span></span>

-   <span data-ttu-id="0b93b-110">若要設定 credential 物件的使用者名稱和密碼，請呼叫 [**IMFNetCredential：： SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) 和 [**IMFNetCredential：： SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword)。</span><span class="sxs-lookup"><span data-stu-id="0b93b-110">To set the user name and password on the credential object, call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span></span>
-   <span data-ttu-id="0b93b-111">若要設定 credential 物件的快取選項，請呼叫 [**IMFNetCredentialCache：： SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions)。</span><span class="sxs-lookup"><span data-stu-id="0b93b-111">To set the caching options on the credential object, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span></span>

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    <span data-ttu-id="0b93b-112">*DwOptionsFlags* 參數值是在 [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions)列舉中定義。</span><span class="sxs-lookup"><span data-stu-id="0b93b-112">The *dwOptionsFlags* parameter values are defined in the [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) enumeration.</span></span> <span data-ttu-id="0b93b-113">若要在持續性儲存體中儲存 URL 的使用者認證，請設定 MFNET \_ 認證 \_ 儲存旗標。</span><span class="sxs-lookup"><span data-stu-id="0b93b-113">To save user credentials for a URL in a persistent storage, set the MFNET\_CREDENTIAL\_SAVE flag.</span></span> <span data-ttu-id="0b93b-114">如果 [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) 呼叫成功完成，則後續的 [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 呼叫會搜尋持續性儲存體中的認證。</span><span class="sxs-lookup"><span data-stu-id="0b93b-114">If the [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) call completes successfully, then the subsequent call to [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) searches for the credentials in the persistent storage.</span></span> <span data-ttu-id="0b93b-115">如果找到相符的結果，這個方法會傳回包含資訊之 credential 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0b93b-115">If a match is found, this method returns a pointer to the credential object that contains the information.</span></span>

    <span data-ttu-id="0b93b-116">根據預設，透過網路傳送的使用者認證會經過加密。</span><span class="sxs-lookup"><span data-stu-id="0b93b-116">By default, user credentials sent over the network are encrypted.</span></span> <span data-ttu-id="0b93b-117">若要將此變更為純文字，請設定 MFNET \_ 認證 \_ 允許 \_ 純 \_ 文本旗標。</span><span class="sxs-lookup"><span data-stu-id="0b93b-117">To change this to clear text, set the MFNET\_CREDENTIAL\_ALLOW\_CLEAR\_TEXT flag.</span></span>

    <span data-ttu-id="0b93b-118">若要從登錄中移除資訊，請呼叫 [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 以取得認證物件，然後呼叫 [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) 並將 *dwOptionsFlags* 設定為 MFNET credential 沒有快取 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="0b93b-118">To remove information from the registry, call [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) to get the credential object, and then call [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) and set *dwOptionsFlags* to MFNET\_CREDENTIAL\_DONT\_CACHE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b93b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b93b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b93b-120">網路來源驗證</span><span class="sxs-lookup"><span data-stu-id="0b93b-120">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



