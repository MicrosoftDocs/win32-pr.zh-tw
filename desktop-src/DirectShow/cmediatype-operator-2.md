---
description: 這個運算子會多載指派運算子來複製媒體類型。
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: CMediaType. CMediaType：： operator = method (Mtype. h) -Mtype 參數
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
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106980257"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="a38c7-103">CMediaType. CMediaType：： operator = method (Mtype .h) </span><span class="sxs-lookup"><span data-stu-id="a38c7-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="a38c7-104">這個運算子會多載指派運算子來複製媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a38c7-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="a38c7-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="a38c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="a38c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38c7-107">*mtype* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="a38c7-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a38c7-108">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。</span><span class="sxs-lookup"><span data-stu-id="a38c7-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38c7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a38c7-109">Return value</span></span>

<span data-ttu-id="a38c7-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a38c7-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38c7-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a38c7-111">Requirements</span></span>



| <span data-ttu-id="a38c7-112">需求</span><span class="sxs-lookup"><span data-stu-id="a38c7-112">Requirement</span></span> | <span data-ttu-id="a38c7-113">值</span><span class="sxs-lookup"><span data-stu-id="a38c7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38c7-114">標頭</span><span class="sxs-lookup"><span data-stu-id="a38c7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a38c7-115"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a38c7-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a38c7-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="a38c7-116">Library</span></span><br/> | <dl> <span data-ttu-id="a38c7-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a38c7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a38c7-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a38c7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38c7-119">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="a38c7-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




