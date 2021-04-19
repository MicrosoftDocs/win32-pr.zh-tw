---
description: Get \_ OutputStreams 方法會抓取媒體來源中包含的音訊和影片資料流程數目。 任何其他資料流程類型（例如資料流程）都會被忽略。
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'IMediaDet：： get_OutputStreams 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991162"
---
# <a name="imediadetget_outputstreams-method"></a><span data-ttu-id="3b37c-104">IMediaDet：： get \_ OutputStreams 方法</span><span class="sxs-lookup"><span data-stu-id="3b37c-104">IMediaDet::get\_OutputStreams method</span></span>

> [!Note]  
> <span data-ttu-id="3b37c-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3b37c-105">\[Deprecated.</span></span> <span data-ttu-id="3b37c-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3b37c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3b37c-107">方法會抓取 `get_OutputStreams` 媒體來源中包含的音訊和影片資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="3b37c-107">The `get_OutputStreams` method retrieves the number of audio and video streams contained in the media source.</span></span> <span data-ttu-id="3b37c-108">任何其他資料流程類型（例如資料流程）都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="3b37c-108">Any other stream types, such as data streams, are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b37c-109">語法</span><span class="sxs-lookup"><span data-stu-id="3b37c-109">Syntax</span></span>


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3b37c-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b37c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b37c-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="3b37c-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3b37c-112">接收輸出資料流程的數目。</span><span class="sxs-lookup"><span data-stu-id="3b37c-112">Receives the number of output streams.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b37c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b37c-113">Return value</span></span>

<span data-ttu-id="3b37c-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3b37c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b37c-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b37c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b37c-116">備註</span><span class="sxs-lookup"><span data-stu-id="3b37c-116">Remarks</span></span>

<span data-ttu-id="3b37c-117">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p 的 \_**](imediadet-put-filename.md) 檔案名稱，以設定檔案名。</span><span class="sxs-lookup"><span data-stu-id="3b37c-117">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="3b37c-118">如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="3b37c-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="3b37c-119">如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。</span><span class="sxs-lookup"><span data-stu-id="3b37c-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="3b37c-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3b37c-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b37c-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3b37c-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3b37c-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3b37c-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b37c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b37c-123">Requirements</span></span>



| <span data-ttu-id="3b37c-124">需求</span><span class="sxs-lookup"><span data-stu-id="3b37c-124">Requirement</span></span> | <span data-ttu-id="3b37c-125">值</span><span class="sxs-lookup"><span data-stu-id="3b37c-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b37c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3b37c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3b37c-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b37c-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3b37c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b37c-128">Library</span></span><br/> | <dl> <span data-ttu-id="3b37c-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b37c-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b37c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b37c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b37c-131">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="3b37c-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="3b37c-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="3b37c-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




