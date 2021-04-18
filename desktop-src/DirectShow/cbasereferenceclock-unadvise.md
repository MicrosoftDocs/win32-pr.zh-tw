---
description: Unadvise 方法會移除暫止的建議要求。 這個方法會實 IReferenceClock：： Unadvise 方法。
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: 'CBaseReferenceClock. Unadvise 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976222"
---
# <a name="cbasereferenceclockunadvise-method"></a><span data-ttu-id="6200a-104">CBaseReferenceClock. Unadvise 方法</span><span class="sxs-lookup"><span data-stu-id="6200a-104">CBaseReferenceClock.Unadvise method</span></span>

<span data-ttu-id="6200a-105">`Unadvise`方法會移除暫止的建議要求。</span><span class="sxs-lookup"><span data-stu-id="6200a-105">The `Unadvise` method removes a pending advise request.</span></span> <span data-ttu-id="6200a-106">這個方法會實 [**IReferenceClock：： Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) 方法。</span><span class="sxs-lookup"><span data-stu-id="6200a-106">This method implements the [**IReferenceClock::Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6200a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6200a-107">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="6200a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6200a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6200a-109">*dwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="6200a-109">*dwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="6200a-110">要移除之要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6200a-110">Identifier of the request to remove.</span></span> <span data-ttu-id="6200a-111">在 *pdwAdviseToken* 參數中使用 [**CBaseReferenceClock：： AdviseTime**](cbasereferenceclock-advisetime.md)或 [**CBaseReferenceClock：： AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)方法所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="6200a-111">Use the value returned by the [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) or [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) methods in the *pdwAdviseToken* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6200a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6200a-112">Return value</span></span>

<span data-ttu-id="6200a-113">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6200a-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="6200a-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6200a-114">Return code</span></span>                                                                             | <span data-ttu-id="6200a-115">Description</span><span class="sxs-lookup"><span data-stu-id="6200a-115">Description</span></span>           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="6200a-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="6200a-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6200a-117">找不到。</span><span class="sxs-lookup"><span data-stu-id="6200a-117">Not found.</span></span><br/> |
| <dl> <span data-ttu-id="6200a-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6200a-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6200a-119">成功。</span><span class="sxs-lookup"><span data-stu-id="6200a-119">Success.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="6200a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6200a-120">Requirements</span></span>



| <span data-ttu-id="6200a-121">需求</span><span class="sxs-lookup"><span data-stu-id="6200a-121">Requirement</span></span> | <span data-ttu-id="6200a-122">值</span><span class="sxs-lookup"><span data-stu-id="6200a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6200a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6200a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6200a-124"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6200a-124"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6200a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6200a-125">Library</span></span><br/> | <dl> <span data-ttu-id="6200a-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6200a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6200a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6200a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6200a-128">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="6200a-128">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




