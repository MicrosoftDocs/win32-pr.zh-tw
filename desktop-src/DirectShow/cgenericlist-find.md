---
description: Find 方法會抓取保留指定專案的第一個位置。
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: 'CGenericList： Find 方法 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989876"
---
# <a name="cgenericlistfind-method"></a><span data-ttu-id="6ca67-103">CGenericList，Find 方法</span><span class="sxs-lookup"><span data-stu-id="6ca67-103">CGenericList.Find method</span></span>

<span data-ttu-id="6ca67-104">`Find`方法會抓取保留指定專案的第一個位置。</span><span class="sxs-lookup"><span data-stu-id="6ca67-104">The `Find` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca67-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ca67-105">Syntax</span></span>


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="6ca67-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ca67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca67-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="6ca67-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="6ca67-108">**物件** 類型物件的指標， (範本類型) 。</span><span class="sxs-lookup"><span data-stu-id="6ca67-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca67-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ca67-109">Return value</span></span>

<span data-ttu-id="6ca67-110">傳回位置值，如果專案不在清單中，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="6ca67-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca67-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ca67-111">Requirements</span></span>



| <span data-ttu-id="6ca67-112">需求</span><span class="sxs-lookup"><span data-stu-id="6ca67-112">Requirement</span></span> | <span data-ttu-id="6ca67-113">值</span><span class="sxs-lookup"><span data-stu-id="6ca67-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca67-114">標頭</span><span class="sxs-lookup"><span data-stu-id="6ca67-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6ca67-115"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6ca67-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6ca67-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ca67-116">Library</span></span><br/> | <dl> <span data-ttu-id="6ca67-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6ca67-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca67-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ca67-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca67-119">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="6ca67-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




