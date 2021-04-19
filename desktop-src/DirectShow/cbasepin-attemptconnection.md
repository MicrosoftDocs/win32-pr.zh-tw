---
description: AttemptConnection 方法會使用指定的媒體類型連接到另一個 pin。
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: 'CBasePin. AttemptConnection 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976241"
---
# <a name="cbasepinattemptconnection-method"></a><span data-ttu-id="90127-103">CBasePin. AttemptConnection 方法</span><span class="sxs-lookup"><span data-stu-id="90127-103">CBasePin.AttemptConnection method</span></span>

<span data-ttu-id="90127-104">`AttemptConnection`方法會使用指定的媒體類型連接到另一個 pin。</span><span class="sxs-lookup"><span data-stu-id="90127-104">The `AttemptConnection` method connects to another pin using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="90127-105">語法</span><span class="sxs-lookup"><span data-stu-id="90127-105">Syntax</span></span>


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="90127-106">參數</span><span class="sxs-lookup"><span data-stu-id="90127-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90127-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="90127-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="90127-108">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="90127-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="90127-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="90127-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="90127-110">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="90127-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90127-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="90127-111">Return value</span></span>

<span data-ttu-id="90127-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="90127-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="90127-113">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="90127-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="90127-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="90127-114">Return code</span></span>                                                                                                | <span data-ttu-id="90127-115">Description</span><span class="sxs-lookup"><span data-stu-id="90127-115">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="90127-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="90127-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="90127-117">成功。</span><span class="sxs-lookup"><span data-stu-id="90127-117">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="90127-118"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="90127-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="90127-119">媒體類型無法接受。</span><span class="sxs-lookup"><span data-stu-id="90127-119">The media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90127-120">備註</span><span class="sxs-lookup"><span data-stu-id="90127-120">Remarks</span></span>

<span data-ttu-id="90127-121">這個方法會嘗試連接具有特定媒體類型的兩個 pin。</span><span class="sxs-lookup"><span data-stu-id="90127-121">This method attempts to connect the two pins with a specific media type.</span></span> <span data-ttu-id="90127-122">如果類型無法接受，則方法會失敗，而不會嘗試其他媒體類型。</span><span class="sxs-lookup"><span data-stu-id="90127-122">If the type is not acceptable, the method fails without trying other media types.</span></span>

<span data-ttu-id="90127-123">如果媒體類型是可接受的，這個方法會呼叫接收釘選的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法。</span><span class="sxs-lookup"><span data-stu-id="90127-123">If the media type is acceptable, this method calls the receiving pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="90127-124">然後，它會呼叫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 方法來完成連接。</span><span class="sxs-lookup"><span data-stu-id="90127-124">Then it calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method to complete the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="90127-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="90127-125">Requirements</span></span>



| <span data-ttu-id="90127-126">需求</span><span class="sxs-lookup"><span data-stu-id="90127-126">Requirement</span></span> | <span data-ttu-id="90127-127">值</span><span class="sxs-lookup"><span data-stu-id="90127-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90127-128">標頭</span><span class="sxs-lookup"><span data-stu-id="90127-128">Header</span></span><br/>  | <dl> <span data-ttu-id="90127-129"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="90127-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="90127-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="90127-130">Library</span></span><br/> | <dl> <span data-ttu-id="90127-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="90127-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90127-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90127-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90127-133">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="90127-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




