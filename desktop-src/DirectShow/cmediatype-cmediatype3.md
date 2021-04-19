---
description: 深入瞭解 CMediaType. CMediaType (Mtype 的) 方法。 這個方法會使用 ' mtype ' 和 ' phr ' 參數。
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: CMediaType. CMediaType (Mtype. h) -Mtype 和 phr 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106997432"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a><span data-ttu-id="3e976-104">CMediaType. CMediaType (Mtype. h) -Mtype 和 phr 參數</span><span class="sxs-lookup"><span data-stu-id="3e976-104">CMediaType.CMediaType constructor (Mtype.h) - mtype and phr parameters</span></span>

<span data-ttu-id="3e976-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="3e976-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e976-106">語法</span><span class="sxs-lookup"><span data-stu-id="3e976-106">Syntax</span></span>


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="3e976-107">參數</span><span class="sxs-lookup"><span data-stu-id="3e976-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e976-108">*mtype* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="3e976-108">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3e976-109">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。</span><span class="sxs-lookup"><span data-stu-id="3e976-109">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="3e976-110">此函式會將媒體類型複製到新的物件，包括格式區塊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3e976-110">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="3e976-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="3e976-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3e976-112">接收 HRESULT 值之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="3e976-112">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="3e976-113">這個參數可以是 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="3e976-113">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="3e976-114">否則，呼叫端必須在呼叫此函式之前，將值設定為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3e976-114">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="3e976-115">如果此函式失敗，則會將值設定為失敗碼。</span><span class="sxs-lookup"><span data-stu-id="3e976-115">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e976-116">備註</span><span class="sxs-lookup"><span data-stu-id="3e976-116">Remarks</span></span>

<span data-ttu-id="3e976-117">此函式會呼叫 [**CMediaType：： InitMediaType**](cmediatype-initmediatype.md) 方法來初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3e976-117">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e976-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e976-118">Requirements</span></span>

| <span data-ttu-id="3e976-119">需求</span><span class="sxs-lookup"><span data-stu-id="3e976-119">Requirement</span></span>                   | <span data-ttu-id="3e976-120">值</span><span class="sxs-lookup"><span data-stu-id="3e976-120">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e976-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3e976-121">Header</span></span>  | <span data-ttu-id="3e976-122">Mtype (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="3e976-122">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="3e976-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e976-123">Library</span></span> | <span data-ttu-id="3e976-124"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="3e976-124">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3e976-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e976-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e976-126">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="3e976-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




