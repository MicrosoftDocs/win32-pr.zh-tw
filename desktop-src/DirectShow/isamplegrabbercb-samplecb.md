---
description: SampleCB 方法是一種回呼方法，可接收媒體範例的指標。
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'ISampleGrabberCB：： SampleCB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996255"
---
# <a name="isamplegrabbercbsamplecb-method"></a><span data-ttu-id="107b3-103">ISampleGrabberCB：： SampleCB 方法</span><span class="sxs-lookup"><span data-stu-id="107b3-103">ISampleGrabberCB::SampleCB method</span></span>

> [!Note]  
> <span data-ttu-id="107b3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="107b3-104">\[Deprecated.</span></span> <span data-ttu-id="107b3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="107b3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="107b3-106">`SampleCB`方法是可接收媒體範例指標的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="107b3-106">The `SampleCB` method is a callback method that receives a pointer to the media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="107b3-107">語法</span><span class="sxs-lookup"><span data-stu-id="107b3-107">Syntax</span></span>


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="107b3-108">參數</span><span class="sxs-lookup"><span data-stu-id="107b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="107b3-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="107b3-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="107b3-110">取樣的開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="107b3-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="107b3-111">*pSample*</span><span class="sxs-lookup"><span data-stu-id="107b3-111">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="107b3-112">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="107b3-112">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="107b3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="107b3-113">Return value</span></span>

<span data-ttu-id="107b3-114">\_如果成功，則傳回 [確定]，否則傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="107b3-114">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="107b3-115">備註</span><span class="sxs-lookup"><span data-stu-id="107b3-115">Remarks</span></span>

<span data-ttu-id="107b3-116">若要設定回呼，請呼叫 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md)。</span><span class="sxs-lookup"><span data-stu-id="107b3-116">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="107b3-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="107b3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="107b3-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="107b3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="107b3-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="107b3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="107b3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="107b3-120">Requirements</span></span>



| <span data-ttu-id="107b3-121">需求</span><span class="sxs-lookup"><span data-stu-id="107b3-121">Requirement</span></span> | <span data-ttu-id="107b3-122">值</span><span class="sxs-lookup"><span data-stu-id="107b3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="107b3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="107b3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="107b3-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="107b3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="107b3-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="107b3-125">Library</span></span><br/> | <dl> <span data-ttu-id="107b3-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="107b3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="107b3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="107b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107b3-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="107b3-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="107b3-129">**ISampleGrabberCB 介面**</span><span class="sxs-lookup"><span data-stu-id="107b3-129">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




