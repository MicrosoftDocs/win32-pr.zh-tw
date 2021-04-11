---
title: 安裝線上商店的命令列參數
description: 安裝線上商店的命令列參數
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player 線上商店，設定命令列參數
- 線上商店，安裝命令列參數
- 輸入1個線上商店，安裝命令列參數
- 輸入2個線上商店，安裝命令列參數
- 設定命令列參數
- Windows Media Player 線上商店，命令列參數
- 線上商店、命令列參數
- 輸入1個線上商店、命令列參數
- 類型2線上商店，命令列參數
- 命令列參數
- Windows Media Player 線上商店、參數
- 線上商店、參數
- 輸入1個線上商店、參數
- 類型2線上商店、參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021381"
---
# <a name="setup-command-line-parameters-for-online-stores"></a><span data-ttu-id="e721a-117">安裝線上商店的命令列參數</span><span class="sxs-lookup"><span data-stu-id="e721a-117">Setup Command-line Parameters for Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="e721a-118">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="e721a-118">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e721a-119">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="e721a-119">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e721a-120">在 Windows XP 上安裝 Windows Media Player 10 或 Windows Media Player 11 時，您可以附加命令列參數，以指定使用者所看到的第一個線上商店。</span><span class="sxs-lookup"><span data-stu-id="e721a-120">When installing Windows Media Player 10 or Windows Media Player 11 on Windows XP, you can append command-line parameters to specify the first online store that the user sees.</span></span>

<span data-ttu-id="e721a-121">語法</span><span class="sxs-lookup"><span data-stu-id="e721a-121">Syntax</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



<span data-ttu-id="e721a-122">參數</span><span class="sxs-lookup"><span data-stu-id="e721a-122">Parameters</span></span>

<span data-ttu-id="e721a-123">DefaultService (必要) </span><span class="sxs-lookup"><span data-stu-id="e721a-123">DefaultService (required)</span></span>

<span data-ttu-id="e721a-124">線上商店的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="e721a-124">The key name for the online store.</span></span> <span data-ttu-id="e721a-125">這個值必須符合 ServiceInfo 檔中 **ServiceInfo** 元素之索引 **鍵** 屬性的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="e721a-125">This value must match the key name in the **Key** attribute of the **ServiceInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="e721a-126">ServiceInfo (必要) </span><span class="sxs-lookup"><span data-stu-id="e721a-126">ServiceInfo (required)</span></span>

<span data-ttu-id="e721a-127">安裝在使用者電腦上之 ServiceInfo 檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e721a-127">The fully qualified path to a ServiceInfo document installed on the user's computer.</span></span>

<span data-ttu-id="e721a-128">ServiceExtra (選用) </span><span class="sxs-lookup"><span data-stu-id="e721a-128">ServiceExtra (optional)</span></span>

<span data-ttu-id="e721a-129">Windows Media Player 10 的查詢字串會在線上抓取檔時附加至 ServiceInfo 檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="e721a-129">A query string that Windows Media Player 10 will append to the URL for the ServiceInfo document when it retrieves the document online.</span></span>

## <a name="remarks"></a><span data-ttu-id="e721a-130">備註</span><span class="sxs-lookup"><span data-stu-id="e721a-130">Remarks</span></span>

<span data-ttu-id="e721a-131">如需使用您的應用程式轉散發 Windows Media Player 軟體的詳細資訊，請參閱轉散發 [Windows Media Player 軟體](redistributing-windows-media-player-software.md)。</span><span class="sxs-lookup"><span data-stu-id="e721a-131">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="e721a-132">當使用者的電腦未連線到網際網路時，會使用本機 ServiceInfo 檔中包含的資訊來設定初始使用中服務的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="e721a-132">When the user's computer is not connected to the Internet, the information contained in the local ServiceInfo document is used to configure Windows Media Player for the initial active service.</span></span>

<span data-ttu-id="e721a-133">命令列參數會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e721a-133">Command-line parameters are case sensitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e721a-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="e721a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e721a-135">**共同品牌的線上商店**</span><span class="sxs-lookup"><span data-stu-id="e721a-135">**Co-Branding Online Stores**</span></span>](co-branding-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e721a-136">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="e721a-136">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e721a-137">**Install 元素**</span><span class="sxs-lookup"><span data-stu-id="e721a-137">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="e721a-138">**設定初始線上商店**</span><span class="sxs-lookup"><span data-stu-id="e721a-138">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




