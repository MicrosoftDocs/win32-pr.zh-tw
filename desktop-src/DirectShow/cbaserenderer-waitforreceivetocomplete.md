---
description: WaitForReceiveToComplete 方法會等候 CBaseRenderer：： Receive 方法完成。
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: 'CBaseRenderer. WaitForReceiveToComplete 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986572"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a><span data-ttu-id="5b94e-103">CBaseRenderer. WaitForReceiveToComplete 方法</span><span class="sxs-lookup"><span data-stu-id="5b94e-103">CBaseRenderer.WaitForReceiveToComplete method</span></span>

<span data-ttu-id="5b94e-104">`WaitForReceiveToComplete`方法 [**會等候 CBaseRenderer：： Receive**](cbaserenderer-receive.md)方法完成。</span><span class="sxs-lookup"><span data-stu-id="5b94e-104">The `WaitForReceiveToComplete` method waits for the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method to complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b94e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b94e-105">Syntax</span></span>


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a><span data-ttu-id="5b94e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b94e-106">Parameters</span></span>

<span data-ttu-id="5b94e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5b94e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b94e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b94e-108">Return value</span></span>

<span data-ttu-id="5b94e-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5b94e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b94e-110">備註</span><span class="sxs-lookup"><span data-stu-id="5b94e-110">Remarks</span></span>

<span data-ttu-id="5b94e-111">[**CBaseRenderer：： Stop**](cbaserenderer-stop.md)和 [**CBaseRenderer：： BeginFlush**](cbaserenderer-beginflush.md)方法會呼叫這個方法，將狀態變更與 **Receive** 方法進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="5b94e-111">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method to synchronize the state change with the **Receive** method.</span></span>

<span data-ttu-id="5b94e-112">具體來說，這個方法會在等候 [**CBaseRenderer：： m \_ bInReceive**](cbaserenderer-m-binreceive.md) 旗標變成 **FALSE** 時，分派訊息。</span><span class="sxs-lookup"><span data-stu-id="5b94e-112">Specifically, this method dispatches messages while it waits for the [**CBaseRenderer::m\_bInReceive**](cbaserenderer-m-binreceive.md) flag to become **FALSE**.</span></span> <span data-ttu-id="5b94e-113">[**CBaseRenderer：:P reparereceive**](cbaserenderer-preparereceive.md)方法中的旗標會變成 **TRUE** ，並在 **Receive** 方法呼叫 [**CBaseRenderer：:P reparerender**](cbaserenderer-preparerender.md)方法之後切換回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5b94e-113">The flag becomes **TRUE** in the [**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md) method and switches back to **FALSE** after the **Receive** method calls the [**CBaseRenderer::PrepareRender**](cbaserenderer-preparerender.md) method.</span></span> <span data-ttu-id="5b94e-114">衍生的類別可以使用 **PrepareRender** 來設定調色板。</span><span class="sxs-lookup"><span data-stu-id="5b94e-114">The derived class can use **PrepareRender** to set the palette.</span></span> <span data-ttu-id="5b94e-115">等候 **PrepareRender** 完成可確保在狀態變更發生之前，會先分派元件變更訊息。</span><span class="sxs-lookup"><span data-stu-id="5b94e-115">Waiting for **PrepareRender** to complete ensures that palette-change messages are dispatched before the state change occurs.</span></span> <span data-ttu-id="5b94e-116">這樣可以避免潛在的鎖死。</span><span class="sxs-lookup"><span data-stu-id="5b94e-116">This avoids a potential deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b94e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b94e-117">Requirements</span></span>



| <span data-ttu-id="5b94e-118">需求</span><span class="sxs-lookup"><span data-stu-id="5b94e-118">Requirement</span></span> | <span data-ttu-id="5b94e-119">值</span><span class="sxs-lookup"><span data-stu-id="5b94e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b94e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5b94e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5b94e-121"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5b94e-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b94e-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b94e-122">Library</span></span><br/> | <dl> <span data-ttu-id="5b94e-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5b94e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b94e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b94e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b94e-125">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="5b94e-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




