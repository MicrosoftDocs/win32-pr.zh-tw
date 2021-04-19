---
description: GetSetupData 方法會捕獲篩選的註冊資料。
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: 'CBaseFilter. GetSetupData 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979461"
---
# <a name="cbasefiltergetsetupdata-method"></a><span data-ttu-id="02a2e-103">CBaseFilter. GetSetupData 方法</span><span class="sxs-lookup"><span data-stu-id="02a2e-103">CBaseFilter.GetSetupData method</span></span>

<span data-ttu-id="02a2e-104">方法會抓取 `GetSetupData` 篩選的註冊資料。</span><span class="sxs-lookup"><span data-stu-id="02a2e-104">The `GetSetupData` method retrieves the registration data for the filter.</span></span>

> [!Note]  
> <span data-ttu-id="02a2e-105">這個方法已過時。</span><span class="sxs-lookup"><span data-stu-id="02a2e-105">This method is obsolete.</span></span> <span data-ttu-id="02a2e-106">它是由 [**CBaseFilter：： Register**](cbasefilter-register.md) 和 [**CBaseFilter：：取消註冊**](cbasefilter-unregister.md) 方法所呼叫。</span><span class="sxs-lookup"><span data-stu-id="02a2e-106">It is called by the [**CBaseFilter::Register**](cbasefilter-register.md) and [**CBaseFilter::Unregister**](cbasefilter-unregister.md) methods.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="02a2e-107">語法</span><span class="sxs-lookup"><span data-stu-id="02a2e-107">Syntax</span></span>


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a><span data-ttu-id="02a2e-108">參數</span><span class="sxs-lookup"><span data-stu-id="02a2e-108">Parameters</span></span>

<span data-ttu-id="02a2e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="02a2e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02a2e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="02a2e-110">Return value</span></span>

<span data-ttu-id="02a2e-111">傳回 [**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md) 結構的指標，其中包含篩選準則的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="02a2e-111">Returns a pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure containing registration information for the filter.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a2e-112">備註</span><span class="sxs-lookup"><span data-stu-id="02a2e-112">Remarks</span></span>

<span data-ttu-id="02a2e-113">基類會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="02a2e-113">The base class returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a2e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="02a2e-114">Requirements</span></span>



| <span data-ttu-id="02a2e-115">需求</span><span class="sxs-lookup"><span data-stu-id="02a2e-115">Requirement</span></span> | <span data-ttu-id="02a2e-116">值</span><span class="sxs-lookup"><span data-stu-id="02a2e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02a2e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="02a2e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="02a2e-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="02a2e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02a2e-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="02a2e-119">Library</span></span><br/> | <dl> <span data-ttu-id="02a2e-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="02a2e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a2e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02a2e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a2e-122">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="02a2e-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




