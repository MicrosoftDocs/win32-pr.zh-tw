---
description: Get \_ BitErrorRate 方法會捕獲影片的近似位錯誤率。
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: 'CBaseControlVideo.get_BitErrorRate 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976052"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a><span data-ttu-id="ad6d6-103">CBaseControlVideo. 取得 \_ BitErrorRate 方法</span><span class="sxs-lookup"><span data-stu-id="ad6d6-103">CBaseControlVideo.get\_BitErrorRate method</span></span>

<span data-ttu-id="ad6d6-104">方法會抓取 `get_BitErrorRate` 影片的近似位錯誤率。</span><span class="sxs-lookup"><span data-stu-id="ad6d6-104">The `get_BitErrorRate` method retrieves an approximate bit error rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad6d6-105">Syntax</span></span>


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a><span data-ttu-id="ad6d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad6d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad6d6-107">*pBitErrorRate*</span><span class="sxs-lookup"><span data-stu-id="ad6d6-107">*pBitErrorRate*</span></span> 
</dt> <dd>

<span data-ttu-id="ad6d6-108">位錯誤率的指標 (大約這個多個位) 的一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad6d6-108">Pointer to the bit error rate (one error for approximately this many bits).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad6d6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad6d6-109">Return value</span></span>

<span data-ttu-id="ad6d6-110">如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的可用記憶體，則傳回 E OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ad6d6-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad6d6-111">備註</span><span class="sxs-lookup"><span data-stu-id="ad6d6-111">Remarks</span></span>

<span data-ttu-id="ad6d6-112">此成員函式會實 [**IBasicVideo：： get \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="ad6d6-112">This member function implements the [**IBasicVideo::get\_BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) method.</span></span> <span data-ttu-id="ad6d6-113">它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) 方法，從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="ad6d6-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) method to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6d6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad6d6-114">Requirements</span></span>



| <span data-ttu-id="ad6d6-115">需求</span><span class="sxs-lookup"><span data-stu-id="ad6d6-115">Requirement</span></span> | <span data-ttu-id="ad6d6-116">值</span><span class="sxs-lookup"><span data-stu-id="ad6d6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6d6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ad6d6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ad6d6-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ad6d6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad6d6-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="ad6d6-119">Library</span></span><br/> | <dl> <span data-ttu-id="ad6d6-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ad6d6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6d6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad6d6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6d6-122">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="ad6d6-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




