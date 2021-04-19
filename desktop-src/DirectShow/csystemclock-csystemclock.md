---
description: 函式方法。
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
ms.openlocfilehash: fea99d95aa4c1b1cadefbb95384fb871374362f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999623"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="6a9de-103">CSystemClock. CSystemClock 函數</span><span class="sxs-lookup"><span data-stu-id="6a9de-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="6a9de-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="6a9de-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9de-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a9de-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6a9de-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a9de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9de-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6a9de-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6a9de-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="6a9de-108">String containing the debug name of the object.</span></span> <span data-ttu-id="6a9de-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="6a9de-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a9de-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="6a9de-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6a9de-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="6a9de-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="6a9de-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="6a9de-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6a9de-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6a9de-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a9de-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="6a9de-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6a9de-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="6a9de-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="6a9de-116">如果發生錯誤，方法會在此參數中傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6a9de-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a9de-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a9de-117">Requirements</span></span>



| <span data-ttu-id="6a9de-118">需求</span><span class="sxs-lookup"><span data-stu-id="6a9de-118">Requirement</span></span> | <span data-ttu-id="6a9de-119">值</span><span class="sxs-lookup"><span data-stu-id="6a9de-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9de-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6a9de-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6a9de-121"><dt>Sysclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6a9de-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6a9de-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a9de-122">Library</span></span><br/> | <dl> <span data-ttu-id="6a9de-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6a9de-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




