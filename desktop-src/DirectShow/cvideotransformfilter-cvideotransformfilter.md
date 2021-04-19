---
description: 函式方法。
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: 'CVideoTransformFilter. CVideoTransformFilter (Vtrans. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63e642182a0f968db5bda06e0af410d02455eb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990953"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="83664-103">CVideoTransformFilter. CVideoTransformFilter 函數</span><span class="sxs-lookup"><span data-stu-id="83664-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="83664-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="83664-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="83664-105">語法</span><span class="sxs-lookup"><span data-stu-id="83664-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="83664-106">參數</span><span class="sxs-lookup"><span data-stu-id="83664-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83664-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="83664-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="83664-108">包含篩選的偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="83664-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="83664-109">如需詳細資訊，請參閱 [**CBaseObject：： CBaseObject**](cbaseobject-cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="83664-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="83664-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="83664-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="83664-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="83664-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="83664-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="83664-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="83664-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="83664-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="83664-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="83664-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="83664-115">篩選準則的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="83664-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83664-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="83664-116">Requirements</span></span>



| <span data-ttu-id="83664-117">需求</span><span class="sxs-lookup"><span data-stu-id="83664-117">Requirement</span></span> | <span data-ttu-id="83664-118">值</span><span class="sxs-lookup"><span data-stu-id="83664-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83664-119">標頭</span><span class="sxs-lookup"><span data-stu-id="83664-119">Header</span></span><br/>  | <dl> <span data-ttu-id="83664-120"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="83664-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="83664-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="83664-121">Library</span></span><br/> | <dl> <span data-ttu-id="83664-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="83664-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83664-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83664-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83664-124">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="83664-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




