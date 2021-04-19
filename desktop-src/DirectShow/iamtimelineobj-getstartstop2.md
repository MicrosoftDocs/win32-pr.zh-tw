---
description: GetStartStop2 方法會抓取物件的開始和停止時間（相對於物件的父系）。 這個方法相當於 IAMTimelineObj：： GetStartStop，但會接受 REFTIME 的值。
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'IAMTimelineObj：： GetStartStop2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983005"
---
# <a name="iamtimelineobjgetstartstop2-method"></a><span data-ttu-id="f92e4-104">IAMTimelineObj：： GetStartStop2 方法</span><span class="sxs-lookup"><span data-stu-id="f92e4-104">IAMTimelineObj::GetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="f92e4-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="f92e4-105">\[Deprecated.</span></span> <span data-ttu-id="f92e4-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="f92e4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f92e4-107">方法會抓取 `GetStartStop2` 物件的開始和停止時間（相對於物件的父系）。</span><span class="sxs-lookup"><span data-stu-id="f92e4-107">The `GetStartStop2` method retrieves the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="f92e4-108">這個方法相當於 [**IAMTimelineObj：： GetStartStop**](iamtimelineobj-getstartstop.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="f92e4-108">This method is equivalent to [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f92e4-109">語法</span><span class="sxs-lookup"><span data-stu-id="f92e4-109">Syntax</span></span>


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="f92e4-110">參數</span><span class="sxs-lookup"><span data-stu-id="f92e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f92e4-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="f92e4-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f92e4-112">接收開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f92e4-112">Receives the start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="f92e4-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="f92e4-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f92e4-114">接收停止時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f92e4-114">Receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f92e4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f92e4-115">Return value</span></span>

<span data-ttu-id="f92e4-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f92e4-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f92e4-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f92e4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f92e4-118">備註</span><span class="sxs-lookup"><span data-stu-id="f92e4-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f92e4-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="f92e4-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f92e4-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="f92e4-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f92e4-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="f92e4-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f92e4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f92e4-122">Requirements</span></span>



| <span data-ttu-id="f92e4-123">需求</span><span class="sxs-lookup"><span data-stu-id="f92e4-123">Requirement</span></span> | <span data-ttu-id="f92e4-124">值</span><span class="sxs-lookup"><span data-stu-id="f92e4-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f92e4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f92e4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f92e4-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f92e4-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f92e4-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="f92e4-127">Library</span></span><br/> | <dl> <span data-ttu-id="f92e4-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f92e4-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f92e4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f92e4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f92e4-130">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="f92e4-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f92e4-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="f92e4-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




