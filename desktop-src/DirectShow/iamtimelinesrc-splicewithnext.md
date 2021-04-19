---
description: SpliceWithNext 方法會將來源物件加入至另一個來源物件。
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'IAMTimelineSrc：： SpliceWithNext 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999322"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a><span data-ttu-id="6eaba-103">IAMTimelineSrc：： SpliceWithNext 方法</span><span class="sxs-lookup"><span data-stu-id="6eaba-103">IAMTimelineSrc::SpliceWithNext method</span></span>

> [!Note]  
> <span data-ttu-id="6eaba-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6eaba-104">\[Deprecated.</span></span> <span data-ttu-id="6eaba-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6eaba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6eaba-106">方法會將 `SpliceWithNext` 來源物件聯結至另一個來源物件。</span><span class="sxs-lookup"><span data-stu-id="6eaba-106">The `SpliceWithNext` method joins the source object to another source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eaba-107">語法</span><span class="sxs-lookup"><span data-stu-id="6eaba-107">Syntax</span></span>


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a><span data-ttu-id="6eaba-108">參數</span><span class="sxs-lookup"><span data-stu-id="6eaba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eaba-109">*pNext*</span><span class="sxs-lookup"><span data-stu-id="6eaba-109">*pNext*</span></span> 
</dt> <dd>

<span data-ttu-id="6eaba-110">要聯結至目前來源之來源物件的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="6eaba-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object to join to the current source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eaba-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6eaba-111">Return value</span></span>

<span data-ttu-id="6eaba-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6eaba-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6eaba-113">可能的傳回值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="6eaba-113">Possible return values include the following:</span></span>



| <span data-ttu-id="6eaba-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6eaba-114">Return code</span></span>                                                                                   | <span data-ttu-id="6eaba-115">Description</span><span class="sxs-lookup"><span data-stu-id="6eaba-115">Description</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6eaba-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6eaba-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6eaba-117">成功。</span><span class="sxs-lookup"><span data-stu-id="6eaba-117">Success.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6eaba-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6eaba-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6eaba-119">無效引數。</span><span class="sxs-lookup"><span data-stu-id="6eaba-119">Invalid argument.</span></span><br/>                                             |
| <dl> <span data-ttu-id="6eaba-120"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="6eaba-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="6eaba-121">*PNext* 參數所指定的物件不是來源物件。</span><span class="sxs-lookup"><span data-stu-id="6eaba-121">Object specified by *pNext* parameter is not a source object.</span></span><br/> |
| <dl> <span data-ttu-id="6eaba-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6eaba-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6eaba-123">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="6eaba-123">**NULL** pointer argument.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="6eaba-124">備註</span><span class="sxs-lookup"><span data-stu-id="6eaba-124">Remarks</span></span>

<span data-ttu-id="6eaba-125">目前已執行，這個方法會捨棄對 *pNext* 的任何影響。</span><span class="sxs-lookup"><span data-stu-id="6eaba-125">As currently implemented, this method discards any effects on *pNext*.</span></span>

<span data-ttu-id="6eaba-126">若要讓這個方法成功， *pNext* 必須是目前來源物件的相符框架，定義如下：</span><span class="sxs-lookup"><span data-stu-id="6eaba-126">For this method to succeed, *pNext* must be a match frame of the current source object, defined as follows:</span></span>

-   <span data-ttu-id="6eaba-127">它必須共用相同的原始檔。</span><span class="sxs-lookup"><span data-stu-id="6eaba-127">It must share the same source file.</span></span>
-   <span data-ttu-id="6eaba-128">媒體開始時間必須等於目前來源的媒體停止時間。</span><span class="sxs-lookup"><span data-stu-id="6eaba-128">The media start time must equal the media stop time of the current source.</span></span>
-   <span data-ttu-id="6eaba-129">播放速率必須相同。</span><span class="sxs-lookup"><span data-stu-id="6eaba-129">The playback rate must be the same.</span></span> <span data-ttu-id="6eaba-130">播放速率是媒體持續時間除以時間軸持續時間。</span><span class="sxs-lookup"><span data-stu-id="6eaba-130">Playback rate is media duration divided by timeline duration.</span></span>

> [!Note]  
> <span data-ttu-id="6eaba-131">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6eaba-131">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6eaba-132">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6eaba-132">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6eaba-133">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6eaba-133">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6eaba-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="6eaba-134">Requirements</span></span>



| <span data-ttu-id="6eaba-135">需求</span><span class="sxs-lookup"><span data-stu-id="6eaba-135">Requirement</span></span> | <span data-ttu-id="6eaba-136">值</span><span class="sxs-lookup"><span data-stu-id="6eaba-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaba-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6eaba-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6eaba-138"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6eaba-138"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6eaba-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="6eaba-139">Library</span></span><br/> | <dl> <span data-ttu-id="6eaba-140"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eaba-140"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eaba-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6eaba-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eaba-142">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="6eaba-142">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="6eaba-143">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="6eaba-143">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




