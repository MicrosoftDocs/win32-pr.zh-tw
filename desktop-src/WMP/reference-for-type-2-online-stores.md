---
title: 類型 2 線上商店的參考
description: 類型 2 線上商店的參考
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player 線上商店，參考
- 線上商店、參考
- 類型2線上商店，參考
- type 2 線上商店的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "103681580"
---
# <a name="reference-for-type-2-online-stores"></a><span data-ttu-id="cb61a-107">類型 2 線上商店的參考</span><span class="sxs-lookup"><span data-stu-id="cb61a-107">Reference for Type 2 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="cb61a-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="cb61a-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="cb61a-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="cb61a-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="cb61a-110">Windows Media Player 10 或更新版本會提供支援類型2線上商店的物件、介面、屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="cb61a-110">Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores.</span></span> <span data-ttu-id="cb61a-111">下列各節將詳細說明這些詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cb61a-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="cb61a-112">區段</span><span class="sxs-lookup"><span data-stu-id="cb61a-112">Section</span></span>                                                                                                        | <span data-ttu-id="cb61a-113">描述</span><span class="sxs-lookup"><span data-stu-id="cb61a-113">Description</span></span>                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb61a-114">IWMPSubscriptionService 介面</span><span class="sxs-lookup"><span data-stu-id="cb61a-114">IWMPSubscriptionService Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | <span data-ttu-id="cb61a-115">提供方法來增強 (DRM) 的數位版權管理，並起始背景進程。</span><span class="sxs-lookup"><span data-stu-id="cb61a-115">Provides methods to augment digital rights management (DRM) and initiate background processes.</span></span>                                                                              |
| [<span data-ttu-id="cb61a-116">IWMPSubscriptionService2 介面</span><span class="sxs-lookup"><span data-stu-id="cb61a-116">IWMPSubscriptionService2 Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | <span data-ttu-id="cb61a-117">提供起始背景進程的方法、提供線上商店活動的相關資訊，以及提供 Windows Media Player 核心介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cb61a-117">Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface.</span></span> |
| [<span data-ttu-id="cb61a-118">IWMPSubscriptionServiceCallback 介面</span><span class="sxs-lookup"><span data-stu-id="cb61a-118">IWMPSubscriptionServiceCallback Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | <span data-ttu-id="cb61a-119">定義線上商店用來在背景進程完成時通知 Windows Media Player 的方法。</span><span class="sxs-lookup"><span data-stu-id="cb61a-119">Defines a method that online stores use to notify Windows Media Player when a background process is completed.</span></span>                                                              |
| [<span data-ttu-id="cb61a-120">WMPNotifySubscriptionPluginAddRemove</span><span class="sxs-lookup"><span data-stu-id="cb61a-120">WMPNotifySubscriptionPluginAddRemove</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | <span data-ttu-id="cb61a-121">用來通知 Windows Media Player 外掛程式已安裝或卸載的函式。</span><span class="sxs-lookup"><span data-stu-id="cb61a-121">A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.</span></span>                                                                            |
| [<span data-ttu-id="cb61a-122">DownloadCollection 物件</span><span class="sxs-lookup"><span data-stu-id="cb61a-122">DownloadCollection Object</span></span>](downloadcollection-object.md)                                                     | <span data-ttu-id="cb61a-123">提供方法和屬性來管理下載專案的集合。</span><span class="sxs-lookup"><span data-stu-id="cb61a-123">Provides methods and properties to manage collections of download items.</span></span>                                                                                                    |
| [<span data-ttu-id="cb61a-124">DownloadItem 物件</span><span class="sxs-lookup"><span data-stu-id="cb61a-124">DownloadItem Object</span></span>](downloaditem-object.md)                                                                 | <span data-ttu-id="cb61a-125">提供與下載要求相關的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="cb61a-125">Provides methods and properties relating to download requests.</span></span>                                                                                                              |
| [<span data-ttu-id="cb61a-126">DownloadManager 物件</span><span class="sxs-lookup"><span data-stu-id="cb61a-126">DownloadManager Object</span></span>](downloadmanager-object.md)                                                           | <span data-ttu-id="cb61a-127">提供管理下載集合的方法。</span><span class="sxs-lookup"><span data-stu-id="cb61a-127">Provides methods to manage download collections.</span></span>                                                                                                                            |
| [<span data-ttu-id="cb61a-128">類型2線上商店的外部物件</span><span class="sxs-lookup"><span data-stu-id="cb61a-128">External Object for Type 2 Online Stores</span></span>](external-object-for-type-2-online-stores.md)                       | <span data-ttu-id="cb61a-129">提供可從線上商店網頁存取的屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="cb61a-129">Provides properties, methods, and an event accessible from online store webpages.</span></span>                                                                                           |
| [<span data-ttu-id="cb61a-130">類型2線上商店的列舉</span><span class="sxs-lookup"><span data-stu-id="cb61a-130">Enumerations for Type 2 Online Stores</span></span>](enumerations-for-type-2-online-stores.md)                             | <span data-ttu-id="cb61a-131">描述線上商店使用的列舉。</span><span class="sxs-lookup"><span data-stu-id="cb61a-131">Describes enumerations used by online stores.</span></span>                                                                                                                               |
| [<span data-ttu-id="cb61a-132">Windows Media Player BITS 作業慣例</span><span class="sxs-lookup"><span data-stu-id="cb61a-132">Windows Media Player BITS Job Convention</span></span>](windows-media-player-bits-job-convention.md)                       | <span data-ttu-id="cb61a-133">描述使用背景智慧型傳送服務 (位) 的慣例。</span><span class="sxs-lookup"><span data-stu-id="cb61a-133">Describes a convention for using the Background Intelligent Transfer Service (BITS).</span></span>                                                                                        |
| [<span data-ttu-id="cb61a-134">Type 2 線上商店的登錄機碼和專案</span><span class="sxs-lookup"><span data-stu-id="cb61a-134">Registry Keys and Entries for a Type 2 Online Store</span></span>](registry-keys-and-entries-for-a-type-2-online-store.md) | <span data-ttu-id="cb61a-135">描述線上商店必須在使用者電腦上的登錄中建立的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="cb61a-135">Describes registry entries that an online store must create in the registry on the user's computer.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="cb61a-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb61a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb61a-137">**輸入2個線上商店**</span><span class="sxs-lookup"><span data-stu-id="cb61a-137">**Type 2 Online Stores**</span></span>](type-2-online-stores.md)
</dt> </dl>

 

 




