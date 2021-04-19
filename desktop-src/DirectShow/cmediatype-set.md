---
description: CMediaType 方法 (Mtype 會) 設定另一種媒體類型的媒體類型。 方法使用 ' cmtype ' 參數。
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: CMediaType： Set 方法 (Mtype .h) -cmtype [ref] 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106992761"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a><span data-ttu-id="1a640-104">CMediaType： Set 方法 (Mtype .h) -cmtype [ref] 參數</span><span class="sxs-lookup"><span data-stu-id="1a640-104">CMediaType.Set method (Mtype.h) - cmtype [ref] parameter</span></span>

<span data-ttu-id="1a640-105">`Set`方法會設定另一種媒體類型的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a640-105">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a640-106">語法</span><span class="sxs-lookup"><span data-stu-id="1a640-106">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="1a640-107">參數</span><span class="sxs-lookup"><span data-stu-id="1a640-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a640-108">*cmtype* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="1a640-108">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1a640-109">[**CMediaType**](cmediatype.md)物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1a640-109">Reference to a [**CMediaType**](cmediatype.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a640-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a640-110">Return value</span></span>

<span data-ttu-id="1a640-111">傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。</span><span class="sxs-lookup"><span data-stu-id="1a640-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a640-112">備註</span><span class="sxs-lookup"><span data-stu-id="1a640-112">Remarks</span></span>

<span data-ttu-id="1a640-113">這個方法會從 *cmtype* 複製整個媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a640-113">This method copies the entire media type from *cmtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a640-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a640-114">Requirements</span></span>

| <span data-ttu-id="1a640-115">需求</span><span class="sxs-lookup"><span data-stu-id="1a640-115">Requirement</span></span>                   | <span data-ttu-id="1a640-116">值</span><span class="sxs-lookup"><span data-stu-id="1a640-116">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a640-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1a640-117">Header</span></span>  | <span data-ttu-id="1a640-118">Mtype (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="1a640-118">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="1a640-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a640-119">Library</span></span> | <span data-ttu-id="1a640-120"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="1a640-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="1a640-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a640-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a640-122">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="1a640-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




