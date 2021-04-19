---
description: TypesMatch 方法會判斷輸入媒體類型是否符合輸出媒體類型。
ms.assetid: e814d532-70ce-4f9b-9ce3-172daea0dad5
title: 'CTransInPlaceFilter. TypesMatch 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.TypesMatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea8f3da122b8c8dbc6ba113d8088f71d5b19f104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990690"
---
# <a name="ctransinplacefiltertypesmatch-method"></a><span data-ttu-id="bc1ce-103">CTransInPlaceFilter. TypesMatch 方法</span><span class="sxs-lookup"><span data-stu-id="bc1ce-103">CTransInPlaceFilter.TypesMatch method</span></span>

<span data-ttu-id="bc1ce-104">`TypesMatch`方法會判斷輸入媒體類型是否符合輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="bc1ce-104">The `TypesMatch` method determines whether the input media type matches the output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc1ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc1ce-105">Syntax</span></span>


```C++
BOOL TypesMatch();
```



## <a name="parameters"></a><span data-ttu-id="bc1ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc1ce-106">Parameters</span></span>

<span data-ttu-id="bc1ce-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bc1ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc1ce-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc1ce-108">Return value</span></span>

<span data-ttu-id="bc1ce-109">如果輸入和輸出媒體類型相同，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bc1ce-109">Returns **TRUE** if the input and output media types are the same, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc1ce-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc1ce-110">Requirements</span></span>



| <span data-ttu-id="bc1ce-111">需求</span><span class="sxs-lookup"><span data-stu-id="bc1ce-111">Requirement</span></span> | <span data-ttu-id="bc1ce-112">值</span><span class="sxs-lookup"><span data-stu-id="bc1ce-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc1ce-113">標頭</span><span class="sxs-lookup"><span data-stu-id="bc1ce-113">Header</span></span><br/>  | <dl> <span data-ttu-id="bc1ce-114"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bc1ce-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bc1ce-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc1ce-115">Library</span></span><br/> | <dl> <span data-ttu-id="bc1ce-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bc1ce-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc1ce-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc1ce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc1ce-118">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="bc1ce-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




