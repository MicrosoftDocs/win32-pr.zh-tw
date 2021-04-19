---
description: EVR 屬性
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: EVR 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508b036a7880c48e65d3c07a80ba5baaa5a52306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973596"
---
# <a name="evr-attributes"></a><span data-ttu-id="32737-103">EVR 屬性</span><span class="sxs-lookup"><span data-stu-id="32737-103">EVR Attributes</span></span>

<span data-ttu-id="32737-104">您可以使用下列屬性來設定增強型影片轉譯器 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="32737-104">The following attributes can be used to configure the Enhanced Video Renderer (EVR).</span></span>



| <span data-ttu-id="32737-105">屬性</span><span class="sxs-lookup"><span data-stu-id="32737-105">Attribute</span></span>                                                                                                         | <span data-ttu-id="32737-106">描述</span><span class="sxs-lookup"><span data-stu-id="32737-106">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32737-107">EVRConfig \_ AllowBatching</span><span class="sxs-lookup"><span data-stu-id="32737-107">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)                                                           | <span data-ttu-id="32737-108">允許 EVR 對 Microsoft Direct3D **IDirect3DDevice9：:P 重發** 的方法進行批次呼叫。</span><span class="sxs-lookup"><span data-stu-id="32737-108">Allows the EVR to batch calls to the Microsoft Direct3D **IDirect3DDevice9::Present** method.</span></span>                            |
| [<span data-ttu-id="32737-109">EVRConfig \_ AllowDropToBob</span><span class="sxs-lookup"><span data-stu-id="32737-109">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)                                                         | <span data-ttu-id="32737-110">允許 EVR 利用 bob 去交錯來改善效能。</span><span class="sxs-lookup"><span data-stu-id="32737-110">Allows the EVR to improve performance by using bob deinterlacing.</span></span>                                                        |
| [<span data-ttu-id="32737-111">EVRConfig \_ AllowDropToHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="32737-111">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)                                     | <span data-ttu-id="32737-112">允許 EVR 藉由略過每個交錯框架的第二個欄位來改善效能。</span><span class="sxs-lookup"><span data-stu-id="32737-112">Allows the EVR to improve performance by skipping the second field of every interlaced frame.</span></span>                            |
| [<span data-ttu-id="32737-113">EVRConfig \_ AllowDropToThrottle</span><span class="sxs-lookup"><span data-stu-id="32737-113">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)                                               | <span data-ttu-id="32737-114">允許 EVR 限制其輸出，以符合 GPU 頻寬。</span><span class="sxs-lookup"><span data-stu-id="32737-114">Allows the EVR to limit its output to match GPU bandwidth.</span></span>                                                               |
| [<span data-ttu-id="32737-115">EVRConfig \_ AllowScaling</span><span class="sxs-lookup"><span data-stu-id="32737-115">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)                                                             | <span data-ttu-id="32737-116">允許 EVR 在小於輸出矩形的矩形內混合影片，然後調整結果。</span><span class="sxs-lookup"><span data-stu-id="32737-116">Allows the EVR to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span> |
| [<span data-ttu-id="32737-117">EVRConfig \_ ForceBatching</span><span class="sxs-lookup"><span data-stu-id="32737-117">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)                                                           | <span data-ttu-id="32737-118">強制 EVR 對 **IDirect3D9Device：:P 重發** 的方法進行批次呼叫。</span><span class="sxs-lookup"><span data-stu-id="32737-118">Forces the EVR to batch calls to the **IDirect3D9Device::Present** method.</span></span>                                               |
| [<span data-ttu-id="32737-119">EVRConfig \_ ForceBob</span><span class="sxs-lookup"><span data-stu-id="32737-119">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)                                                                     | <span data-ttu-id="32737-120">強制 EVR 使用 bob 去交錯。</span><span class="sxs-lookup"><span data-stu-id="32737-120">Forces the EVR to use bob deinterlacing.</span></span>                                                                                 |
| [<span data-ttu-id="32737-121">EVRConfig \_ ForceHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="32737-121">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)                                                 | <span data-ttu-id="32737-122">強制 EVR 略過每個交錯框架的第二個欄位。</span><span class="sxs-lookup"><span data-stu-id="32737-122">Forces the EVR to skip the second field of every interlaced frame.</span></span>                                                       |
| [<span data-ttu-id="32737-123">EVRConfig \_ ForceScaling</span><span class="sxs-lookup"><span data-stu-id="32737-123">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)                                                             | <span data-ttu-id="32737-124">強制 EVR 在小於輸出矩形的矩形內混合影片，然後調整結果。</span><span class="sxs-lookup"><span data-stu-id="32737-124">Forces the EVR to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span> |
| [<span data-ttu-id="32737-125">EVRConfig \_ ForceThrottle</span><span class="sxs-lookup"><span data-stu-id="32737-125">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)                                                           | <span data-ttu-id="32737-126">強制 EVR 將其輸出限制為符合 GPU 頻寬。</span><span class="sxs-lookup"><span data-stu-id="32737-126">Forces the EVR to limit its output to match GPU bandwidth.</span></span>                                                               |
| [<span data-ttu-id="32737-127">**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="32737-127">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_ACTIVATE**</span></span>](mf-activate-custom-video-mixer-activate-attribute.md)         | <span data-ttu-id="32737-128">指定啟用物件，為增強型影片轉譯器 (EVR) 建立自訂的視頻混音器。</span><span class="sxs-lookup"><span data-stu-id="32737-128">Specifies an activation object that creates a custom video mixer for the enhanced video renderer (EVR).</span></span>                  |
| [<span data-ttu-id="32737-129">**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="32737-129">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**</span></span>](mf-activate-custom-video-mixer-clsid-attribute.md)               | <span data-ttu-id="32737-130">EVR 之自訂視頻混音器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="32737-130">CLSID of a custom video mixer for the EVR.</span></span>                                                                               |
| [<span data-ttu-id="32737-131">**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="32737-131">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_FLAGS**</span></span>](mf-activate-custom-video-mixer-flags-attribute.md)               | <span data-ttu-id="32737-132">指定如何為 EVR 建立自訂混音器。</span><span class="sxs-lookup"><span data-stu-id="32737-132">Specifies how to create a custom mixer for the EVR.</span></span>                                                                      |
| [<span data-ttu-id="32737-133">**MF \_ 啟用 \_ 自訂 \_ 影片 \_ 演講者 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="32737-133">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="32737-134">指定啟用物件，以建立 EVR 的自訂影片展示者。</span><span class="sxs-lookup"><span data-stu-id="32737-134">Specifies an activation object that creates a custom video presenter for the EVR.</span></span>                                        |
| [<span data-ttu-id="32737-135">**MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="32737-135">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="32737-136">EVR 之自訂影片展示者的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="32737-136">CLSID of a custom video presenter for the EVR.</span></span>                                                                           |
| [<span data-ttu-id="32737-137">**MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="32737-137">**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS**</span></span>](mf-activate-custom-video-presenter-flags-attribute.md)       | <span data-ttu-id="32737-138">指定如何建立 EVR 的自訂展示者。</span><span class="sxs-lookup"><span data-stu-id="32737-138">Specifies how to create a custom presenter for the EVR.</span></span>                                                                  |
| [<span data-ttu-id="32737-139">**MF \_ 啟用 \_ 影片 \_ 視窗**</span><span class="sxs-lookup"><span data-stu-id="32737-139">**MF\_ACTIVATE\_VIDEO\_WINDOW**</span></span>](mf-activate-video-window-attribute.md)                                         | <span data-ttu-id="32737-140">影片裁剪視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="32737-140">Handle to the video clipping window.</span></span>                                                                                     |
| [<span data-ttu-id="32737-141">**MF \_ SA \_ 需求 \_ 範例 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="32737-141">**MF\_SA\_REQUIRED\_SAMPLE\_COUNT**</span></span>](mf-sa-required-sample-count-attribute.md)                                  | <span data-ttu-id="32737-142">指出 EVR 媒體接收器需要去交錯的未壓縮緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="32737-142">Indicates the number of uncompressed buffers that the EVR media sink requires for deinterlacing.</span></span>                         |
| [<span data-ttu-id="32737-143">**影片 \_ 縮放 \_ 矩形**</span><span class="sxs-lookup"><span data-stu-id="32737-143">**VIDEO\_ZOOM\_RECT**</span></span>](video-zoom-rect-attribute.md)                                                            | <span data-ttu-id="32737-144">指定 EVR 混音器的縮放矩形。</span><span class="sxs-lookup"><span data-stu-id="32737-144">Specifies the zoom rectangle for the EVR mixer.</span></span>                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="32737-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="32737-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32737-146">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="32737-146">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="32737-147">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="32737-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



