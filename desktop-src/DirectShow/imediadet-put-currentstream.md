---
description: Put \_ CurrentStream 方法會指定要使用之媒體偵測器的串流號碼。
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: 'IMediaDet：:p ut_CurrentStream 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000399"
---
# <a name="imediadetput_currentstream-method"></a><span data-ttu-id="97deb-103">IMediaDet：:p 的 \_ CurrentStream 方法</span><span class="sxs-lookup"><span data-stu-id="97deb-103">IMediaDet::put\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="97deb-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="97deb-104">\[Deprecated.</span></span> <span data-ttu-id="97deb-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="97deb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="97deb-106">`put_CurrentStream`方法會指定要使用之媒體偵測器的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="97deb-106">The `put_CurrentStream` method specifies the stream number for the media detector to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="97deb-107">語法</span><span class="sxs-lookup"><span data-stu-id="97deb-107">Syntax</span></span>


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="97deb-108">參數</span><span class="sxs-lookup"><span data-stu-id="97deb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97deb-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97deb-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97deb-110">資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="97deb-110">Stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97deb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="97deb-111">Return value</span></span>

<span data-ttu-id="97deb-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="97deb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="97deb-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="97deb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="97deb-114">備註</span><span class="sxs-lookup"><span data-stu-id="97deb-114">Remarks</span></span>

<span data-ttu-id="97deb-115">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p 的 \_**](imediadet-put-filename.md) 檔案名稱，以設定檔案名。</span><span class="sxs-lookup"><span data-stu-id="97deb-115">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="97deb-116">呼叫 [**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md) ，以判斷原始程式檔中包含的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="97deb-116">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to determine the number of streams contained in the source file.</span></span>

<span data-ttu-id="97deb-117">如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="97deb-117">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="97deb-118">如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。</span><span class="sxs-lookup"><span data-stu-id="97deb-118">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="97deb-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="97deb-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="97deb-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="97deb-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="97deb-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="97deb-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97deb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="97deb-122">Requirements</span></span>



| <span data-ttu-id="97deb-123">需求</span><span class="sxs-lookup"><span data-stu-id="97deb-123">Requirement</span></span> | <span data-ttu-id="97deb-124">值</span><span class="sxs-lookup"><span data-stu-id="97deb-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97deb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="97deb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="97deb-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="97deb-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="97deb-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="97deb-127">Library</span></span><br/> | <dl> <span data-ttu-id="97deb-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97deb-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97deb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97deb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97deb-130">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="97deb-130">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="97deb-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="97deb-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




