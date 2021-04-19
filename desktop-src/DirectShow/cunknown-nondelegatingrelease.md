---
description: 遞減物件的參考計數。 這個方法會實 INonDelegatingUnknown：： NonDelegatingRelease 方法。
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: 'CUnknown. NonDelegatingRelease 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990954"
---
# <a name="cunknownnondelegatingrelease-method"></a><span data-ttu-id="12dfa-104">CUnknown. NonDelegatingRelease 方法</span><span class="sxs-lookup"><span data-stu-id="12dfa-104">CUnknown.NonDelegatingRelease method</span></span>

<span data-ttu-id="12dfa-105">遞減物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="12dfa-105">Decrements the reference count on the object.</span></span> <span data-ttu-id="12dfa-106">這個方法會實 **INonDelegatingUnknown：： NonDelegatingRelease** 方法。</span><span class="sxs-lookup"><span data-stu-id="12dfa-106">This method implements the **INonDelegatingUnknown::NonDelegatingRelease** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12dfa-107">語法</span><span class="sxs-lookup"><span data-stu-id="12dfa-107">Syntax</span></span>


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a><span data-ttu-id="12dfa-108">參數</span><span class="sxs-lookup"><span data-stu-id="12dfa-108">Parameters</span></span>

<span data-ttu-id="12dfa-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="12dfa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12dfa-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="12dfa-110">Return value</span></span>

<span data-ttu-id="12dfa-111">傳回參考計數。</span><span class="sxs-lookup"><span data-stu-id="12dfa-111">Returns the reference count.</span></span>

## <a name="remarks"></a><span data-ttu-id="12dfa-112">備註</span><span class="sxs-lookup"><span data-stu-id="12dfa-112">Remarks</span></span>

<span data-ttu-id="12dfa-113">當參考計數到達零時，物件就會刪除本身。</span><span class="sxs-lookup"><span data-stu-id="12dfa-113">When the reference count reaches zero, the object deletes itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="12dfa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="12dfa-114">Requirements</span></span>



| <span data-ttu-id="12dfa-115">需求</span><span class="sxs-lookup"><span data-stu-id="12dfa-115">Requirement</span></span> | <span data-ttu-id="12dfa-116">值</span><span class="sxs-lookup"><span data-stu-id="12dfa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12dfa-117">標頭</span><span class="sxs-lookup"><span data-stu-id="12dfa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="12dfa-118"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="12dfa-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12dfa-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="12dfa-119">Library</span></span><br/> | <dl> <span data-ttu-id="12dfa-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="12dfa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




