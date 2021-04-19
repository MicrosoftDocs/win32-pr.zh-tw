---
description: BufferCB 方法是可接收範例緩衝區指標的回呼方法。
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'ISampleGrabberCB：： BufferCB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001936"
---
# <a name="isamplegrabbercbbuffercb-method"></a><span data-ttu-id="87273-103">ISampleGrabberCB：： BufferCB 方法</span><span class="sxs-lookup"><span data-stu-id="87273-103">ISampleGrabberCB::BufferCB method</span></span>

> [!Note]  
> <span data-ttu-id="87273-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="87273-104">\[Deprecated.</span></span> <span data-ttu-id="87273-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="87273-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="87273-106">**BufferCB** 方法是可接收範例緩衝區指標的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="87273-106">The **BufferCB** method is a callback method that receives a pointer to the sample buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="87273-107">語法</span><span class="sxs-lookup"><span data-stu-id="87273-107">Syntax</span></span>


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a><span data-ttu-id="87273-108">參數</span><span class="sxs-lookup"><span data-stu-id="87273-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87273-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="87273-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="87273-110">取樣的開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="87273-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="87273-111">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="87273-111">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="87273-112">包含範例資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="87273-112">Pointer to a buffer that contains the sample data.</span></span> <span data-ttu-id="87273-113">資料的格式取決於範例抓取器輸入釘選的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="87273-113">The format of the data depends on the media type of the Sample Grabber's input pin.</span></span> <span data-ttu-id="87273-114">若要取得媒體類型，請呼叫 [**ISampleGrabber：： GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md)。</span><span class="sxs-lookup"><span data-stu-id="87273-114">To get the media type, call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="87273-115">*BufferLen*</span><span class="sxs-lookup"><span data-stu-id="87273-115">*BufferLen*</span></span> 
</dt> <dd>

<span data-ttu-id="87273-116">*PBuffer* 所指向之緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="87273-116">Length of the buffer pointed to by *pBuffer*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87273-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="87273-117">Return value</span></span>

<span data-ttu-id="87273-118">\_如果成功，則傳回 [確定]，否則傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="87273-118">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87273-119">備註</span><span class="sxs-lookup"><span data-stu-id="87273-119">Remarks</span></span>

<span data-ttu-id="87273-120">此回呼方法會接收最新媒體範例中的資料指標。</span><span class="sxs-lookup"><span data-stu-id="87273-120">This callback method receives a pointer to the data in the most recent media sample.</span></span>

> [!Note]  
> <span data-ttu-id="87273-121">這個方法會接收原始範例資料的指標，而不是複本。</span><span class="sxs-lookup"><span data-stu-id="87273-121">This method receives a pointer to the original sample data, not a copy.</span></span> <span data-ttu-id="87273-122">原始檔案不正確地指定 *pBuffer* 包含一份資料複本。</span><span class="sxs-lookup"><span data-stu-id="87273-122">The original documentation incorrectly stated that *pBuffer* contains a copy of the data.</span></span>

 

<span data-ttu-id="87273-123">若要設定回呼，請呼叫 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md)。</span><span class="sxs-lookup"><span data-stu-id="87273-123">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="87273-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="87273-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="87273-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="87273-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="87273-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="87273-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87273-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="87273-127">Requirements</span></span>



| <span data-ttu-id="87273-128">需求</span><span class="sxs-lookup"><span data-stu-id="87273-128">Requirement</span></span> | <span data-ttu-id="87273-129">值</span><span class="sxs-lookup"><span data-stu-id="87273-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87273-130">標頭</span><span class="sxs-lookup"><span data-stu-id="87273-130">Header</span></span><br/>  | <dl> <span data-ttu-id="87273-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="87273-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="87273-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="87273-132">Library</span></span><br/> | <dl> <span data-ttu-id="87273-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="87273-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87273-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87273-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87273-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="87273-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="87273-136">**ISampleGrabberCB 介面**</span><span class="sxs-lookup"><span data-stu-id="87273-136">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




