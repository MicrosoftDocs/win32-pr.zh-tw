---
description: 清除方法會通知基類： pin 已啟動或停止排清。
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: 'CBaseStreamControl 方法 (Strmctl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981312"
---
# <a name="cbasestreamcontrolflushing-method"></a><span data-ttu-id="3b6f3-103">CBaseStreamControl 方法</span><span class="sxs-lookup"><span data-stu-id="3b6f3-103">CBaseStreamControl.Flushing method</span></span>

<span data-ttu-id="3b6f3-104">`Flushing`方法會通知基類： pin 已啟動或停止排清。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-104">The `Flushing` method notifies the base class that the pin has started or stopped flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b6f3-105">Syntax</span></span>


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a><span data-ttu-id="3b6f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b6f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6f3-107">*bInProgress*</span><span class="sxs-lookup"><span data-stu-id="3b6f3-107">*bInProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="3b6f3-108">指定布林值，指出是否正在清除釘選。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-108">Specifies a Boolean value that indicates whether the pin is flushing.</span></span> <span data-ttu-id="3b6f3-109">當 pin 開始排清作業時，使用值 **TRUE** ，當 pin 結束排清作業時，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-109">Use the value **TRUE** when the pin begins a flush operation, and **FALSE** when the pin ends a flush operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6f3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b6f3-110">Return value</span></span>

<span data-ttu-id="3b6f3-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b6f3-112">備註</span><span class="sxs-lookup"><span data-stu-id="3b6f3-112">Remarks</span></span>

<span data-ttu-id="3b6f3-113">Pin 必須從其 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 和 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法中呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-113">The pin must call this method from within its [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span> <span data-ttu-id="3b6f3-114">在 **BeginFlush** 中指定 **TRUE** ，並在 **EndFlush** 中指定 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-114">Specify **TRUE** in **BeginFlush** and **FALSE** in **EndFlush**.</span></span>

<span data-ttu-id="3b6f3-115">這個方法會導致 [**CBaseStreamControl：： CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) 方法停止等候。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-115">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="3b6f3-116">當釘選時， **CheckStreamState** 一律會傳回資料流程 \_ 捨棄。</span><span class="sxs-lookup"><span data-stu-id="3b6f3-116">While the pin is flushing, **CheckStreamState** always returns STREAM\_DISCARDING.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b6f3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b6f3-117">Requirements</span></span>



| <span data-ttu-id="3b6f3-118">需求</span><span class="sxs-lookup"><span data-stu-id="3b6f3-118">Requirement</span></span> | <span data-ttu-id="3b6f3-119">值</span><span class="sxs-lookup"><span data-stu-id="3b6f3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6f3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3b6f3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3b6f3-121"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3b6f3-121"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b6f3-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b6f3-122">Library</span></span><br/> | <dl> <span data-ttu-id="3b6f3-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3b6f3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b6f3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b6f3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6f3-125">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="3b6f3-125">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




