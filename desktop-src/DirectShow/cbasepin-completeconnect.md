---
description: CompleteConnect 方法會完成與另一個 pin 的連接。
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: 'CBasePin. CompleteConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990093"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="87455-103">CBasePin. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="87455-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="87455-104">`CompleteConnect`方法會完成與另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="87455-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="87455-105">語法</span><span class="sxs-lookup"><span data-stu-id="87455-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="87455-106">參數</span><span class="sxs-lookup"><span data-stu-id="87455-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87455-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="87455-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="87455-108">指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="87455-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87455-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="87455-109">Return value</span></span>

<span data-ttu-id="87455-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="87455-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="87455-111">備註</span><span class="sxs-lookup"><span data-stu-id="87455-111">Remarks</span></span>

<span data-ttu-id="87455-112">在連接程式結束時，會在這兩個 pin 上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="87455-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="87455-113">連接的 pin 會從 [**CBasePin：： Connect**](cbasepin-connect.md) 方法內呼叫它，而接收的 pin 會從 [**CBasePin：： ReceiveConnection**](cbasepin-receiveconnection.md) 方法中呼叫它。</span><span class="sxs-lookup"><span data-stu-id="87455-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="87455-114">在基類中，此方法只會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="87455-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="87455-115">如果衍生類別具有完成連接的任何需求，則應該覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="87455-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="87455-116">例如， [**CBaseOutputPin**](cbaseoutputpin.md) 類別會使用此方法來決定記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="87455-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="87455-117">如果此方法失敗，整體連接嘗試也會失敗，而且 pin 會與接收的 pin 中斷連線。</span><span class="sxs-lookup"><span data-stu-id="87455-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="87455-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="87455-118">Requirements</span></span>



| <span data-ttu-id="87455-119">需求</span><span class="sxs-lookup"><span data-stu-id="87455-119">Requirement</span></span> | <span data-ttu-id="87455-120">值</span><span class="sxs-lookup"><span data-stu-id="87455-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87455-121">標頭</span><span class="sxs-lookup"><span data-stu-id="87455-121">Header</span></span><br/>  | <dl> <span data-ttu-id="87455-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="87455-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87455-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="87455-123">Library</span></span><br/> | <dl> <span data-ttu-id="87455-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="87455-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87455-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87455-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87455-126">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="87455-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




