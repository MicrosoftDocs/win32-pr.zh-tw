---
description: 提供自訂的影片調整
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: 提供自訂的影片調整
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108905"
---
# <a name="providing-a-custom-video-resizer"></a><span data-ttu-id="2e7dd-103">提供自訂的影片調整</span><span class="sxs-lookup"><span data-stu-id="2e7dd-103">Providing a Custom Video Resizer</span></span>

<span data-ttu-id="2e7dd-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2e7dd-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

> [!Note]  
> <span data-ttu-id="2e7dd-105">這項功能需要 DirectX 9.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-105">This feature requires DirectX 9.0 or later.</span></span>

 

<span data-ttu-id="2e7dd-106">當 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 調整大小的影片來源剪輯時，預設行為是 *StretchBlt*，這是快速但不是消除鋸齒的。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-106">When [DirectShow Editing Services](directshow-editing-services.md) (DES) resizes a video source clip, the default behavior is a *StretchBlt*, which is fast but not anti-aliased.</span></span> <span data-ttu-id="2e7dd-107">您可以藉由將自訂的調整器實作為 DirectShow 轉換篩選，來變更調整大小行為。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-107">You can change the resizing behavior by implementing a custom resizer as a DirectShow transform filter.</span></span> <span data-ttu-id="2e7dd-108">篩選器必須公開 [**IResize**](iresize.md) 介面，這可讓 DES 指定輸入和輸出影片大小。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-108">The filter must expose the [**IResize**](iresize.md) interface, which enables DES to specify the input and output video size.</span></span> <span data-ttu-id="2e7dd-109">如需撰寫轉換篩選的相關資訊，請參閱 [寫入轉換](writing-transform-filters.md)篩選。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-109">For information about writing a transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span> <span data-ttu-id="2e7dd-110">建議使用 **CTransformFilter** 基類做為起始點。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-110">The **CTransformFilter** base class is recommended as the starting point.</span></span> <span data-ttu-id="2e7dd-111">當您執行篩選準則時，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="2e7dd-111">When you implement the filter, note the following:</span></span>

-   <span data-ttu-id="2e7dd-112">支援篩選 (的 **IResize** 介面，而不是) 的釘選。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-112">Support the **IResize** interface on the filter (not the pins).</span></span>
-   <span data-ttu-id="2e7dd-113">篩選器只應接受 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式 (格式 \_ VideoInfo) 。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-113">The filter should accept only [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) formats (FORMAT\_VideoInfo).</span></span> <span data-ttu-id="2e7dd-114">拒絕其他格式類型。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-114">Reject other format types.</span></span>
-   <span data-ttu-id="2e7dd-115">DES 的影片格式可能是任何未壓縮的 RGB 類型，包括32位 RGB 與 Alpha (MEDIASUBTYPE \_ ARGB32) 。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-115">The video format from DES may be any uncompressed RGB type, including 32-bit RGB with alpha (MEDIASUBTYPE\_ARGB32).</span></span> <span data-ttu-id="2e7dd-116">您的篩選可以安全地拒絕 **biHeight** < 0 的格式。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-116">Your filter can safely reject formats with **biHeight** < 0.</span></span>
-   <span data-ttu-id="2e7dd-117">在轉譯引擎連接篩選器的輸出圖釘之前，它會呼叫 [**IResize：:p \_**](iresize-put-mediatype.md) 的 ui 媒體設定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-117">Before the Render Engine connects the filter's output pin, it calls [**IResize::put\_MediaType**](iresize-put-mediatype.md) to set the output type.</span></span> <span data-ttu-id="2e7dd-118">它也可能會呼叫 [**IResize：:p 的工作 \_ 空間大小**](iresize-put-size.md) 來調整輸出大小。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-118">It may also call [**IResize::put\_Size**](iresize-put-size.md) to adjust the output size.</span></span> <span data-ttu-id="2e7dd-119">它可以在連接輸出釘選之前，以任何順序呼叫這兩個方法，不限次數。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-119">It can call these two methods in any order, any number of times, before it connects the output pin.</span></span>
-   <span data-ttu-id="2e7dd-120">轉譯引擎連接輸出釘選之後，可能會再次呼叫 **put \_ 大小** 。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-120">After the Render Engine connects the output pin, it might call **put\_Size** again.</span></span> <span data-ttu-id="2e7dd-121">調整器篩選器應該以新的大小重新連接其輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-121">The resizer filter should reconnect its output pin with the new size.</span></span>
-   <span data-ttu-id="2e7dd-122">在篩選的 [**CTransformFilter：： Transform**](ctransformfilter-transform.md) 方法內，將輸入影片延展至輸出大小。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-122">Inside the filter's [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, stretch the input video to the output size.</span></span>
-   <span data-ttu-id="2e7dd-123">您的篩選準則絕對不應該在輸出範例上設定不連續旗標，或將媒體類型附加至輸出範例。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-123">Your filter should never set the discontinuity flag on the output sample, or attach a media type to the output sample.</span></span>
-   <span data-ttu-id="2e7dd-124">若要將篩選的狀態儲存在 GraphEdit (. grf) 檔中，請執行 **IPersistStream** 介面。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-124">To save the filter's state in a GraphEdit (.grf) file, implement the **IPersistStream** interface.</span></span> <span data-ttu-id="2e7dd-125"> (這是選擇性的，但對測試而言很有用。 ) </span><span class="sxs-lookup"><span data-stu-id="2e7dd-125">(This is optional, but useful for testing.)</span></span>

<span data-ttu-id="2e7dd-126">若要使用 [調整] 篩選準則，您必須在使用者的系統上將篩選註冊為 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-126">To use the resizer filter, the filter must be registered as a COM object on the user's system.</span></span> <span data-ttu-id="2e7dd-127">在應用程式呈現影片專案之前，請查詢 [**IRenderEngine2**](irenderengine2.md) 介面的轉譯引擎，並以調整器篩選的 CLSID 呼叫 [**IRenderEngine2：： SetResizerGUID**](irenderengine2-setresizerguid.md) 。</span><span class="sxs-lookup"><span data-stu-id="2e7dd-127">Before the application renders the video project, query the Render Engine for the [**IRenderEngine2**](irenderengine2.md) interface and call [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) with the CLSID of the resizer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e7dd-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e7dd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e7dd-129">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="2e7dd-129">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



