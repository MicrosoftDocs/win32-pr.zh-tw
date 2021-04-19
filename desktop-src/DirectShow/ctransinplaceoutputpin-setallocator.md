---
description: SetAllocator 方法會指定連接的配置器。
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: 'CTransInPlaceOutputPin. SetAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990149"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a><span data-ttu-id="b0d9d-103">CTransInPlaceOutputPin. SetAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="b0d9d-103">CTransInPlaceOutputPin.SetAllocator method</span></span>

<span data-ttu-id="b0d9d-104">方法會指定連接的配置器 `SetAllocator` 。</span><span class="sxs-lookup"><span data-stu-id="b0d9d-104">The `SetAllocator` method specifies an allocator for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d9d-105">語法</span><span class="sxs-lookup"><span data-stu-id="b0d9d-105">Syntax</span></span>


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="b0d9d-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0d9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d9d-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="b0d9d-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="b0d9d-108">配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b0d9d-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d9d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0d9d-109">Return value</span></span>

<span data-ttu-id="b0d9d-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b0d9d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d9d-111">備註</span><span class="sxs-lookup"><span data-stu-id="b0d9d-111">Remarks</span></span>

<span data-ttu-id="b0d9d-112">此篩選器的輸出 pin 永遠不會提供配置器。</span><span class="sxs-lookup"><span data-stu-id="b0d9d-112">The output pin for this filter never provides an allocator.</span></span> <span data-ttu-id="b0d9d-113">這個方法會指定輸出圖釘的配置器。</span><span class="sxs-lookup"><span data-stu-id="b0d9d-113">This method specifies the allocator for the output pin.</span></span> <span data-ttu-id="b0d9d-114">它會設定 [**CBaseOutputPin：： m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) 成員變數的值。</span><span class="sxs-lookup"><span data-stu-id="b0d9d-114">It sets the value of the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d9d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0d9d-115">Requirements</span></span>



| <span data-ttu-id="b0d9d-116">需求</span><span class="sxs-lookup"><span data-stu-id="b0d9d-116">Requirement</span></span> | <span data-ttu-id="b0d9d-117">值</span><span class="sxs-lookup"><span data-stu-id="b0d9d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d9d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b0d9d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b0d9d-119"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b0d9d-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0d9d-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="b0d9d-120">Library</span></span><br/> | <dl> <span data-ttu-id="b0d9d-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b0d9d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d9d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0d9d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d9d-123">**CTransInPlaceOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="b0d9d-123">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




