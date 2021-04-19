---
description: CBaseObject 類別是用來執行 DirectShow 物件的抽象類別。 若要執行元件物件模型 (COM) 物件，請使用衍生自 CBaseObject 的 CUnknown 類別。
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: 'CBaseObject 類別 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994012"
---
# <a name="cbaseobject-class"></a><span data-ttu-id="e18ca-104">CBaseObject 類別</span><span class="sxs-lookup"><span data-stu-id="e18ca-104">CBaseObject class</span></span>

<span data-ttu-id="e18ca-105">**CBaseObject** 類別是用來執行 DirectShow 物件的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="e18ca-105">The **CBaseObject** class is an abstract class for implementing DirectShow objects.</span></span> <span data-ttu-id="e18ca-106">若要執行元件物件模型 (COM) 物件，請使用衍生自 **CBaseObject** 的 [**CUnknown**](cunknown.md)類別。</span><span class="sxs-lookup"><span data-stu-id="e18ca-106">To implement Component Object Model (COM) objects, use the [**CUnknown**](cunknown.md) class, which derives from **CBaseObject**.</span></span>



| <span data-ttu-id="e18ca-107">類別方法</span><span class="sxs-lookup"><span data-stu-id="e18ca-107">Class Methods</span></span>                                      | <span data-ttu-id="e18ca-108">Description</span><span class="sxs-lookup"><span data-stu-id="e18ca-108">Description</span></span>                            |
|----------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="e18ca-109">**CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="e18ca-109">**CBaseObject**</span></span>](cbaseobject-cbaseobject.md)     | <span data-ttu-id="e18ca-110">函式方法。</span><span class="sxs-lookup"><span data-stu-id="e18ca-110">Constructor method.</span></span>                    |
| [<span data-ttu-id="e18ca-111">**~ CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="e18ca-111">**~CBaseObject**</span></span>](cbaseobject--cbaseobject.md)   | <span data-ttu-id="e18ca-112">函式方法。</span><span class="sxs-lookup"><span data-stu-id="e18ca-112">Destructor method.</span></span>                     |
| [<span data-ttu-id="e18ca-113">**ObjectsActive**</span><span class="sxs-lookup"><span data-stu-id="e18ca-113">**ObjectsActive**</span></span>](cbaseobject-objectsactive.md) | <span data-ttu-id="e18ca-114">捕獲使用中物件的計數。</span><span class="sxs-lookup"><span data-stu-id="e18ca-114">Retrieves the count of active objects.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e18ca-115">備註</span><span class="sxs-lookup"><span data-stu-id="e18ca-115">Remarks</span></span>

<span data-ttu-id="e18ca-116">大部分的 DirectShow 基底類別都衍生自 **CBaseObject**。</span><span class="sxs-lookup"><span data-stu-id="e18ca-116">Most of the DirectShow base classes derive from **CBaseObject**.</span></span> <span data-ttu-id="e18ca-117">這個類別會在執行時間將所有的 DirectShow 物件計數保持在作用中狀態，以提供偵錯工具的協助。</span><span class="sxs-lookup"><span data-stu-id="e18ca-117">This class provides debugging assistance by keeping a count of all the DirectShow objects active during run time.</span></span> <span data-ttu-id="e18ca-118">物件計數會儲存在類別靜態成員變數中：</span><span class="sxs-lookup"><span data-stu-id="e18ca-118">The object count is stored in a class-static member variable:</span></span>


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



<span data-ttu-id="e18ca-119">在「偵錯工具」組建中，如果物件計數大於零，則會判斷提示 DLL 是否已卸載。</span><span class="sxs-lookup"><span data-stu-id="e18ca-119">In debug builds, the DLL will assert if it is unloaded while the object count is greater than zero.</span></span> <span data-ttu-id="e18ca-120">這可讓您更輕鬆地追蹤參考計數問題所造成的流失問題。</span><span class="sxs-lookup"><span data-stu-id="e18ca-120">This makes it easier to track down leaks caused by reference-counting problems.</span></span>

<span data-ttu-id="e18ca-121">**CBaseObject** 的函式會接受一個引數，也就是物件的偵錯工具名稱。</span><span class="sxs-lookup"><span data-stu-id="e18ca-121">The **CBaseObject** constructor takes one argument, a debugging name for the object.</span></span> <span data-ttu-id="e18ca-122">這個名稱會儲存在 DLL 的全域資料表中。</span><span class="sxs-lookup"><span data-stu-id="e18ca-122">This name is stored in a global table in the DLL.</span></span> <span data-ttu-id="e18ca-123">[**DbgDumpObjectRegister**](dbgdumpobjectregister.md)函式會格式化 DLL 中的作用中物件清單，並將其傳送至 debug 輸出。</span><span class="sxs-lookup"><span data-stu-id="e18ca-123">The [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function formats a list of the objects active in the DLL, and sends it to the debug output.</span></span>

## <a name="requirements"></a><span data-ttu-id="e18ca-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e18ca-124">Requirements</span></span>



| <span data-ttu-id="e18ca-125">需求</span><span class="sxs-lookup"><span data-stu-id="e18ca-125">Requirement</span></span> | <span data-ttu-id="e18ca-126">值</span><span class="sxs-lookup"><span data-stu-id="e18ca-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e18ca-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e18ca-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e18ca-128"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e18ca-128"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e18ca-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e18ca-129">Library</span></span><br/> | <dl> <span data-ttu-id="e18ca-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e18ca-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e18ca-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e18ca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18ca-132">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="e18ca-132">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




