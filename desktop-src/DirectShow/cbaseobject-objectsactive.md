---
description: ObjectsActive 方法會抓取整個進程的作用中物件計數。
ms.assetid: adbc023a-22b7-44e9-b078-a26831f961cc
title: 'CBaseObject. ObjectsActive 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.ObjectsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a3aee21fd9835b28bdcc23eabe30c1d2b5217b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000731"
---
# <a name="cbaseobjectobjectsactive-method"></a><span data-ttu-id="62cef-103">CBaseObject. ObjectsActive 方法</span><span class="sxs-lookup"><span data-stu-id="62cef-103">CBaseObject.ObjectsActive method</span></span>

<span data-ttu-id="62cef-104">方法會抓取 `ObjectsActive` 整個進程的作用中物件計數。</span><span class="sxs-lookup"><span data-stu-id="62cef-104">The `ObjectsActive` method retrieves a process-wide count of active objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="62cef-105">語法</span><span class="sxs-lookup"><span data-stu-id="62cef-105">Syntax</span></span>


```C++
static LONG ObjectsActive();
```



## <a name="parameters"></a><span data-ttu-id="62cef-106">參數</span><span class="sxs-lookup"><span data-stu-id="62cef-106">Parameters</span></span>

<span data-ttu-id="62cef-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="62cef-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62cef-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="62cef-108">Return value</span></span>

<span data-ttu-id="62cef-109">傳回使用中物件的數目。</span><span class="sxs-lookup"><span data-stu-id="62cef-109">Returns the number of active objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="62cef-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="62cef-110">Requirements</span></span>



| <span data-ttu-id="62cef-111">需求</span><span class="sxs-lookup"><span data-stu-id="62cef-111">Requirement</span></span> | <span data-ttu-id="62cef-112">值</span><span class="sxs-lookup"><span data-stu-id="62cef-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62cef-113">標頭</span><span class="sxs-lookup"><span data-stu-id="62cef-113">Header</span></span><br/>  | <dl> <span data-ttu-id="62cef-114"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="62cef-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62cef-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="62cef-115">Library</span></span><br/> | <dl> <span data-ttu-id="62cef-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="62cef-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62cef-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62cef-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cef-118">**CBaseObject 類別**</span><span class="sxs-lookup"><span data-stu-id="62cef-118">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




