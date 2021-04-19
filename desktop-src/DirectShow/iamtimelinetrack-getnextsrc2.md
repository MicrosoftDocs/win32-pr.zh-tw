---
description: GetNextSrc2 方法會在曲目中搜尋在指定時間或之後出現的下一個來源。 這個方法相當於 IAMTimelineTrack：： GetNextSrc，但會接受 REFTIME 值。
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'IAMTimelineTrack：： GetNextSrc2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982946"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a><span data-ttu-id="6b427-104">IAMTimelineTrack：： GetNextSrc2 方法</span><span class="sxs-lookup"><span data-stu-id="6b427-104">IAMTimelineTrack::GetNextSrc2 method</span></span>

> [!Note]  
> <span data-ttu-id="6b427-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6b427-105">\[Deprecated.</span></span> <span data-ttu-id="6b427-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6b427-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6b427-107">`GetNextSrc2`方法會在曲目中搜尋在指定時間或之後出現的下一個來源。</span><span class="sxs-lookup"><span data-stu-id="6b427-107">The `GetNextSrc2` method searches the track for the next source that appears at the specified time or later.</span></span> <span data-ttu-id="6b427-108">這個方法相當於 [**IAMTimelineTrack：： GetNextSrc**](iamtimelinetrack-getnextsrc.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="6b427-108">This method is equivalent to [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b427-109">語法</span><span class="sxs-lookup"><span data-stu-id="6b427-109">Syntax</span></span>


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="6b427-110">參數</span><span class="sxs-lookup"><span data-stu-id="6b427-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b427-111">*ppSrc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6b427-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b427-112">接收來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6b427-112">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6b427-113">*接腳*</span><span class="sxs-lookup"><span data-stu-id="6b427-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="6b427-114">在輸入時，包含搜尋的開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6b427-114">On input, contains the start time for the search, in seconds.</span></span> <span data-ttu-id="6b427-115">如果方法會抓取來源，則會將值設定為來源的停止時間。</span><span class="sxs-lookup"><span data-stu-id="6b427-115">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="6b427-116">如果方法未抓取來源，此值就會變成無效，而且應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="6b427-116">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b427-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b427-117">Return value</span></span>

<span data-ttu-id="6b427-118">\_如果方法會抓取來源，則傳回 [確定]， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="6b427-118">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b427-119">備註</span><span class="sxs-lookup"><span data-stu-id="6b427-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b427-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6b427-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6b427-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6b427-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6b427-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6b427-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b427-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b427-123">Requirements</span></span>



| <span data-ttu-id="6b427-124">需求</span><span class="sxs-lookup"><span data-stu-id="6b427-124">Requirement</span></span> | <span data-ttu-id="6b427-125">值</span><span class="sxs-lookup"><span data-stu-id="6b427-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b427-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6b427-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6b427-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b427-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6b427-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b427-128">Library</span></span><br/> | <dl> <span data-ttu-id="6b427-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b427-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b427-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b427-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b427-131">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="6b427-131">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="6b427-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="6b427-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




