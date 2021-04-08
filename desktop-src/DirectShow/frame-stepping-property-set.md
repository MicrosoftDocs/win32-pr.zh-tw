---
description: 框架逐步執行屬性集
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: 框架逐步執行屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687996"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="e471d-103">框架逐步執行屬性集</span><span class="sxs-lookup"><span data-stu-id="e471d-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="e471d-104">在 Microsoft DirectShow 下執行框架精確搜尋的解碼器必須實作為 \_ KSPROPSETID \_ FrameStep 屬性集，以搭配 [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) 介面使用。</span><span class="sxs-lookup"><span data-stu-id="e471d-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="e471d-105">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="e471d-105">Property Set GUID</span></span> | <span data-ttu-id="e471d-106">AM \_ KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="e471d-106">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="e471d-107">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="e471d-107">Property ID</span></span>                              | <span data-ttu-id="e471d-108">描述</span><span class="sxs-lookup"><span data-stu-id="e471d-108">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e471d-109">AM \_ 屬性 \_ FRAMESTEP \_ 步驟</span><span class="sxs-lookup"><span data-stu-id="e471d-109">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="e471d-110">指示解碼器開始步驟作業，並傳遞指定步驟數目的 [**AM \_ 屬性 \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) 結構。</span><span class="sxs-lookup"><span data-stu-id="e471d-110">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="e471d-111">AM \_ 屬性 \_ FRAMESTEP \_ 取消</span><span class="sxs-lookup"><span data-stu-id="e471d-111">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="e471d-112">指示解碼器取消目前的步驟作業。</span><span class="sxs-lookup"><span data-stu-id="e471d-112">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="e471d-113">沒有任何實例資料與這個屬性相關聯。</span><span class="sxs-lookup"><span data-stu-id="e471d-113">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="e471d-114">AM \_ 屬性 \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="e471d-114">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="e471d-115">\_此指令程式會在此指令上傳回 S OK，表示它可以執行框架逐步執行， \_ 否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="e471d-115">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="e471d-116">設定這個屬性時，不會傳遞任何實例資料。</span><span class="sxs-lookup"><span data-stu-id="e471d-116">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="e471d-117">AM \_ 屬性 \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="e471d-117">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="e471d-118">\_此指令程式會在此指示上傳回 S OK，表示它可以一次執行多個框架， \_ 否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="e471d-118">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="e471d-119">設定這個屬性時，不會傳遞任何實例資料。</span><span class="sxs-lookup"><span data-stu-id="e471d-119">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e471d-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="e471d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e471d-121">屬性集</span><span class="sxs-lookup"><span data-stu-id="e471d-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



