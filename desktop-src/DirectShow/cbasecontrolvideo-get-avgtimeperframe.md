---
description: Get \_ AvgTimePerFrame 方法會抓取每個畫面格的平均時間。
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: 'CBaseControlVideo.get_AvgTimePerFrame 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989794"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a><span data-ttu-id="50cb3-103">CBaseControlVideo. 取得 \_ AvgTimePerFrame 方法</span><span class="sxs-lookup"><span data-stu-id="50cb3-103">CBaseControlVideo.get\_AvgTimePerFrame method</span></span>

<span data-ttu-id="50cb3-104">方法會抓取 `get_AvgTimePerFrame` 每個框架的平均時間。</span><span class="sxs-lookup"><span data-stu-id="50cb3-104">The `get_AvgTimePerFrame` method retrieves the average time per frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="50cb3-105">語法</span><span class="sxs-lookup"><span data-stu-id="50cb3-105">Syntax</span></span>


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a><span data-ttu-id="50cb3-106">參數</span><span class="sxs-lookup"><span data-stu-id="50cb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50cb3-107">*pAvgTimePerFrame*</span><span class="sxs-lookup"><span data-stu-id="50cb3-107">*pAvgTimePerFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="50cb3-108">每個框架的平均時間指標。</span><span class="sxs-lookup"><span data-stu-id="50cb3-108">Pointer to the average time per frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50cb3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="50cb3-109">Return value</span></span>

<span data-ttu-id="50cb3-110">如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的可用記憶體，則傳回 E OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="50cb3-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="50cb3-111">備註</span><span class="sxs-lookup"><span data-stu-id="50cb3-111">Remarks</span></span>

<span data-ttu-id="50cb3-112">此成員函式會實 [**IBasicVideo：： get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) 方法。</span><span class="sxs-lookup"><span data-stu-id="50cb3-112">This member function implements the [**IBasicVideo::get\_AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) method.</span></span> <span data-ttu-id="50cb3-113">它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) 成員函式，以從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="50cb3-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) member function to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="50cb3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="50cb3-114">Requirements</span></span>



| <span data-ttu-id="50cb3-115">需求</span><span class="sxs-lookup"><span data-stu-id="50cb3-115">Requirement</span></span> | <span data-ttu-id="50cb3-116">值</span><span class="sxs-lookup"><span data-stu-id="50cb3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50cb3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="50cb3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="50cb3-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="50cb3-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50cb3-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="50cb3-119">Library</span></span><br/> | <dl> <span data-ttu-id="50cb3-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="50cb3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50cb3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50cb3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cb3-122">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="50cb3-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




