---
description: EffectInsBefore 方法會將效果插入物件中指定的優先權層級。
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'IAMTimelineEffectable：： EffectInsBefore 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996105"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a><span data-ttu-id="fe02a-103">IAMTimelineEffectable：： EffectInsBefore 方法</span><span class="sxs-lookup"><span data-stu-id="fe02a-103">IAMTimelineEffectable::EffectInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="fe02a-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fe02a-104">\[Deprecated.</span></span> <span data-ttu-id="fe02a-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fe02a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe02a-106">方法會將 `EffectInsBefore` 效果插入物件中指定的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="fe02a-106">The `EffectInsBefore` method inserts an effect into the object at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe02a-107">語法</span><span class="sxs-lookup"><span data-stu-id="fe02a-107">Syntax</span></span>


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="fe02a-108">參數</span><span class="sxs-lookup"><span data-stu-id="fe02a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe02a-109">*.Pfx*</span><span class="sxs-lookup"><span data-stu-id="fe02a-109">*pFX*</span></span> 
</dt> <dd>

<span data-ttu-id="fe02a-110">效果的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="fe02a-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="fe02a-111">*優先順序*</span><span class="sxs-lookup"><span data-stu-id="fe02a-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="fe02a-112">要插入效果的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="fe02a-112">Priority level at which to insert the effect.</span></span> <span data-ttu-id="fe02a-113">使用值-1，在優先順序清單的結尾插入效果。</span><span class="sxs-lookup"><span data-stu-id="fe02a-113">Use the value –1 to insert the effect at the end of the priority list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe02a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe02a-114">Return value</span></span>

<span data-ttu-id="fe02a-115">\_如果成功，則傳回 S OK \_ ，如果物件不是有效的，則傳回 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="fe02a-115">Returns S\_OK if successful or E\_NOTIMPL if the object is not an effect.</span></span> <span data-ttu-id="fe02a-116">否則，會傳回另一個 **HRESULT** 值，指出錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="fe02a-116">Otherwise, returns another **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe02a-117">備註</span><span class="sxs-lookup"><span data-stu-id="fe02a-117">Remarks</span></span>

<span data-ttu-id="fe02a-118">必要時，效果的開始和停止時間會在物件的時間範圍界限內裁剪。</span><span class="sxs-lookup"><span data-stu-id="fe02a-118">The start and stop times of the effect are clipped within the bounds of the object's time range, if necessary.</span></span> <span data-ttu-id="fe02a-119">如果在指定的優先權層級已經有效果，該點的所有效果都會移至優先順序清單，以騰出空間給新的效果。</span><span class="sxs-lookup"><span data-stu-id="fe02a-119">If there is already an effect at the specified priority level, all the effects from that point on move down the priority list to make room for the new effect.</span></span>

> [!Note]  
> <span data-ttu-id="fe02a-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fe02a-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe02a-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fe02a-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fe02a-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fe02a-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe02a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe02a-123">Requirements</span></span>



| <span data-ttu-id="fe02a-124">需求</span><span class="sxs-lookup"><span data-stu-id="fe02a-124">Requirement</span></span> | <span data-ttu-id="fe02a-125">值</span><span class="sxs-lookup"><span data-stu-id="fe02a-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe02a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="fe02a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fe02a-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe02a-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fe02a-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe02a-128">Library</span></span><br/> | <dl> <span data-ttu-id="fe02a-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe02a-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe02a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe02a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe02a-131">**IAMTimelineEffectable 介面**</span><span class="sxs-lookup"><span data-stu-id="fe02a-131">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="fe02a-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="fe02a-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




