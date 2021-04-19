---
title: 訊息驗證
description: 訊息驗證
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Media 裝置管理員，訊息驗證
- 裝置管理員，訊息驗證
- 桌面應用程式，訊息驗證
- 服務提供者，訊息驗證
- 程式設計指南，訊息驗證
- 訊息驗證
- " (MAC) 的訊息驗證碼"
- 'MAC (訊息驗證碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967404"
---
# <a name="message-authentication"></a><span data-ttu-id="e6e2b-111">訊息驗證</span><span class="sxs-lookup"><span data-stu-id="e6e2b-111">Message Authentication</span></span>

<span data-ttu-id="e6e2b-112">訊息驗證是一種程式，可讓應用程式和服務提供者確認它們之間傳遞的資料並未遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-112">Message authentication is a process that enables applications and service providers to verify that data passed between them has not been tampered with.</span></span> <span data-ttu-id="e6e2b-113">Windows Media 裝置管理員可讓應用程式和服務提供者使用訊息驗證代碼 (Mac) 來執行訊息驗證。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-113">Windows Media Device Manager allows applications and service providers to perform message authentication by using message authentication codes (MACs).</span></span> <span data-ttu-id="e6e2b-114">以下是 MAC 驗證的運作方式：</span><span class="sxs-lookup"><span data-stu-id="e6e2b-114">Here is how MAC authentication works:</span></span>

<span data-ttu-id="e6e2b-115">資料傳送者（通常是服務提供者）會透過單向密碼編譯函式傳遞一或多個資料片段，該函式會針對所有資料產生單一簽章（MAC）。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-115">The data sender, usually the service provider, passes one or more pieces of data through a one-way cryptographic function that produces a single signature, the MAC, for all the data.</span></span> <span data-ttu-id="e6e2b-116">接著，傳送者會將所有簽署的資料和 MAC 一起傳送給接收者， (通常是應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-116">The sender then sends all the signed pieces of data together with the MAC to the receiver (usually the application).</span></span> <span data-ttu-id="e6e2b-117">接收者會透過相同的密碼編譯函式來傳遞資料，以產生 MAC，並將其與所傳送的 MAC 進行比較。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-117">The receiver passes the data through the same cryptographic function to generate a MAC and compares it to the MAC that was sent.</span></span> <span data-ttu-id="e6e2b-118">如果 MAC 相符，就不會修改資料。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-118">If the MAC matches, the data has not been modified.</span></span>

<span data-ttu-id="e6e2b-119">若要執行 MAC 驗證，應用程式或服務提供者需要加密金鑰和相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-119">To perform MAC authentication, the application or service provider requires an encryption key and a matching certificate.</span></span> <span data-ttu-id="e6e2b-120">如需如何取得這些資訊的相關資訊，請參閱 [適用于開發的工具](tools-for-development.md)。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-120">For information on where to get these, see [Tools for Development](tools-for-development.md).</span></span>

<span data-ttu-id="e6e2b-121">下列步驟描述傳送者如何簽署資料，並于稍後由接收者檢查。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-121">The following steps describe how data is signed by the sender, and later checked by the receiver.</span></span> <span data-ttu-id="e6e2b-122">在 Windows Media 裝置管理員中，服務提供者會使用 [CSecureChannelServer](csecurechannelserver-class.md) 類別來產生 mac，而應用程式會使用 [CSecureChannelClient](csecurechannelclient-class.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-122">In Windows Media Device Manager, the service provider uses the [CSecureChannelServer](csecurechannelserver-class.md) class to generate MACs, and the application uses the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span> <span data-ttu-id="e6e2b-123">這兩個類別都提供具有相同參數的相同函式，因此下列步驟適用于這兩個類別。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-123">Both classes provide identical functions with identical parameters, so the following steps apply to both classes.</span></span>

<span data-ttu-id="e6e2b-124">傳送者 (通常是服務提供者) ：</span><span class="sxs-lookup"><span data-stu-id="e6e2b-124">The sender (typically the service provider):</span></span>

1.  <span data-ttu-id="e6e2b-125">取得要簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-125">Get the data to be signed.</span></span>
2.  <span data-ttu-id="e6e2b-126">藉由呼叫 **MACInit** 來建立新的 MAC 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-126">Create a new MAC handle by calling **MACInit**.</span></span>
3.  <span data-ttu-id="e6e2b-127">藉由呼叫 **MACUpdate**，加入要簽署至控制碼的資料片段。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-127">Add a piece of data to be signed to the handle by calling **MACUpdate**.</span></span> <span data-ttu-id="e6e2b-128">此函式會接受先前建立的控制碼，以及必須簽署的資料片段。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-128">This function accepts the previously created handle, plus a piece of data that must be signed.</span></span>
4.  <span data-ttu-id="e6e2b-129">使用必須簽署的每個額外資料片段重複步驟3。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-129">Repeat step 3 with each additional piece of data that must be signed.</span></span> <span data-ttu-id="e6e2b-130">將資料新增至 MAC 的順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-130">It does not matter in what order data is added to the MAC.</span></span>
5.  <span data-ttu-id="e6e2b-131">藉由呼叫 **MACFinal**，從控制碼將 MAC 複製到新的位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-131">Copy the MAC from the handle to a new byte buffer by calling **MACFinal**.</span></span> <span data-ttu-id="e6e2b-132">此函式會接受 MAC 控制碼和您配置的緩衝區，並將 MAC 從控制碼複製到提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-132">This function accepts the MAC handle and a buffer that you allocate, and copies the MAC from the handle into the provided buffer.</span></span>

<span data-ttu-id="e6e2b-133">執行 MAC 驗證時，傳送者和接收者都必須將相同的資料放入 MAC 中。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-133">When performing MAC authentication, it is important that both the sender and the receiver are putting the same data into the MAC.</span></span> <span data-ttu-id="e6e2b-134">針對提供 MAC 的應用程式方法，通常所有參數都包含在 MAC 值 (除了 MAC 本身，當然) 。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-134">For the application methods that provide a MAC, typically all parameters are included in the MAC value (except for the MAC itself, of course).</span></span> <span data-ttu-id="e6e2b-135">例如，請考慮 **IWMDMOperation：： TransferObjectData** 方法：</span><span class="sxs-lookup"><span data-stu-id="e6e2b-135">For example, consider the **IWMDMOperation::TransferObjectData** method:</span></span>

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

<span data-ttu-id="e6e2b-136">在此方法中，MAC 會包含 *.pdata* 和 *pdwSize*。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-136">In this method, the MAC would include *pData* and *pdwSize*.</span></span> <span data-ttu-id="e6e2b-137">如果您未包含這兩個參數，則您建立的 MAC 不會符合傳遞給 *abMac* 的 mac。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-137">If you do not include both the parameters, the MAC you create will not match the MAC passed to *abMac*.</span></span> <span data-ttu-id="e6e2b-138">服務提供者必須務必將應用程式方法中的所有必要參數放入 MAC 值中。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-138">A service provider must be sure to put all the required parameters in the application method into the MAC value.</span></span>

<span data-ttu-id="e6e2b-139">下列 c + + 程式碼示範如何在服務提供者的 [**IMDSPStorageGlobals：： GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)執行中建立 MAC。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-139">The following C++ code demonstrates creating a MAC in a service provider's implementation of [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span></span>


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



<span data-ttu-id="e6e2b-140">接收器通常會 (應用程式) ：</span><span class="sxs-lookup"><span data-stu-id="e6e2b-140">The receiver (typically the application):</span></span>

<span data-ttu-id="e6e2b-141">如果接收者尚未執行 [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) 介面，則應該執行與傳送者相同的步驟，然後再比較這兩個 MAC 值。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-141">If the receiver has not implemented the [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) interface, it should perform the same steps as the sender, and then compare the two MAC values.</span></span> <span data-ttu-id="e6e2b-142">下列 c + + 程式碼範例示範應用程式如何檢查在呼叫 [**IWMDMStorageGlobals：： GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) 時所收到的 MAC，以確保序號在傳輸時不會遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="e6e2b-142">The following C++ code example shows how an application would check the MAC received in a call to [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) to ensure that the serial number was not tampered with in transit.</span></span>


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e6e2b-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6e2b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6e2b-144">**使用安全驗證通道**</span><span class="sxs-lookup"><span data-stu-id="e6e2b-144">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




