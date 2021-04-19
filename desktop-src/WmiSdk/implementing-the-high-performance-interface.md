---
description: 由於 WMI 將高效能提供者載入至 WMI 或用戶端應用程式，因此您必須將高效能提供者設計為同進程伺服器。
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: 執行 High-Performance 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996856"
---
# <a name="implementing-the-high-performance-interface"></a><span data-ttu-id="dfa1f-103">執行 High-Performance 介面</span><span class="sxs-lookup"><span data-stu-id="dfa1f-103">Implementing the High-Performance Interface</span></span>

<span data-ttu-id="dfa1f-104">由於 WMI 將高效能提供者載入至 WMI 或用戶端應用程式，因此您必須將高效能提供者設計為同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-104">Because WMI loads a high-performance provider in-process to either WMI or a client application, you must design your high-performance provider as an in-process server.</span></span> <span data-ttu-id="dfa1f-105">此外，您必須在 [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) 和 [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) 介面中執行高效能的提供者方法。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-105">In addition, you must implement the high-performance provider methods in the [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) and [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interfaces.</span></span>

<span data-ttu-id="dfa1f-106">您應該將高效能提供者實作為同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-106">You should implement a high-performance provider as an in-process server.</span></span> <span data-ttu-id="dfa1f-107">當您在執行同進程伺服器的安全性時，您應該注意的其中一項功能就是提供者如何識別其本身的位置。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-107">One feature you should be aware of when implementing the security of an in-process server is how the provider identifies its own location.</span></span> <span data-ttu-id="dfa1f-108">將內含式載入至 WMI 時，WMI 會使用 CLSID 將提供者具現化。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-108">When loaded in-process to WMI, WMI instantiates the provider using a CLSID.</span></span> <span data-ttu-id="dfa1f-109">當載入至用戶端應用程式的進程時，用戶端應用程式會使用 **ClientLoadableCLSID** 屬性來具現化提供者。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-109">When loaded in process to a client application, the client application instantiates the provider with the **ClientLoadableCLSID** property.</span></span> <span data-ttu-id="dfa1f-110">藉由為 CLSID 和 **ClientLoadableCLSID** 提供不同的值，您可以允許提供者判斷它是否已載入至 WMI 或用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-110">By giving different values to a CLSID and **ClientLoadableCLSID**, you allow the provider to determine if it is loaded in-process to WMI or to a client application.</span></span> <span data-ttu-id="dfa1f-111">如果位於 WMI 進程中，提供者應該使用 **ClientLoadableCLSID** 來執行任何必要的用戶端模擬。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-111">If located in a WMI process, the provider should do any necessary client impersonation by using **ClientLoadableCLSID**.</span></span> <span data-ttu-id="dfa1f-112">如果位於用戶端進程中，提供者會繼承呼叫它的執行緒存取權杖。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-112">If located in a client process, the provider inherits the access token of the thread it is called on.</span></span> <span data-ttu-id="dfa1f-113">如需有關如何執行同進程伺服器的詳細資訊，請參閱 MSDN 的 [COM 章節](https://msdn.microsoft.com/library/aa139695.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-113">For more information about implementing an in-process server, see the [COM section](https://msdn.microsoft.com/library/aa139695.aspx) of MSDN.</span></span>

<span data-ttu-id="dfa1f-114">作為同進程伺服器，高效能的提供者會使用重新整理程式物件將遠端用戶端的資料保持在最新的。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-114">As an in-process server, a high-performance provider uses a refresher object to keep data current for the remote client.</span></span> <span data-ttu-id="dfa1f-115">下表列出您必須為高效能提供者執行的方法。</span><span class="sxs-lookup"><span data-stu-id="dfa1f-115">The following table lists methods that you must implement for a high-performance provider.</span></span>



| <span data-ttu-id="dfa1f-116">方法</span><span class="sxs-lookup"><span data-stu-id="dfa1f-116">Method</span></span>                                                                                              | <span data-ttu-id="dfa1f-117">功能</span><span class="sxs-lookup"><span data-stu-id="dfa1f-117">Feature</span></span>                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="dfa1f-118">**IWbemHiPerfProvider::QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="dfa1f-118">**IWbemHiPerfProvider::QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | <span data-ttu-id="dfa1f-119">查詢</span><span class="sxs-lookup"><span data-stu-id="dfa1f-119">Queries</span></span>                                           |
| [<span data-ttu-id="dfa1f-120">**IWbemHiPerfProvider::GetObjects**</span><span class="sxs-lookup"><span data-stu-id="dfa1f-120">**IWbemHiPerfProvider::GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | <span data-ttu-id="dfa1f-121">物件抓取</span><span class="sxs-lookup"><span data-stu-id="dfa1f-121">Object retrieval</span></span>                                  |
| [<span data-ttu-id="dfa1f-122">**IWbemHiPerfProvider::CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="dfa1f-122">**IWbemHiPerfProvider::CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | <span data-ttu-id="dfa1f-123">建立複習</span><span class="sxs-lookup"><span data-stu-id="dfa1f-123">Creates a refresher</span></span>                               |
| [<span data-ttu-id="dfa1f-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="dfa1f-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | <span data-ttu-id="dfa1f-125">建立可重新整理的實例物件</span><span class="sxs-lookup"><span data-stu-id="dfa1f-125">Creates a refreshable instance object</span></span>             |
| [<span data-ttu-id="dfa1f-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="dfa1f-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | <span data-ttu-id="dfa1f-127">建立可重新整理的列舉值</span><span class="sxs-lookup"><span data-stu-id="dfa1f-127">Creates a refreshable enumerator</span></span>                  |
| [<span data-ttu-id="dfa1f-128">**IWbemHiPerfProvider::StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="dfa1f-128">**IWbemHiPerfProvider::StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | <span data-ttu-id="dfa1f-129">停止重新整理列舉值或實例物件</span><span class="sxs-lookup"><span data-stu-id="dfa1f-129">Stops refreshing an enumerator or instance object</span></span> |
| [<span data-ttu-id="dfa1f-130">**IWbemRefresher：： Refresh**</span><span class="sxs-lookup"><span data-stu-id="dfa1f-130">**IWbemRefresher::Refresh**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | <span data-ttu-id="dfa1f-131">建立複習</span><span class="sxs-lookup"><span data-stu-id="dfa1f-131">Creates a refresher</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="dfa1f-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="dfa1f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfa1f-133">讓執行個體提供者成為 High-Performance 提供者</span><span class="sxs-lookup"><span data-stu-id="dfa1f-133">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



