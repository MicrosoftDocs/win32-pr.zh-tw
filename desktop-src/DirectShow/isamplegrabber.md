---
description: ISampleGrabber 介面是由範例捕獲篩選器所公開。 它可讓應用程式在整個篩選圖形中移動時，取得個別的媒體範例。
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: 'ISampleGrabber 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976549"
---
# <a name="isamplegrabber-interface"></a><span data-ttu-id="43f95-104">ISampleGrabber 介面</span><span class="sxs-lookup"><span data-stu-id="43f95-104">ISampleGrabber interface</span></span>

> [!Note]  
> <span data-ttu-id="43f95-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="43f95-105">\[Deprecated.</span></span> <span data-ttu-id="43f95-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="43f95-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43f95-107">**ISampleGrabber** 介面是由 [**範例捕獲**](sample-grabber-filter.md)篩選器所公開。</span><span class="sxs-lookup"><span data-stu-id="43f95-107">The **ISampleGrabber** interface is exposed by the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="43f95-108">它可讓應用程式在整個篩選圖形中移動時，取得個別的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="43f95-108">It enables an application to retrieve individual media samples as they move through the filter graph.</span></span>

## <a name="members"></a><span data-ttu-id="43f95-109">成員</span><span class="sxs-lookup"><span data-stu-id="43f95-109">Members</span></span>

<span data-ttu-id="43f95-110">**ISampleGrabber** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="43f95-110">The **ISampleGrabber** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="43f95-111">**ISampleGrabber** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="43f95-111">**ISampleGrabber** also has these types of members:</span></span>

-   [<span data-ttu-id="43f95-112">方法</span><span class="sxs-lookup"><span data-stu-id="43f95-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43f95-113">方法</span><span class="sxs-lookup"><span data-stu-id="43f95-113">Methods</span></span>

<span data-ttu-id="43f95-114">**ISampleGrabber** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="43f95-114">The **ISampleGrabber** interface has these methods.</span></span>



| <span data-ttu-id="43f95-115">方法</span><span class="sxs-lookup"><span data-stu-id="43f95-115">Method</span></span>                                                                | <span data-ttu-id="43f95-116">描述</span><span class="sxs-lookup"><span data-stu-id="43f95-116">Description</span></span>                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43f95-117">**GetConnectedMediaType**</span><span class="sxs-lookup"><span data-stu-id="43f95-117">**GetConnectedMediaType**</span></span>](isamplegrabber-getconnectedmediatype.md) | <span data-ttu-id="43f95-118">抓取範例抓取之輸入 pin 的連接媒體類型。</span><span class="sxs-lookup"><span data-stu-id="43f95-118">Retrieves the media type for the connection on the input pin of Sample Grabber.</span></span><br/>                                        |
| [<span data-ttu-id="43f95-119">**GetCurrentBuffer**</span><span class="sxs-lookup"><span data-stu-id="43f95-119">**GetCurrentBuffer**</span></span>](isamplegrabber-getcurrentbuffer.md)           | <span data-ttu-id="43f95-120">抓取篩選器最近收到的範例複本。</span><span class="sxs-lookup"><span data-stu-id="43f95-120">Retrieves a copy of the sample that the filter received most recently.</span></span><br/>                                                 |
| [<span data-ttu-id="43f95-121">**GetCurrentSample**</span><span class="sxs-lookup"><span data-stu-id="43f95-121">**GetCurrentSample**</span></span>](isamplegrabber-getcurrentsample.md)           | <span data-ttu-id="43f95-122">未實作。</span><span class="sxs-lookup"><span data-stu-id="43f95-122">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="43f95-123">**SetBufferSamples**</span><span class="sxs-lookup"><span data-stu-id="43f95-123">**SetBufferSamples**</span></span>](isamplegrabber-setbuffersamples.md)           | <span data-ttu-id="43f95-124">指定是否在通過篩選時，將範例資料複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="43f95-124">Specifies whether to copy sample data into a buffer as it goes through the filter.</span></span><br/>                                     |
| [<span data-ttu-id="43f95-125">**SetCallback**</span><span class="sxs-lookup"><span data-stu-id="43f95-125">**SetCallback**</span></span>](isamplegrabber-setcallback.md)                     | <span data-ttu-id="43f95-126">指定要對傳入範例呼叫的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="43f95-126">Specifies a callback method to call on incoming samples.</span></span><br/>                                                               |
| [<span data-ttu-id="43f95-127">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="43f95-127">**SetMediaType**</span></span>](isamplegrabber-setmediatype.md)                   | <span data-ttu-id="43f95-128">在範例抓取程式的輸入釘選上指定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="43f95-128">Specifies the media type for the connection on the input pin of the Sample Grabber.</span></span><br/>                                    |
| [<span data-ttu-id="43f95-129">**SetOneShot**</span><span class="sxs-lookup"><span data-stu-id="43f95-129">**SetOneShot**</span></span>](isamplegrabber-setoneshot.md)                       | <span data-ttu-id="43f95-130">指定 [**範例**](sample-grabber-filter.md) 抓取篩選器是否會在篩選器收到範例後停止。</span><span class="sxs-lookup"><span data-stu-id="43f95-130">Specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43f95-131">備註</span><span class="sxs-lookup"><span data-stu-id="43f95-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43f95-132">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="43f95-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43f95-133">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="43f95-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43f95-134">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="43f95-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43f95-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="43f95-135">Requirements</span></span>



| <span data-ttu-id="43f95-136">需求</span><span class="sxs-lookup"><span data-stu-id="43f95-136">Requirement</span></span> | <span data-ttu-id="43f95-137">值</span><span class="sxs-lookup"><span data-stu-id="43f95-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43f95-138">標頭</span><span class="sxs-lookup"><span data-stu-id="43f95-138">Header</span></span><br/>  | <dl> <span data-ttu-id="43f95-139"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="43f95-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="43f95-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="43f95-140">Library</span></span><br/> | <dl> <span data-ttu-id="43f95-141"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43f95-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f95-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43f95-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f95-143">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="43f95-143">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 
