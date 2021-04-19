---
description: InsertSpace2 方法會分割存在於指定時間的任何物件，並在兩者之間插入空格。 這個方法相當於 IAMTimelineTrack：： InsertSpace，但會接受 REFTIME 的值。
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'IAMTimelineTrack：： InsertSpace2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990127"
---
# <a name="iamtimelinetrackinsertspace2-method"></a><span data-ttu-id="445ec-104">IAMTimelineTrack：： InsertSpace2 方法</span><span class="sxs-lookup"><span data-stu-id="445ec-104">IAMTimelineTrack::InsertSpace2 method</span></span>

> [!Note]  
> <span data-ttu-id="445ec-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="445ec-105">\[Deprecated.</span></span> <span data-ttu-id="445ec-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="445ec-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="445ec-107">`InsertSpace2`方法會分割存在於指定時間的任何物件，並在兩者之間插入空格。</span><span class="sxs-lookup"><span data-stu-id="445ec-107">The `InsertSpace2` method splits any objects that exist at the specified time and inserts space between them.</span></span> <span data-ttu-id="445ec-108">這個方法相當於 [**IAMTimelineTrack：： InsertSpace**](iamtimelinetrack-insertspace.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="445ec-108">This method is equivalent to [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="445ec-109">語法</span><span class="sxs-lookup"><span data-stu-id="445ec-109">Syntax</span></span>


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="445ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="445ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="445ec-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="445ec-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="445ec-112">建立分割的時間，以及插入的空間開始點（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="445ec-112">Time at which to create the split, and the starting point of the inserted space, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="445ec-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="445ec-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="445ec-114">插入空間的結束點（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="445ec-114">End point of the inserted space, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="445ec-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="445ec-115">Return value</span></span>

<span data-ttu-id="445ec-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="445ec-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="445ec-117">可能的傳回值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="445ec-117">Possible return values include the following:</span></span>



| <span data-ttu-id="445ec-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="445ec-118">Return code</span></span>                                                                                   | <span data-ttu-id="445ec-119">Description</span><span class="sxs-lookup"><span data-stu-id="445ec-119">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="445ec-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="445ec-120"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="445ec-121">在指定的時間沒有任何物件。</span><span class="sxs-lookup"><span data-stu-id="445ec-121">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="445ec-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="445ec-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="445ec-123">成功。</span><span class="sxs-lookup"><span data-stu-id="445ec-123">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="445ec-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="445ec-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="445ec-125">無效引數。</span><span class="sxs-lookup"><span data-stu-id="445ec-125">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="445ec-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="445ec-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="445ec-127">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="445ec-127">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="445ec-128">備註</span><span class="sxs-lookup"><span data-stu-id="445ec-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="445ec-129">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="445ec-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="445ec-130">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="445ec-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="445ec-131">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="445ec-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="445ec-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="445ec-132">Requirements</span></span>



| <span data-ttu-id="445ec-133">需求</span><span class="sxs-lookup"><span data-stu-id="445ec-133">Requirement</span></span> | <span data-ttu-id="445ec-134">值</span><span class="sxs-lookup"><span data-stu-id="445ec-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="445ec-135">標頭</span><span class="sxs-lookup"><span data-stu-id="445ec-135">Header</span></span><br/>  | <dl> <span data-ttu-id="445ec-136"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="445ec-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="445ec-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="445ec-137">Library</span></span><br/> | <dl> <span data-ttu-id="445ec-138"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="445ec-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445ec-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="445ec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445ec-140">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="445ec-140">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="445ec-141">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="445ec-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




