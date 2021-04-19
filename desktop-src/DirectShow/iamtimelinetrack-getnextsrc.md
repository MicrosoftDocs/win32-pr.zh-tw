---
description: GetNextSrc 方法會在曲目中搜尋在指定時間或之後出現的下一個來源。
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'IAMTimelineTrack：： GetNextSrc 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000686"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a><span data-ttu-id="edc07-103">IAMTimelineTrack：： GetNextSrc 方法</span><span class="sxs-lookup"><span data-stu-id="edc07-103">IAMTimelineTrack::GetNextSrc method</span></span>

> [!Note]  
> <span data-ttu-id="edc07-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="edc07-104">\[Deprecated.</span></span> <span data-ttu-id="edc07-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="edc07-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="edc07-106">`GetNextSrc`方法會在曲目中搜尋在指定時間或之後出現的下一個來源。</span><span class="sxs-lookup"><span data-stu-id="edc07-106">The `GetNextSrc` method searches the track for the next source that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc07-107">語法</span><span class="sxs-lookup"><span data-stu-id="edc07-107">Syntax</span></span>


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="edc07-108">參數</span><span class="sxs-lookup"><span data-stu-id="edc07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc07-109">*ppSrc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="edc07-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edc07-110">接收來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="edc07-110">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="edc07-111">*接腳*</span><span class="sxs-lookup"><span data-stu-id="edc07-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="edc07-112">變數的指標，其中包含搜尋的開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="edc07-112">Pointer to a variable that contains the start time for the search, in 100-nanosecond units.</span></span> <span data-ttu-id="edc07-113">如果方法會抓取來源，則會將值設定為來源的停止時間。</span><span class="sxs-lookup"><span data-stu-id="edc07-113">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="edc07-114">如果方法未抓取來源，此值就會變成無效，而且應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="edc07-114">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc07-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="edc07-115">Return value</span></span>

<span data-ttu-id="edc07-116">\_如果方法會抓取來源，則傳回 [確定]， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="edc07-116">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="edc07-117">備註</span><span class="sxs-lookup"><span data-stu-id="edc07-117">Remarks</span></span>

<span data-ttu-id="edc07-118">如果由 *引線* 指定的時間介於來源的開始和停止時間之間，則該方法會抓取該來源。</span><span class="sxs-lookup"><span data-stu-id="edc07-118">If the time specified by *pInOut* falls between the start and stop times of a source, the method retrieves that source.</span></span>

<span data-ttu-id="edc07-119">如果方法傳回 S \_ OK，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="edc07-119">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="edc07-120">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="edc07-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="edc07-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="edc07-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="edc07-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="edc07-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="edc07-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="edc07-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="edc07-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="edc07-124">Requirements</span></span>



| <span data-ttu-id="edc07-125">需求</span><span class="sxs-lookup"><span data-stu-id="edc07-125">Requirement</span></span> | <span data-ttu-id="edc07-126">值</span><span class="sxs-lookup"><span data-stu-id="edc07-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edc07-127">標頭</span><span class="sxs-lookup"><span data-stu-id="edc07-127">Header</span></span><br/>  | <dl> <span data-ttu-id="edc07-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="edc07-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="edc07-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="edc07-129">Library</span></span><br/> | <dl> <span data-ttu-id="edc07-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="edc07-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edc07-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edc07-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc07-132">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="edc07-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="edc07-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="edc07-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




