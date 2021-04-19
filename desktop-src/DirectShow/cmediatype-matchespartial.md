---
description: MatchesPartial 方法會判斷此媒體類型是否符合部分指定的媒體類型。
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: 'CMediaType. MatchesPartial 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994794"
---
# <a name="cmediatypematchespartial-method"></a><span data-ttu-id="948db-103">CMediaType. MatchesPartial 方法</span><span class="sxs-lookup"><span data-stu-id="948db-103">CMediaType.MatchesPartial method</span></span>

<span data-ttu-id="948db-104">`MatchesPartial`方法會判斷此媒體類型是否符合部分指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="948db-104">The `MatchesPartial` method determines if this media type matches a partially specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="948db-105">語法</span><span class="sxs-lookup"><span data-stu-id="948db-105">Syntax</span></span>


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a><span data-ttu-id="948db-106">參數</span><span class="sxs-lookup"><span data-stu-id="948db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948db-107">*ppartial*</span><span class="sxs-lookup"><span data-stu-id="948db-107">*ppartial*</span></span> 
</dt> <dd>

<span data-ttu-id="948db-108">要比對之媒體類型的指標。</span><span class="sxs-lookup"><span data-stu-id="948db-108">Pointer to the media type to match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948db-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="948db-109">Return value</span></span>

<span data-ttu-id="948db-110">如果媒體類型相符，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="948db-110">Returns **TRUE** if the media types match.</span></span> <span data-ttu-id="948db-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="948db-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="948db-112">備註</span><span class="sxs-lookup"><span data-stu-id="948db-112">Remarks</span></span>

<span data-ttu-id="948db-113">*Ppartial* 指定的媒體類型可以有 \_ 主要類型、子類型或格式類型的 GUID Null 值。</span><span class="sxs-lookup"><span data-stu-id="948db-113">The media type specified by *ppartial* can have a value of GUID\_NULL for the major type, subtype, or format type.</span></span> <span data-ttu-id="948db-114">任何具有 GUID \_ Null 值的成員都不會進行測試。</span><span class="sxs-lookup"><span data-stu-id="948db-114">Any members with GUID\_NULL values are not tested.</span></span> <span data-ttu-id="948db-115"> (生效，GUID \_ null 可作為萬用字元。具有 guid null 以外值的 ) 成員 \_ 必須符合，才能讓媒體類型相符。</span><span class="sxs-lookup"><span data-stu-id="948db-115">(In effect, GUID\_NULL acts as a wildcard.) Members with values other than GUID\_NULL must match for the media type to match.</span></span>

## <a name="requirements"></a><span data-ttu-id="948db-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="948db-116">Requirements</span></span>



| <span data-ttu-id="948db-117">需求</span><span class="sxs-lookup"><span data-stu-id="948db-117">Requirement</span></span> | <span data-ttu-id="948db-118">值</span><span class="sxs-lookup"><span data-stu-id="948db-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="948db-119">標頭</span><span class="sxs-lookup"><span data-stu-id="948db-119">Header</span></span><br/>  | <dl> <span data-ttu-id="948db-120"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="948db-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="948db-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="948db-121">Library</span></span><br/> | <dl> <span data-ttu-id="948db-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="948db-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="948db-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="948db-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948db-124">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="948db-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




