---
description: 函式方法。
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: 'CBaseObject. CBaseObject (Combase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001800"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="22130-103">CBaseObject. CBaseObject 函數</span><span class="sxs-lookup"><span data-stu-id="22130-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="22130-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="22130-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22130-105">語法</span><span class="sxs-lookup"><span data-stu-id="22130-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="22130-106">參數</span><span class="sxs-lookup"><span data-stu-id="22130-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22130-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="22130-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="22130-108">字串，包含物件的名稱，用於進行調試。</span><span class="sxs-lookup"><span data-stu-id="22130-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22130-109">備註</span><span class="sxs-lookup"><span data-stu-id="22130-109">Remarks</span></span>

<span data-ttu-id="22130-110">這個方法會遞增使用中物件的計數。</span><span class="sxs-lookup"><span data-stu-id="22130-110">This method increments the active-object count.</span></span> <span data-ttu-id="22130-111"> (參閱 [**CBaseObject：： ObjectsActive**](cbaseobject-objectsactive.md)) 。</span><span class="sxs-lookup"><span data-stu-id="22130-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="22130-112">在靜態記憶體中配置 *pName* 參數：</span><span class="sxs-lookup"><span data-stu-id="22130-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="22130-113">[**名稱**](name.md)宏會在零售組建中編譯為 **Null** ，因此靜態字串只會出現在偵錯工具組建中。</span><span class="sxs-lookup"><span data-stu-id="22130-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="22130-114">如需詳細資訊，請參閱 [**DbgDumpObjectRegister**](dbgdumpobjectregister.md)。</span><span class="sxs-lookup"><span data-stu-id="22130-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22130-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="22130-115">Requirements</span></span>



| <span data-ttu-id="22130-116">需求</span><span class="sxs-lookup"><span data-stu-id="22130-116">Requirement</span></span> | <span data-ttu-id="22130-117">值</span><span class="sxs-lookup"><span data-stu-id="22130-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22130-118">標頭</span><span class="sxs-lookup"><span data-stu-id="22130-118">Header</span></span><br/>  | <dl> <span data-ttu-id="22130-119"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="22130-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22130-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="22130-120">Library</span></span><br/> | <dl> <span data-ttu-id="22130-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="22130-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22130-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22130-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22130-123">**CBaseObject 類別**</span><span class="sxs-lookup"><span data-stu-id="22130-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




