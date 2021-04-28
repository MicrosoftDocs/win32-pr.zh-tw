---
description: CSystemClock。 CSystemClock 函式-函數方法。
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: 'CSystemClock. CSystemClock (Sysclock. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11ba7449b086f84dc2caff19da922c03f9c7103b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095196"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="838ed-103">CSystemClock. CSystemClock 函數</span><span class="sxs-lookup"><span data-stu-id="838ed-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="838ed-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="838ed-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="838ed-105">語法</span><span class="sxs-lookup"><span data-stu-id="838ed-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="838ed-106">參數</span><span class="sxs-lookup"><span data-stu-id="838ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838ed-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="838ed-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="838ed-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="838ed-108">String containing the debug name of the object.</span></span> <span data-ttu-id="838ed-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="838ed-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="838ed-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="838ed-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="838ed-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="838ed-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="838ed-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="838ed-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="838ed-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="838ed-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="838ed-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="838ed-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="838ed-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="838ed-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="838ed-116">如果發生錯誤，方法會在此參數中傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="838ed-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="838ed-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="838ed-117">Requirements</span></span>



| <span data-ttu-id="838ed-118">需求</span><span class="sxs-lookup"><span data-stu-id="838ed-118">Requirement</span></span> | <span data-ttu-id="838ed-119">值</span><span class="sxs-lookup"><span data-stu-id="838ed-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838ed-120">標頭</span><span class="sxs-lookup"><span data-stu-id="838ed-120">Header</span></span><br/>  | <dl> <span data-ttu-id="838ed-121"><dt>Sysclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="838ed-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="838ed-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="838ed-122">Library</span></span><br/> | <dl> <span data-ttu-id="838ed-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="838ed-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




