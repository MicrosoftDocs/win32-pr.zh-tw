---
description: Set 方法會設定另一種媒體類型的媒體類型。
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: CMediaType： Set 方法 (Mtype .h) -Mtype [ref] 參數
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
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "107001056"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="da0c6-103">CMediaType： Set 方法 (Mtype. h) </span><span class="sxs-lookup"><span data-stu-id="da0c6-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="da0c6-104">`Set`方法會設定另一種媒體類型的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="da0c6-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="da0c6-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="da0c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="da0c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da0c6-107">*mtype* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="da0c6-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="da0c6-108">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。</span><span class="sxs-lookup"><span data-stu-id="da0c6-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da0c6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="da0c6-109">Return value</span></span>

<span data-ttu-id="da0c6-110">傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。</span><span class="sxs-lookup"><span data-stu-id="da0c6-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="da0c6-111">備註</span><span class="sxs-lookup"><span data-stu-id="da0c6-111">Remarks</span></span>

<span data-ttu-id="da0c6-112">這個方法會從 *mtype* 複製整個媒體類型。</span><span class="sxs-lookup"><span data-stu-id="da0c6-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0c6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="da0c6-113">Requirements</span></span>



| <span data-ttu-id="da0c6-114">需求</span><span class="sxs-lookup"><span data-stu-id="da0c6-114">Requirement</span></span> | <span data-ttu-id="da0c6-115">值</span><span class="sxs-lookup"><span data-stu-id="da0c6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da0c6-116">標頭</span><span class="sxs-lookup"><span data-stu-id="da0c6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="da0c6-117"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="da0c6-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="da0c6-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="da0c6-118">Library</span></span><br/> | <dl> <span data-ttu-id="da0c6-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="da0c6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da0c6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da0c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0c6-121">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="da0c6-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




