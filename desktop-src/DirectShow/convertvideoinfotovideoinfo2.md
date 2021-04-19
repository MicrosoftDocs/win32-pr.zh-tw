---
description: ConvertVideoInfoToVideoInfo2 函式會將使用 VIDEOINFOHEADER 的媒體類型轉換成一個使用 VIDEOINFOHEADER2 的媒體類型。
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: 'ConvertVideoInfoToVideoInfo2 函式 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976538"
---
# <a name="convertvideoinfotovideoinfo2-function"></a><span data-ttu-id="fc5fa-103">ConvertVideoInfoToVideoInfo2 函式</span><span class="sxs-lookup"><span data-stu-id="fc5fa-103">ConvertVideoInfoToVideoInfo2 function</span></span>

<span data-ttu-id="fc5fa-104">`ConvertVideoInfoToVideoInfo2`函數會將使用 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)的媒體類型轉換成使用 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="fc5fa-104">The `ConvertVideoInfoToVideoInfo2` function converts a media type that uses [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) to one that uses [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc5fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc5fa-105">Syntax</span></span>


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="fc5fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc5fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc5fa-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="fc5fa-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="fc5fa-108">要轉換的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fc5fa-108">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to convert.</span></span> <span data-ttu-id="fc5fa-109">結構的格式類型必須是 \_ VideoInfo。</span><span class="sxs-lookup"><span data-stu-id="fc5fa-109">The structure must have format type FORMAT\_VideoInfo.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc5fa-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc5fa-110">Return value</span></span>

<span data-ttu-id="fc5fa-111">傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。</span><span class="sxs-lookup"><span data-stu-id="fc5fa-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc5fa-112">備註</span><span class="sxs-lookup"><span data-stu-id="fc5fa-112">Remarks</span></span>

<span data-ttu-id="fc5fa-113">此函式會配置新的 **VIDEOINFOHEADER2** 結構、將 **VIDEOINFOHEADER** 結構的成員複製到其中，然後以媒體類型的格式區塊中的新結構取代舊的結構。</span><span class="sxs-lookup"><span data-stu-id="fc5fa-113">This function allocates a new **VIDEOINFOHEADER2** structure, copies the members of the **VIDEOINFOHEADER** structure into it, and replaces the old structure with the new structure in the format block of the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5fa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc5fa-114">Requirements</span></span>



| <span data-ttu-id="fc5fa-115">需求</span><span class="sxs-lookup"><span data-stu-id="fc5fa-115">Requirement</span></span> | <span data-ttu-id="fc5fa-116">值</span><span class="sxs-lookup"><span data-stu-id="fc5fa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5fa-117">標頭</span><span class="sxs-lookup"><span data-stu-id="fc5fa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fc5fa-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fc5fa-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc5fa-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc5fa-119">Library</span></span><br/> | <dl> <span data-ttu-id="fc5fa-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fc5fa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc5fa-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc5fa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5fa-122">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="fc5fa-122">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




