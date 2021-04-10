---
title: 輸入1線上商店外掛程式
description: 輸入1線上商店外掛程式
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player 線上商店、外掛程式
- 線上商店、外掛程式
- 輸入1個線上商店、外掛程式
- Windows Media Player 線上商店、IWMPContentPartner 介面
- 線上商店、IWMPContentPartner 介面
- 輸入1個線上商店、IWMPContentPartner 介面
- 外掛程式，Windows Media Player 線上商店
- 外掛程式，線上商店
- 外掛程式，請輸入1個線上商店
- 外掛程式，IWMPContentPartner 介面
- Windows Media Player 外掛程式，請輸入1個線上商店
- Windows Media Player 外掛程式，線上商店
- Windows Media Player 外掛程式，Windows Media Player 線上商店
- Windows Media Player 外掛程式、IWMPContentPartner 介面
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023176"
---
# <a name="type-1-online-store-plug-in"></a><span data-ttu-id="27d56-118">輸入1線上商店外掛程式</span><span class="sxs-lookup"><span data-stu-id="27d56-118">Type 1 Online Store Plug-in</span></span>

<span data-ttu-id="27d56-119">若要利用程式庫整合功能，請輸入1線上商店提供者必須建立可執行 [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) 介面的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="27d56-119">To take advantage of library integration features, type 1 online store providers must create a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="27d56-120">這個介面會提供 Windows Media Player 呼叫的方法，以通知線上商店有關播放程式中發生的活動，以及抓取有關線上商店內容、目錄或商店本身的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="27d56-120">This interface provides the methods that Windows Media Player calls to notify the online store about activities taking place in the Player and to retrieve specific information about online store content, the catalog, or the store itself.</span></span>

<span data-ttu-id="27d56-121">在 Windows Media Player 具現化外掛程式之後，Player 會呼叫 [IWMPContentPartner：： SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)，並提供 **IWMPContentPartnerCallback** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="27d56-121">After Windows Media Player instantiates the plug-in, the Player calls [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback), and provides a pointer to the **IWMPContentPartnerCallback** interface.</span></span> <span data-ttu-id="27d56-122">此介面可讓線上商店利用方法來呼叫 Windows Media Player，以提供狀態資訊或起始特定進程，例如下載音樂播放軌。</span><span class="sxs-lookup"><span data-stu-id="27d56-122">This interface gives the online store a way to make calls into Windows Media Player to provide status information or to initiate specific processes, such as downloading a music track.</span></span>

<span data-ttu-id="27d56-123">Windows Media Player 和外掛程式是在不同的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="27d56-123">Windows Media Player and the plug-in run in separate processes.</span></span> <span data-ttu-id="27d56-124">外掛程式是在預設 DLL 代理 dllhost.exe 中執行的同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="27d56-124">The plug-in is an in-process server that runs in the default DLL surrogate, dllhost.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27d56-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="27d56-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27d56-126">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="27d56-126">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="27d56-127">**IWMPContentPartner 介面**</span><span class="sxs-lookup"><span data-stu-id="27d56-127">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[<span data-ttu-id="27d56-128">**IWMPContentPartnerCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="27d56-128">**IWMPContentPartnerCallback Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




