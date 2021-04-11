---
description: 子
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: 子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850967"
---
# <a name="subobjects"></a><span data-ttu-id="6fcc4-103">子</span><span class="sxs-lookup"><span data-stu-id="6fcc4-103">Subobjects</span></span>

<span data-ttu-id="6fcc4-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6fcc4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6fcc4-105">來源、效果和轉換都有指向其他 COM *物件的內部指標，稱為子* 物件。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-105">Sources, effects, and transitions have internal pointers to other COM objects, called *subobjects*.</span></span> <span data-ttu-id="6fcc4-106">子物件會執行物件的實際工作。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-106">The subobject performs the actual work of the object.</span></span> <span data-ttu-id="6fcc4-107">來源的子物件是建立影片或音訊資料的元件。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-107">The subobject of a source is the component that creates the video or audio data.</span></span> <span data-ttu-id="6fcc4-108">效果或轉換的子物件是轉換資料的元件;例如，在影片效果中，它會在影片串流中建立視覺效果。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-108">The subobject of an effect or transition is the component that transforms the data; for example, in a video effect, it creates the visual effect in the video stream.</span></span>

<span data-ttu-id="6fcc4-109">子物件的類型取決於物件的類型：</span><span class="sxs-lookup"><span data-stu-id="6fcc4-109">The type of subobject depends on the type of object:</span></span>

-   <span data-ttu-id="6fcc4-110">來源：任何 DirectShow 來源篩選器或剖析器篩選器，支援搜尋並產生 DES 支援的格式。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-110">Source: Any DirectShow source filter or parser filter that supports seeking and produces a format that DES supports.</span></span> <span data-ttu-id="6fcc4-111">如果有 DirectShow 篩選器可將它解碼，則它可以是壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-111">It can be a compressed format if DirectShow filters exist to decode it.</span></span>
-   <span data-ttu-id="6fcc4-112">效果：適用于影片、任何2D 單一輸入 Microsoft® DirectX®轉換物件。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-112">Effect: For video, any 2-D one-input Microsoft® DirectX® Transform object.</span></span> <span data-ttu-id="6fcc4-113">適用于音訊、任何 DirectShow 音訊效果篩選。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-113">For audio, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="6fcc4-114">轉換：適用于影片、任何雙 D 雙輸入 DirectX 轉換物件。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-114">Transition: For video, any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="6fcc4-115">音訊不支援轉換。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-115">Audio does not support transitions.</span></span>

<span data-ttu-id="6fcc4-116">群組、組合和追蹤沒有子群組。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-116">Groups, compositions, and tracks do not have subobjects.</span></span>

<span data-ttu-id="6fcc4-117">應用程式不會直接設定子物件指標。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-117">The application does not directly set the subobject pointer.</span></span> <span data-ttu-id="6fcc4-118">針對效果和轉換，應用程式會呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法來指定子物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-118">For effects and transitions, the application calls the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method to specify the GUID of the subobject.</span></span> <span data-ttu-id="6fcc4-119">針對來源物件，應用程式通常會呼叫 [**IAMTimelineSrc：： SetMediaName**](iamtimelinesrc-setmedianame.md) 來指定原始程式檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-119">For source objects, an application typically calls the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) to specify the name of a source file.</span></span> <span data-ttu-id="6fcc4-120">但是， **SetSubObjectGUID** 方法也可以用於來源物件，以指定篩選 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-120">However, the **SetSubObjectGUID** method can also be used for source objects, to specify the class identifier (CLSID) of a filter.</span></span>

<span data-ttu-id="6fcc4-121">如需詳細資訊，請參閱使用 [來源](working-with-sources.md) 及 [處理效果和轉換](working-with-effects-and-transitions.md)。</span><span class="sxs-lookup"><span data-stu-id="6fcc4-121">For more information, see [Working with Sources](working-with-sources.md) and [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fcc4-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fcc4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fcc4-123">時間軸元件的總覽</span><span class="sxs-lookup"><span data-stu-id="6fcc4-123">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



