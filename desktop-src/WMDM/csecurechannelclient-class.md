---
title: CSecureChannelClient 類別
description: CSecureChannelClient 類別
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media 裝置管理員、CSecureChannelClient 類別
- 裝置管理員，CSecureChannelClient 類別
- 桌面應用程式，CSecureChannelClient 類別
- 程式設計參考，CSecureChannelClient 類別
- Windows Media 裝置管理員的參考，CSecureChannelClient 類別
- CSecureChannelClient 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967671"
---
# <a name="csecurechannelclient-class"></a><span data-ttu-id="56ec6-109">CSecureChannelClient 類別</span><span class="sxs-lookup"><span data-stu-id="56ec6-109">CSecureChannelClient Class</span></span>

<span data-ttu-id="56ec6-110">**CSecureChannelClient** 類別是一個 helper 類別， (不是可讓應用程式自行驗證、加密和解密資料，以及建立 mac 的介面) 。</span><span class="sxs-lookup"><span data-stu-id="56ec6-110">The **CSecureChannelClient** class is a helper class (not an interface) that enables applications to authenticate themselves, encrypt and decrypt data, and create MACs.</span></span>

<span data-ttu-id="56ec6-111">**CSecureChannelClient** 類別會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="56ec6-111">The **CSecureChannelClient** class exposes the following methods.</span></span>



| <span data-ttu-id="56ec6-112">方法</span><span class="sxs-lookup"><span data-stu-id="56ec6-112">Method</span></span>                                                            | <span data-ttu-id="56ec6-113">描述</span><span class="sxs-lookup"><span data-stu-id="56ec6-113">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ec6-114">[**身份 驗證**](/previous-versions/ms983906(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="56ec6-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span></span>         | <span data-ttu-id="56ec6-115">觸發元件之間的憑證交換以建立信任。</span><span class="sxs-lookup"><span data-stu-id="56ec6-115">Triggers the exchange of certificates between components to establish trust.</span></span>                                              |
| <span data-ttu-id="56ec6-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56ec6-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span></span>         | <span data-ttu-id="56ec6-117">解密透過參數接收的資料。</span><span class="sxs-lookup"><span data-stu-id="56ec6-117">Decrypts data received through a parameter.</span></span>                                                                               |
| <span data-ttu-id="56ec6-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56ec6-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span></span>         | <span data-ttu-id="56ec6-119">加密透過參數送出的資料。</span><span class="sxs-lookup"><span data-stu-id="56ec6-119">Encrypts data being sent out through a parameter.</span></span>                                                                         |
| <span data-ttu-id="56ec6-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="56ec6-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span></span> | <span data-ttu-id="56ec6-121">確認已成功建立安全驗證通道。</span><span class="sxs-lookup"><span data-stu-id="56ec6-121">Verifies that a secure authentication channel has been successfully established.</span></span> <span data-ttu-id="56ec6-122">應用程式不會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="56ec6-122">This method is not used by applications.</span></span> |
| <span data-ttu-id="56ec6-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="56ec6-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span></span>               | <span data-ttu-id="56ec6-124">抓取本機和遠端元件的應用程式安全性層級。</span><span class="sxs-lookup"><span data-stu-id="56ec6-124">Retrieves the application security levels of the local and remote components.</span></span>                                             |
| <span data-ttu-id="56ec6-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56ec6-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span></span>       | <span data-ttu-id="56ec6-126">抓取目前的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="56ec6-126">Retrieves the current session key.</span></span> <span data-ttu-id="56ec6-127">應用程式不會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="56ec6-127">This method is not used by applications.</span></span>                                               |
| <span data-ttu-id="56ec6-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56ec6-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span></span>                 | <span data-ttu-id="56ec6-129">釋放 (MAC) 通道的訊息驗證碼，並抓取最終的 MAC 值。</span><span class="sxs-lookup"><span data-stu-id="56ec6-129">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>                                   |
| <span data-ttu-id="56ec6-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56ec6-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span></span>                   | <span data-ttu-id="56ec6-131">取得 (MAC) 通道的訊息驗證碼。</span><span class="sxs-lookup"><span data-stu-id="56ec6-131">Acquires a message authentication code (MAC) channel.</span></span>                                                                     |
| <span data-ttu-id="56ec6-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56ec6-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span></span>               | <span data-ttu-id="56ec6-133">將值新增至 (MAC) 的訊息驗證程式代碼。</span><span class="sxs-lookup"><span data-stu-id="56ec6-133">Adds a value to a message authentication code (MAC).</span></span>                                                                      |
| <span data-ttu-id="56ec6-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="56ec6-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span></span>     | <span data-ttu-id="56ec6-135">指定安全驗證通道 (SAC) 用戶端的憑證和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="56ec6-135">Specifies the certificate and private key of the secure authenticated channel (SAC) client.</span></span>                               |
| <span data-ttu-id="56ec6-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56ec6-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span></span>         | <span data-ttu-id="56ec6-137">選取用於安全驗證通道 (SAC) 通訊的介面。</span><span class="sxs-lookup"><span data-stu-id="56ec6-137">Selects the interface used for secure authenticated channel (SAC) communications.</span></span>                                         |
| <span data-ttu-id="56ec6-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="56ec6-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span></span>       | <span data-ttu-id="56ec6-139">設定用來與其他元件通訊的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="56ec6-139">Sets the session key that is used to communicate with another component.</span></span> <span data-ttu-id="56ec6-140">應用程式不會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="56ec6-140">This method is not used by applications.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="56ec6-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="56ec6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56ec6-142">**CSecureChannelServer 類別**</span><span class="sxs-lookup"><span data-stu-id="56ec6-142">**CSecureChannelServer Class**</span></span>](csecurechannelserver-class.md)
</dt> <dt>

[<span data-ttu-id="56ec6-143">**IComponentAuthenticate 介面**</span><span class="sxs-lookup"><span data-stu-id="56ec6-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="56ec6-144">**應用程式的介面**</span><span class="sxs-lookup"><span data-stu-id="56ec6-144">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> </dl>

 

 