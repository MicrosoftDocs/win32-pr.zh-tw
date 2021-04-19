---
description: 這個運算子會測試 CMediaType 物件之間是否不相等。
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: 'CMediaType. CMediaType：： operator！ = 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe3d5b60ed1990423d5ad9375ffdf192da313b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990571"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="1af92-103">CMediaType. CMediaType：： operator！ = 方法</span><span class="sxs-lookup"><span data-stu-id="1af92-103">CMediaType.CMediaType::operator!= method</span></span>

<span data-ttu-id="1af92-104">這個運算子會測試 [**CMediaType**](cmediatype.md) 物件之間是否不相等。</span><span class="sxs-lookup"><span data-stu-id="1af92-104">This operator tests for inequality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af92-105">語法</span><span class="sxs-lookup"><span data-stu-id="1af92-105">Syntax</span></span>


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="1af92-106">參數</span><span class="sxs-lookup"><span data-stu-id="1af92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af92-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="1af92-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1af92-108">要比較的 **CMediaType** 物件參考。</span><span class="sxs-lookup"><span data-stu-id="1af92-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af92-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1af92-109">Return value</span></span>

<span data-ttu-id="1af92-110">如果 *rt* 不等於這個物件，**則傳回 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="1af92-110">Returns **TRUE** if *rt* is not equal to this object.</span></span> <span data-ttu-id="1af92-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1af92-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af92-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1af92-112">Requirements</span></span>



| <span data-ttu-id="1af92-113">需求</span><span class="sxs-lookup"><span data-stu-id="1af92-113">Requirement</span></span> | <span data-ttu-id="1af92-114">值</span><span class="sxs-lookup"><span data-stu-id="1af92-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af92-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1af92-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1af92-116"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1af92-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1af92-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="1af92-117">Library</span></span><br/> | <dl> <span data-ttu-id="1af92-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1af92-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af92-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1af92-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af92-120">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="1af92-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




