---
description: SetControlVideoPin 方法會設定篩選所使用的 pin。
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: 'CBaseControlVideo. SetControlVideoPin 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000691"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a><span data-ttu-id="2dd35-103">CBaseControlVideo. SetControlVideoPin 方法</span><span class="sxs-lookup"><span data-stu-id="2dd35-103">CBaseControlVideo.SetControlVideoPin method</span></span>

<span data-ttu-id="2dd35-104">`SetControlVideoPin`方法會設定篩選所使用的 pin。</span><span class="sxs-lookup"><span data-stu-id="2dd35-104">The `SetControlVideoPin` method sets the pin used by the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd35-105">語法</span><span class="sxs-lookup"><span data-stu-id="2dd35-105">Syntax</span></span>


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="2dd35-106">參數</span><span class="sxs-lookup"><span data-stu-id="2dd35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd35-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="2dd35-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2dd35-108">用來同步處理介面之 pin 的指標。</span><span class="sxs-lookup"><span data-stu-id="2dd35-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd35-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2dd35-109">Return value</span></span>

<span data-ttu-id="2dd35-110">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2dd35-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dd35-111">備註</span><span class="sxs-lookup"><span data-stu-id="2dd35-111">Remarks</span></span>

<span data-ttu-id="2dd35-112">只有在成功連接篩選器時，才能呼叫介面。</span><span class="sxs-lookup"><span data-stu-id="2dd35-112">The interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="2dd35-113">物件會透過這個方法傳遞給與其進行同步處理的 pin;在大部分的情況下，它會在有介面方法被呼叫時，判斷 pin 是否已連接，如果失敗，則會傳回 VFW \_ E \_ 未 \_ 連接。</span><span class="sxs-lookup"><span data-stu-id="2dd35-113">The object is passed through this method to the pin with which it is synchronized; in most cases it will determine if the pin is connected when it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd35-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dd35-114">Requirements</span></span>



| <span data-ttu-id="2dd35-115">需求</span><span class="sxs-lookup"><span data-stu-id="2dd35-115">Requirement</span></span> | <span data-ttu-id="2dd35-116">值</span><span class="sxs-lookup"><span data-stu-id="2dd35-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd35-117">標頭</span><span class="sxs-lookup"><span data-stu-id="2dd35-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2dd35-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2dd35-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2dd35-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="2dd35-119">Library</span></span><br/> | <dl> <span data-ttu-id="2dd35-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2dd35-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dd35-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dd35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd35-122">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="2dd35-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




