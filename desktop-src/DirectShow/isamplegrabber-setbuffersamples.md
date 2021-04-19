---
description: SetBufferSamples 方法會指定是否要在經過篩選時，將範例資料複製到緩衝區。
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'ISampleGrabber：： SetBufferSamples 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990710"
---
# <a name="isamplegrabbersetbuffersamples-method"></a><span data-ttu-id="d2bf8-103">ISampleGrabber：： SetBufferSamples 方法</span><span class="sxs-lookup"><span data-stu-id="d2bf8-103">ISampleGrabber::SetBufferSamples method</span></span>

> [!Note]  
> <span data-ttu-id="d2bf8-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-104">\[Deprecated.</span></span> <span data-ttu-id="d2bf8-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d2bf8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2bf8-106">**SetBufferSamples** 方法會指定是否要在經過篩選時，將範例資料複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-106">The **SetBufferSamples** method specifies whether to copy sample data into a buffer as it goes through the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2bf8-107">語法</span><span class="sxs-lookup"><span data-stu-id="d2bf8-107">Syntax</span></span>


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a><span data-ttu-id="d2bf8-108">參數</span><span class="sxs-lookup"><span data-stu-id="d2bf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2bf8-109">*BufferThem*</span><span class="sxs-lookup"><span data-stu-id="d2bf8-109">*BufferThem*</span></span> 
</dt> <dd>

<span data-ttu-id="d2bf8-110">指定是否要緩衝範例資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-110">Boolean value specifying whether to buffer sample data.</span></span> <span data-ttu-id="d2bf8-111">若 **為 TRUE**，則篩選會將範例資料複製到內部緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-111">If **TRUE**, the filter copies sample data into an internal buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2bf8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2bf8-112">Return value</span></span>

<span data-ttu-id="d2bf8-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2bf8-114">備註</span><span class="sxs-lookup"><span data-stu-id="d2bf8-114">Remarks</span></span>

<span data-ttu-id="d2bf8-115">若要取得複製的緩衝區，請呼叫 [**ISampleGrabber：： GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-115">To get the copied buffer, call [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="d2bf8-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2bf8-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d2bf8-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d2bf8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2bf8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2bf8-119">Requirements</span></span>



| <span data-ttu-id="d2bf8-120">需求</span><span class="sxs-lookup"><span data-stu-id="d2bf8-120">Requirement</span></span> | <span data-ttu-id="d2bf8-121">值</span><span class="sxs-lookup"><span data-stu-id="d2bf8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2bf8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d2bf8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d2bf8-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2bf8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d2bf8-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2bf8-124">Library</span></span><br/> | <dl> <span data-ttu-id="d2bf8-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2bf8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2bf8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2bf8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2bf8-127">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="d2bf8-127">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="d2bf8-128">**ISampleGrabber 介面**</span><span class="sxs-lookup"><span data-stu-id="d2bf8-128">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




