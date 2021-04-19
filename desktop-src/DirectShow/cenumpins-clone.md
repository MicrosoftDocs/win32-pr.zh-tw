---
description: Clone 方法會使用相同的列舉狀態來建立列舉值的複本。 這個方法會實 IEnumPins：： Clone 方法。
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: 'CEnumPins 複製方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000867"
---
# <a name="cenumpinsclone-method"></a><span data-ttu-id="c390a-104">CEnumPins 複製方法</span><span class="sxs-lookup"><span data-stu-id="c390a-104">CEnumPins.Clone method</span></span>

<span data-ttu-id="c390a-105">`Clone`方法會使用相同的列舉狀態來建立列舉值的複本。</span><span class="sxs-lookup"><span data-stu-id="c390a-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="c390a-106">這個方法會實 [**IEnumPins：： Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) 方法。</span><span class="sxs-lookup"><span data-stu-id="c390a-106">This method implements the [**IEnumPins::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c390a-107">語法</span><span class="sxs-lookup"><span data-stu-id="c390a-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="c390a-108">參數</span><span class="sxs-lookup"><span data-stu-id="c390a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c390a-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="c390a-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="c390a-110">接收新列舉值之 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="c390a-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c390a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c390a-111">Return value</span></span>

<span data-ttu-id="c390a-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c390a-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c390a-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c390a-113">Return code</span></span>                                                                                                | <span data-ttu-id="c390a-114">Description</span><span class="sxs-lookup"><span data-stu-id="c390a-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c390a-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c390a-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c390a-116">成功。</span><span class="sxs-lookup"><span data-stu-id="c390a-116">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="c390a-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c390a-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="c390a-118">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="c390a-118">Insufficient memory.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c390a-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c390a-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="c390a-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="c390a-120">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="c390a-121"><dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt></span><span class="sxs-lookup"><span data-stu-id="c390a-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="c390a-122">篩選的狀態已變更，且現在與列舉值不一致。</span><span class="sxs-lookup"><span data-stu-id="c390a-122">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c390a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c390a-123">Requirements</span></span>



| <span data-ttu-id="c390a-124">需求</span><span class="sxs-lookup"><span data-stu-id="c390a-124">Requirement</span></span> | <span data-ttu-id="c390a-125">值</span><span class="sxs-lookup"><span data-stu-id="c390a-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c390a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c390a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c390a-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c390a-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c390a-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c390a-128">Library</span></span><br/> | <dl> <span data-ttu-id="c390a-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c390a-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c390a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c390a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c390a-131">**CEnumPins 類別**</span><span class="sxs-lookup"><span data-stu-id="c390a-131">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




