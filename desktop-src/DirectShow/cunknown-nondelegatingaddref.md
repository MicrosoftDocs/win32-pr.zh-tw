---
description: NonDelegatingAddRef 方法會遞增物件的參考計數。 這個方法會實 INonDelegatingUnknown：： NonDelegatingAddRef 方法。
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: 'CUnknown. NonDelegatingAddRef 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingAddRef
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f97260c03f0931e94e8ce6de8b7816789b2fe66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996239"
---
# <a name="cunknownnondelegatingaddref-method"></a><span data-ttu-id="dd1a3-104">CUnknown. NonDelegatingAddRef 方法</span><span class="sxs-lookup"><span data-stu-id="dd1a3-104">CUnknown.NonDelegatingAddRef method</span></span>

<span data-ttu-id="dd1a3-105">`NonDelegatingAddRef`方法會遞增物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="dd1a3-105">The `NonDelegatingAddRef` method increments the reference count on the object.</span></span> <span data-ttu-id="dd1a3-106">這個方法會實 **INonDelegatingUnknown：： NonDelegatingAddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="dd1a3-106">This method implements the **INonDelegatingUnknown::NonDelegatingAddRef** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="dd1a3-107">Syntax</span></span>


```C++
ULONG NonDelegatingAddRef();
```



## <a name="parameters"></a><span data-ttu-id="dd1a3-108">參數</span><span class="sxs-lookup"><span data-stu-id="dd1a3-108">Parameters</span></span>

<span data-ttu-id="dd1a3-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dd1a3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd1a3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd1a3-110">Return value</span></span>

<span data-ttu-id="dd1a3-111">傳回參考計數。</span><span class="sxs-lookup"><span data-stu-id="dd1a3-111">Returns the reference count.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1a3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd1a3-112">Requirements</span></span>



| <span data-ttu-id="dd1a3-113">需求</span><span class="sxs-lookup"><span data-stu-id="dd1a3-113">Requirement</span></span> | <span data-ttu-id="dd1a3-114">值</span><span class="sxs-lookup"><span data-stu-id="dd1a3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1a3-115">標頭</span><span class="sxs-lookup"><span data-stu-id="dd1a3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="dd1a3-116"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dd1a3-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd1a3-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="dd1a3-117">Library</span></span><br/> | <dl> <span data-ttu-id="dd1a3-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dd1a3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




