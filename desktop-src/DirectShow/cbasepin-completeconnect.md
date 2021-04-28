---
description: CBasePin. CompleteConnect 方法-CompleteConnect 方法會完成與另一個 pin 的連接。
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
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096036"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="97d33-103">CBasePin. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="97d33-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="97d33-104">`CompleteConnect`方法會完成與另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="97d33-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d33-105">語法</span><span class="sxs-lookup"><span data-stu-id="97d33-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="97d33-106">參數</span><span class="sxs-lookup"><span data-stu-id="97d33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d33-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="97d33-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="97d33-108">指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="97d33-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d33-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="97d33-109">Return value</span></span>

<span data-ttu-id="97d33-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="97d33-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d33-111">備註</span><span class="sxs-lookup"><span data-stu-id="97d33-111">Remarks</span></span>

<span data-ttu-id="97d33-112">在連接程式結束時，會在這兩個 pin 上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="97d33-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="97d33-113">連接的 pin 會從 [**CBasePin：： Connect**](cbasepin-connect.md) 方法內呼叫它，而接收的 pin 會從 [**CBasePin：： ReceiveConnection**](cbasepin-receiveconnection.md) 方法中呼叫它。</span><span class="sxs-lookup"><span data-stu-id="97d33-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="97d33-114">在基類中，此方法只會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="97d33-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="97d33-115">如果衍生類別具有完成連接的任何需求，則應該覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="97d33-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="97d33-116">例如， [**CBaseOutputPin**](cbaseoutputpin.md) 類別會使用此方法來決定記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="97d33-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="97d33-117">如果此方法失敗，整體連接嘗試也會失敗，而且 pin 會與接收的 pin 中斷連線。</span><span class="sxs-lookup"><span data-stu-id="97d33-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d33-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="97d33-118">Requirements</span></span>



| <span data-ttu-id="97d33-119">需求</span><span class="sxs-lookup"><span data-stu-id="97d33-119">Requirement</span></span> | <span data-ttu-id="97d33-120">值</span><span class="sxs-lookup"><span data-stu-id="97d33-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d33-121">標頭</span><span class="sxs-lookup"><span data-stu-id="97d33-121">Header</span></span><br/>  | <dl> <span data-ttu-id="97d33-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="97d33-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97d33-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="97d33-123">Library</span></span><br/> | <dl> <span data-ttu-id="97d33-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="97d33-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97d33-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97d33-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d33-126">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="97d33-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




