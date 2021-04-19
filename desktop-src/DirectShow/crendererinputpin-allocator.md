---
description: 配置器方法會捕獲記憶體配置器的指標。
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: 'CRendererInputPin 配置器方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987151"
---
# <a name="crendererinputpinallocator-method"></a><span data-ttu-id="79592-103">CRendererInputPin 配置器方法</span><span class="sxs-lookup"><span data-stu-id="79592-103">CRendererInputPin.Allocator method</span></span>

<span data-ttu-id="79592-104">方法會捕獲記憶體配置器的 `Allocator` 指標。</span><span class="sxs-lookup"><span data-stu-id="79592-104">The `Allocator` method retrieves a pointer to the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="79592-105">語法</span><span class="sxs-lookup"><span data-stu-id="79592-105">Syntax</span></span>


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a><span data-ttu-id="79592-106">參數</span><span class="sxs-lookup"><span data-stu-id="79592-106">Parameters</span></span>

<span data-ttu-id="79592-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="79592-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79592-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="79592-108">Return value</span></span>

<span data-ttu-id="79592-109">傳回配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="79592-109">Returns a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="79592-110">備註</span><span class="sxs-lookup"><span data-stu-id="79592-110">Remarks</span></span>

<span data-ttu-id="79592-111">這個方法會傳回 [**CBaseInputPin：： m \_ pAllocator**](cbaseinputpin-m-pallocator.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="79592-111">This method returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span> <span data-ttu-id="79592-112">方法不會遞增介面上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="79592-112">The method does not increment the reference count on the interface.</span></span> <span data-ttu-id="79592-113">這個方法完全是存取子方法。</span><span class="sxs-lookup"><span data-stu-id="79592-113">This method is strictly an accessor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="79592-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="79592-114">Requirements</span></span>



| <span data-ttu-id="79592-115">需求</span><span class="sxs-lookup"><span data-stu-id="79592-115">Requirement</span></span> | <span data-ttu-id="79592-116">值</span><span class="sxs-lookup"><span data-stu-id="79592-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79592-117">標頭</span><span class="sxs-lookup"><span data-stu-id="79592-117">Header</span></span><br/>  | <dl> <span data-ttu-id="79592-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="79592-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79592-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="79592-119">Library</span></span><br/> | <dl> <span data-ttu-id="79592-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="79592-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79592-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79592-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79592-122">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="79592-122">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




