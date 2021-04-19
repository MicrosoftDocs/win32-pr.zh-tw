---
description: Format 方法會抓取格式區塊的指標。
ms.assetid: 368055cd-4592-4144-aef9-d7e830fc4de1
title: 'CMediaType： Format 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Format
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbfa7508ac8bb7e95134231c3567a9b6d4701224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001526"
---
# <a name="cmediatypeformat-method"></a><span data-ttu-id="72bb1-103">CMediaType 格式方法</span><span class="sxs-lookup"><span data-stu-id="72bb1-103">CMediaType.Format method</span></span>

<span data-ttu-id="72bb1-104">方法會抓取 `Format` 格式區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="72bb1-104">The `Format` method retrieves a pointer to the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="72bb1-105">語法</span><span class="sxs-lookup"><span data-stu-id="72bb1-105">Syntax</span></span>


```C++
BYTE* Format() const;
```



## <a name="parameters"></a><span data-ttu-id="72bb1-106">參數</span><span class="sxs-lookup"><span data-stu-id="72bb1-106">Parameters</span></span>

<span data-ttu-id="72bb1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="72bb1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72bb1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="72bb1-108">Return value</span></span>

<span data-ttu-id="72bb1-109">傳回 **pbFormat** 成員。</span><span class="sxs-lookup"><span data-stu-id="72bb1-109">Returns the **pbFormat** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="72bb1-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="72bb1-110">Requirements</span></span>



| <span data-ttu-id="72bb1-111">需求</span><span class="sxs-lookup"><span data-stu-id="72bb1-111">Requirement</span></span> | <span data-ttu-id="72bb1-112">值</span><span class="sxs-lookup"><span data-stu-id="72bb1-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bb1-113">標頭</span><span class="sxs-lookup"><span data-stu-id="72bb1-113">Header</span></span><br/>  | <dl> <span data-ttu-id="72bb1-114"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="72bb1-114"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="72bb1-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="72bb1-115">Library</span></span><br/> | <dl> <span data-ttu-id="72bb1-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="72bb1-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72bb1-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72bb1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72bb1-118">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="72bb1-118">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




