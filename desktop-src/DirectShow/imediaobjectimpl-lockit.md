---
description: LockIt 類別是鎖定和解除鎖定的內部類別。
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'IMediaObjectImpl：： LockIt 類別 (Dmoimpl .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994224"
---
# <a name="imediaobjectimpllockit-class"></a><span data-ttu-id="9bd79-103">IMediaObjectImpl：： LockIt 類別</span><span class="sxs-lookup"><span data-stu-id="9bd79-103">IMediaObjectImpl::LockIt Class</span></span>

<span data-ttu-id="9bd79-104">`LockIt`類別是鎖定和解除鎖定的內部類別。</span><span class="sxs-lookup"><span data-stu-id="9bd79-104">The `LockIt` class is an internal class that locks and unlocks the DMO.</span></span>

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a><span data-ttu-id="9bd79-105">參數</span><span class="sxs-lookup"><span data-stu-id="9bd79-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd79-106"><span id="p"></span><span id="P"></span>*P*</span><span class="sxs-lookup"><span data-stu-id="9bd79-106"><span id="p"></span><span id="P"></span>*p*</span></span>
</dt> <dd>

<span data-ttu-id="9bd79-107">衍生物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9bd79-107">Pointer to the derived object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bd79-108">備註</span><span class="sxs-lookup"><span data-stu-id="9bd79-108">Remarks</span></span>

<span data-ttu-id="9bd79-109">此 `LockIt` 函式會鎖定，而此函式會解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="9bd79-109">The `LockIt` constructor locks the DMO, and the destructor unlocks the DMO.</span></span> <span data-ttu-id="9bd79-110">若要從您的衍生類別內鎖定物件，請宣告類型的本機變數 `LockIt` 。</span><span class="sxs-lookup"><span data-stu-id="9bd79-110">To lock the object from inside your derived class, declare a local variable of type `LockIt`.</span></span> <span data-ttu-id="9bd79-111">當物件保持在範圍內時，會鎖定 `LockIt` ：</span><span class="sxs-lookup"><span data-stu-id="9bd79-111">The DMO is locked while the `LockIt` object remains in scope:</span></span>


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



<span data-ttu-id="9bd79-112">**IMediaObjectImpl** 中的方法會自動鎖定。</span><span class="sxs-lookup"><span data-stu-id="9bd79-112">The methods in **IMediaObjectImpl** automatically lock the DMO.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd79-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bd79-113">Requirements</span></span>



| <span data-ttu-id="9bd79-114">需求</span><span class="sxs-lookup"><span data-stu-id="9bd79-114">Requirement</span></span> | <span data-ttu-id="9bd79-115">值</span><span class="sxs-lookup"><span data-stu-id="9bd79-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd79-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9bd79-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9bd79-117"><dt>Dmoimpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bd79-117"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="9bd79-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="9bd79-118">Library</span></span><br/> | <dl> <span data-ttu-id="9bd79-119"><dt>Dmoguids .lib;</dt><dt>Msdmo .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bd79-119"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bd79-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bd79-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd79-121">**IMediaObjectImpl 類別範本**</span><span class="sxs-lookup"><span data-stu-id="9bd79-121">**IMediaObjectImpl Class Template**</span></span>](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




