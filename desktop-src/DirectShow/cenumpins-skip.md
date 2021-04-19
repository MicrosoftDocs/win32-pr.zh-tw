---
description: Skip 方法會略過列舉順序中指定的 pin 數目。 這個方法會實 IEnumPins：： Skip 方法。
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: 'CEnumPins. Skip 方法 (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982676"
---
# <a name="cenumpinsskip-method"></a><span data-ttu-id="3e8dc-104">CEnumPins. Skip 方法</span><span class="sxs-lookup"><span data-stu-id="3e8dc-104">CEnumPins.Skip method</span></span>

<span data-ttu-id="3e8dc-105">`Skip`方法會在列舉順序中略過指定數目的釘選。</span><span class="sxs-lookup"><span data-stu-id="3e8dc-105">The `Skip` method skips over a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="3e8dc-106">這個方法會實 [**IEnumPins：： Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) 方法。</span><span class="sxs-lookup"><span data-stu-id="3e8dc-106">This method implements the [**IEnumPins::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8dc-107">語法</span><span class="sxs-lookup"><span data-stu-id="3e8dc-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a><span data-ttu-id="3e8dc-108">參數</span><span class="sxs-lookup"><span data-stu-id="3e8dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8dc-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="3e8dc-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="3e8dc-110">要略過的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="3e8dc-110">Number of pins to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8dc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e8dc-111">Return value</span></span>

<span data-ttu-id="3e8dc-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3e8dc-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3e8dc-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3e8dc-113">Return code</span></span>                                                                                                | <span data-ttu-id="3e8dc-114">Description</span><span class="sxs-lookup"><span data-stu-id="3e8dc-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e8dc-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3e8dc-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="3e8dc-116">略過序列結尾的尾端。</span><span class="sxs-lookup"><span data-stu-id="3e8dc-116">Skipped past the end of the sequence.</span></span><br/>                                       |
| <dl> <span data-ttu-id="3e8dc-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3e8dc-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3e8dc-118">成功。</span><span class="sxs-lookup"><span data-stu-id="3e8dc-118">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="3e8dc-119"><dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt></span><span class="sxs-lookup"><span data-stu-id="3e8dc-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="3e8dc-120">篩選的狀態已變更，且現在與列舉值不一致。</span><span class="sxs-lookup"><span data-stu-id="3e8dc-120">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e8dc-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e8dc-121">Requirements</span></span>



| <span data-ttu-id="3e8dc-122">需求</span><span class="sxs-lookup"><span data-stu-id="3e8dc-122">Requirement</span></span> | <span data-ttu-id="3e8dc-123">值</span><span class="sxs-lookup"><span data-stu-id="3e8dc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8dc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3e8dc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3e8dc-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3e8dc-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3e8dc-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e8dc-126">Library</span></span><br/> | <dl> <span data-ttu-id="3e8dc-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3e8dc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8dc-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e8dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8dc-129">**CEnumPins 類別**</span><span class="sxs-lookup"><span data-stu-id="3e8dc-129">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




