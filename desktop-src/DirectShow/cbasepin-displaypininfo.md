---
description: DisplayPinInfo 方法會在調試過程中追蹤 pin 連接。
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: 'CBasePin. DisplayPinInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998876"
---
# <a name="cbasepindisplaypininfo-method"></a><span data-ttu-id="7711c-103">CBasePin. DisplayPinInfo 方法</span><span class="sxs-lookup"><span data-stu-id="7711c-103">CBasePin.DisplayPinInfo method</span></span>

<span data-ttu-id="7711c-104">`DisplayPinInfo`方法會在調試過程中追蹤 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="7711c-104">The `DisplayPinInfo` method traces a pin connection during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="7711c-105">語法</span><span class="sxs-lookup"><span data-stu-id="7711c-105">Syntax</span></span>


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="7711c-106">參數</span><span class="sxs-lookup"><span data-stu-id="7711c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7711c-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="7711c-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="7711c-108">接收的釘選指標。</span><span class="sxs-lookup"><span data-stu-id="7711c-108">Pointer to the receiving pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7711c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7711c-109">Return value</span></span>

<span data-ttu-id="7711c-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7711c-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7711c-111">備註</span><span class="sxs-lookup"><span data-stu-id="7711c-111">Remarks</span></span>

<span data-ttu-id="7711c-112">在 debug 組建中，這個方法會呼叫 [**DbgLog**](dbglog.md) 函數來追蹤連接嘗試。</span><span class="sxs-lookup"><span data-stu-id="7711c-112">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to trace a connection attempt.</span></span> <span data-ttu-id="7711c-113">在零售組建中，此方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="7711c-113">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7711c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7711c-114">Requirements</span></span>



| <span data-ttu-id="7711c-115">需求</span><span class="sxs-lookup"><span data-stu-id="7711c-115">Requirement</span></span> | <span data-ttu-id="7711c-116">值</span><span class="sxs-lookup"><span data-stu-id="7711c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7711c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7711c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7711c-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7711c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7711c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7711c-119">Library</span></span><br/> | <dl> <span data-ttu-id="7711c-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7711c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7711c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7711c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7711c-122">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="7711c-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




