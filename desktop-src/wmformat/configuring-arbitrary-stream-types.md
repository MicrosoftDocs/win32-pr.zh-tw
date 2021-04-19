---
title: 設定任意資料流程類型
description: 設定任意資料流程類型
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- 資料流程，設定任意資料流程類型
- 編解碼器，設定任意資料流程類型
- 資料流程，GenProfile
- 編解碼器、GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965794"
---
# <a name="configuring-arbitrary-stream-types"></a><span data-ttu-id="dc739-108">設定任意資料流程類型</span><span class="sxs-lookup"><span data-stu-id="dc739-108">Configuring Arbitrary Stream Types</span></span>

<span data-ttu-id="dc739-109">大部分的任意串流類型只需要位元速率、緩衝區視窗，以及 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構中適當的主要媒體類型。</span><span class="sxs-lookup"><span data-stu-id="dc739-109">Most arbitrary stream types just need a bit rate, a buffer window, and a proper major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="dc739-110">不過，有些任意類型需要進行額外的設定。</span><span class="sxs-lookup"><span data-stu-id="dc739-110">However, some arbitrary types require additional configuration.</span></span>

<span data-ttu-id="dc739-111">如果您在設定資料流程時遇到問題，請參閱此 SDK 隨附的範例應用程式（稱為 GenProfile）。</span><span class="sxs-lookup"><span data-stu-id="dc739-111">If you have trouble configuring a stream, refer to the sample application called GenProfile, which is included with this SDK.</span></span> <span data-ttu-id="dc739-112">GenProfile 中定義的程式庫包含包含所有資料流程類型的程式碼。</span><span class="sxs-lookup"><span data-stu-id="dc739-112">The library defined in GenProfile contains code for including all types of streams.</span></span> <span data-ttu-id="dc739-113">如需 GenProfile 和其他範例的詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="dc739-113">For more information about GenProfile and the other samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="dc739-114">下列各節說明如何設定任意的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="dc739-114">The following sections describe how to configure arbitrary stream types.</span></span>



| <span data-ttu-id="dc739-115">區段</span><span class="sxs-lookup"><span data-stu-id="dc739-115">Section</span></span>                                                                                                                                        | <span data-ttu-id="dc739-116">描述</span><span class="sxs-lookup"><span data-stu-id="dc739-116">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc739-117">設定腳本資料流程</span><span class="sxs-lookup"><span data-stu-id="dc739-117">Configuring Script Streams</span></span>](configuring-script-streams.md)                                                                                   | <span data-ttu-id="dc739-118">描述如何設定腳本資料流程。</span><span class="sxs-lookup"><span data-stu-id="dc739-118">Describes how to configure script streams.</span></span>                                                  |
| [<span data-ttu-id="dc739-119">設定檔案傳輸資料流程</span><span class="sxs-lookup"><span data-stu-id="dc739-119">Configuring File Transfer Streams</span></span>](configuring-file-transfer-streams.md)                                                                     | <span data-ttu-id="dc739-120">說明如何設定檔案傳輸串流。</span><span class="sxs-lookup"><span data-stu-id="dc739-120">Describes how to configure file transfer streams.</span></span>                                           |
| [<span data-ttu-id="dc739-121">設定 Web 資料流程</span><span class="sxs-lookup"><span data-stu-id="dc739-121">Configuring Web Streams</span></span>](configuring-web-streams.md)                                                                                         | <span data-ttu-id="dc739-122">描述如何設定 Web 資料流程。</span><span class="sxs-lookup"><span data-stu-id="dc739-122">Describes how to configure Web streams.</span></span>                                                     |
| [<span data-ttu-id="dc739-123">設定文字資料流程</span><span class="sxs-lookup"><span data-stu-id="dc739-123">Configuring Text Streams</span></span>](configuring-text-streams.md)                                                                                       | <span data-ttu-id="dc739-124">描述如何設定文字串流。</span><span class="sxs-lookup"><span data-stu-id="dc739-124">Describes how to configure text streams.</span></span>                                                    |
| [<span data-ttu-id="dc739-125">設定自訂任意資料流程</span><span class="sxs-lookup"><span data-stu-id="dc739-125">Configuring Custom Arbitrary Streams</span></span>](configuring-custom-arbitrary-streams.md)                                                               | <span data-ttu-id="dc739-126">描述如何設定自訂任意資料流程類型的資料流程。</span><span class="sxs-lookup"><span data-stu-id="dc739-126">Describes how to configure streams for custom arbitrary stream types.</span></span>                       |
| [<span data-ttu-id="dc739-127">計算任意資料流程的位元速率和緩衝區視窗值</span><span class="sxs-lookup"><span data-stu-id="dc739-127">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | <span data-ttu-id="dc739-128">描述如何計算任意資料流程的位元速率和緩衝區視窗設定。</span><span class="sxs-lookup"><span data-stu-id="dc739-128">Describes how to calculate the bit rate and buffer window settings for an arbitrary stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dc739-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc739-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc739-130">**任意資料流程**</span><span class="sxs-lookup"><span data-stu-id="dc739-130">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="dc739-131">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="dc739-131">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




