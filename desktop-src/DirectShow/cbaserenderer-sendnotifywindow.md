---
description: SendNotifyWindow 方法會通知影片視窗控制碼的上游篩選。
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: 'CBaseRenderer. SendNotifyWindow 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990574"
---
# <a name="cbaserenderersendnotifywindow-method"></a><span data-ttu-id="31527-103">CBaseRenderer. SendNotifyWindow 方法</span><span class="sxs-lookup"><span data-stu-id="31527-103">CBaseRenderer.SendNotifyWindow method</span></span>

<span data-ttu-id="31527-104">`SendNotifyWindow`方法會通知影片視窗控制碼的上游篩選。</span><span class="sxs-lookup"><span data-stu-id="31527-104">The `SendNotifyWindow` method notifies the upstream filter of the video window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="31527-105">語法</span><span class="sxs-lookup"><span data-stu-id="31527-105">Syntax</span></span>


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="31527-106">參數</span><span class="sxs-lookup"><span data-stu-id="31527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31527-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="31527-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="31527-108">上游篩選器輸出釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="31527-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the upstream filter's output pin.</span></span>

</dd> <dt>

<span data-ttu-id="31527-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="31527-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="31527-110">影片視窗的控制碼，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31527-110">Handle to the video window, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31527-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="31527-111">Return value</span></span>

<span data-ttu-id="31527-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="31527-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31527-113">備註</span><span class="sxs-lookup"><span data-stu-id="31527-113">Remarks</span></span>

<span data-ttu-id="31527-114">如果上游篩選的輸出釘選支援 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面，這個方法會將 [**EC \_ 通知 \_ 視窗**](ec-notify-window.md) 事件程式碼連同視窗控制碼一起傳送給它。</span><span class="sxs-lookup"><span data-stu-id="31527-114">If the output pin of the upstream filter supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, this method sends it the [**EC\_NOTIFY\_WINDOW**](ec-notify-window.md) event code along with the window handle.</span></span>

<span data-ttu-id="31527-115">影片轉譯器可覆寫其 [**CBaseRenderer：： CompleteConnect**](cbaserenderer-completeconnect.md) 方法，以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="31527-115">Video renderers can override their [**CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) methods to call this method.</span></span> <span data-ttu-id="31527-116">它會提供一種機制，以通知視窗控制碼的上游篩選。</span><span class="sxs-lookup"><span data-stu-id="31527-116">It provides a mechanism for informing the upstream filter of the window handle.</span></span> <span data-ttu-id="31527-117">如果您這樣做，請也覆寫 [**CBaseRenderer：： BreakConnect**](cbaserenderer-breakconnect.md) 方法，並 `SendNotifyWindow` 使用 **Null** 控制碼來呼叫。</span><span class="sxs-lookup"><span data-stu-id="31527-117">If you do this, override the [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) method as well, and call `SendNotifyWindow` with a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="31527-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="31527-118">Requirements</span></span>



| <span data-ttu-id="31527-119">需求</span><span class="sxs-lookup"><span data-stu-id="31527-119">Requirement</span></span> | <span data-ttu-id="31527-120">值</span><span class="sxs-lookup"><span data-stu-id="31527-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31527-121">標頭</span><span class="sxs-lookup"><span data-stu-id="31527-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31527-122"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="31527-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31527-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="31527-123">Library</span></span><br/> | <dl> <span data-ttu-id="31527-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="31527-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31527-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31527-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31527-126">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="31527-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




