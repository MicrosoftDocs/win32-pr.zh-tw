---
title: 類型 1 線上商店的參考
description: 類型 1 線上商店的參考
ms.assetid: e6f45a50-029e-4347-9b25-10e9e32a56eb
keywords:
- Windows Media Player 線上商店，參考
- 線上商店、參考
- 輸入1個線上商店，參考
- 類型1線上商店的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475f7dee43f2f6152c3b3ebd0e6090a1efb33a72
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374792"
---
# <a name="reference-for-type-1-online-stores"></a><span data-ttu-id="7542d-107">類型 1 線上商店的參考</span><span class="sxs-lookup"><span data-stu-id="7542d-107">Reference for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="7542d-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="7542d-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7542d-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="7542d-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7542d-110">Windows Media Player 11 提供目錄編譯器、物件，以及數個支援類型1線上商店的介面。</span><span class="sxs-lookup"><span data-stu-id="7542d-110">Windows Media Player 11 provides a catalog compiler, an object, and several interfaces that support type 1 online stores.</span></span> <span data-ttu-id="7542d-111">下列各節將詳細說明這些詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7542d-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="7542d-112">區段</span><span class="sxs-lookup"><span data-stu-id="7542d-112">Section</span></span>                                                                                    | <span data-ttu-id="7542d-113">描述</span><span class="sxs-lookup"><span data-stu-id="7542d-113">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7542d-114">類型1線上商店的目錄編譯器</span><span class="sxs-lookup"><span data-stu-id="7542d-114">Catalog Compiler for Type 1 Online Stores</span></span>](catalog-compiler-for-type-1-online-stores.md) | <span data-ttu-id="7542d-115">提供編譯器的參考資料，讓線上商店用來編譯其音樂目錄。</span><span class="sxs-lookup"><span data-stu-id="7542d-115">Provides reference material for the compiler that an online store uses to compile its music catalog.</span></span>                                                                                                                               |
| [<span data-ttu-id="7542d-116">IWMPContentContainer 介面</span><span class="sxs-lookup"><span data-stu-id="7542d-116">IWMPContentContainer Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)                                 | <span data-ttu-id="7542d-117">提供線上商店的外掛程式呼叫以檢查內容容器的方法參考頁面。</span><span class="sxs-lookup"><span data-stu-id="7542d-117">Provides reference pages for methods that the online store's plug-in calls to inspect a content container.</span></span> <span data-ttu-id="7542d-118">內容容器代表要下載或購買的一組媒體專案。</span><span class="sxs-lookup"><span data-stu-id="7542d-118">A content container represents a set of media items to be downloaded or purchased.</span></span> <span data-ttu-id="7542d-119">由 Windows Media Player 所執行。</span><span class="sxs-lookup"><span data-stu-id="7542d-119">Implemented by Windows Media Player.</span></span> |
| [<span data-ttu-id="7542d-120">IWMPContentContainerList 介面</span><span class="sxs-lookup"><span data-stu-id="7542d-120">IWMPContentContainerList Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)                         | <span data-ttu-id="7542d-121">提供線上商店的外掛程式呼叫以檢查內容容器清單的方法參考頁面。</span><span class="sxs-lookup"><span data-stu-id="7542d-121">Provides reference pages for methods that the online store's plug-in calls to inspect a list of content containers.</span></span> <span data-ttu-id="7542d-122">由 Windows Media Player 所執行。</span><span class="sxs-lookup"><span data-stu-id="7542d-122">Implemented by Windows Media Player.</span></span>                                                                           |
| [<span data-ttu-id="7542d-123">IWMPContentPartner 介面</span><span class="sxs-lookup"><span data-stu-id="7542d-123">IWMPContentPartner Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)                                     | <span data-ttu-id="7542d-124">提供方法的參考頁面，這些方法會 Windows Media Player 呼叫以從線上商店取得資訊，以及通知線上商店有關使用者的動作。</span><span class="sxs-lookup"><span data-stu-id="7542d-124">Provides reference pages for methods that Windows Media Player calls to get information from the online store and to notify the online store about the user's actions.</span></span> <span data-ttu-id="7542d-125">由線上商店的外掛程式所執行。</span><span class="sxs-lookup"><span data-stu-id="7542d-125">Implemented by the online store's plug-in.</span></span>                  |
| [<span data-ttu-id="7542d-126">IWMPContentPartnerCallback 介面</span><span class="sxs-lookup"><span data-stu-id="7542d-126">IWMPContentPartnerCallback Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)                     | <span data-ttu-id="7542d-127">提供線上商店的外掛程式呼叫的方法參考頁面，以通知 Windows Media Player 非同步作業是否完成。</span><span class="sxs-lookup"><span data-stu-id="7542d-127">Provides reference pages for methods that the online store's plug-in calls to notify Windows Media Player about the completion of asynchronous operations.</span></span> <span data-ttu-id="7542d-128">由 Windows Media Player 所執行。</span><span class="sxs-lookup"><span data-stu-id="7542d-128">Implemented by Windows Media Player.</span></span>                                    |
| [<span data-ttu-id="7542d-129">類型1線上商店的外部物件</span><span class="sxs-lookup"><span data-stu-id="7542d-129">External Object for Type 1 Online Stores</span></span>](external-object-for-type-1-online-stores.md)   | <span data-ttu-id="7542d-130">提供在線上商店提供的網頁中，腳本所使用之屬性、方法和事件的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="7542d-130">Provides reference pages for properties, methods, and events used by script in webpages provided by the online store.</span></span>                                                                                                              |
| [<span data-ttu-id="7542d-131">類型1線上商店的列舉</span><span class="sxs-lookup"><span data-stu-id="7542d-131">Enumerations for Type 1 Online Stores</span></span>](enumerations-for-type-1-online-stores.md)         | <span data-ttu-id="7542d-132">提供用於 Windows Media Player 與線上商店外掛程式之間通訊的列舉參考頁面。</span><span class="sxs-lookup"><span data-stu-id="7542d-132">Provides reference pages for the enumerations used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                               |
| [<span data-ttu-id="7542d-133">類型1線上商店的結構</span><span class="sxs-lookup"><span data-stu-id="7542d-133">Structures for Type 1 Online Stores</span></span>](structures-for-type-1-online-stores.md)             | <span data-ttu-id="7542d-134">針對 Windows Media Player 與線上商店的外掛程式之間的通訊所使用的結構提供參考頁面。</span><span class="sxs-lookup"><span data-stu-id="7542d-134">Provides reference pages for the structures used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="7542d-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="7542d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7542d-136">**輸入1個線上商店**</span><span class="sxs-lookup"><span data-stu-id="7542d-136">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




