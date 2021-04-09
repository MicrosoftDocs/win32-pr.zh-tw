---
title: 設定初始線上商店
description: 設定初始線上商店
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Windows Media Player 線上商店，設定初始線上商店
- 線上商店，設定初始線上商店
- 輸入1個線上商店，設定初始線上商店
- 輸入2個線上商店，設定初始線上商店
- Windows Media Player 線上商店，第一個已觀看的線上商店
- 線上商店，第一個已觀看的線上商店
- 輸入1個線上商店，第一個已觀看的線上商店
- 輸入2個線上商店，第一個已觀看的線上商店
- 第一個線上商店已觀看
- 設定初始線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840476"
---
# <a name="setting-the-initial-online-store"></a><span data-ttu-id="8f97a-113">設定初始線上商店</span><span class="sxs-lookup"><span data-stu-id="8f97a-113">Setting the Initial Online Store</span></span>

<span data-ttu-id="8f97a-114">如需使用您的應用程式轉散發 Windows Media Player 軟體的詳細資訊，請參閱轉散發 [Windows Media Player 軟體](redistributing-windows-media-player-software.md)。</span><span class="sxs-lookup"><span data-stu-id="8f97a-114">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="8f97a-115">當使用者第一次安裝 Windows Media Player 時，安裝應用程式會將初始使用中的線上商店設定為 Microsoft 所選擇的預設值。</span><span class="sxs-lookup"><span data-stu-id="8f97a-115">When a user first installs Windows Media Player, the setup application sets the initial active online store to a default chosen by Microsoft.</span></span> <span data-ttu-id="8f97a-116">個人電腦的原始設備製造商 (Oem) 可以選擇變更此設定。</span><span class="sxs-lookup"><span data-stu-id="8f97a-116">Personal computer original equipment manufacturers (OEMs) can choose to change this setting.</span></span>

<span data-ttu-id="8f97a-117">若要指定及設定使用者安裝 Windows Media Player 時所看到的第一個線上商店，您必須：</span><span class="sxs-lookup"><span data-stu-id="8f97a-117">To specify and configure the first online store that the user sees when he or she installs Windows Media Player, you must:</span></span>

-   <span data-ttu-id="8f97a-118">建立您在使用者的硬碟上安裝的 ServiceInfo 檔。</span><span class="sxs-lookup"><span data-stu-id="8f97a-118">Create a ServiceInfo document that you install on the user's hard disk.</span></span> <span data-ttu-id="8f97a-119">本檔包含如何設定初始主動線上商店的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8f97a-119">This document contains the information about how to configure the initial active online store.</span></span>
-   <span data-ttu-id="8f97a-120">執行安裝應用程式時，請附加一組命令列參數。</span><span class="sxs-lookup"><span data-stu-id="8f97a-120">Append a set of command-line parameters when running the setup application.</span></span>

<span data-ttu-id="8f97a-121">安裝 Windows Media Player 和設定初始線上商店的案例有三種。</span><span class="sxs-lookup"><span data-stu-id="8f97a-121">There are three scenarios for installing Windows Media Player and setting the initial online store.</span></span> <span data-ttu-id="8f97a-122">下列各節提供每個案例的詳細資料：</span><span class="sxs-lookup"><span data-stu-id="8f97a-122">The following sections provide more details about each scenario:</span></span>

-   [<span data-ttu-id="8f97a-123">離線時安裝</span><span class="sxs-lookup"><span data-stu-id="8f97a-123">Installing While Offline</span></span>](installing-while-offline.md)
-   [<span data-ttu-id="8f97a-124">在線上從 CD 安裝</span><span class="sxs-lookup"><span data-stu-id="8f97a-124">Installing from a CD While Online</span></span>](installing-from-a-cd-while-online.md)
-   [<span data-ttu-id="8f97a-125">在線上時從 Web 安裝</span><span class="sxs-lookup"><span data-stu-id="8f97a-125">Installing from the Web While Online</span></span>](installing-from-the-web-while-online.md)

## <a name="related-topics"></a><span data-ttu-id="8f97a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f97a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f97a-127">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="8f97a-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8f97a-128">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="8f97a-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="8f97a-129">**安裝線上商店的命令列參數**</span><span class="sxs-lookup"><span data-stu-id="8f97a-129">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




