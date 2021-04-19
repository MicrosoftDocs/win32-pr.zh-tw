---
description: IAMTimelineEffectable 介面會提供方法，將效果新增至 DirectShow 編輯服務 (DES) 中的時間軸物件，以及操作物件的效果。
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: 'IAMTimelineEffectable 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990629"
---
# <a name="iamtimelineeffectable-interface"></a><span data-ttu-id="7ad7c-103">IAMTimelineEffectable 介面</span><span class="sxs-lookup"><span data-stu-id="7ad7c-103">IAMTimelineEffectable interface</span></span>

> [!Note]  
> <span data-ttu-id="7ad7c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-104">\[Deprecated.</span></span> <span data-ttu-id="7ad7c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7ad7c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ad7c-106">`IAMTimelineEffectable`介面會提供方法，將效果新增至[DirectShow 編輯服務](directshow-editing-services.md) (DES) 的時間軸物件，以及操作物件的效果。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-106">The `IAMTimelineEffectable` interface provides methods for adding effects to a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES), and for manipulating the effects on an object.</span></span> <span data-ttu-id="7ad7c-107">所有可能套用效果的物件都會執行此介面;這包括來源、追蹤和組合。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-107">All objects that can have effects applied to them implement this interface; this includes sources, tracks, and compositions.</span></span>

<span data-ttu-id="7ad7c-108">執行這個介面的物件可以有任意數目的效果。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-108">An object that implements this interface can have any number of effects.</span></span> <span data-ttu-id="7ad7c-109">針對每個物件，轉譯引擎會依優先權順序套用其效果，從優先權層級0開始。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-109">For each object, the render engine applies its effects in order of priority, starting with priority level 0.</span></span>

## <a name="members"></a><span data-ttu-id="7ad7c-110">成員</span><span class="sxs-lookup"><span data-stu-id="7ad7c-110">Members</span></span>

<span data-ttu-id="7ad7c-111">**IAMTimelineEffectable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-111">The **IAMTimelineEffectable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7ad7c-112">**IAMTimelineEffectable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7ad7c-112">**IAMTimelineEffectable** also has these types of members:</span></span>

-   [<span data-ttu-id="7ad7c-113">方法</span><span class="sxs-lookup"><span data-stu-id="7ad7c-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ad7c-114">方法</span><span class="sxs-lookup"><span data-stu-id="7ad7c-114">Methods</span></span>

<span data-ttu-id="7ad7c-115">**IAMTimelineEffectable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-115">The **IAMTimelineEffectable** interface has these methods.</span></span>



| <span data-ttu-id="7ad7c-116">方法</span><span class="sxs-lookup"><span data-stu-id="7ad7c-116">Method</span></span>                                                                     | <span data-ttu-id="7ad7c-117">描述</span><span class="sxs-lookup"><span data-stu-id="7ad7c-117">Description</span></span>                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="7ad7c-118">**EffectGetCount**</span><span class="sxs-lookup"><span data-stu-id="7ad7c-118">**EffectGetCount**</span></span>](iamtimelineeffectable-effectgetcount.md)             | <span data-ttu-id="7ad7c-119">捕獲此物件的效果數目。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-119">Retrieves the number of effects on this object.</span></span><br/>                    |
| [<span data-ttu-id="7ad7c-120">**EffectInsBefore**</span><span class="sxs-lookup"><span data-stu-id="7ad7c-120">**EffectInsBefore**</span></span>](iamtimelineeffectable-effectinsbefore.md)           | <span data-ttu-id="7ad7c-121">將效果插入物件中指定的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-121">Inserts an effect into the object at the specified priority level.</span></span><br/> |
| [<span data-ttu-id="7ad7c-122">**EffectSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="7ad7c-122">**EffectSwapPriorities**</span></span>](iamtimelineeffectable-effectswappriorities.md) | <span data-ttu-id="7ad7c-123">切換兩個效果的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-123">Switches the priority levels of two effects.</span></span><br/>                       |
| [<span data-ttu-id="7ad7c-124">**GetEffect**</span><span class="sxs-lookup"><span data-stu-id="7ad7c-124">**GetEffect**</span></span>](iamtimelineeffectable-geteffect.md)                       | <span data-ttu-id="7ad7c-125">抓取指定優先權層級的效果。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-125">Retrieves the effect at the specified priority level.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="7ad7c-126">備註</span><span class="sxs-lookup"><span data-stu-id="7ad7c-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ad7c-127">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ad7c-128">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ad7c-129">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="7ad7c-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ad7c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ad7c-130">Requirements</span></span>



| <span data-ttu-id="7ad7c-131">需求</span><span class="sxs-lookup"><span data-stu-id="7ad7c-131">Requirement</span></span> | <span data-ttu-id="7ad7c-132">值</span><span class="sxs-lookup"><span data-stu-id="7ad7c-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad7c-133">標頭</span><span class="sxs-lookup"><span data-stu-id="7ad7c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="7ad7c-134"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad7c-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ad7c-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ad7c-135">Library</span></span><br/> | <dl> <span data-ttu-id="7ad7c-136"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ad7c-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
