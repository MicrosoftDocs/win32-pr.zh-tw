---
description: CreateMediaType 函式會配置新的 AM \_ 媒體 \_ 類型結構，包括格式區塊。
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: 'CreateMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999657"
---
# <a name="createmediatype-function"></a><span data-ttu-id="b5fdf-103">CreateMediaType 函式</span><span class="sxs-lookup"><span data-stu-id="b5fdf-103">CreateMediaType function</span></span>

<span data-ttu-id="b5fdf-104">**CreateMediaType** 函式會配置新的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構，包括格式區塊。</span><span class="sxs-lookup"><span data-stu-id="b5fdf-104">The **CreateMediaType** function allocates a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5fdf-105">語法</span><span class="sxs-lookup"><span data-stu-id="b5fdf-105">Syntax</span></span>


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="b5fdf-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5fdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5fdf-107">*.Psrc*</span><span class="sxs-lookup"><span data-stu-id="b5fdf-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="b5fdf-108">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b5fdf-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="b5fdf-109">方法會將此結構複製到新結構中。</span><span class="sxs-lookup"><span data-stu-id="b5fdf-109">The method copies this structure into the new structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5fdf-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5fdf-110">Return value</span></span>

<span data-ttu-id="b5fdf-111">傳回新的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構，如果發生錯誤則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b5fdf-111">Returns a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, or **NULL** if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5fdf-112">備註</span><span class="sxs-lookup"><span data-stu-id="b5fdf-112">Remarks</span></span>

<span data-ttu-id="b5fdf-113">若要釋放此函數所配置的記憶體，請呼叫 [**DeleteMediaType**](deletemediatype.md)。</span><span class="sxs-lookup"><span data-stu-id="b5fdf-113">To free the memory allocated by this function, call [**DeleteMediaType**](deletemediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5fdf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5fdf-114">Requirements</span></span>



| <span data-ttu-id="b5fdf-115">需求</span><span class="sxs-lookup"><span data-stu-id="b5fdf-115">Requirement</span></span> | <span data-ttu-id="b5fdf-116">值</span><span class="sxs-lookup"><span data-stu-id="b5fdf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fdf-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b5fdf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b5fdf-118"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b5fdf-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b5fdf-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5fdf-119">Library</span></span><br/> | <dl> <span data-ttu-id="b5fdf-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b5fdf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5fdf-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5fdf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5fdf-122">**媒體類型函式**</span><span class="sxs-lookup"><span data-stu-id="b5fdf-122">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




