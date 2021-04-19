---
description: GetVideoFormat 方法會抓取表示目前影片格式的影片範例。
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: 'CBaseControlVideo. GetVideoFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981394"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a><span data-ttu-id="eab11-103">CBaseControlVideo. GetVideoFormat 方法</span><span class="sxs-lookup"><span data-stu-id="eab11-103">CBaseControlVideo.GetVideoFormat method</span></span>

<span data-ttu-id="eab11-104">`GetVideoFormat`方法會抓取表示目前影片格式的影片範例。</span><span class="sxs-lookup"><span data-stu-id="eab11-104">The `GetVideoFormat` method retrieves a video sample that represents the current video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab11-105">語法</span><span class="sxs-lookup"><span data-stu-id="eab11-105">Syntax</span></span>


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a><span data-ttu-id="eab11-106">參數</span><span class="sxs-lookup"><span data-stu-id="eab11-106">Parameters</span></span>

<span data-ttu-id="eab11-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="eab11-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eab11-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="eab11-108">Return value</span></span>

<span data-ttu-id="eab11-109">傳回 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的指標，其中包含目前的影片格式。</span><span class="sxs-lookup"><span data-stu-id="eab11-109">Returns a pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the current video format.</span></span>

## <a name="remarks"></a><span data-ttu-id="eab11-110">備註</span><span class="sxs-lookup"><span data-stu-id="eab11-110">Remarks</span></span>

<span data-ttu-id="eab11-111">若要透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)傳回和檢查特定資訊，物件必須知道目前的影片格式。</span><span class="sxs-lookup"><span data-stu-id="eab11-111">To return and check certain information through [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), the object must know the current video format.</span></span> <span data-ttu-id="eab11-112">它會藉由呼叫衍生類別必須覆寫的純虛擬方法來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="eab11-112">It gets this information by calling this pure virtual method that derived classes must override.</span></span> <span data-ttu-id="eab11-113">下列 [**CBaseControlVideo**](cbasecontrolvideo.md) 成員函式會呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="eab11-113">This member function is called by the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="eab11-114">**CBaseControlVideo::OnVideoSizeChange**</span><span class="sxs-lookup"><span data-stu-id="eab11-114">**CBaseControlVideo::OnVideoSizeChange**</span></span>](cbasecontrolvideo-onvideosizechange.md)
-   [<span data-ttu-id="eab11-115">**CBaseControlVideo：： get \_ AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="eab11-115">**CBaseControlVideo::get\_AvgTimePerFrame**</span></span>](cbasecontrolvideo-get-avgtimeperframe.md)
-   [<span data-ttu-id="eab11-116">**CBaseControlVideo：：取得 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="eab11-116">**CBaseControlVideo::get\_BitRate**</span></span>](cbasecontrolvideo-get-bitrate.md)
-   [<span data-ttu-id="eab11-117">**CBaseControlVideo：： get \_ BitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="eab11-117">**CBaseControlVideo::get\_BitErrorRate**</span></span>](cbasecontrolvideo-get-biterrorrate.md)
-   [<span data-ttu-id="eab11-118">**CBaseControlVideo：： get \_ VideoWidth**</span><span class="sxs-lookup"><span data-stu-id="eab11-118">**CBaseControlVideo::get\_VideoWidth**</span></span>](cbasecontrolvideo-get-videowidth.md)
-   [<span data-ttu-id="eab11-119">**CBaseControlVideo：： get \_ VideoHeight**</span><span class="sxs-lookup"><span data-stu-id="eab11-119">**CBaseControlVideo::get\_VideoHeight**</span></span>](cbasecontrolvideo-get-videoheight.md)
-   [<span data-ttu-id="eab11-120">**CBaseControlVideo::GetVideoPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="eab11-120">**CBaseControlVideo::GetVideoPaletteEntries**</span></span>](cbasecontrolvideo-getvideopaletteentries.md)
-   [<span data-ttu-id="eab11-121">**CBaseControlVideo::GetVideoSize**</span><span class="sxs-lookup"><span data-stu-id="eab11-121">**CBaseControlVideo::GetVideoSize**</span></span>](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a><span data-ttu-id="eab11-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="eab11-122">Requirements</span></span>



| <span data-ttu-id="eab11-123">需求</span><span class="sxs-lookup"><span data-stu-id="eab11-123">Requirement</span></span> | <span data-ttu-id="eab11-124">值</span><span class="sxs-lookup"><span data-stu-id="eab11-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab11-125">標頭</span><span class="sxs-lookup"><span data-stu-id="eab11-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eab11-126"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eab11-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eab11-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="eab11-127">Library</span></span><br/> | <dl> <span data-ttu-id="eab11-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eab11-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eab11-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eab11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab11-130">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="eab11-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




