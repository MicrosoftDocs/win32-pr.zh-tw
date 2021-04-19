---
description: DeleteMediaType 函式會刪除配置的 AM \_ 媒體 \_ 類型結構，包括格式區塊。
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: 'DeleteMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993285"
---
# <a name="deletemediatype-function"></a><span data-ttu-id="67bb9-103">DeleteMediaType 函式</span><span class="sxs-lookup"><span data-stu-id="67bb9-103">DeleteMediaType function</span></span>

<span data-ttu-id="67bb9-104">**DeleteMediaType** 函式會刪除配置的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構，包括格式區塊。</span><span class="sxs-lookup"><span data-stu-id="67bb9-104">The **DeleteMediaType** function deletes an allocated [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="67bb9-105">語法</span><span class="sxs-lookup"><span data-stu-id="67bb9-105">Syntax</span></span>


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="67bb9-106">參數</span><span class="sxs-lookup"><span data-stu-id="67bb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67bb9-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="67bb9-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="67bb9-108">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="67bb9-108">A pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67bb9-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="67bb9-109">Return value</span></span>

<span data-ttu-id="67bb9-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="67bb9-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67bb9-111">備註</span><span class="sxs-lookup"><span data-stu-id="67bb9-111">Remarks</span></span>

<span data-ttu-id="67bb9-112">使用此函式釋放使用 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 或 [**CreateMediaType**](createmediatype.md)所配置的任何媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="67bb9-112">Use this function to release any media type structure that was allocated using either [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) or [**CreateMediaType**](createmediatype.md).</span></span>

<span data-ttu-id="67bb9-113">此函式定義于 [DirectShow 基底類別](directshow-base-classes.md) 庫中。</span><span class="sxs-lookup"><span data-stu-id="67bb9-113">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="67bb9-114">如果您不想要連結至基底類別庫，您可以使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="67bb9-114">If you prefer not to link to the base class library, you can use the following code:</span></span>


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


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="67bb9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="67bb9-115">Requirements</span></span>



| <span data-ttu-id="67bb9-116">需求</span><span class="sxs-lookup"><span data-stu-id="67bb9-116">Requirement</span></span> | <span data-ttu-id="67bb9-117">值</span><span class="sxs-lookup"><span data-stu-id="67bb9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67bb9-118">標頭</span><span class="sxs-lookup"><span data-stu-id="67bb9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="67bb9-119"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="67bb9-119"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="67bb9-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="67bb9-120">Library</span></span><br/> | <dl> <span data-ttu-id="67bb9-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="67bb9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67bb9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67bb9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67bb9-123">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="67bb9-123">**FreeMediaType**</span></span>](freemediatype.md)
</dt> <dt>

[<span data-ttu-id="67bb9-124">**媒體類型函式**</span><span class="sxs-lookup"><span data-stu-id="67bb9-124">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

