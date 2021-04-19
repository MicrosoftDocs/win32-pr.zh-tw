---
description: TransAdd 方法會將轉換新增至物件。 物件可以有多個轉換，但是不能在時間內重迭。 轉換必須落在物件的時間界限內。
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'IAMTimelineTransable：： TransAdd 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984443"
---
# <a name="iamtimelinetransabletransadd-method"></a><span data-ttu-id="838ab-105">IAMTimelineTransable：： TransAdd 方法</span><span class="sxs-lookup"><span data-stu-id="838ab-105">IAMTimelineTransable::TransAdd method</span></span>

> [!Note]  
> <span data-ttu-id="838ab-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="838ab-106">\[Deprecated.</span></span> <span data-ttu-id="838ab-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="838ab-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="838ab-108">`TransAdd`方法會將轉換新增至物件。</span><span class="sxs-lookup"><span data-stu-id="838ab-108">The `TransAdd` method adds a transition to the object.</span></span> <span data-ttu-id="838ab-109">物件可以有多個轉換，但是不能在時間內重迭。</span><span class="sxs-lookup"><span data-stu-id="838ab-109">An object can have multiple transitions, but they must not overlap in time.</span></span> <span data-ttu-id="838ab-110">轉換必須落在物件的時間界限內。</span><span class="sxs-lookup"><span data-stu-id="838ab-110">Transitions must fall within the time boundaries of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="838ab-111">語法</span><span class="sxs-lookup"><span data-stu-id="838ab-111">Syntax</span></span>


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a><span data-ttu-id="838ab-112">參數</span><span class="sxs-lookup"><span data-stu-id="838ab-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838ab-113">*pTrans*</span><span class="sxs-lookup"><span data-stu-id="838ab-113">*pTrans*</span></span> 
</dt> <dd>

<span data-ttu-id="838ab-114">要加入之轉換的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="838ab-114">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the transition to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838ab-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="838ab-115">Return value</span></span>

<span data-ttu-id="838ab-116">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="838ab-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="838ab-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="838ab-117">Return code</span></span>                                                                                   | <span data-ttu-id="838ab-118">Description</span><span class="sxs-lookup"><span data-stu-id="838ab-118">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="838ab-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="838ab-120">成功。</span><span class="sxs-lookup"><span data-stu-id="838ab-120">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="838ab-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="838ab-122">無法插入轉換。</span><span class="sxs-lookup"><span data-stu-id="838ab-122">Cannot insert the transition.</span></span><br/>              |
| <dl> <span data-ttu-id="838ab-123"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="838ab-124">*pTrans* 不是轉換的指標。</span><span class="sxs-lookup"><span data-stu-id="838ab-124">*pTrans* is not a pointer to a transition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="838ab-125">備註</span><span class="sxs-lookup"><span data-stu-id="838ab-125">Remarks</span></span>

<span data-ttu-id="838ab-126">如果轉換與現有的轉換重迭，則方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="838ab-126">If the transition overlaps an existing transition, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="838ab-127">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="838ab-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="838ab-128">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="838ab-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="838ab-129">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="838ab-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="838ab-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="838ab-130">Requirements</span></span>



| <span data-ttu-id="838ab-131">需求</span><span class="sxs-lookup"><span data-stu-id="838ab-131">Requirement</span></span> | <span data-ttu-id="838ab-132">值</span><span class="sxs-lookup"><span data-stu-id="838ab-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="838ab-133">標頭</span><span class="sxs-lookup"><span data-stu-id="838ab-133">Header</span></span><br/>  | <dl> <span data-ttu-id="838ab-134"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="838ab-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="838ab-135">Library</span></span><br/> | <dl> <span data-ttu-id="838ab-136"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="838ab-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="838ab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838ab-138">**IAMTimelineTransable 介面**</span><span class="sxs-lookup"><span data-stu-id="838ab-138">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="838ab-139">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="838ab-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




