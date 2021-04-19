---
description: GetSampleGrabber 方法會抓取 ISampleGrabber 介面的指標，讓應用程式能夠從媒體資料流程中取出個別樣本。
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'IMediaDet：： GetSampleGrabber 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994686"
---
# <a name="imediadetgetsamplegrabber-method"></a><span data-ttu-id="ed6a6-103">IMediaDet：： GetSampleGrabber 方法</span><span class="sxs-lookup"><span data-stu-id="ed6a6-103">IMediaDet::GetSampleGrabber method</span></span>

> [!Note]  
> <span data-ttu-id="ed6a6-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-104">\[Deprecated.</span></span> <span data-ttu-id="ed6a6-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ed6a6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ed6a6-106">方法會抓取 `GetSampleGrabber` [**ISampleGrabber**](isamplegrabber.md) 介面的指標，此介面可讓應用程式從媒體資料流程中取出個別樣本。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-106">The `GetSampleGrabber` method retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface, which enables an application to retrieve individual samples from a media stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed6a6-107">語法</span><span class="sxs-lookup"><span data-stu-id="ed6a6-107">Syntax</span></span>


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="ed6a6-108">參數</span><span class="sxs-lookup"><span data-stu-id="ed6a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed6a6-109">*ppVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed6a6-109">*ppVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6a6-110">接收 [**ISampleGrabber**](isamplegrabber.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-110">Receives a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed6a6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed6a6-111">Return value</span></span>

<span data-ttu-id="ed6a6-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed6a6-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed6a6-114">備註</span><span class="sxs-lookup"><span data-stu-id="ed6a6-114">Remarks</span></span>

<span data-ttu-id="ed6a6-115">呼叫 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) ，然後再呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-115">Call [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) before calling this method.</span></span> <span data-ttu-id="ed6a6-116">[**ISampleGrabber**](isamplegrabber.md)介面可讓您從資料流程中取出個別的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-116">The [**ISampleGrabber**](isamplegrabber.md) interface enables you to retrieve individual media samples from the stream.</span></span> <span data-ttu-id="ed6a6-117">如果您只需要影片框架中的點陣圖，請改為呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-117">If you just need a bitmap from a video frame, call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method instead.</span></span> <span data-ttu-id="ed6a6-118">**ISampleGrabber** 介面更有彈性，但應用程式需要更多工作。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-118">The **ISampleGrabber** interface is more flexible, but requires more work by the application.</span></span>

<span data-ttu-id="ed6a6-119">如果這個方法成功，則傳回的 [**ISampleGrabber**](isamplegrabber.md) 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-119">If this method succeeds, the [**ISampleGrabber**](isamplegrabber.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="ed6a6-120">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="ed6a6-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ed6a6-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ed6a6-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ed6a6-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ed6a6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed6a6-124">Requirements</span></span>



| <span data-ttu-id="ed6a6-125">需求</span><span class="sxs-lookup"><span data-stu-id="ed6a6-125">Requirement</span></span> | <span data-ttu-id="ed6a6-126">值</span><span class="sxs-lookup"><span data-stu-id="ed6a6-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed6a6-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ed6a6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ed6a6-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed6a6-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ed6a6-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed6a6-129">Library</span></span><br/> | <dl> <span data-ttu-id="ed6a6-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed6a6-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed6a6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed6a6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed6a6-132">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="ed6a6-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="ed6a6-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ed6a6-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




