---
description: CBaseObject. ~ CBaseObject 的函式-函式方法。
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: 'CBaseObject. ~ CBaseObject (Combase 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 552dbcc764f335e639cb50e2e01411dee200068f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096236"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="2f6cf-103">CBaseObject. ~ CBaseObject 的函式</span><span class="sxs-lookup"><span data-stu-id="2f6cf-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="2f6cf-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f6cf-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f6cf-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="2f6cf-106">備註</span><span class="sxs-lookup"><span data-stu-id="2f6cf-106">Remarks</span></span>

<span data-ttu-id="2f6cf-107">這個方法會遞減使用中物件的計數。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-107">This method decrements the active-object count.</span></span> <span data-ttu-id="2f6cf-108"> (參閱 [**CBaseObject：： ObjectsActive**](cbaseobject-objectsactive.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6cf-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f6cf-109">Requirements</span></span>



| <span data-ttu-id="2f6cf-110">需求</span><span class="sxs-lookup"><span data-stu-id="2f6cf-110">Requirement</span></span> | <span data-ttu-id="2f6cf-111">值</span><span class="sxs-lookup"><span data-stu-id="2f6cf-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6cf-112">標頭</span><span class="sxs-lookup"><span data-stu-id="2f6cf-112">Header</span></span><br/>  | <dl> <span data-ttu-id="2f6cf-113"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2f6cf-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f6cf-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f6cf-114">Library</span></span><br/> | <dl> <span data-ttu-id="2f6cf-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2f6cf-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f6cf-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f6cf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6cf-117">**CBaseObject 類別**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




