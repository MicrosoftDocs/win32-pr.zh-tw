---
description: FreeMediaType 函式會刪除 AM \_ 媒體類型結構中的格式區塊 \_ 。
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: 'FreeMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984809"
---
# <a name="freemediatype-function"></a><span data-ttu-id="127df-103">FreeMediaType 函式</span><span class="sxs-lookup"><span data-stu-id="127df-103">FreeMediaType function</span></span>

<span data-ttu-id="127df-104">**FreeMediaType** 函式會刪除 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構中的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="127df-104">The **FreeMediaType** function deletes the format block in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="127df-105">語法</span><span class="sxs-lookup"><span data-stu-id="127df-105">Syntax</span></span>


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a><span data-ttu-id="127df-106">參數</span><span class="sxs-lookup"><span data-stu-id="127df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="127df-107">*mt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="127df-107">*mt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="127df-108">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。</span><span class="sxs-lookup"><span data-stu-id="127df-108">A reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="127df-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="127df-109">Return value</span></span>

<span data-ttu-id="127df-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="127df-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="127df-111">備註</span><span class="sxs-lookup"><span data-stu-id="127df-111">Remarks</span></span>

<span data-ttu-id="127df-112">格式區塊會配置在堆積上。</span><span class="sxs-lookup"><span data-stu-id="127df-112">The format block is allocated on the heap.</span></span> <span data-ttu-id="127df-113">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)的 **pbFormat** 成員指向格式區塊。</span><span class="sxs-lookup"><span data-stu-id="127df-113">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) points to the format block.</span></span> <span data-ttu-id="127df-114">使用此函式只釋出格式區塊。</span><span class="sxs-lookup"><span data-stu-id="127df-114">Use this function to free just the format block.</span></span> <span data-ttu-id="127df-115">若要刪除配置的 **AM \_ 媒體 \_ 類型** 結構，請呼叫 [**DeleteMediaType**](deletemediatype.md)。</span><span class="sxs-lookup"><span data-stu-id="127df-115">To delete an allocated **AM\_MEDIA\_TYPE** structure, call [**DeleteMediaType**](deletemediatype.md).</span></span>

<span data-ttu-id="127df-116">此函式定義于 [DirectShow 基底類別](directshow-base-classes.md) 庫中。</span><span class="sxs-lookup"><span data-stu-id="127df-116">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="127df-117">如果您不想要連結至基底類別庫，您可以使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="127df-117">If you prefer not to link to the base class library, you can use the following code:</span></span>


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="127df-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="127df-118">Requirements</span></span>



| <span data-ttu-id="127df-119">需求</span><span class="sxs-lookup"><span data-stu-id="127df-119">Requirement</span></span> | <span data-ttu-id="127df-120">值</span><span class="sxs-lookup"><span data-stu-id="127df-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="127df-121">標頭</span><span class="sxs-lookup"><span data-stu-id="127df-121">Header</span></span><br/>  | <dl> <span data-ttu-id="127df-122"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="127df-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="127df-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="127df-123">Library</span></span><br/> | <dl> <span data-ttu-id="127df-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="127df-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="127df-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="127df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127df-126">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="127df-126">**DeleteMediaType**</span></span>](deletemediatype.md)
</dt> <dt>

[<span data-ttu-id="127df-127">**媒體類型函式**</span><span class="sxs-lookup"><span data-stu-id="127df-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




