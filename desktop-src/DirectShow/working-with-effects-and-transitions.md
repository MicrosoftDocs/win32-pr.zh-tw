---
description: 使用效果和轉換
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: 使用效果和轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945432"
---
# <a name="working-with-effects-and-transitions"></a><span data-ttu-id="e39e5-103">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="e39e5-103">Working with Effects and Transitions</span></span>

<span data-ttu-id="e39e5-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e39e5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e39e5-105">效果會修改單一剪輯、追蹤或組合。</span><span class="sxs-lookup"><span data-stu-id="e39e5-105">Effects modify a single clip, track, or composition.</span></span> <span data-ttu-id="e39e5-106">轉換會從一個曲目建立 seques，或 compositionsto 另一個。</span><span class="sxs-lookup"><span data-stu-id="e39e5-106">Transitions create seques from one track or compositionsto another.</span></span>

<span data-ttu-id="e39e5-107">[DirectShow 編輯服務](directshow-editing-services.md) 會使用 DirectX 轉換物件來進行影片轉換和影片效果。</span><span class="sxs-lookup"><span data-stu-id="e39e5-107">[DirectShow Editing Services](directshow-editing-services.md) uses DirectX Transform objects for its video transitions and video effects.</span></span> <span data-ttu-id="e39e5-108">針對影片轉換，請使用任何2D 雙輸入 DirectX 轉換物件。</span><span class="sxs-lookup"><span data-stu-id="e39e5-108">For video transitions, use any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="e39e5-109">針對影片效果，請使用任何2-d 的單一輸入 DirectX 轉換物件。</span><span class="sxs-lookup"><span data-stu-id="e39e5-109">For video effects, use any 2-D one-input DirectX Transform object.</span></span> <span data-ttu-id="e39e5-110">Microsoft 不再支援協力廠商 DirectX 轉換物件的開發。</span><span class="sxs-lookup"><span data-stu-id="e39e5-110">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="e39e5-111">但是，有數個會隨 DirectShow 提供，有些則是由 Microsoft Internet Explorer 提供。</span><span class="sxs-lookup"><span data-stu-id="e39e5-111">However, several are provided with DirectShow and others are provided with Microsoft Internet Explorer.</span></span> <span data-ttu-id="e39e5-112">如需 Internet Explorer 所提供之轉換的詳細資訊，請參閱 [視覺化篩選和轉換參考](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e39e5-112">For more information about the transitions provided with Internet Explorer, see [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span></span>

<span data-ttu-id="e39e5-113">針對音訊效果，您可以使用任何 DirectShow 音訊效果篩選。</span><span class="sxs-lookup"><span data-stu-id="e39e5-113">For audio effects, you can use any DirectShow audio effect filter.</span></span> <span data-ttu-id="e39e5-114">DES 也會提供 [音量信封效果](volume-envelope-effect.md) ，以在播放軌或剪輯上設定音量。</span><span class="sxs-lookup"><span data-stu-id="e39e5-114">DES also provides a [Volume Envelope Effect](volume-envelope-effect.md) for setting the volume on a track or clip.</span></span> <span data-ttu-id="e39e5-115">DES 不支援音訊轉換。</span><span class="sxs-lookup"><span data-stu-id="e39e5-115">DES does not support audio transitions.</span></span>

<span data-ttu-id="e39e5-116">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="e39e5-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e39e5-117">新增效果和轉換物件</span><span class="sxs-lookup"><span data-stu-id="e39e5-117">Adding Effect and Transition Objects</span></span>](adding-effect-and-transition-objects.md)
-   [<span data-ttu-id="e39e5-118">預覽效果和轉換</span><span class="sxs-lookup"><span data-stu-id="e39e5-118">Previewing Effects and Transitions</span></span>](previewing-effects-and-transitions.md)
-   [<span data-ttu-id="e39e5-119">列舉效果和轉換</span><span class="sxs-lookup"><span data-stu-id="e39e5-119">Enumerating Effects and Transitions</span></span>](enumerating-effects-and-transitions.md)
-   [<span data-ttu-id="e39e5-120">設定效果和轉換的屬性</span><span class="sxs-lookup"><span data-stu-id="e39e5-120">Setting Properties on Effects and Transitions</span></span>](setting-properties-on-effects-and-transitions.md)
-   [<span data-ttu-id="e39e5-121">轉換方向</span><span class="sxs-lookup"><span data-stu-id="e39e5-121">Transition Direction</span></span>](transition-direction.md)

## <a name="related-topics"></a><span data-ttu-id="e39e5-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e39e5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e39e5-123">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="e39e5-123">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
