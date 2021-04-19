---
description: FixTimes 方法會將指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'IAMTimelineObj：： FixTimes 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995515"
---
# <a name="iamtimelineobjfixtimes-method"></a><span data-ttu-id="9f60b-103">IAMTimelineObj：： FixTimes 方法</span><span class="sxs-lookup"><span data-stu-id="9f60b-103">IAMTimelineObj::FixTimes method</span></span>

> [!Note]  
> <span data-ttu-id="9f60b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="9f60b-104">\[Deprecated.</span></span> <span data-ttu-id="9f60b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="9f60b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f60b-106">方法會將 `FixTimes` 指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。</span><span class="sxs-lookup"><span data-stu-id="9f60b-106">The `FixTimes` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f60b-107">語法</span><span class="sxs-lookup"><span data-stu-id="9f60b-107">Syntax</span></span>


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="9f60b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9f60b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f60b-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="9f60b-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9f60b-110">變數的指標，該變數包含開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="9f60b-110">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="9f60b-111">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="9f60b-111">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="9f60b-112">*pStop*</span><span class="sxs-lookup"><span data-stu-id="9f60b-112">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="9f60b-113">包含停止時間之變數的指標，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="9f60b-113">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="9f60b-114">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="9f60b-114">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f60b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f60b-115">Return value</span></span>

<span data-ttu-id="9f60b-116">\_如果成功，則傳回 S OK， \_ 如果物件不是群組的一部分，則傳回 E NOTINTREE。</span><span class="sxs-lookup"><span data-stu-id="9f60b-116">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f60b-117">備註</span><span class="sxs-lookup"><span data-stu-id="9f60b-117">Remarks</span></span>

<span data-ttu-id="9f60b-118">在轉譯期間，DES 會將物件的開始和停止時間四捨五入至最接近的框架界限。</span><span class="sxs-lookup"><span data-stu-id="9f60b-118">During rendering, DES rounds the object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="9f60b-119">不過，DES 不會覆寫物件的時間。</span><span class="sxs-lookup"><span data-stu-id="9f60b-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="9f60b-120">如果您變更群組畫面播放速率，則永遠會從原始時間計算舍入的時間。</span><span class="sxs-lookup"><span data-stu-id="9f60b-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="9f60b-121">如需詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="9f60b-121">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="9f60b-122">您可以使用這個方法來判斷轉譯專案中的精確開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="9f60b-122">Use this method to determine accurate start and stop times in the rendered project.</span></span> <span data-ttu-id="9f60b-123">例如，您應該搜尋舍入時間，而不是物件的原始開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="9f60b-123">For example, you should seek to the rounded times, rather than the object's original start and stop times.</span></span> <span data-ttu-id="9f60b-124">呼叫 [**IAMTimelineObj：： GetStartStop**](iamtimelineobj-getstartstop.md) 來取得原始時間，並將這些值傳遞至 `FixTimes` 。</span><span class="sxs-lookup"><span data-stu-id="9f60b-124">Call [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) to obtain the original times, and pass those values to `FixTimes`.</span></span>

> [!Note]  
> <span data-ttu-id="9f60b-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="9f60b-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f60b-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9f60b-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9f60b-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="9f60b-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f60b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f60b-128">Requirements</span></span>



| <span data-ttu-id="9f60b-129">需求</span><span class="sxs-lookup"><span data-stu-id="9f60b-129">Requirement</span></span> | <span data-ttu-id="9f60b-130">值</span><span class="sxs-lookup"><span data-stu-id="9f60b-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f60b-131">標頭</span><span class="sxs-lookup"><span data-stu-id="9f60b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9f60b-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f60b-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9f60b-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f60b-133">Library</span></span><br/> | <dl> <span data-ttu-id="9f60b-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f60b-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f60b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f60b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f60b-136">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="9f60b-136">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="9f60b-137">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="9f60b-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




