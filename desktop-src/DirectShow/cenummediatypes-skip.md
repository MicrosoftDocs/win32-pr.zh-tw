---
description: Skip 方法會略過指定數目的媒體類型。 這個方法會實 IEnumMediaTypes：： Skip 方法。
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: 'CEnumMediaTypes. Skip 方法 (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995358"
---
# <a name="cenummediatypesskip-method"></a><span data-ttu-id="0f825-104">CEnumMediaTypes. Skip 方法</span><span class="sxs-lookup"><span data-stu-id="0f825-104">CEnumMediaTypes.Skip method</span></span>

<span data-ttu-id="0f825-105">`Skip`方法會略過指定數目的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0f825-105">The `Skip` method skips over a specified number of media types.</span></span> <span data-ttu-id="0f825-106">這個方法會實 [**IEnumMediaTypes：： Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) 方法。</span><span class="sxs-lookup"><span data-stu-id="0f825-106">This method implements the [**IEnumMediaTypes::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f825-107">語法</span><span class="sxs-lookup"><span data-stu-id="0f825-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="0f825-108">參數</span><span class="sxs-lookup"><span data-stu-id="0f825-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f825-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="0f825-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="0f825-110">要略過的媒體類型數目。</span><span class="sxs-lookup"><span data-stu-id="0f825-110">Number of media types to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f825-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f825-111">Return value</span></span>

<span data-ttu-id="0f825-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0f825-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0f825-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0f825-113">Return code</span></span>                                                                                                | <span data-ttu-id="0f825-114">Description</span><span class="sxs-lookup"><span data-stu-id="0f825-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f825-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="0f825-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="0f825-116">略過序列結尾的尾端。</span><span class="sxs-lookup"><span data-stu-id="0f825-116">Skipped past the end of the sequence.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0f825-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0f825-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0f825-118">成功。</span><span class="sxs-lookup"><span data-stu-id="0f825-118">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="0f825-119"><dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt></span><span class="sxs-lookup"><span data-stu-id="0f825-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="0f825-120">Pin 的狀態已變更，且現在與列舉值不一致。</span><span class="sxs-lookup"><span data-stu-id="0f825-120">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f825-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f825-121">Requirements</span></span>



| <span data-ttu-id="0f825-122">需求</span><span class="sxs-lookup"><span data-stu-id="0f825-122">Requirement</span></span> | <span data-ttu-id="0f825-123">值</span><span class="sxs-lookup"><span data-stu-id="0f825-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f825-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0f825-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0f825-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0f825-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f825-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f825-126">Library</span></span><br/> | <dl> <span data-ttu-id="0f825-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0f825-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f825-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f825-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f825-129">**CEnumMediaTypes 類別**</span><span class="sxs-lookup"><span data-stu-id="0f825-129">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




