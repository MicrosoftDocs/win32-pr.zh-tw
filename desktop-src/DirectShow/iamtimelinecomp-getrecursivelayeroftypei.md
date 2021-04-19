---
description: 不支援。 請改為呼叫 IAMTimelineComp：： GetRecursiveLayerOfType 方法。
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'IAMTimelineComp：： GetRecursiveLayerOfTypeI 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999178"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a><span data-ttu-id="446da-104">IAMTimelineComp：： GetRecursiveLayerOfTypeI 方法</span><span class="sxs-lookup"><span data-stu-id="446da-104">IAMTimelineComp::GetRecursiveLayerOfTypeI method</span></span>

> [!Note]  
> <span data-ttu-id="446da-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="446da-105">\[Deprecated.</span></span> <span data-ttu-id="446da-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="446da-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="446da-107">不支援。</span><span class="sxs-lookup"><span data-stu-id="446da-107">Not supported.</span></span> <span data-ttu-id="446da-108">請改為呼叫 [**IAMTimelineComp：： GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="446da-108">Call the [**IAMTimelineComp::GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="446da-109">語法</span><span class="sxs-lookup"><span data-stu-id="446da-109">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="446da-110">參數</span><span class="sxs-lookup"><span data-stu-id="446da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="446da-111">*ppVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="446da-111">*ppVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="446da-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="446da-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="446da-113">*pWhichLayer*</span><span class="sxs-lookup"><span data-stu-id="446da-113">*pWhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="446da-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="446da-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="446da-115">*型別*</span><span class="sxs-lookup"><span data-stu-id="446da-115">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="446da-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="446da-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="446da-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="446da-117">Return value</span></span>

<span data-ttu-id="446da-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="446da-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="446da-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="446da-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="446da-120">備註</span><span class="sxs-lookup"><span data-stu-id="446da-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="446da-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="446da-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="446da-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="446da-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="446da-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="446da-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="446da-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="446da-124">Requirements</span></span>



| <span data-ttu-id="446da-125">需求</span><span class="sxs-lookup"><span data-stu-id="446da-125">Requirement</span></span> | <span data-ttu-id="446da-126">值</span><span class="sxs-lookup"><span data-stu-id="446da-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="446da-127">標頭</span><span class="sxs-lookup"><span data-stu-id="446da-127">Header</span></span><br/>  | <dl> <span data-ttu-id="446da-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="446da-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="446da-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="446da-129">Library</span></span><br/> | <dl> <span data-ttu-id="446da-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="446da-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="446da-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="446da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446da-132">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="446da-132">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> </dl>

 

 




