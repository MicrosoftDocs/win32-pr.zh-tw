---
description: InsertSpace 方法會分割存在於指定時間的任何物件，並在兩者之間插入空格。
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'IAMTimelineTrack：： InsertSpace 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000699"
---
# <a name="iamtimelinetrackinsertspace-method"></a><span data-ttu-id="07850-103">IAMTimelineTrack：： InsertSpace 方法</span><span class="sxs-lookup"><span data-stu-id="07850-103">IAMTimelineTrack::InsertSpace method</span></span>

> [!Note]  
> <span data-ttu-id="07850-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="07850-104">\[Deprecated.</span></span> <span data-ttu-id="07850-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="07850-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="07850-106">`InsertSpace`方法會分割存在於指定時間的任何物件，並在兩者之間插入空格。</span><span class="sxs-lookup"><span data-stu-id="07850-106">The `InsertSpace` method splits any objects that exist at the specified time and inserts space between them.</span></span>

## <a name="syntax"></a><span data-ttu-id="07850-107">語法</span><span class="sxs-lookup"><span data-stu-id="07850-107">Syntax</span></span>


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="07850-108">參數</span><span class="sxs-lookup"><span data-stu-id="07850-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07850-109">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="07850-109">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="07850-110">建立分割的時間，以及插入空間的起點（以 100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="07850-110">Time at which to create the split, and the starting point of the inserted space, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="07850-111">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="07850-111">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="07850-112">插入空間的結束點，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="07850-112">End point of the inserted space, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07850-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="07850-113">Return value</span></span>

<span data-ttu-id="07850-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="07850-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="07850-115">可能的傳回值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="07850-115">Possible return values include the following:</span></span>



| <span data-ttu-id="07850-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="07850-116">Return code</span></span>                                                                                   | <span data-ttu-id="07850-117">Description</span><span class="sxs-lookup"><span data-stu-id="07850-117">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="07850-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="07850-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="07850-119">在指定的時間沒有任何物件。</span><span class="sxs-lookup"><span data-stu-id="07850-119">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="07850-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="07850-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="07850-121">成功。</span><span class="sxs-lookup"><span data-stu-id="07850-121">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="07850-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="07850-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="07850-123">無效引數。</span><span class="sxs-lookup"><span data-stu-id="07850-123">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="07850-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="07850-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="07850-125">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="07850-125">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="07850-126">備註</span><span class="sxs-lookup"><span data-stu-id="07850-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="07850-127">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="07850-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="07850-128">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="07850-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="07850-129">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="07850-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07850-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="07850-130">Requirements</span></span>



| <span data-ttu-id="07850-131">需求</span><span class="sxs-lookup"><span data-stu-id="07850-131">Requirement</span></span> | <span data-ttu-id="07850-132">值</span><span class="sxs-lookup"><span data-stu-id="07850-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07850-133">標頭</span><span class="sxs-lookup"><span data-stu-id="07850-133">Header</span></span><br/>  | <dl> <span data-ttu-id="07850-134"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="07850-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="07850-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="07850-135">Library</span></span><br/> | <dl> <span data-ttu-id="07850-136"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07850-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07850-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07850-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07850-138">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="07850-138">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="07850-139">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="07850-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




