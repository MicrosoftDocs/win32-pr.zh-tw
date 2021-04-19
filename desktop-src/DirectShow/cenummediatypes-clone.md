---
description: Clone 方法會使用相同的列舉狀態來建立列舉值的複本。 這個方法會實 IEnumMediaTypes：： Clone 方法。
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: 'CEnumMediaTypes 複製方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981374"
---
# <a name="cenummediatypesclone-method"></a><span data-ttu-id="16abc-104">CEnumMediaTypes 複製方法</span><span class="sxs-lookup"><span data-stu-id="16abc-104">CEnumMediaTypes.Clone method</span></span>

<span data-ttu-id="16abc-105">`Clone`方法會使用相同的列舉狀態來建立列舉值的複本。</span><span class="sxs-lookup"><span data-stu-id="16abc-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="16abc-106">這個方法會實 [**IEnumMediaTypes：： Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) 方法。</span><span class="sxs-lookup"><span data-stu-id="16abc-106">This method implements the [**IEnumMediaTypes::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16abc-107">語法</span><span class="sxs-lookup"><span data-stu-id="16abc-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="16abc-108">參數</span><span class="sxs-lookup"><span data-stu-id="16abc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16abc-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="16abc-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="16abc-110">接收新列舉值之 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="16abc-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16abc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="16abc-111">Return value</span></span>

<span data-ttu-id="16abc-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="16abc-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="16abc-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="16abc-113">Return code</span></span>                                                                                                | <span data-ttu-id="16abc-114">Description</span><span class="sxs-lookup"><span data-stu-id="16abc-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16abc-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="16abc-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="16abc-116">成功。</span><span class="sxs-lookup"><span data-stu-id="16abc-116">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="16abc-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="16abc-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="16abc-118">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="16abc-118">Insufficient memory.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="16abc-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="16abc-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="16abc-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="16abc-120">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="16abc-121"><dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt></span><span class="sxs-lookup"><span data-stu-id="16abc-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="16abc-122">Pin 的狀態已變更，且現在與列舉值不一致。</span><span class="sxs-lookup"><span data-stu-id="16abc-122">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16abc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="16abc-123">Requirements</span></span>



| <span data-ttu-id="16abc-124">需求</span><span class="sxs-lookup"><span data-stu-id="16abc-124">Requirement</span></span> | <span data-ttu-id="16abc-125">值</span><span class="sxs-lookup"><span data-stu-id="16abc-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16abc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="16abc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="16abc-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="16abc-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16abc-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="16abc-128">Library</span></span><br/> | <dl> <span data-ttu-id="16abc-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="16abc-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16abc-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16abc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16abc-131">**CEnumMediaTypes 類別**</span><span class="sxs-lookup"><span data-stu-id="16abc-131">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




