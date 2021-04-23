---
description: 框架逐步執行屬性集
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: 框架逐步執行屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908446"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="65192-103">框架逐步執行屬性集</span><span class="sxs-lookup"><span data-stu-id="65192-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="65192-104">在 Microsoft DirectShow 下執行框架精確搜尋的解碼器必須實作為 \_ KSPROPSETID \_ FrameStep 屬性集，以搭配 [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) 介面使用。</span><span class="sxs-lookup"><span data-stu-id="65192-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



| <span data-ttu-id="65192-105">標籤</span><span class="sxs-lookup"><span data-stu-id="65192-105">Label</span></span> | <span data-ttu-id="65192-106">值</span><span class="sxs-lookup"><span data-stu-id="65192-106">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="65192-107">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="65192-107">Property Set GUID</span></span> | <span data-ttu-id="65192-108">AM \_ KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="65192-108">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="65192-109">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="65192-109">Property ID</span></span>                              | <span data-ttu-id="65192-110">描述</span><span class="sxs-lookup"><span data-stu-id="65192-110">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65192-111">AM \_ 屬性 \_ FRAMESTEP \_ 步驟</span><span class="sxs-lookup"><span data-stu-id="65192-111">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="65192-112">指示解碼器開始步驟作業，並傳遞指定步驟數目的 [**AM \_ 屬性 \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) 結構。</span><span class="sxs-lookup"><span data-stu-id="65192-112">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="65192-113">AM \_ 屬性 \_ FRAMESTEP \_ 取消</span><span class="sxs-lookup"><span data-stu-id="65192-113">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="65192-114">指示解碼器取消目前的步驟作業。</span><span class="sxs-lookup"><span data-stu-id="65192-114">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="65192-115">沒有任何實例資料與這個屬性相關聯。</span><span class="sxs-lookup"><span data-stu-id="65192-115">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="65192-116">AM \_ 屬性 \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="65192-116">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="65192-117">\_此指令程式會在此指令上傳回 S OK，表示它可以執行框架逐步執行， \_ 否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="65192-117">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="65192-118">設定這個屬性時，不會傳遞任何實例資料。</span><span class="sxs-lookup"><span data-stu-id="65192-118">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="65192-119">AM \_ 屬性 \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="65192-119">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="65192-120">\_此指令程式會在此指示上傳回 S OK，表示它可以一次執行多個框架， \_ 否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="65192-120">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="65192-121">設定這個屬性時，不會傳遞任何實例資料。</span><span class="sxs-lookup"><span data-stu-id="65192-121">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="65192-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="65192-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65192-123">屬性集</span><span class="sxs-lookup"><span data-stu-id="65192-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



