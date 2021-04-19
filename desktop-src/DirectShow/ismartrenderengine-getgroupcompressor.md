---
description: GetGroupCompressor 方法會抓取指定群組的壓縮篩選。
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'ISmartRenderEngine：： GetGroupCompressor 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978729"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a><span data-ttu-id="0e752-103">ISmartRenderEngine：： GetGroupCompressor 方法</span><span class="sxs-lookup"><span data-stu-id="0e752-103">ISmartRenderEngine::GetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="0e752-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="0e752-104">\[Deprecated.</span></span> <span data-ttu-id="0e752-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="0e752-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e752-106">方法會抓取 `GetGroupCompressor` 指定群組的壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="0e752-106">The `GetGroupCompressor` method retrieves the compression filter for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e752-107">語法</span><span class="sxs-lookup"><span data-stu-id="0e752-107">Syntax</span></span>


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="0e752-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e752-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e752-109">*群組*</span><span class="sxs-lookup"><span data-stu-id="0e752-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="0e752-110">群組以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="0e752-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="0e752-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="0e752-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="0e752-112">接收壓縮篩選之 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0e752-112">Receives a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span> <span data-ttu-id="0e752-113">如果沒有壓縮篩選，則會接收 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="0e752-113">It receives the value **NULL** if there is no compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e752-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e752-114">Return value</span></span>

<span data-ttu-id="0e752-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0e752-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e752-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0e752-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e752-117">備註</span><span class="sxs-lookup"><span data-stu-id="0e752-117">Remarks</span></span>

<span data-ttu-id="0e752-118">使用這個方法可設定壓縮篩選的屬性，例如，主要畫面格速率。</span><span class="sxs-lookup"><span data-stu-id="0e752-118">Use this method to set properties on the compression filter, such as the key-frame rate.</span></span> <span data-ttu-id="0e752-119">請在呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md)之後，但在轉譯專案之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0e752-119">Call this method after calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), but before rendering the project.</span></span> <span data-ttu-id="0e752-120">然後查詢壓縮篩選器的輸出圖釘以取得 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面，其中包含設定壓縮參數的方法。</span><span class="sxs-lookup"><span data-stu-id="0e752-120">Then query the compression filter's output pin for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, which contains methods for setting compression parameters.</span></span> <span data-ttu-id="0e752-121">當您完成時，請釋放介面。</span><span class="sxs-lookup"><span data-stu-id="0e752-121">Release the interface when you are done.</span></span> <span data-ttu-id="0e752-122">如果您對時間軸進行任何後續的變更，請呼叫 **ConnectFrontEnd**，然後再次呼叫 **GetGroupCompressor** ，以重設壓縮參數。</span><span class="sxs-lookup"><span data-stu-id="0e752-122">If you make any subsequent changes to the timeline, call **ConnectFrontEnd**, and then call **GetGroupCompressor** again to reset the compression parameters.</span></span>

<span data-ttu-id="0e752-123">傳回時，如果 pCompressor 的值 \* 為非 **Null**，則 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="0e752-123">On return, if the value of \**pCompressor* is non-**NULL**, the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface has an outstanding reference count.</span></span> <span data-ttu-id="0e752-124">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="0e752-124">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="0e752-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="0e752-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e752-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0e752-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e752-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="0e752-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e752-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e752-128">Requirements</span></span>



| <span data-ttu-id="0e752-129">需求</span><span class="sxs-lookup"><span data-stu-id="0e752-129">Requirement</span></span> | <span data-ttu-id="0e752-130">值</span><span class="sxs-lookup"><span data-stu-id="0e752-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e752-131">標頭</span><span class="sxs-lookup"><span data-stu-id="0e752-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0e752-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e752-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e752-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e752-133">Library</span></span><br/> | <dl> <span data-ttu-id="0e752-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e752-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e752-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e752-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e752-136">**ISmartRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="0e752-136">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="0e752-137">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="0e752-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




