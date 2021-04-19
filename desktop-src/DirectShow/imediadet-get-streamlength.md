---
description: Get \_ StreamLength 方法會抓取目前資料流程的持續時間。
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'IMediaDet：： get_StreamLength 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 61fe92fcb845a626fafc8ebb49126a35cf633aea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990083"
---
# <a name="imediadetget_streamlength-method"></a><span data-ttu-id="b35f2-103">IMediaDet：： get \_ StreamLength 方法</span><span class="sxs-lookup"><span data-stu-id="b35f2-103">IMediaDet::get\_StreamLength method</span></span>

> [!Note]  
> <span data-ttu-id="b35f2-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b35f2-104">\[Deprecated.</span></span> <span data-ttu-id="b35f2-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b35f2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b35f2-106">方法會抓取 `get_StreamLength` 目前資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="b35f2-106">The `get_StreamLength` method retrieves the duration of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35f2-107">語法</span><span class="sxs-lookup"><span data-stu-id="b35f2-107">Syntax</span></span>


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b35f2-108">參數</span><span class="sxs-lookup"><span data-stu-id="b35f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b35f2-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="b35f2-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b35f2-110">接收資料流程的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b35f2-110">Receives the duration of the stream, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b35f2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b35f2-111">Return value</span></span>

<span data-ttu-id="b35f2-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b35f2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b35f2-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b35f2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b35f2-114">備註</span><span class="sxs-lookup"><span data-stu-id="b35f2-114">Remarks</span></span>

<span data-ttu-id="b35f2-115">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="b35f2-115">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="b35f2-116">如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="b35f2-116">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="b35f2-117">如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。</span><span class="sxs-lookup"><span data-stu-id="b35f2-117">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="b35f2-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b35f2-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b35f2-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b35f2-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b35f2-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b35f2-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b35f2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b35f2-121">Requirements</span></span>



| <span data-ttu-id="b35f2-122">需求</span><span class="sxs-lookup"><span data-stu-id="b35f2-122">Requirement</span></span> | <span data-ttu-id="b35f2-123">值</span><span class="sxs-lookup"><span data-stu-id="b35f2-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b35f2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b35f2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b35f2-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b35f2-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b35f2-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="b35f2-126">Library</span></span><br/> | <dl> <span data-ttu-id="b35f2-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b35f2-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b35f2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b35f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35f2-129">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="b35f2-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="b35f2-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="b35f2-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




