---
description: SrcAdd 方法會將來源新增至追蹤。
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'IAMTimelineTrack：： SrcAdd 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990125"
---
# <a name="iamtimelinetracksrcadd-method"></a><span data-ttu-id="11ef6-103">IAMTimelineTrack：： SrcAdd 方法</span><span class="sxs-lookup"><span data-stu-id="11ef6-103">IAMTimelineTrack::SrcAdd method</span></span>

> [!Note]  
> <span data-ttu-id="11ef6-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="11ef6-104">\[Deprecated.</span></span> <span data-ttu-id="11ef6-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="11ef6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="11ef6-106">`SrcAdd`方法會將來源新增至追蹤。</span><span class="sxs-lookup"><span data-stu-id="11ef6-106">The `SrcAdd` method adds a source to the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ef6-107">語法</span><span class="sxs-lookup"><span data-stu-id="11ef6-107">Syntax</span></span>


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="11ef6-108">參數</span><span class="sxs-lookup"><span data-stu-id="11ef6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ef6-109">*.Psrc*</span><span class="sxs-lookup"><span data-stu-id="11ef6-109">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="11ef6-110">來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="11ef6-110">Pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ef6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="11ef6-111">Return value</span></span>

<span data-ttu-id="11ef6-112">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="11ef6-112">Returns S\_OK if successful.</span></span> <span data-ttu-id="11ef6-113">\_如果物件不是來源物件，則傳回 E NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="11ef6-113">Returns E\_NOINTERFACE if the object is not a source object.</span></span> <span data-ttu-id="11ef6-114">否則，會傳回 **HRESULT** 值，指出錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="11ef6-114">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="11ef6-115">備註</span><span class="sxs-lookup"><span data-stu-id="11ef6-115">Remarks</span></span>

<span data-ttu-id="11ef6-116">在呼叫這個方法之前，請先設定來源的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="11ef6-116">Set the source's start and stop times before calling this method.</span></span> <span data-ttu-id="11ef6-117"> (呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="11ef6-117">(Call [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)</span></span>

<span data-ttu-id="11ef6-118">目前，DES 無法同時轉譯超過75個以視訊壓縮管理員壓縮的來源 (BC-VCM-LVM-HYPERV) 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="11ef6-118">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="11ef6-119">此外，如果整個專案包含75以上的來源，您必須使用動態重新連接，否則 DES 無法預覽專案。</span><span class="sxs-lookup"><span data-stu-id="11ef6-119">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="11ef6-120">如需詳細資訊，請參閱 [**IRenderEngine：： SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)。</span><span class="sxs-lookup"><span data-stu-id="11ef6-120">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="11ef6-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="11ef6-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="11ef6-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="11ef6-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="11ef6-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="11ef6-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11ef6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="11ef6-124">Requirements</span></span>



| <span data-ttu-id="11ef6-125">需求</span><span class="sxs-lookup"><span data-stu-id="11ef6-125">Requirement</span></span> | <span data-ttu-id="11ef6-126">值</span><span class="sxs-lookup"><span data-stu-id="11ef6-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11ef6-127">標頭</span><span class="sxs-lookup"><span data-stu-id="11ef6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="11ef6-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="11ef6-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="11ef6-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="11ef6-129">Library</span></span><br/> | <dl> <span data-ttu-id="11ef6-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="11ef6-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ef6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11ef6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ef6-132">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="11ef6-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="11ef6-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="11ef6-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




