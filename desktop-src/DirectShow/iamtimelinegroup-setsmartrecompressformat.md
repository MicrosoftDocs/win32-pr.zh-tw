---
description: SetSmartRecompressFormat 方法會指定要用於智慧型 recompression 的影片壓縮格式。
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'IAMTimelineGroup：： SetSmartRecompressFormat 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995959"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a><span data-ttu-id="53959-103">IAMTimelineGroup：： SetSmartRecompressFormat 方法</span><span class="sxs-lookup"><span data-stu-id="53959-103">IAMTimelineGroup::SetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="53959-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="53959-104">\[Deprecated.</span></span> <span data-ttu-id="53959-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="53959-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53959-106">`SetSmartRecompressFormat`方法會指定要用於智慧型 recompression 的影片壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="53959-106">The `SetSmartRecompressFormat` method specifies a video compression format to use for smart recompression.</span></span>

<span data-ttu-id="53959-107">音訊群組不支援 Smart recompression。</span><span class="sxs-lookup"><span data-stu-id="53959-107">Smart recompression is not supported for audio groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="53959-108">語法</span><span class="sxs-lookup"><span data-stu-id="53959-108">Syntax</span></span>


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="53959-109">參數</span><span class="sxs-lookup"><span data-stu-id="53959-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53959-110">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="53959-110">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="53959-111">描述壓縮格式之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="53959-111">Pointer to a structure describing the compression format.</span></span> <span data-ttu-id="53959-112">目前，只有 [**SCompFmt0**](scompfmt0.md) 結構有效。</span><span class="sxs-lookup"><span data-stu-id="53959-112">Currently, only the [**SCompFmt0**](scompfmt0.md) structure is valid.</span></span> <span data-ttu-id="53959-113">您必須將此參數轉換為 **long** 類型的指標。</span><span class="sxs-lookup"><span data-stu-id="53959-113">You must cast this parameter to a pointer of type **long**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53959-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="53959-114">Return value</span></span>

<span data-ttu-id="53959-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="53959-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53959-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53959-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53959-117">備註</span><span class="sxs-lookup"><span data-stu-id="53959-117">Remarks</span></span>

<span data-ttu-id="53959-118">在呼叫這個方法之前，請在相同群組上呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md) 方法，以指定未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="53959-118">Before calling this method, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method on the same group, to specify an uncompressed format.</span></span>

<span data-ttu-id="53959-119">如果 `SetSmartRecompressFormat` 方法成功，您可以使用智慧型轉譯引擎來輸出壓縮的影片資料流程。</span><span class="sxs-lookup"><span data-stu-id="53959-119">If the `SetSmartRecompressFormat` method succeeds, you can use the Smart Render Engine to output a compressed video stream.</span></span> <span data-ttu-id="53959-120">壓縮的影片將會有在 *pformatetc 架構* 參數中指定的寬度、高度和畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="53959-120">The compressed video will have the width, height, and frame rate that was specified in the *pFormat* parameter.</span></span> <span data-ttu-id="53959-121">這些值將會覆寫 **SetMediaType** 方法中針對未壓縮格式所指定的值。</span><span class="sxs-lookup"><span data-stu-id="53959-121">These values will override those given for the uncompressed format in the **SetMediaType** method.</span></span> <span data-ttu-id="53959-122">不過，若要取得智慧 recompression 的優點，這兩種格式應該相符。</span><span class="sxs-lookup"><span data-stu-id="53959-122">However, to get the benefits of smart recompression, the two formats should match.</span></span> <span data-ttu-id="53959-123">換句話說，壓縮和未壓縮的格式應該具有相同的高度、寬度和畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="53959-123">In other words, the compressed and uncompressed formats should have the same height, width, and frame rate.</span></span>

<span data-ttu-id="53959-124">如果智慧型轉譯引擎無法產生壓縮的格式，則會改為產生未壓縮的影片資料流程。</span><span class="sxs-lookup"><span data-stu-id="53959-124">If the Smart Render Engine is unable to produce the compressed format, it will produce an uncompressed video stream instead.</span></span> <span data-ttu-id="53959-125">如果發生這種情況，智慧轉譯引擎會報告 DEX \_ 識別碼在 \_ \_ \_ [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法期間找不到壓縮程式轉譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="53959-125">If that occurs, the Smart Render Engine reports a DEX\_IDS\_CANT\_FIND\_COMPRESSOR rendering error during the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="53959-126">應用程式可以透過 [**IAMErrorLog：： LogError**](iamerrorlog-logerror.md) 方法攔截這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="53959-126">The application can catch this error through the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="53959-127"> (如需詳細資訊，請參閱 [記錄錯誤](logging-errors.md) 和轉譯 [錯誤](rendering-errors.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="53959-127">(For more information, see [Logging Errors](logging-errors.md) and [Rendering Errors](rendering-errors.md).)</span></span>

<span data-ttu-id="53959-128">智慧型 recompression 格式不是持續性。</span><span class="sxs-lookup"><span data-stu-id="53959-128">The smart recompression format is not persistent.</span></span> <span data-ttu-id="53959-129">如果應用程式使用智慧型 recompression，它必須在每次載入專案檔時設定 recompression 格式。</span><span class="sxs-lookup"><span data-stu-id="53959-129">If an application uses smart recompression, it must set the recompression format whenever it loads a project file.</span></span>

> [!Note]  
> <span data-ttu-id="53959-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="53959-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53959-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="53959-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53959-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="53959-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53959-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="53959-133">Requirements</span></span>



| <span data-ttu-id="53959-134">需求</span><span class="sxs-lookup"><span data-stu-id="53959-134">Requirement</span></span> | <span data-ttu-id="53959-135">值</span><span class="sxs-lookup"><span data-stu-id="53959-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53959-136">標頭</span><span class="sxs-lookup"><span data-stu-id="53959-136">Header</span></span><br/>  | <dl> <span data-ttu-id="53959-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="53959-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53959-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="53959-138">Library</span></span><br/> | <dl> <span data-ttu-id="53959-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="53959-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53959-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53959-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53959-141">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="53959-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="53959-142">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="53959-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="53959-143">智慧型轉譯引擎</span><span class="sxs-lookup"><span data-stu-id="53959-143">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> <dt>

[<span data-ttu-id="53959-144">將專案寫入檔案</span><span class="sxs-lookup"><span data-stu-id="53959-144">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




