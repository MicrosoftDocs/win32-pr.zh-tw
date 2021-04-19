---
description: CMediaType. CMediaType：： operator = 方法 (Mtype. h) 多載指派運算子來複製媒體類型。
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: CMediaType. CMediaType：： operator = method (Mtype. h) -cmtype 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106982249"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a><span data-ttu-id="578dc-103">CMediaType. CMediaType：： operator = method (Mtype. h) -cmtype 參數</span><span class="sxs-lookup"><span data-stu-id="578dc-103">CMediaType.CMediaType::operator= method (Mtype.h) - cmtype parameter</span></span>

<span data-ttu-id="578dc-104">這個運算子會多載指派運算子來複製媒體類型。</span><span class="sxs-lookup"><span data-stu-id="578dc-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="578dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="578dc-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="578dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="578dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578dc-107">*cmtype* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="578dc-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="578dc-108">**CMediaType** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="578dc-108">Reference to a **CMediaType** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="578dc-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="578dc-109">Return value</span></span>

<span data-ttu-id="578dc-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="578dc-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="578dc-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="578dc-111">Requirements</span></span>

| <span data-ttu-id="578dc-112">需求</span><span class="sxs-lookup"><span data-stu-id="578dc-112">Requirement</span></span>                   | <span data-ttu-id="578dc-113">值</span><span class="sxs-lookup"><span data-stu-id="578dc-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="578dc-114">標頭</span><span class="sxs-lookup"><span data-stu-id="578dc-114">Header</span></span>  | <span data-ttu-id="578dc-115">Mtype (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="578dc-115">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="578dc-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="578dc-116">Library</span></span> | <span data-ttu-id="578dc-117"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="578dc-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="578dc-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="578dc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578dc-119">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="578dc-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




