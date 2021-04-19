---
description: 這個運算子會測試 CMediaType 物件是否相等。
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'CMediaType. CMediaType：： operator = = 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984782"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="f2fd4-103">CMediaType. CMediaType：： operator = = 方法</span><span class="sxs-lookup"><span data-stu-id="f2fd4-103">CMediaType.CMediaType::operator== method</span></span>

<span data-ttu-id="f2fd4-104">這個運算子會測試 [**CMediaType**](cmediatype.md) 物件是否相等。</span><span class="sxs-lookup"><span data-stu-id="f2fd4-104">This operator tests for equality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fd4-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2fd4-105">Syntax</span></span>


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="f2fd4-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2fd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2fd4-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="f2fd4-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fd4-108">要比較的 **CMediaType** 物件參考。</span><span class="sxs-lookup"><span data-stu-id="f2fd4-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2fd4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2fd4-109">Return value</span></span>

<span data-ttu-id="f2fd4-110">如果 *rt* 等於這個物件，**則傳回 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f2fd4-110">Returns **TRUE** if *rt* is equal to this object.</span></span> <span data-ttu-id="f2fd4-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f2fd4-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fd4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2fd4-112">Requirements</span></span>



| <span data-ttu-id="f2fd4-113">需求</span><span class="sxs-lookup"><span data-stu-id="f2fd4-113">Requirement</span></span> | <span data-ttu-id="f2fd4-114">值</span><span class="sxs-lookup"><span data-stu-id="f2fd4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fd4-115">標頭</span><span class="sxs-lookup"><span data-stu-id="f2fd4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f2fd4-116"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f2fd4-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f2fd4-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2fd4-117">Library</span></span><br/> | <dl> <span data-ttu-id="f2fd4-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f2fd4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2fd4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2fd4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fd4-120">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="f2fd4-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




