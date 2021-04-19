---
description: CreateEmptyNode 方法會建立新的時間軸物件。
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'IAMTimeline：： CreateEmptyNode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993303"
---
# <a name="iamtimelinecreateemptynode-method"></a><span data-ttu-id="fe00f-103">IAMTimeline：： CreateEmptyNode 方法</span><span class="sxs-lookup"><span data-stu-id="fe00f-103">IAMTimeline::CreateEmptyNode method</span></span>

> [!Note]  
> <span data-ttu-id="fe00f-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fe00f-104">\[Deprecated.</span></span> <span data-ttu-id="fe00f-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fe00f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe00f-106">`CreateEmptyNode`方法會建立新的時間軸物件。</span><span class="sxs-lookup"><span data-stu-id="fe00f-106">The `CreateEmptyNode` method creates a new timeline object.</span></span>

<span data-ttu-id="fe00f-107">您可以使用這個方法來建立時間軸物件，而不是 **CoCreateInstance** 函式，因為此方法會執行重要的初始化常式。</span><span class="sxs-lookup"><span data-stu-id="fe00f-107">Use this method to create timeline objects, rather than the **CoCreateInstance** function, because this method performs important initialization routines.</span></span> <span data-ttu-id="fe00f-108">這個方法所建立的每個物件至少都支援 [**IAMTimelineObj**](iamtimelineobj.md) 介面，以及該物件類型特定的其他介面。</span><span class="sxs-lookup"><span data-stu-id="fe00f-108">Every object created by this method supports at least the [**IAMTimelineObj**](iamtimelineobj.md) interface, along with other interfaces specific to that type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe00f-109">語法</span><span class="sxs-lookup"><span data-stu-id="fe00f-109">Syntax</span></span>


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="fe00f-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe00f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe00f-111">*ppObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe00f-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe00f-112">接收新物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fe00f-112">Receives a pointer to the new object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="fe00f-113">*型別*</span><span class="sxs-lookup"><span data-stu-id="fe00f-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="fe00f-114">[**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md)列舉類型的成員，指定要建立之物件的類型。</span><span class="sxs-lookup"><span data-stu-id="fe00f-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe00f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe00f-115">Return value</span></span>

<span data-ttu-id="fe00f-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fe00f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe00f-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe00f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe00f-118">備註</span><span class="sxs-lookup"><span data-stu-id="fe00f-118">Remarks</span></span>

<span data-ttu-id="fe00f-119">請勿將新的物件加入至另一個時間軸實例。</span><span class="sxs-lookup"><span data-stu-id="fe00f-119">Do not add the new object to another timeline instance.</span></span> <span data-ttu-id="fe00f-120">時間軸中的每個物件都必須由該時間軸建立。</span><span class="sxs-lookup"><span data-stu-id="fe00f-120">Every object in a timeline must be created by that timeline.</span></span>

<span data-ttu-id="fe00f-121">如果方法成功，則傳回的 [**IAMTimelineObj**](iamtimelineobj.md) 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="fe00f-121">If the method succeeds, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="fe00f-122">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="fe00f-122">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="fe00f-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fe00f-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe00f-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fe00f-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fe00f-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fe00f-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe00f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe00f-126">Requirements</span></span>



| <span data-ttu-id="fe00f-127">需求</span><span class="sxs-lookup"><span data-stu-id="fe00f-127">Requirement</span></span> | <span data-ttu-id="fe00f-128">值</span><span class="sxs-lookup"><span data-stu-id="fe00f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe00f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="fe00f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fe00f-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe00f-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fe00f-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe00f-131">Library</span></span><br/> | <dl> <span data-ttu-id="fe00f-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe00f-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe00f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe00f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe00f-134">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="fe00f-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="fe00f-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="fe00f-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




