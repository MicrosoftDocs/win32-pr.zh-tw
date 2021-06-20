---
title: 'Windows Media Player SDK (所需的介面) '
description: 瞭解 Windows Media Player 在 DirectShow 或媒體基礎中實施的必要介面。
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406091"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="30f43-108">Windows Media Player SDK (所需的介面) </span><span class="sxs-lookup"><span data-stu-id="30f43-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="30f43-109">Windows Media Player 使用下列其中一個管線呈現音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="30f43-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="30f43-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="30f43-110">DirectShow</span></span>
-   <span data-ttu-id="30f43-111">媒體基礎</span><span class="sxs-lookup"><span data-stu-id="30f43-111">Media Foundation</span></span>

<span data-ttu-id="30f43-112">在 Microsoft Windows XP 及更早版本中，Player 會使用 DirectShow。</span><span class="sxs-lookup"><span data-stu-id="30f43-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="30f43-113">在 Windows Vista 中，播放的有時會使用 DirectShow，有時會使用媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="30f43-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="30f43-114">DSP 外掛程式會執行下列部分或所有介面：</span><span class="sxs-lookup"><span data-stu-id="30f43-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="30f43-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="30f43-115">**IMediaObject**</span></span>
-   <span data-ttu-id="30f43-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="30f43-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="30f43-117">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="30f43-117">**IMFTransform**</span></span>
-   <span data-ttu-id="30f43-118">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="30f43-118">**IMFGetService**</span></span>
-   <span data-ttu-id="30f43-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="30f43-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="30f43-120">可在 DirectShow 管線中執行的外掛程式，可執行 **IMediaObject** 和 **IWMPPluginEnable** 。</span><span class="sxs-lookup"><span data-stu-id="30f43-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="30f43-121">它也可以在媒體基礎所提供包裝函式內的媒體基礎管線中執行。</span><span class="sxs-lookup"><span data-stu-id="30f43-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="30f43-122">這種類型的外掛程式稱為 Microsoft DirectX Media 物件 (的) 。</span><span class="sxs-lookup"><span data-stu-id="30f43-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="30f43-123">很常見的方式是將 SQL-DMO 視為類似 DirectShow 中的篩選物件。</span><span class="sxs-lookup"><span data-stu-id="30f43-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="30f43-124">SQL-DMO 檔位於 Windows SDK 的 [DirectShow] 區段中。</span><span class="sxs-lookup"><span data-stu-id="30f43-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="30f43-125"> (執行 **IMFTransform** 和 **IMFGetService** 的外掛程式可以原生方式執行，媒體基礎管線中) 不需要任何包裝函式。</span><span class="sxs-lookup"><span data-stu-id="30f43-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="30f43-126">此類型的外掛程式稱為媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="30f43-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="30f43-127">MFT 檔位於 Windows SDK 的媒體基礎區段中。</span><span class="sxs-lookup"><span data-stu-id="30f43-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="30f43-128">實 **IMediaObject**、 **IWMPPluginEnable**、 **IMFTransform** 和 **IMFGetService** 的外掛程式可以在 DirectShow 管線中執行，也可以在媒體基礎管線中以原生方式執行。</span><span class="sxs-lookup"><span data-stu-id="30f43-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="30f43-129">這種類型的外掛程式（稱為 *雙重模式的 DSP 外掛程式*）可以扮演或 MFT 的角色。</span><span class="sxs-lookup"><span data-stu-id="30f43-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="30f43-130">當 Windows Media Player 在媒體基礎管線中使用雙重模式的 DSP 外掛程式時，它會先查詢 **IMFTransform** 介面。</span><span class="sxs-lookup"><span data-stu-id="30f43-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="30f43-131">如果查詢失敗，請 Windows Media Player **IMediaObject** 介面的查詢。</span><span class="sxs-lookup"><span data-stu-id="30f43-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="30f43-132">如果 **IMediaObject** 查詢成功，則外掛程式會包裝並新增至媒體基礎管線。</span><span class="sxs-lookup"><span data-stu-id="30f43-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="30f43-133">無論管線為何，允許使用者設定屬性的任何 DSP 外掛程式都必須執行 **ISpecifyPropertyPages**。</span><span class="sxs-lookup"><span data-stu-id="30f43-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30f43-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="30f43-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30f43-135">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="30f43-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="30f43-136">**DSP 外掛程式介面**</span><span class="sxs-lookup"><span data-stu-id="30f43-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="30f43-137">**DSP 外掛程式封裝**</span><span class="sxs-lookup"><span data-stu-id="30f43-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




