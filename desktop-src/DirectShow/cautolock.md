---
description: CAutoLock 類別會保留程式碼區塊範圍的重要區段。
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: 'CAutoLock 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977516"
---
# <a name="cautolock-class"></a><span data-ttu-id="ce712-103">CAutoLock 類別</span><span class="sxs-lookup"><span data-stu-id="ce712-103">CAutoLock class</span></span>

<span data-ttu-id="ce712-104">`CAutoLock`類別會保留程式碼區塊範圍的重要區段。</span><span class="sxs-lookup"><span data-stu-id="ce712-104">The `CAutoLock` class holds a critical section for the scope of a code block.</span></span>

<span data-ttu-id="ce712-105">這個類別會與 [**CCritSec**](ccritsec.md) 類別搭配使用，這是重要區段物件的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="ce712-105">This class works in conjunction with the [**CCritSec**](ccritsec.md) class, which is a wrapper for critical section objects.</span></span> <span data-ttu-id="ce712-106">此 `CAutoLock` 函式會鎖定重要區段，並將它解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="ce712-106">The `CAutoLock` constructor locks the critical section, and the destructor unlocks it.</span></span> <span data-ttu-id="ce712-107">`CAutoLock`您可以使用物件做為區域變數，藉由確保所有程式碼路徑都能解除鎖定重要區段，來鎖定重要區段。</span><span class="sxs-lookup"><span data-stu-id="ce712-107">By using a `CAutoLock` object as a local variable, you can lock a critical section with the guarantee that all code paths will unlock the critical section.</span></span>

<span data-ttu-id="ce712-108">下列程式碼範例顯示如何使用這個類別：</span><span class="sxs-lookup"><span data-stu-id="ce712-108">The following code example shows how to use this class:</span></span>


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



<span data-ttu-id="ce712-109">此類別中的方法不是設計成要覆寫。</span><span class="sxs-lookup"><span data-stu-id="ce712-109">The methods in this class are not designed to be overridden.</span></span>



| <span data-ttu-id="ce712-110">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="ce712-110">Protected Member Variables</span></span>                 | <span data-ttu-id="ce712-111">Description</span><span class="sxs-lookup"><span data-stu-id="ce712-111">Description</span></span>                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="ce712-112">**m \_ pLock**</span><span class="sxs-lookup"><span data-stu-id="ce712-112">**m\_pLock**</span></span>](cautolock-m-plock.md)      | <span data-ttu-id="ce712-113">此鎖定的重要區段。</span><span class="sxs-lookup"><span data-stu-id="ce712-113">Critical section for this lock.</span></span>                                  |
| <span data-ttu-id="ce712-114">公用方法</span><span class="sxs-lookup"><span data-stu-id="ce712-114">Public Methods</span></span>                             | <span data-ttu-id="ce712-115">Description</span><span class="sxs-lookup"><span data-stu-id="ce712-115">Description</span></span>                                                      |
| [<span data-ttu-id="ce712-116">**CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="ce712-116">**CAutoLock**</span></span>](cautolock-cautolock.md)   | <span data-ttu-id="ce712-117">函式方法。</span><span class="sxs-lookup"><span data-stu-id="ce712-117">Constructor method.</span></span> <span data-ttu-id="ce712-118">鎖定指定的重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="ce712-118">Locks the specified critical section object.</span></span> |
| [<span data-ttu-id="ce712-119">**~ CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="ce712-119">**~CAutoLock**</span></span>](cautolock--cautolock.md) | <span data-ttu-id="ce712-120">函式方法。</span><span class="sxs-lookup"><span data-stu-id="ce712-120">Destructor method.</span></span> <span data-ttu-id="ce712-121">解除鎖定重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="ce712-121">Unlocks the critical section object.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="ce712-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce712-122">Requirements</span></span>



| <span data-ttu-id="ce712-123">需求</span><span class="sxs-lookup"><span data-stu-id="ce712-123">Requirement</span></span> | <span data-ttu-id="ce712-124">值</span><span class="sxs-lookup"><span data-stu-id="ce712-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce712-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ce712-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ce712-126"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ce712-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ce712-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce712-127">Library</span></span><br/> | <dl> <span data-ttu-id="ce712-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ce712-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




