---
description: CSource。 CSource 函式-函數方法。
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: CSource)  (Source .h 的函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fab398f3f4e3fdd8c23ce1e1c08f5c130478dfb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085356"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="21d0e-103">CSource. CSource 函數</span><span class="sxs-lookup"><span data-stu-id="21d0e-103">CSource.CSource constructor</span></span>

<span data-ttu-id="21d0e-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="21d0e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d0e-105">語法</span><span class="sxs-lookup"><span data-stu-id="21d0e-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="21d0e-106">參數</span><span class="sxs-lookup"><span data-stu-id="21d0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21d0e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="21d0e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="21d0e-108">包含物件名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="21d0e-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="21d0e-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="21d0e-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="21d0e-110">*lpunk*</span><span class="sxs-lookup"><span data-stu-id="21d0e-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="21d0e-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="21d0e-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="21d0e-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="21d0e-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="21d0e-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="21d0e-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21d0e-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="21d0e-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="21d0e-115">篩選準則的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="21d0e-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21d0e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="21d0e-116">Requirements</span></span>



| <span data-ttu-id="21d0e-117">需求</span><span class="sxs-lookup"><span data-stu-id="21d0e-117">Requirement</span></span> | <span data-ttu-id="21d0e-118">值</span><span class="sxs-lookup"><span data-stu-id="21d0e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21d0e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="21d0e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="21d0e-120"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="21d0e-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="21d0e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="21d0e-121">Library</span></span><br/> | <dl> <span data-ttu-id="21d0e-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="21d0e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21d0e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21d0e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d0e-124">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="21d0e-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




