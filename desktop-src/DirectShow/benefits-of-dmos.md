---
description: DMOs 的優點
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: DMOs 的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187533"
---
# <a name="benefits-of-dmos"></a><span data-ttu-id="4e3da-103">DMOs 的優點</span><span class="sxs-lookup"><span data-stu-id="4e3da-103">Benefits of DMOs</span></span>

<span data-ttu-id="4e3da-104">DMOs 提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="4e3da-104">DMOs offer the following advantages:</span></span>

-   <span data-ttu-id="4e3da-105">它們通常比 DirectShow 篩選器更小且更簡單，因為它們支援較少的功能。</span><span class="sxs-lookup"><span data-stu-id="4e3da-105">They are generally smaller and simpler than DirectShow filters, because they support less functionality.</span></span>
-   <span data-ttu-id="4e3da-106">它們比 DirectShow 篩選更有彈性，因為它們不需要篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="4e3da-106">They are more flexible than DirectShow filters because they do not require a filter graph.</span></span> <span data-ttu-id="4e3da-107">當您需要 DirectShow 提供的服務時（例如同步處理、智慧型連接、資料流程的自動處理和執行緒管理），您可以使用它們搭配 DirectShow。</span><span class="sxs-lookup"><span data-stu-id="4e3da-107">You can use them with DirectShow when you need the services that DirectShow provides, such as synchronization, intelligent connection, automatic handling of data flow, and thread management.</span></span> <span data-ttu-id="4e3da-108">不需要這些服務的用戶端可以直接存取 DMOs。</span><span class="sxs-lookup"><span data-stu-id="4e3da-108">Clients that do not need these services can access DMOs directly.</span></span>
-   <span data-ttu-id="4e3da-109">DMOs 一律會執行同步資料處理，以消除您撰寫篩選時必須考慮的許多執行緒問題。</span><span class="sxs-lookup"><span data-stu-id="4e3da-109">DMOs always perform synchronous data processing, which eliminates many of the threading issues that you must consider if you write a filter.</span></span>
-   <span data-ttu-id="4e3da-110">不同于傳統的 BC-VCM-LVM-HYPERV 編解碼器，DMOs 是以元件物件模型 (COM) 為基礎，因此可以透過 **QueryInterface** 延伸。</span><span class="sxs-lookup"><span data-stu-id="4e3da-110">Unlike traditional ACM and VCM codecs, DMOs are based on the Component Object Model (COM), so they can be extended through **QueryInterface**.</span></span>
-   <span data-ttu-id="4e3da-111">DMOs 支援比或 BC-VCM-LVM-HYPERV 編解碼器更一般化的串流模型。</span><span class="sxs-lookup"><span data-stu-id="4e3da-111">DMOs support a more generalized streaming model than ACM or VCM codecs.</span></span> <span data-ttu-id="4e3da-112">就像 DirectShow 篩選器一樣，DMOs 可以支援多個輸入和多個輸出。</span><span class="sxs-lookup"><span data-stu-id="4e3da-112">Like DirectShow filters, DMOs can support multiple inputs and multiple outputs.</span></span>

<span data-ttu-id="4e3da-113">基於這些理由，現在建議使用 DMOs 作為撰寫編碼器、解碼器和音訊效果的解決方案。</span><span class="sxs-lookup"><span data-stu-id="4e3da-113">For these reasons, DMOs are now recommended as the solution for writing encoders, decoders, and audio effects.</span></span> <span data-ttu-id="4e3da-114">您也可以視應用程式的需求而定，其他許多案例也是可行的。</span><span class="sxs-lookup"><span data-stu-id="4e3da-114">Many other scenarios are possible as well, depending on the needs of the application.</span></span>

<span data-ttu-id="4e3da-115">DMOs 與 DirectShow 濾波器有何不同</span><span class="sxs-lookup"><span data-stu-id="4e3da-115">How DMOs Differ from DirectShow Filters</span></span>

<span data-ttu-id="4e3da-116">DirectShow 篩選器無法在 DirectShow 篩選圖形之外運作。</span><span class="sxs-lookup"><span data-stu-id="4e3da-116">DirectShow filters cannot function outside of a DirectShow filter graph.</span></span> <span data-ttu-id="4e3da-117">在 DirectShow 中，篩選圖形管理員會在應用程式和篩選器之間協調。</span><span class="sxs-lookup"><span data-stu-id="4e3da-117">In DirectShow, the Filter Graph Manager mediates between the application and the filters.</span></span> <span data-ttu-id="4e3da-118">DirectShow 篩選器會執行串流資料所需的大部分工作，包括：</span><span class="sxs-lookup"><span data-stu-id="4e3da-118">DirectShow filters do most of the work required to stream data, including:</span></span>

-   <span data-ttu-id="4e3da-119">配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4e3da-119">Allocating buffers.</span></span>
-   <span data-ttu-id="4e3da-120">協調媒體類型和連接至其他篩選器。</span><span class="sxs-lookup"><span data-stu-id="4e3da-120">Negotiating media types and connections to other filters.</span></span>
-   <span data-ttu-id="4e3da-121">透過篩選圖形推送資料。</span><span class="sxs-lookup"><span data-stu-id="4e3da-121">Pushing data through the filter graph.</span></span>
-   <span data-ttu-id="4e3da-122">將事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="4e3da-122">Sending events to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="4e3da-123">同步處理多個執行緒。</span><span class="sxs-lookup"><span data-stu-id="4e3da-123">Synchronizing multiple threads.</span></span>

<span data-ttu-id="4e3da-124">相反地，一說，每一種事都沒有。</span><span class="sxs-lookup"><span data-stu-id="4e3da-124">In contrast, a DMO does none of these things.</span></span> <span data-ttu-id="4e3da-125">相反地，這些類型的工作是用戶端使用 SQL-DMO 的責任。</span><span class="sxs-lookup"><span data-stu-id="4e3da-125">Instead, these kinds of tasks are the responsibility of the client using the DMO.</span></span> <span data-ttu-id="4e3da-126">用戶端會配置緩衝區，並將資料填滿，然後將它們傳遞給該。</span><span class="sxs-lookup"><span data-stu-id="4e3da-126">The client allocates buffers, fills them with data, and delivers them to the DMO.</span></span> <span data-ttu-id="4e3da-127">SQL-DMO 會處理資料，而用戶端會抓取產生的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4e3da-127">The DMO processes the data, and the client retrieves the resulting output buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e3da-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e3da-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e3da-129">關於 DMOs</span><span class="sxs-lookup"><span data-stu-id="4e3da-129">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



