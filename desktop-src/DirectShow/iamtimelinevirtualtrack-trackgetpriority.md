---
description: TrackGetPriority 方法會抓取物件的優先權層級。
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'IAMTimelineVirtualTrack：： TrackGetPriority 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987924"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a><span data-ttu-id="9e725-103">IAMTimelineVirtualTrack：： TrackGetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="9e725-103">IAMTimelineVirtualTrack::TrackGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="9e725-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="9e725-104">\[Deprecated.</span></span> <span data-ttu-id="9e725-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="9e725-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e725-106">方法會抓取 `TrackGetPriority` 物件的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="9e725-106">The `TrackGetPriority` method retrieves the object's priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e725-107">語法</span><span class="sxs-lookup"><span data-stu-id="9e725-107">Syntax</span></span>


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="9e725-108">參數</span><span class="sxs-lookup"><span data-stu-id="9e725-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e725-109">*pPriority*</span><span class="sxs-lookup"><span data-stu-id="9e725-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="9e725-110">收到優先權層級之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="9e725-110">Pointer to a variable that receives the priority level.</span></span> <span data-ttu-id="9e725-111">如果物件不是時間軸的一部分，此值會設定為–1。</span><span class="sxs-lookup"><span data-stu-id="9e725-111">If the object is not part of a timeline, the value is set to –1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e725-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e725-112">Return value</span></span>

<span data-ttu-id="9e725-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9e725-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e725-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9e725-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e725-115">備註</span><span class="sxs-lookup"><span data-stu-id="9e725-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e725-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="9e725-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e725-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9e725-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e725-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="9e725-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e725-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e725-119">Requirements</span></span>



| <span data-ttu-id="9e725-120">需求</span><span class="sxs-lookup"><span data-stu-id="9e725-120">Requirement</span></span> | <span data-ttu-id="9e725-121">值</span><span class="sxs-lookup"><span data-stu-id="9e725-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e725-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9e725-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9e725-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e725-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e725-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e725-124">Library</span></span><br/> | <dl> <span data-ttu-id="9e725-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e725-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e725-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e725-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e725-127">**IAMTimelineVirtualTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="9e725-127">**IAMTimelineVirtualTrack Interface**</span></span>](iamtimelinevirtualtrack.md)
</dt> <dt>

[<span data-ttu-id="9e725-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="9e725-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




