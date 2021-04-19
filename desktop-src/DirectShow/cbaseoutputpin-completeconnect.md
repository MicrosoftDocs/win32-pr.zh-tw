---
description: CompleteConnect 方法會完成輸入 pin 的連接。
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: 'CBaseOutputPin. CompleteConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984116"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="06ecd-103">CBaseOutputPin. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="06ecd-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="06ecd-104">`CompleteConnect`方法會完成輸入 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="06ecd-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ecd-105">語法</span><span class="sxs-lookup"><span data-stu-id="06ecd-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="06ecd-106">參數</span><span class="sxs-lookup"><span data-stu-id="06ecd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ecd-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="06ecd-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="06ecd-108">輸入釘選的指標。</span><span class="sxs-lookup"><span data-stu-id="06ecd-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06ecd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="06ecd-109">Return value</span></span>

<span data-ttu-id="06ecd-110">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="06ecd-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="06ecd-111">備註</span><span class="sxs-lookup"><span data-stu-id="06ecd-111">Remarks</span></span>

<span data-ttu-id="06ecd-112">這個方法會覆寫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="06ecd-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="06ecd-113">它會呼叫 [**DecideAllocator**](cbaseoutputpin-decideallocator.md) 方法，以選取要用於此連接的記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="06ecd-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="06ecd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="06ecd-114">Requirements</span></span>



| <span data-ttu-id="06ecd-115">需求</span><span class="sxs-lookup"><span data-stu-id="06ecd-115">Requirement</span></span> | <span data-ttu-id="06ecd-116">值</span><span class="sxs-lookup"><span data-stu-id="06ecd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ecd-117">標頭</span><span class="sxs-lookup"><span data-stu-id="06ecd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="06ecd-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="06ecd-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06ecd-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="06ecd-119">Library</span></span><br/> | <dl> <span data-ttu-id="06ecd-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="06ecd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06ecd-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06ecd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ecd-122">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="06ecd-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




