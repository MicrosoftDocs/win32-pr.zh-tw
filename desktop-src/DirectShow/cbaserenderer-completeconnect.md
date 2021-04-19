---
description: CompleteConnect 方法會完成輸入 pin 與另一個 pin 的連接。
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: 'CBaseRenderer. CompleteConnect 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976128"
---
# <a name="cbaserenderercompleteconnect-method"></a><span data-ttu-id="d8db7-103">CBaseRenderer. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="d8db7-103">CBaseRenderer.CompleteConnect method</span></span>

<span data-ttu-id="d8db7-104">`CompleteConnect`方法會完成輸入 pin 與另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="d8db7-104">The `CompleteConnect` method completes the input pin's connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8db7-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8db7-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="d8db7-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8db7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8db7-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="d8db7-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="d8db7-108">輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d8db7-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8db7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8db7-109">Return value</span></span>

<span data-ttu-id="d8db7-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d8db7-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8db7-111">備註</span><span class="sxs-lookup"><span data-stu-id="d8db7-111">Remarks</span></span>

<span data-ttu-id="d8db7-112">篩選器的輸入圖釘會從其本身的方法中呼叫這個方法 `CompleteConnect` ，以完成 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="d8db7-112">The filter's input pin calls this method from inside its own `CompleteConnect` method, which is called in order to complete a pin connection.</span></span> <span data-ttu-id="d8db7-113"> (如需詳細資訊，請參閱 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md)。 ) 篩選準則會呼叫 [**CBaseRenderer：： SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) 方法來啟用 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d8db7-113">(For more information, see [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) The filter calls the [**CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) method to enable [**EC\_REPAINT**](ec-repaint.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8db7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8db7-114">Requirements</span></span>



| <span data-ttu-id="d8db7-115">需求</span><span class="sxs-lookup"><span data-stu-id="d8db7-115">Requirement</span></span> | <span data-ttu-id="d8db7-116">值</span><span class="sxs-lookup"><span data-stu-id="d8db7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8db7-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d8db7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d8db7-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d8db7-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8db7-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8db7-119">Library</span></span><br/> | <dl> <span data-ttu-id="d8db7-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d8db7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8db7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8db7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8db7-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="d8db7-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




