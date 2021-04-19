---
description: SetRecompFormatFromSource 方法會使用原始檔中的壓縮格式來設定影片 recompression 格式。
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'IAMTimelineGroup：： SetRecompFormatFromSource 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980170"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a><span data-ttu-id="01ece-103">IAMTimelineGroup：： SetRecompFormatFromSource 方法</span><span class="sxs-lookup"><span data-stu-id="01ece-103">IAMTimelineGroup::SetRecompFormatFromSource method</span></span>

> [!Note]  
> <span data-ttu-id="01ece-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="01ece-104">\[Deprecated.</span></span> <span data-ttu-id="01ece-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="01ece-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="01ece-106">`SetRecompFormatFromSource`方法會使用原始檔中的壓縮格式來設定影片 recompression 格式。</span><span class="sxs-lookup"><span data-stu-id="01ece-106">The `SetRecompFormatFromSource` method sets the video recompression format using the compression format from a source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ece-107">語法</span><span class="sxs-lookup"><span data-stu-id="01ece-107">Syntax</span></span>


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="01ece-108">參數</span><span class="sxs-lookup"><span data-stu-id="01ece-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ece-109">*pSource*</span><span class="sxs-lookup"><span data-stu-id="01ece-109">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="01ece-110">來源物件之 [**IAMTimelineSrc**](iamtimelinesrc.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="01ece-110">Pointer to the [**IAMTimelineSrc**](iamtimelinesrc.md) interface of the source object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ece-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="01ece-111">Return value</span></span>

<span data-ttu-id="01ece-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="01ece-112">Returns an **HRESULT** values.</span></span> <span data-ttu-id="01ece-113">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="01ece-113">Possible values include the following.</span></span>



| <span data-ttu-id="01ece-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="01ece-114">Return code</span></span>                                                                                             | <span data-ttu-id="01ece-115">Description</span><span class="sxs-lookup"><span data-stu-id="01ece-115">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01ece-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="01ece-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="01ece-117">成功。</span><span class="sxs-lookup"><span data-stu-id="01ece-117">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="01ece-118"><dt>**E \_ NO \_ 時間軸**</dt></span><span class="sxs-lookup"><span data-stu-id="01ece-118"><dt>**E\_NO\_TIMELINE**</dt></span></span> </dl>          | <span data-ttu-id="01ece-119">群組不在時間軸內。</span><span class="sxs-lookup"><span data-stu-id="01ece-119">The group is not within a timeline.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="01ece-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="01ece-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="01ece-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="01ece-121">Insufficient memory.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="01ece-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="01ece-122"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="01ece-123">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="01ece-123">**NULL** pointer argument.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="01ece-124"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="01ece-124"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="01ece-125">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="01ece-125">Invalid media type.</span></span> <span data-ttu-id="01ece-126">群組不是影片群組，或原始程式檔沒有影片串流。</span><span class="sxs-lookup"><span data-stu-id="01ece-126">The group is not a video group, or the source file has no video stream.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="01ece-127">備註</span><span class="sxs-lookup"><span data-stu-id="01ece-127">Remarks</span></span>

<span data-ttu-id="01ece-128">這個方法會尋找與 *pSource* 相關聯的原始程式檔、捕獲檔案中第一個影片資料流程的媒體類型，並使用該類型設定群組壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="01ece-128">This method finds the source file associated with *pSource*, retrieves the media type of the first video stream in the file, and sets the group compression format using that type.</span></span> <span data-ttu-id="01ece-129">如需壓縮格式的詳細資訊，請參閱 [**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)。</span><span class="sxs-lookup"><span data-stu-id="01ece-129">For more information about compression formats, see [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span></span>

> [!Note]  
> <span data-ttu-id="01ece-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="01ece-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="01ece-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="01ece-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="01ece-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="01ece-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01ece-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="01ece-133">Requirements</span></span>



| <span data-ttu-id="01ece-134">需求</span><span class="sxs-lookup"><span data-stu-id="01ece-134">Requirement</span></span> | <span data-ttu-id="01ece-135">值</span><span class="sxs-lookup"><span data-stu-id="01ece-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01ece-136">標頭</span><span class="sxs-lookup"><span data-stu-id="01ece-136">Header</span></span><br/>  | <dl> <span data-ttu-id="01ece-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="01ece-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="01ece-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="01ece-138">Library</span></span><br/> | <dl> <span data-ttu-id="01ece-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="01ece-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01ece-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01ece-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ece-141">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="01ece-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="01ece-142">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="01ece-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




