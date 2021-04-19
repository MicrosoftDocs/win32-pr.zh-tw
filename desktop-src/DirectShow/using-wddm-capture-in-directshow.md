---
description: 在 DirectShow 中使用 WDDM Capture
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: 在 DirectShow 中使用 WDDM Capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992059"
---
# <a name="using-wddm-capture-in-directshow"></a><span data-ttu-id="bf7f4-103">在 DirectShow 中使用 WDDM Capture</span><span class="sxs-lookup"><span data-stu-id="bf7f4-103">Using WDDM Capture in DirectShow</span></span>

<span data-ttu-id="bf7f4-104">本主題適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-104">This topic applies to Windows Vista and later.</span></span>

<span data-ttu-id="bf7f4-105">有些視訊卡有整合的影片捕捉功能。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-105">Some video cards have integrated video capture functionality.</span></span> <span data-ttu-id="bf7f4-106">在這些卡片上，已捕捉的影片畫面會放在視訊記憶體中 (VRAM) 。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-106">On these cards, captured video frames are placed in video memory (VRAM).</span></span> <span data-ttu-id="bf7f4-107">在 Windows Vista 之前，沒有標準的機制可處理畫面格保持在 VRAM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-107">Prior to Windows Vista, there was no standard mechanism for processing the frames while they remained in VRAM.</span></span> <span data-ttu-id="bf7f4-108">相反地，必須將資料複製到系統記憶體中，然後再將資料複製回 VRAM 以供顯示。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-108">Instead, the data had to be copied into system memory, processed, and then copied back to VRAM for display.</span></span> <span data-ttu-id="bf7f4-109">在 Windows Vista 中，DirectShow 現在支援一種機制，可讓整個處理管線的影片畫面保持 VRAM，從 capture 到顯示。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-109">In Windows Vista, DirectShow now supports a mechanism for keeping the video frames in VRAM throughout the processing pipeline, from capture to display.</span></span>

<span data-ttu-id="bf7f4-110">KsProxy 篩選器會藉由查詢 KSPROPERTY \_ 慣用 \_ 捕獲介面屬性的驅動程式，來判斷驅動程式是否支援 VRAM 介面捕捉 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-110">The KsProxy filter determines if the driver supports VRAM surface capture by querying the driver for the KSPROPERTY\_PREFERRED\_CAPTURE\_SURFACE property.</span></span> <span data-ttu-id="bf7f4-111"> (此屬性記載于 Windows 驅動程式套件檔中。 ) 如果驅動程式支援 VRAM surface capture，KsProxy 會配置一種特殊類型的媒體範例，其中包含 Direct3D 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-111">(This property is documented in the Windows Driver Kit documentation.) If the driver supports VRAM surface capture, KsProxy allocates a special kind of media sample that holds a pointer to a Direct3D surface.</span></span>

<span data-ttu-id="bf7f4-112">接下來，KsProxy 會判斷下游篩選器是否支援 DirectX Video 加速 (DXVA) 2.0，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf7f4-112">Next, KsProxy determines whether the downstream filter supports DirectX Video Acceleration (DXVA) 2.0, as follows:</span></span>

1.  <span data-ttu-id="bf7f4-113">KsProxy 會查詢 **IMFGetService** 介面的下游輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-113">KsProxy queries the downstream input pin for the **IMFGetService** interface.</span></span>
2.  <span data-ttu-id="bf7f4-114">如果釘選公開 **IMFGetService**，KsProxy 會針對 **IDirect3DDeviceManager** 介面呼叫 **IMFGetService：： GetService** 。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-114">If the pin exposes **IMFGetService**, KsProxy calls **IMFGetService::GetService** for the **IDirect3DDeviceManager** interface.</span></span> <span data-ttu-id="bf7f4-115">服務 identier 是 MR \_ VIDEO \_ 加速 \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-115">The service identier is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="bf7f4-116">這兩個介面都記載于媒體基礎 SDK 檔集內。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-116">Both of these interfaces are documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="bf7f4-117">如果下游篩選器不支援 DXVA 2.0，則 KsProxy 會配置額外的系統記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-117">If the downstream filter does not support DXVA 2.0, KsProxy allocates an additional system memory buffer.</span></span> <span data-ttu-id="bf7f4-118">它會使用此緩衝區將影片畫面從 VRAM 複製到系統記憶體。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-118">It uses this buffer to copy the video frames from VRAM to system memory.</span></span> <span data-ttu-id="bf7f4-119">Media 範例的 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 方法會傳回這個系統記憶體緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-119">The media sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to this system memory buffer.</span></span>

<span data-ttu-id="bf7f4-120">但是，如果下游篩選器支援 DXVA 2.0，則 KsProxy 不會配置系統記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-120">However, if the downstream filter does support DXVA 2.0, then KsProxy does not allocate a system memory buffer.</span></span> <span data-ttu-id="bf7f4-121">在此情況下， **GetPointer** 方法會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-121">In that case, the **GetPointer** method returns E\_NOTIMPL.</span></span> <span data-ttu-id="bf7f4-122">相反地，下游篩選器應該會直接存取範例的 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-122">Instead, the downstream filter is expected to access the sample's Direct3D surface directly.</span></span> <span data-ttu-id="bf7f4-123">下游篩選器有兩種方式可取得介面的指標，兩者都是相等的：</span><span class="sxs-lookup"><span data-stu-id="bf7f4-123">There are two ways for the downstream filter to get a pointer to the surface, both of them equivalent:</span></span>

-   <span data-ttu-id="bf7f4-124">查詢 **IMFGetService** 介面的範例，並針對 **IDirect3DSurface9** 介面呼叫 **GetService** 。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-124">Query the sample for the **IMFGetService** interface and call **GetService** for the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="bf7f4-125">服務識別碼是 MR \_ 緩衝區 \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-125">The service identifier is MR\_BUFFER\_SERVICE.</span></span>
-   <span data-ttu-id="bf7f4-126">查詢 [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) 介面的範例，然後呼叫 [**IMediaSample2Config：： GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface)。</span><span class="sxs-lookup"><span data-stu-id="bf7f4-126">Query the sample for the [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) interface and call [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf7f4-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf7f4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf7f4-128">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="bf7f4-128">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



