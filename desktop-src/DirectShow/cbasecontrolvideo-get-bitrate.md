---
description: Get \_ 位元速率方法會抓取影片的近似位元速率。
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: 'CBaseControlVideo.get_BitRate 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976050"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a><span data-ttu-id="a41c6-103">CBaseControlVideo。取得 \_ 位元速率方法</span><span class="sxs-lookup"><span data-stu-id="a41c6-103">CBaseControlVideo.get\_BitRate method</span></span>

<span data-ttu-id="a41c6-104">方法會抓取 `get_BitRate` 影片的近似位速度。</span><span class="sxs-lookup"><span data-stu-id="a41c6-104">The `get_BitRate` method retrieves an approximate bit rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="a41c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="a41c6-105">Syntax</span></span>


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a><span data-ttu-id="a41c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="a41c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a41c6-107">*pBitRate*</span><span class="sxs-lookup"><span data-stu-id="a41c6-107">*pBitRate*</span></span> 
</dt> <dd>

<span data-ttu-id="a41c6-108">位元速率的指標，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="a41c6-108">Pointer to the bit rate, in bits per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a41c6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a41c6-109">Return value</span></span>

<span data-ttu-id="a41c6-110">如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的記憶體可用，則傳回 E OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a41c6-110">Returns NOERROR if successful or E\_OUTOFMEMORY if not enough memory is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="a41c6-111">備註</span><span class="sxs-lookup"><span data-stu-id="a41c6-111">Remarks</span></span>

<span data-ttu-id="a41c6-112">此成員函式會實 [**IBasicVideo：： get \_ 位元速率**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="a41c6-112">This member function implements the [**IBasicVideo::get\_BitRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) method.</span></span> <span data-ttu-id="a41c6-113">它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) ，以從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="a41c6-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="a41c6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a41c6-114">Requirements</span></span>



| <span data-ttu-id="a41c6-115">需求</span><span class="sxs-lookup"><span data-stu-id="a41c6-115">Requirement</span></span> | <span data-ttu-id="a41c6-116">值</span><span class="sxs-lookup"><span data-stu-id="a41c6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a41c6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a41c6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a41c6-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a41c6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a41c6-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a41c6-119">Library</span></span><br/> | <dl> <span data-ttu-id="a41c6-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a41c6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a41c6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a41c6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41c6-122">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="a41c6-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




