---
title: CSecureChannelServer 類別
description: CSecureChannelServer 類別
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media 裝置管理員、CSecureChannelServer 類別
- 裝置管理員，CSecureChannelServer 類別
- 服務提供者、CSecureChannelServer 類別
- 程式設計參考，CSecureChannelServer 類別
- Windows Media 裝置管理員的參考，CSecureChannelServer 類別
- CSecureChannelServer 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682502"
---
# <a name="csecurechannelserver-class"></a><span data-ttu-id="cbd2f-109">CSecureChannelServer 類別</span><span class="sxs-lookup"><span data-stu-id="cbd2f-109">CSecureChannelServer Class</span></span>

<span data-ttu-id="cbd2f-110">**CSecureChannelServer** 類別是一個 helper 類別， (不是介面) ，可讓服務提供者或安全內容提供者使用 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)介面來驗證應用程式、加密和解密資料，以及建立 MAC 簽章。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-110">The **CSecureChannelServer** class is a helper class (not an interface) that enables a service provider or secure content provider to authenticate an application using the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface, to encrypt and decrypt data, and to create MAC signatures.</span></span> <span data-ttu-id="cbd2f-111">驗證程式會要求應用程式建立 **CSecureChannelClient** 物件，並讓服務提供者建立 **CSecureChannelServer** 物件。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-111">The authentication process requires that the application create a **CSecureChannelClient** object and that the service provider create a **CSecureChannelServer** object.</span></span> <span data-ttu-id="cbd2f-112">**CSecureChannelClient** 和 **CSecureChannelServer** 類別是在靜態程式庫（Mssachlp）中宣告。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-112">The **CSecureChannelClient** and **CSecureChannelServer** classes are declared in the static link library, Mssachlp.lib.</span></span> <span data-ttu-id="cbd2f-113">所有 Windows Media 裝置管理員、服務提供者和安全內容提供者介面的方法，都 \_ 可以 \_ 傳回 WMDM E NOTCERTIFIED，表示呼叫者未成功驗證。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-113">All methods of Windows Media Device Manager, service provider, and secure content provider interfaces can return WMDM\_E\_NOTCERTIFIED to indicate that the caller has not authenticated successfully.</span></span>

<span data-ttu-id="cbd2f-114">**CSecureChannelServer** 類別會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-114">The **CSecureChannelServer** class exposes the following methods.</span></span>



| <span data-ttu-id="cbd2f-115">方法</span><span class="sxs-lookup"><span data-stu-id="cbd2f-115">Method</span></span>                                                            | <span data-ttu-id="cbd2f-116">描述</span><span class="sxs-lookup"><span data-stu-id="cbd2f-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd2f-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span></span>         | <span data-ttu-id="cbd2f-118">解密參數中包含的資料。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-118">Decrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="cbd2f-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span></span>         | <span data-ttu-id="cbd2f-120">加密參數中包含的資料。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-120">Encrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="cbd2f-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span></span> | <span data-ttu-id="cbd2f-122">確認已成功建立安全驗證通道。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-122">Verifies that a secure authentication channel has been successfully established.</span></span>            |
| <span data-ttu-id="cbd2f-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span></span>               | <span data-ttu-id="cbd2f-124">抓取本機和遠端元件的應用程式安全性層級。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-124">Retrieves the application security levels of the local and remote components.</span></span>               |
| <span data-ttu-id="cbd2f-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span></span>       | <span data-ttu-id="cbd2f-126">抓取目前的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-126">Retrieves the current session key.</span></span>                                                          |
| <span data-ttu-id="cbd2f-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span></span>                 | <span data-ttu-id="cbd2f-128">釋放 (MAC) 通道的訊息驗證碼，並抓取最終的 MAC 值。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-128">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>     |
| <span data-ttu-id="cbd2f-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span></span>                   | <span data-ttu-id="cbd2f-130">取得 (MAC) 通道的訊息驗證碼。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-130">Acquires a message authentication code (MAC) channel.</span></span>                                       |
| <span data-ttu-id="cbd2f-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span></span>               | <span data-ttu-id="cbd2f-132">使用參數值來更新 (MAC) 值的訊息驗證碼。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-132">Updates the message authentication code (MAC) value with a parameter value.</span></span>                 |
| <span data-ttu-id="cbd2f-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span></span>                   | <span data-ttu-id="cbd2f-134">在元件之間建立安全的已驗證通道。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-134">Establishes a secure authenticated channel between components.</span></span>                              |
| <span data-ttu-id="cbd2f-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span></span>   | <span data-ttu-id="cbd2f-136">報告元件所支援的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-136">Reports the protocols supported by a component.</span></span>                                             |
| <span data-ttu-id="cbd2f-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span></span>     | <span data-ttu-id="cbd2f-138">指定安全驗證通道 (SAC) server 的憑證和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-138">Specifies the certificate and private key of the secure authenticated channel (SAC) server.</span></span> |
| <span data-ttu-id="cbd2f-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cbd2f-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span></span>       | <span data-ttu-id="cbd2f-140">設定用來與其他元件通訊的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="cbd2f-140">Sets the session key that is used to communicate with another component.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="cbd2f-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbd2f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd2f-142">**CSecureChannelClient 類別**</span><span class="sxs-lookup"><span data-stu-id="cbd2f-142">**CSecureChannelClient Class**</span></span>](csecurechannelclient-class.md)
</dt> <dt>

[<span data-ttu-id="cbd2f-143">**IComponentAuthenticate 介面**</span><span class="sxs-lookup"><span data-stu-id="cbd2f-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="cbd2f-144">**服務提供者的介面**</span><span class="sxs-lookup"><span data-stu-id="cbd2f-144">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="cbd2f-145">**使用安全驗證通道**</span><span class="sxs-lookup"><span data-stu-id="cbd2f-145">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 