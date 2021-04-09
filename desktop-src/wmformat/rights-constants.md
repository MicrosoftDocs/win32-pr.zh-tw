---
title: 許可權常數
description: 許可權常數
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- Windows Media Format SDK，常數
- 數位版權管理 (DRM) ，常數
- DRM (數位版權管理) ，常數
- DRM 用戶端擴充 Api，常數
- 用戶端擴充 Api，常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1349da53b63b1b7df59c13e0e69f7fdbf47ee3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092303"
---
# <a name="rights-constants"></a><span data-ttu-id="4acbe-108">許可權常數</span><span class="sxs-lookup"><span data-stu-id="4acbe-108">Rights Constants</span></span>

<span data-ttu-id="4acbe-109">下表所列的常數可用來識別 DRM 動作，以及建立動作清單。</span><span class="sxs-lookup"><span data-stu-id="4acbe-109">The constants listed in the following table are used to identify DRM actions and to build lists of actions.</span></span>



| <span data-ttu-id="4acbe-110">常數</span><span class="sxs-lookup"><span data-stu-id="4acbe-110">Constant</span></span>                                        | <span data-ttu-id="4acbe-111">描述</span><span class="sxs-lookup"><span data-stu-id="4acbe-111">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4acbe-112">g \_ wszWMDRM \_ 時 \_ 標記</span><span class="sxs-lookup"><span data-stu-id="4acbe-112">g\_wszWMDRM\_ACTIONLIST\_TAG</span></span>                    | <span data-ttu-id="4acbe-113">定義動作清單的 XML 元素名稱。</span><span class="sxs-lookup"><span data-stu-id="4acbe-113">Defines the XML element name for an action list.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="4acbe-114">g \_ wszWMDRM \_ 動作 \_ 標記</span><span class="sxs-lookup"><span data-stu-id="4acbe-114">g\_wszWMDRM\_ACTION\_TAG</span></span>                        | <span data-ttu-id="4acbe-115">定義動作清單中專案的 XML 元素名稱。</span><span class="sxs-lookup"><span data-stu-id="4acbe-115">Defines the XML element name for an entry in an action list.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="4acbe-116">g \_ wszWMDRM \_ 右 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="4acbe-116">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="4acbe-117">定義播放內容之許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-117">Defines the string for the right to play content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="4acbe-118">g \_ wszWMDRM \_ RIGHT \_ COPY</span><span class="sxs-lookup"><span data-stu-id="4acbe-118">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="4acbe-119">定義複製內容之許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-119">Defines the string for the right to copy content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="4acbe-120">g \_ wszWMDRM \_ 右 \_ 播放清單 \_ 燒錄</span><span class="sxs-lookup"><span data-stu-id="4acbe-120">g\_wszWMDRM\_RIGHT\_PLAYLIST\_BURN</span></span>              | <span data-ttu-id="4acbe-121">定義在播放清單中將內容燒錄至 CD 之許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-121">Defines the string for the right to burn content to CD as part of a playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="4acbe-122">g \_ wszWMDRM \_ RIGHT \_ 建立 \_ 縮圖 \_ 影像</span><span class="sxs-lookup"><span data-stu-id="4acbe-122">g\_wszWMDRM\_RIGHT\_CREATE\_THUMBNAIL\_IMAGE</span></span>    | <span data-ttu-id="4acbe-123">定義右邊的字串，以從影片內容建立縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="4acbe-123">Defines the string for the right to create a thumbnail image from video content.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="4acbe-124">g \_ wszWMDRM \_ RIGHT \_ 複製 \_ 到 \_ CD</span><span class="sxs-lookup"><span data-stu-id="4acbe-124">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="4acbe-125">定義將內容複寫到 CD 之許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-125">Defines the string for the right to copy content to a CD.</span></span> <span data-ttu-id="4acbe-126">新的授權不應使用此許可權。</span><span class="sxs-lookup"><span data-stu-id="4acbe-126">New licenses should not use this right.</span></span> <span data-ttu-id="4acbe-127">相反地，所有授與複製內容許可權的許可權都應該包含在複製許可權的上方，且播放清單會正確地進行燒錄。</span><span class="sxs-lookup"><span data-stu-id="4acbe-127">Instead, all rights granting permission to copy content should be covered by the copy right and the playlist burn right.</span></span>                                     |
| <span data-ttu-id="4acbe-128">g \_ wszWMDRM \_ RIGHT \_ 複製 \_ 到 \_ SDMI \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="4acbe-128">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="4acbe-129">定義將內容複寫到符合「安全數位音樂」方案 (SDMI) 之裝置許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-129">Defines the string for the right to copy content to a device that conforms to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="4acbe-130">新的授權不應使用此許可權。</span><span class="sxs-lookup"><span data-stu-id="4acbe-130">New licenses should not use this right.</span></span> <span data-ttu-id="4acbe-131">相反地，複製內容的擁有權限都應該包含在複製許可權的涵蓋範圍內。</span><span class="sxs-lookup"><span data-stu-id="4acbe-131">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="4acbe-132">g \_ wszWMDRM \_ RIGHT \_ COPY \_ 至 \_ 非 \_ SDMI \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="4acbe-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="4acbe-133">定義要複製到不符合安全數位音樂方案 (SDMI) 之裝置的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-133">Defines the string for the right to copy to a device that does not conform to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="4acbe-134">新的授權不應使用此許可權。</span><span class="sxs-lookup"><span data-stu-id="4acbe-134">New licenses should not use this right.</span></span> <span data-ttu-id="4acbe-135">相反地，複製內容的擁有權限都應該包含在複製許可權的涵蓋範圍內。</span><span class="sxs-lookup"><span data-stu-id="4acbe-135">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="4acbe-136">g \_ wszWMDRM \_ 右 \_ 備份</span><span class="sxs-lookup"><span data-stu-id="4acbe-136">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="4acbe-137">定義備份授權之許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-137">Defines the string for the right to backup the license.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="4acbe-138">g \_ wszWMDRM \_ RIGHT \_ 協同作業 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="4acbe-138">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="4acbe-139">定義在共用播放清單中以網路播放內容之許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="4acbe-139">Defines the string for the right to play content over a network as part of a shared playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="4acbe-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="4acbe-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4acbe-141">**常數**</span><span class="sxs-lookup"><span data-stu-id="4acbe-141">**Constants**</span></span>](constants.md)
</dt> </dl>

 

 




