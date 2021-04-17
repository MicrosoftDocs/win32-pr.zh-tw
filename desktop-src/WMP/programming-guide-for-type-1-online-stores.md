---
title: 類型1線上商店的程式設計指南
description: 類型1線上商店的程式設計指南
ms.assetid: 6950cab8-4355-4699-8245-f2817c3e25fc
keywords:
- Windows Media Player 線上商店，程式設計手冊
- 線上商店，程式設計指南
- 類型1線上商店，程式設計指南
- 程式設計指南，請輸入1個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea04cb188a68c85173b5b1682235b6964840d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183915"
---
# <a name="programming-guide-for-type-1-online-stores"></a><span data-ttu-id="97453-107">類型1線上商店的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="97453-107">Programming Guide for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="97453-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="97453-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="97453-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="97453-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="97453-110">本章節包含下列主題，可協助您建立類型1線上商店。</span><span class="sxs-lookup"><span data-stu-id="97453-110">This section contains the following topics to help you create a type 1 online store.</span></span>



| <span data-ttu-id="97453-111">區段</span><span class="sxs-lookup"><span data-stu-id="97453-111">Section</span></span>                                                                                                              | <span data-ttu-id="97453-112">描述</span><span class="sxs-lookup"><span data-stu-id="97453-112">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97453-113">類型1線上商店的範例 ServiceInfo 檔</span><span class="sxs-lookup"><span data-stu-id="97453-113">Example ServiceInfo Document for a Type 1 Online Store</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="97453-114">顯示您可以用來作為起點的範例 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="97453-114">Shows an example ServiceInfo document that you can use as a starting point.</span></span>                                                                    |
| [<span data-ttu-id="97453-115">建立類型1線上商店的外掛程式</span><span class="sxs-lookup"><span data-stu-id="97453-115">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)                 | <span data-ttu-id="97453-116">說明如何建立類型1線上商店的必要外掛程式。</span><span class="sxs-lookup"><span data-stu-id="97453-116">Explains how to build the required plug-in for a type 1 online store.</span></span>                                                                          |
| [<span data-ttu-id="97453-117">顯示對話方塊</span><span class="sxs-lookup"><span data-stu-id="97453-117">Displaying Dialog Boxes</span></span>](displaying-dialog-boxes.md)                                                               | <span data-ttu-id="97453-118">說明如何透過 Windows Media Player 叫用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="97453-118">Explains how to invoke dialog boxes through Windows Media Player.</span></span>                                                                              |
| [<span data-ttu-id="97453-119">管理登入</span><span class="sxs-lookup"><span data-stu-id="97453-119">Managing Login</span></span>](managing-login.md)                                                                                 | <span data-ttu-id="97453-120">說明如何與可讓使用者從線上商店登入和登出的 Windows Media Player 使用者介面元素互動。</span><span class="sxs-lookup"><span data-stu-id="97453-120">Explains how to interact with Windows Media Player user interface elements that let users log in to and log out from the online store.</span></span>         |
| [<span data-ttu-id="97453-121">購買媒體內容</span><span class="sxs-lookup"><span data-stu-id="97453-121">Purchasing Media Content</span></span>](purchasing-media-content.md)                                                             | <span data-ttu-id="97453-122">說明當使用者購買媒體內容時，Windows Media Player 和線上商店的外掛程式如何互動。</span><span class="sxs-lookup"><span data-stu-id="97453-122">Explains how Windows Media Player and the online store's plug-in interact when the user purchases media content.</span></span>                               |
| [<span data-ttu-id="97453-123">下載媒體內容</span><span class="sxs-lookup"><span data-stu-id="97453-123">Downloading Media Content</span></span>](downloading-media-content.md)                                                           | <span data-ttu-id="97453-124">說明當使用者下載媒體內容時，Windows Media Player 和線上商店的外掛程式如何互動。</span><span class="sxs-lookup"><span data-stu-id="97453-124">Explains how Windows Media Player and the online store's plug-in interact when the user downloads media content.</span></span>                               |
| [<span data-ttu-id="97453-125">更新授權</span><span class="sxs-lookup"><span data-stu-id="97453-125">Updating Licenses</span></span>](updating-licenses.md)                                                                           | <span data-ttu-id="97453-126">說明 Windows Media Player 和線上商店的外掛程式如何互動，以保持使用者媒體授權的最新狀態。</span><span class="sxs-lookup"><span data-stu-id="97453-126">Explains how Windows Media Player and the online store's plug-in interact to keep the user's media licenses current.</span></span>                           |
| [<span data-ttu-id="97453-127">更新可攜式裝置</span><span class="sxs-lookup"><span data-stu-id="97453-127">Updating Portable Devices</span></span>](updating-portable-devices.md)                                                           | <span data-ttu-id="97453-128">說明當媒體內容在電腦和可攜式裝置之間移動時，Windows Media Player 和線上商店的外掛程式如何互動。</span><span class="sxs-lookup"><span data-stu-id="97453-128">Explains how Windows Media Player and the online store's plug-in interact when media content moves between the computer and a portable device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="97453-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="97453-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97453-130">**輸入1個線上商店**</span><span class="sxs-lookup"><span data-stu-id="97453-130">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




