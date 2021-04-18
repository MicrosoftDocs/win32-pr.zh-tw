---
description: FixTimes2 方法會將指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。 這個方法相當於 IAMTimelineObj：： FixTimes，但會接受 REFTIME 的值。
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'IAMTimelineObj：： FixTimes2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976274"
---
# <a name="iamtimelineobjfixtimes2-method"></a><span data-ttu-id="43a3f-104">IAMTimelineObj：： FixTimes2 方法</span><span class="sxs-lookup"><span data-stu-id="43a3f-104">IAMTimelineObj::FixTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="43a3f-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="43a3f-105">\[Deprecated.</span></span> <span data-ttu-id="43a3f-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="43a3f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43a3f-107">方法會將 `FixTimes2` 指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。</span><span class="sxs-lookup"><span data-stu-id="43a3f-107">The `FixTimes2` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span> <span data-ttu-id="43a3f-108">這個方法相當於 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="43a3f-108">This method is equivalent to [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a3f-109">語法</span><span class="sxs-lookup"><span data-stu-id="43a3f-109">Syntax</span></span>


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="43a3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="43a3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a3f-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="43a3f-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="43a3f-112">包含開始時間（以秒為單位）之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="43a3f-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="43a3f-113">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="43a3f-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="43a3f-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="43a3f-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="43a3f-115">包含停止時間（以秒為單位）之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="43a3f-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="43a3f-116">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="43a3f-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a3f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="43a3f-117">Return value</span></span>

<span data-ttu-id="43a3f-118">\_如果成功，則傳回 S OK， \_ 如果物件不是群組的一部分，則傳回 E NOTINTREE。</span><span class="sxs-lookup"><span data-stu-id="43a3f-118">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a3f-119">備註</span><span class="sxs-lookup"><span data-stu-id="43a3f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43a3f-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="43a3f-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43a3f-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="43a3f-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43a3f-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="43a3f-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43a3f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="43a3f-123">Requirements</span></span>



| <span data-ttu-id="43a3f-124">需求</span><span class="sxs-lookup"><span data-stu-id="43a3f-124">Requirement</span></span> | <span data-ttu-id="43a3f-125">值</span><span class="sxs-lookup"><span data-stu-id="43a3f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43a3f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="43a3f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="43a3f-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="43a3f-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="43a3f-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="43a3f-128">Library</span></span><br/> | <dl> <span data-ttu-id="43a3f-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43a3f-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a3f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43a3f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a3f-131">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="43a3f-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="43a3f-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="43a3f-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




