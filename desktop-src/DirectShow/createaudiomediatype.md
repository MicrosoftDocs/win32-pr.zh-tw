---
description: CreateAudioMediaType 函式會從 WAVEFORMATEX 結構初始化媒體類型。
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: 'CreateAudioMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983153"
---
# <a name="createaudiomediatype-function"></a><span data-ttu-id="bfda0-103">CreateAudioMediaType 函式</span><span class="sxs-lookup"><span data-stu-id="bfda0-103">CreateAudioMediaType function</span></span>

<span data-ttu-id="bfda0-104">**CreateAudioMediaType** 函式會從 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="bfda0-104">The **CreateAudioMediaType** function initializes a media type from a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfda0-105">語法</span><span class="sxs-lookup"><span data-stu-id="bfda0-105">Syntax</span></span>


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a><span data-ttu-id="bfda0-106">參數</span><span class="sxs-lookup"><span data-stu-id="bfda0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfda0-107">*pwfx*</span><span class="sxs-lookup"><span data-stu-id="bfda0-107">*pwfx*</span></span> 
</dt> <dd>

<span data-ttu-id="bfda0-108">所提供 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bfda0-108">Pointer to the supplied [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bfda0-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="bfda0-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="bfda0-110">要初始化的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="bfda0-110">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="bfda0-111">*bSetFormat*</span><span class="sxs-lookup"><span data-stu-id="bfda0-111">*bSetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="bfda0-112">指出是否要初始化格式區塊的旗標。</span><span class="sxs-lookup"><span data-stu-id="bfda0-112">Flag indicating whether to initialize the format block.</span></span> <span data-ttu-id="bfda0-113">指定 **TRUE** 表示將它初始化，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bfda0-113">Specify **TRUE** to initialize it, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfda0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfda0-114">Return value</span></span>

<span data-ttu-id="bfda0-115">如果無法配置記憶體給格式資料，則傳回 E \_ OUTOFMEMORY;\_否則為 [否]。</span><span class="sxs-lookup"><span data-stu-id="bfda0-115">Returns E\_OUTOFMEMORY if memory could not be allocated for the format data; S\_OK otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfda0-116">備註</span><span class="sxs-lookup"><span data-stu-id="bfda0-116">Remarks</span></span>

<span data-ttu-id="bfda0-117">如果 *bSetFormat* 參數為 **TRUE**，方法會配置格式區塊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="bfda0-117">If the *bSetFormat* parameter is **TRUE**, the method allocates the memory for the format block.</span></span> <span data-ttu-id="bfda0-118">如果 *pmt* 參數已經包含配置的格式區塊，就會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="bfda0-118">If the *pmt* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="bfda0-119">若要避免記憶體流失，請在呼叫此函式之前呼叫 [**FreeMediaType**](freemediatype.md) 。</span><span class="sxs-lookup"><span data-stu-id="bfda0-119">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span> <span data-ttu-id="bfda0-120">在方法傳回之後，再次呼叫 **FreeMediaType** ，以釋放格式區塊。</span><span class="sxs-lookup"><span data-stu-id="bfda0-120">After the method returns, call **FreeMediaType** again to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfda0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfda0-121">Requirements</span></span>



| <span data-ttu-id="bfda0-122">需求</span><span class="sxs-lookup"><span data-stu-id="bfda0-122">Requirement</span></span> | <span data-ttu-id="bfda0-123">值</span><span class="sxs-lookup"><span data-stu-id="bfda0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfda0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bfda0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bfda0-125"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bfda0-125"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="bfda0-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="bfda0-126">Library</span></span><br/> | <dl> <span data-ttu-id="bfda0-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bfda0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfda0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfda0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfda0-129">**媒體類型函式**</span><span class="sxs-lookup"><span data-stu-id="bfda0-129">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

