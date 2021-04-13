---
title: 設定持續性
description: 設定持續性
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK，持續性
- Windows Media Format SDK，設定持續性
- Advanced Systems Format (ASF) ，持續性
- ASF (Advanced Systems Format) ，持續性
- Advanced Systems Format (ASF) 、設定持續性
- ASF (Advanced Systems Format) ，設定持續性
- 設定持續性
- 保存性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374554"
---
# <a name="configuration-persistence"></a><span data-ttu-id="d2f08-111">設定持續性</span><span class="sxs-lookup"><span data-stu-id="d2f08-111">Configuration Persistence</span></span>

<span data-ttu-id="d2f08-112">這份檔中所述的任何可寫入屬性都不是由 Windows Media SDK 儲存。</span><span class="sxs-lookup"><span data-stu-id="d2f08-112">None of the write-enabled properties described in this documentation are saved by the Windows Media SDK.</span></span> <span data-ttu-id="d2f08-113">使用 SDK 的每個應用程式都必須視需要提供自己的持續性程式，並在每個 SDK 實例上叫用適當的 set 方法。</span><span class="sxs-lookup"><span data-stu-id="d2f08-113">Each application that uses the SDK must provide its own persistence procedures as needed and invoke the appropriate set method upon each instance of the SDK.</span></span> <span data-ttu-id="d2f08-114">如此一來，某個應用程式所做的設定變更不會影響另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2f08-114">In this way, configuration changes made by one application do not affect another application.</span></span> <span data-ttu-id="d2f08-115">例如，在一個播放程式中變更緩衝時間並不會影響另一個玩家。</span><span class="sxs-lookup"><span data-stu-id="d2f08-115">For example, changing the buffering time in one player does not affect another player.</span></span>

<span data-ttu-id="d2f08-116">這項規則的唯一例外是認證資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f08-116">The one exception to this rule is for the credentials information.</span></span> <span data-ttu-id="d2f08-117">如果應用程式在從 **AcquireCredentials** 呼叫傳回時，必須保存使用者識別碼和密碼資訊，SDK 就會儲存這項資訊。</span><span class="sxs-lookup"><span data-stu-id="d2f08-117">If the application indicates, in its return from the **AcquireCredentials** call, that the user ID and password information must be persisted, the SDK saves this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2f08-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2f08-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f08-119">**執行網路功能**</span><span class="sxs-lookup"><span data-stu-id="d2f08-119">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="d2f08-120">**IWMCredentialCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="d2f08-120">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




