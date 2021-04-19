---
description: Get \_ VideoHeight 方法會抓取原生影片的高度。
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: 'CBaseControlVideo.get_VideoHeight 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993494"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a><span data-ttu-id="cf798-103">CBaseControlVideo. 取得 \_ VideoHeight 方法</span><span class="sxs-lookup"><span data-stu-id="cf798-103">CBaseControlVideo.get\_VideoHeight method</span></span>

<span data-ttu-id="cf798-104">方法會抓取 `get_VideoHeight` 原生影片的高度。</span><span class="sxs-lookup"><span data-stu-id="cf798-104">The `get_VideoHeight` method retrieves the height of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf798-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf798-105">Syntax</span></span>


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a><span data-ttu-id="cf798-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf798-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf798-107">*pVideoHeight*</span><span class="sxs-lookup"><span data-stu-id="cf798-107">*pVideoHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="cf798-108">原生影片高度的指標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf798-108">Pointer to the height of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf798-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf798-109">Return value</span></span>

<span data-ttu-id="cf798-110">如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的可用記憶體，則傳回 E OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="cf798-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf798-111">備註</span><span class="sxs-lookup"><span data-stu-id="cf798-111">Remarks</span></span>

<span data-ttu-id="cf798-112">此成員函式會實 [**IBasicVideo：： get \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) 方法。</span><span class="sxs-lookup"><span data-stu-id="cf798-112">This member function implements the [**IBasicVideo::get\_VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) method.</span></span> <span data-ttu-id="cf798-113">它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) ，以從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="cf798-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf798-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf798-114">Requirements</span></span>



| <span data-ttu-id="cf798-115">需求</span><span class="sxs-lookup"><span data-stu-id="cf798-115">Requirement</span></span> | <span data-ttu-id="cf798-116">值</span><span class="sxs-lookup"><span data-stu-id="cf798-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf798-117">標頭</span><span class="sxs-lookup"><span data-stu-id="cf798-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cf798-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cf798-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cf798-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf798-119">Library</span></span><br/> | <dl> <span data-ttu-id="cf798-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cf798-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf798-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf798-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf798-122">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="cf798-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




