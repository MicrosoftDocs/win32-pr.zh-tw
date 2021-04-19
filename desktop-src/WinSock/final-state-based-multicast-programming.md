---
description: 本節說明使用 IOCTLs 而不是通訊端選項的最終狀態式多播程式設計。 如需最終狀態式多播程式設計與以變更為基礎的多播程式設計有何不同的總覽，請參閱多播程式設計。
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: 以最終狀態為基礎的多播程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973845"
---
# <a name="final-state-based-multicast-programming"></a><span data-ttu-id="1f346-104">以最終狀態為基礎的多播程式設計</span><span class="sxs-lookup"><span data-stu-id="1f346-104">Final-State-Based Multicast Programming</span></span>

<span data-ttu-id="1f346-105">本節說明使用 IOCTLs 而不是通訊端選項的最終狀態式多播程式設計。</span><span class="sxs-lookup"><span data-stu-id="1f346-105">This section describes final-state-based multicast programming using IOCTLs instead of socket options.</span></span> <span data-ttu-id="1f346-106">如需最終狀態式多播程式設計與以變更為基礎的多播程式設計有何不同的總覽，請參閱 [多播程式設計](multicast-programming.md)。</span><span class="sxs-lookup"><span data-stu-id="1f346-106">For an overview of how final-state-based multicast programming differs from change-based multicast programming, see [Multicast Programming](multicast-programming.md).</span></span>

<span data-ttu-id="1f346-107">下表描述用於 Windows 的多播程式設計的 Windows 通訊端 IOCTLs。</span><span class="sxs-lookup"><span data-stu-id="1f346-107">The following table describes the Windows Sockets IOCTLs used for multicast programming on Windows.</span></span> 

| <span data-ttu-id="1f346-108">IOCTL</span><span class="sxs-lookup"><span data-stu-id="1f346-108">IOCTL</span></span>                       | <span data-ttu-id="1f346-109">引數類型</span><span class="sxs-lookup"><span data-stu-id="1f346-109">Argument type</span></span>                                   |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="1f346-110">SIOCSMSFILTER</span><span class="sxs-lookup"><span data-stu-id="1f346-110">SIOCSMSFILTER</span></span>               | <span data-ttu-id="1f346-111">[**群組 \_篩選**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) 結構</span><span class="sxs-lookup"><span data-stu-id="1f346-111">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="1f346-112">SIOCGMSFILTER</span><span class="sxs-lookup"><span data-stu-id="1f346-112">SIOCGMSFILTER</span></span>               | <span data-ttu-id="1f346-113">[**群組 \_篩選**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) 結構</span><span class="sxs-lookup"><span data-stu-id="1f346-113">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="1f346-114">SIO \_ 取得 \_ 多播 \_ 篩選</span><span class="sxs-lookup"><span data-stu-id="1f346-114">SIO\_GET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="1f346-115">[**ip \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) 結構</span><span class="sxs-lookup"><span data-stu-id="1f346-115">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |
| <span data-ttu-id="1f346-116">SIO \_ 設定 \_ 多播 \_ 篩選器</span><span class="sxs-lookup"><span data-stu-id="1f346-116">SIO\_SET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="1f346-117">[**ip \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) 結構</span><span class="sxs-lookup"><span data-stu-id="1f346-117">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |



 

<span data-ttu-id="1f346-118">請注意， **SIOCSMSFILTER** 和 **SIOCGMSFILTER** IOCTLS 可在 Windows Vista 和更新版本上取得。</span><span class="sxs-lookup"><span data-stu-id="1f346-118">Note that the **SIOCSMSFILTER** and **SIOCGMSFILTER** IOCTLS are available on Windows Vista and later.</span></span>

<span data-ttu-id="1f346-119">使用這些 IOCTLs 進行多播程式設計時，在使用大型來源清單時有其效能優勢。</span><span class="sxs-lookup"><span data-stu-id="1f346-119">Using these IOCTLs for multicast programming has performance benefits when working with large source lists.</span></span> <span data-ttu-id="1f346-120">如需有關使用 SIO \_ 取得 \_ 多播 \_ 篩選器或 SIO 設定多播篩選器之參數和設定的詳細資訊 \_ \_ ，請 \_ 參閱 [**群組 \_ 篩選**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="1f346-120">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) reference page.</span></span> <span data-ttu-id="1f346-121">如需有關使用 SIO \_ 取得 \_ 多播 \_ 篩選器或 SIO 設定多播篩選器之參數和設定的詳細資訊 \_ \_ ，請 \_ 參閱 [**ip \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="1f346-121">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) reference page.</span></span>

 

 



