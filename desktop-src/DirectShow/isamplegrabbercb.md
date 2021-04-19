---
description: ISampleGrabberCB 介面提供 ISampleGrabber：： SetCallback 方法的回呼方法。 如果您的應用程式呼叫該方法，則必須執行這個介面。 如需詳細資訊，請參閱 ISampleGrabber。
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: 'ISampleGrabberCB 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994223"
---
# <a name="isamplegrabbercb-interface"></a><span data-ttu-id="564bb-105">ISampleGrabberCB 介面</span><span class="sxs-lookup"><span data-stu-id="564bb-105">ISampleGrabberCB interface</span></span>

> [!Note]  
> <span data-ttu-id="564bb-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="564bb-106">\[Deprecated.</span></span> <span data-ttu-id="564bb-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="564bb-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="564bb-108">`ISampleGrabberCB`介面提供 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md)方法的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="564bb-108">The `ISampleGrabberCB` interface provides callback methods for the [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) method.</span></span> <span data-ttu-id="564bb-109">如果您的應用程式呼叫該方法，則必須執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="564bb-109">If your application calls that method, it must implement this interface.</span></span> <span data-ttu-id="564bb-110">如需詳細資訊，請參閱 [**ISampleGrabber**](isamplegrabber.md)。</span><span class="sxs-lookup"><span data-stu-id="564bb-110">For more information, see [**ISampleGrabber**](isamplegrabber.md).</span></span>

## <a name="members"></a><span data-ttu-id="564bb-111">成員</span><span class="sxs-lookup"><span data-stu-id="564bb-111">Members</span></span>

<span data-ttu-id="564bb-112">**ISampleGrabberCB** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="564bb-112">The **ISampleGrabberCB** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="564bb-113">**ISampleGrabberCB** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="564bb-113">**ISampleGrabberCB** also has these types of members:</span></span>

-   [<span data-ttu-id="564bb-114">方法</span><span class="sxs-lookup"><span data-stu-id="564bb-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="564bb-115">方法</span><span class="sxs-lookup"><span data-stu-id="564bb-115">Methods</span></span>

<span data-ttu-id="564bb-116">**ISampleGrabberCB** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="564bb-116">The **ISampleGrabberCB** interface has these methods.</span></span>



| <span data-ttu-id="564bb-117">方法</span><span class="sxs-lookup"><span data-stu-id="564bb-117">Method</span></span>                                        | <span data-ttu-id="564bb-118">描述</span><span class="sxs-lookup"><span data-stu-id="564bb-118">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="564bb-119">**BufferCB**</span><span class="sxs-lookup"><span data-stu-id="564bb-119">**BufferCB**</span></span>](isamplegrabbercb-buffercb.md) | <span data-ttu-id="564bb-120">回呼方法，這個方法會接收範例緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="564bb-120">Callback method that receives a pointer to the sample buffer.</span></span><br/> |
| [<span data-ttu-id="564bb-121">**SampleCB**</span><span class="sxs-lookup"><span data-stu-id="564bb-121">**SampleCB**</span></span>](isamplegrabbercb-samplecb.md) | <span data-ttu-id="564bb-122">回呼方法，這個方法會接收媒體範例的指標。</span><span class="sxs-lookup"><span data-stu-id="564bb-122">Callback method that receives a pointer to the media sample.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="564bb-123">備註</span><span class="sxs-lookup"><span data-stu-id="564bb-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="564bb-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="564bb-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="564bb-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="564bb-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="564bb-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="564bb-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="564bb-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="564bb-127">Requirements</span></span>



| <span data-ttu-id="564bb-128">需求</span><span class="sxs-lookup"><span data-stu-id="564bb-128">Requirement</span></span> | <span data-ttu-id="564bb-129">值</span><span class="sxs-lookup"><span data-stu-id="564bb-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="564bb-130">標頭</span><span class="sxs-lookup"><span data-stu-id="564bb-130">Header</span></span><br/>  | <dl> <span data-ttu-id="564bb-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="564bb-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="564bb-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="564bb-132">Library</span></span><br/> | <dl> <span data-ttu-id="564bb-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="564bb-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
