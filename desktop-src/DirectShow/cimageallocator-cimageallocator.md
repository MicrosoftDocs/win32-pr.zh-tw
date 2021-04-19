---
description: 函式方法。
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: 'CImageAllocator. CImageAllocator (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f6873e8cc073e0b716f94c980ecceba8f4512f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993414"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="b97c7-103">CImageAllocator. CImageAllocator 函數</span><span class="sxs-lookup"><span data-stu-id="b97c7-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="b97c7-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="b97c7-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="b97c7-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b97c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="b97c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b97c7-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="b97c7-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="b97c7-108">擁有篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="b97c7-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="b97c7-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="b97c7-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b97c7-110">字串的指標，其中包含配置器的偵錯工具名稱。</span><span class="sxs-lookup"><span data-stu-id="b97c7-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="b97c7-111">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="b97c7-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="b97c7-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="b97c7-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b97c7-113">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="b97c7-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="b97c7-114">建立物件之前，請先將值設定為 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="b97c7-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="b97c7-115">如果此函式失敗，則會將值設定為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b97c7-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b97c7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b97c7-116">Requirements</span></span>



| <span data-ttu-id="b97c7-117">需求</span><span class="sxs-lookup"><span data-stu-id="b97c7-117">Requirement</span></span> | <span data-ttu-id="b97c7-118">值</span><span class="sxs-lookup"><span data-stu-id="b97c7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b97c7-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b97c7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b97c7-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b97c7-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b97c7-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="b97c7-121">Library</span></span><br/> | <dl> <span data-ttu-id="b97c7-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b97c7-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b97c7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b97c7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97c7-124">**CImageAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="b97c7-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




