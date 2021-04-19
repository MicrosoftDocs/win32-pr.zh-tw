---
description: GetCountOfType 方法會抓取指定之群組及其所有子系中所包含之指定類型的物件數目。
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'IAMTimeline：： GetCountOfType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977666"
---
# <a name="iamtimelinegetcountoftype-method"></a><span data-ttu-id="5c6c3-103">IAMTimeline：： GetCountOfType 方法</span><span class="sxs-lookup"><span data-stu-id="5c6c3-103">IAMTimeline::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="5c6c3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-104">\[Deprecated.</span></span> <span data-ttu-id="5c6c3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5c6c3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5c6c3-106">方法會抓取指定之 `GetCountOfType` 群組及其所有子系中所包含之指定類型的物件數目。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-106">The `GetCountOfType` method retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6c3-107">語法</span><span class="sxs-lookup"><span data-stu-id="5c6c3-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="5c6c3-108">參數</span><span class="sxs-lookup"><span data-stu-id="5c6c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c6c3-109">*群組*</span><span class="sxs-lookup"><span data-stu-id="5c6c3-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="5c6c3-110">要取得計數之群組的索引編號。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-110">Index number of the group for which to retrieve the count.</span></span>

</dd> <dt>

<span data-ttu-id="5c6c3-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="5c6c3-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="5c6c3-112">以遞迴方式接收群組中包含的指定型別及其所有虛擬追蹤的物件數目。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-112">Receives the number of objects of the specified type contained in the group and all of its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="5c6c3-113">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="5c6c3-113">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="5c6c3-114">接收在 *pVal* 中傳回的計數加上所搜尋的組合數目（包含此項）。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-114">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="5c6c3-115">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="5c6c3-115">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="5c6c3-116">[**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md)列舉類型的成員，指定要計算的物件類型。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-116">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c6c3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c6c3-117">Return value</span></span>

<span data-ttu-id="5c6c3-118">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-118">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="5c6c3-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5c6c3-119">Return code</span></span>                                                                                  | <span data-ttu-id="5c6c3-120">Description</span><span class="sxs-lookup"><span data-stu-id="5c6c3-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5c6c3-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5c6c3-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5c6c3-122">成功。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-122">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="5c6c3-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5c6c3-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5c6c3-124">不正確群組編號。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-124">Invalid group number.</span></span><br/>      |
| <dl> <span data-ttu-id="5c6c3-125"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="5c6c3-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="5c6c3-126">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c6c3-127">備註</span><span class="sxs-lookup"><span data-stu-id="5c6c3-127">Remarks</span></span>

<span data-ttu-id="5c6c3-128">呼叫這個方法相當於在指定的群組上呼叫 [**IAMTimelineComp：： GetCountOfType**](iamtimelinecomp-getcountoftype.md) 。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-128">Calling this method is equivalent to calling [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) on the specified group.</span></span> <span data-ttu-id="5c6c3-129">如需詳細資訊，請參閱該方法的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-129">See the Remarks section of that method for more information.</span></span>

<span data-ttu-id="5c6c3-130">一般來說，應用程式不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-130">Typically, an application will not call this method.</span></span> <span data-ttu-id="5c6c3-131">它是由轉譯引擎在內部呼叫。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-131">It is called internally by the render engine.</span></span>

> [!Note]  
> <span data-ttu-id="5c6c3-132">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5c6c3-133">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5c6c3-134">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5c6c3-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c6c3-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c6c3-135">Requirements</span></span>



| <span data-ttu-id="5c6c3-136">需求</span><span class="sxs-lookup"><span data-stu-id="5c6c3-136">Requirement</span></span> | <span data-ttu-id="5c6c3-137">值</span><span class="sxs-lookup"><span data-stu-id="5c6c3-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6c3-138">標頭</span><span class="sxs-lookup"><span data-stu-id="5c6c3-138">Header</span></span><br/>  | <dl> <span data-ttu-id="5c6c3-139"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c6c3-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5c6c3-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="5c6c3-140">Library</span></span><br/> | <dl> <span data-ttu-id="5c6c3-141"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c6c3-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c6c3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c6c3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c6c3-143">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="5c6c3-143">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="5c6c3-144">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5c6c3-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




