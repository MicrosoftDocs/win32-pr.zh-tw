---
description: 回呼，會通知主機相關要求所傳回的畫面格緩衝區資訊。
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109245"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span data-ttu-id="c86a3-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="c86a3-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback method</span></span>

<span data-ttu-id="c86a3-104">回呼，會通知主機相關要求所傳回的畫面格緩衝區資訊。</span><span class="sxs-lookup"><span data-stu-id="c86a3-104">A callback that notifies the host of framebuffer information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="c86a3-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="c86a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="c86a3-106">Parameters</span></span>

<span data-ttu-id="c86a3-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="c86a3-107">*frameNumber* </span></span>  
<span data-ttu-id="c86a3-108">畫面格編號。</span><span class="sxs-lookup"><span data-stu-id="c86a3-108">The frame number.</span></span>

<span data-ttu-id="c86a3-109">*寬度* </span><span class="sxs-lookup"><span data-stu-id="c86a3-109">*width* </span></span>  
<span data-ttu-id="c86a3-110">框架的寬度。</span><span class="sxs-lookup"><span data-stu-id="c86a3-110">The width of the frame.</span></span>

<span data-ttu-id="c86a3-111">*高度* </span><span class="sxs-lookup"><span data-stu-id="c86a3-111">*height* </span></span>  
<span data-ttu-id="c86a3-112">框架的高度。</span><span class="sxs-lookup"><span data-stu-id="c86a3-112">The height of the frame.</span></span>

<span data-ttu-id="c86a3-113">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="c86a3-113">*renderTargetPtr* </span></span>  
<span data-ttu-id="c86a3-114">結果來源的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="c86a3-114">The render target that the results come from.</span></span> <span data-ttu-id="c86a3-115">它一律是框架緩衝區要求所指定的位置，或者，如果不是繪製呼叫，則第一個 RTV 會 bount 至輸出來源。</span><span class="sxs-lookup"><span data-stu-id="c86a3-115">It is always a slot specified by the frame buffer request, or if not a draw call, then the first RTV bount to the output source.</span></span>

<span data-ttu-id="c86a3-116">*frameDuraction* </span><span class="sxs-lookup"><span data-stu-id="c86a3-116">*frameDuraction* </span></span>  
<span data-ttu-id="c86a3-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="c86a3-117">Not used.</span></span>

<span data-ttu-id="c86a3-118">*大小* </span><span class="sxs-lookup"><span data-stu-id="c86a3-118">*size* </span></span>  
<span data-ttu-id="c86a3-119">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c86a3-119">The size of the output buffer in bytes.</span></span>

<span data-ttu-id="c86a3-120">*count5 \_ 緩衝區* </span><span class="sxs-lookup"><span data-stu-id="c86a3-120">*count5\_buffer* </span></span>  
<span data-ttu-id="c86a3-121">以 R8G8B8A8 UNORM 格式呈現的轉譯目標內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c86a3-121">The contents of the render target in R8G8B8A8\_UNORM format.</span></span>

## <a name="return-value"></a><span data-ttu-id="c86a3-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c86a3-122">Return value</span></span>

<span data-ttu-id="c86a3-123">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c86a3-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c86a3-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c86a3-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c86a3-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c86a3-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c86a3-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c86a3-126">Header</span></span></p></td><td><span data-ttu-id="c86a3-127">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="c86a3-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c86a3-128"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="c86a3-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c86a3-129">**IFrameBufferCallback**</span><span class="sxs-lookup"><span data-stu-id="c86a3-129">**IFrameBufferCallback**</span></span>](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
