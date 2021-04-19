---
description: SplitAt2 方法會在指定的時間分割物件。 這個方法相當於 IAMTimelineSplittable：： SplitAt，但會接受 REFTIME 值。
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'IAMTimelineSplittable：： SplitAt2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000705"
---
# <a name="iamtimelinesplittablesplitat2-method"></a><span data-ttu-id="3fdea-104">IAMTimelineSplittable：： SplitAt2 方法</span><span class="sxs-lookup"><span data-stu-id="3fdea-104">IAMTimelineSplittable::SplitAt2 method</span></span>

> [!Note]  
> <span data-ttu-id="3fdea-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3fdea-105">\[Deprecated.</span></span> <span data-ttu-id="3fdea-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3fdea-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3fdea-107">`SplitAt2`方法會在指定的時間分割物件。</span><span class="sxs-lookup"><span data-stu-id="3fdea-107">The `SplitAt2` method splits the object at the specified time.</span></span> <span data-ttu-id="3fdea-108">這個方法相當於 [**IAMTimelineSplittable：： SplitAt**](iamtimelinesplittable-splitat.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="3fdea-108">This method is equivalent to [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fdea-109">語法</span><span class="sxs-lookup"><span data-stu-id="3fdea-109">Syntax</span></span>


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="3fdea-110">參數</span><span class="sxs-lookup"><span data-stu-id="3fdea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fdea-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="3fdea-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="3fdea-112">分割物件的時間，相對於時間軸的開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fdea-112">Time at which to split the object, relative to the start of the timeline, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fdea-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fdea-113">Return value</span></span>

<span data-ttu-id="3fdea-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3fdea-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3fdea-115">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="3fdea-115">Possible values include the following:</span></span>



| <span data-ttu-id="3fdea-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3fdea-116">Return code</span></span>                                                                                   | <span data-ttu-id="3fdea-117">Description</span><span class="sxs-lookup"><span data-stu-id="3fdea-117">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="3fdea-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3fdea-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="3fdea-119">沒有要分割的專案。</span><span class="sxs-lookup"><span data-stu-id="3fdea-119">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="3fdea-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3fdea-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3fdea-121">成功。</span><span class="sxs-lookup"><span data-stu-id="3fdea-121">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="3fdea-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3fdea-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3fdea-123">此物件目前不存在。</span><span class="sxs-lookup"><span data-stu-id="3fdea-123">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="3fdea-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3fdea-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3fdea-125">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="3fdea-125">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3fdea-126">備註</span><span class="sxs-lookup"><span data-stu-id="3fdea-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3fdea-127">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3fdea-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3fdea-128">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3fdea-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3fdea-129">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3fdea-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fdea-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fdea-130">Requirements</span></span>



| <span data-ttu-id="3fdea-131">需求</span><span class="sxs-lookup"><span data-stu-id="3fdea-131">Requirement</span></span> | <span data-ttu-id="3fdea-132">值</span><span class="sxs-lookup"><span data-stu-id="3fdea-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fdea-133">標頭</span><span class="sxs-lookup"><span data-stu-id="3fdea-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3fdea-134"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3fdea-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3fdea-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="3fdea-135">Library</span></span><br/> | <dl> <span data-ttu-id="3fdea-136"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fdea-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fdea-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fdea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fdea-138">**IAMTimelineSplittable 介面**</span><span class="sxs-lookup"><span data-stu-id="3fdea-138">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="3fdea-139">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="3fdea-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




