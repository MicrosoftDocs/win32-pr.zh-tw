---
description: Get \_ AvgSyncOffset 方法會以毫秒為單位，抓取每個畫面格的到期時間，以及自從串流開始之後，針對所有框架實際呈現的時間。
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: 'CBaseVideoRenderer.get_AvgSyncOffset 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000730"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a><span data-ttu-id="b34b2-103">CBaseVideoRenderer. 取得 \_ AvgSyncOffset 方法</span><span class="sxs-lookup"><span data-stu-id="b34b2-103">CBaseVideoRenderer.get\_AvgSyncOffset method</span></span>

<span data-ttu-id="b34b2-104">`get_AvgSyncOffset`方法會以毫秒為單位，抓取每個框架的到期時間，以及自從串流開始之後，針對所有框架實際轉譯的時間。</span><span class="sxs-lookup"><span data-stu-id="b34b2-104">The `get_AvgSyncOffset` method retrieves the average of the time in milliseconds between when each frame was due and when it was actually rendered for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34b2-105">語法</span><span class="sxs-lookup"><span data-stu-id="b34b2-105">Syntax</span></span>


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a><span data-ttu-id="b34b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="b34b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34b2-107">*piAvg*</span><span class="sxs-lookup"><span data-stu-id="b34b2-107">*piAvg*</span></span> 
</dt> <dd>

<span data-ttu-id="b34b2-108">先前所述的平均時間指標。</span><span class="sxs-lookup"><span data-stu-id="b34b2-108">Pointer to the average of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34b2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b34b2-109">Return value</span></span>

<span data-ttu-id="b34b2-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b34b2-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b34b2-111">備註</span><span class="sxs-lookup"><span data-stu-id="b34b2-111">Remarks</span></span>

<span data-ttu-id="b34b2-112">此成員函式會實 [**IQualProp：： get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) 方法。</span><span class="sxs-lookup"><span data-stu-id="b34b2-112">This member function implements the [**IQualProp::get\_AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34b2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b34b2-113">Requirements</span></span>



| <span data-ttu-id="b34b2-114">需求</span><span class="sxs-lookup"><span data-stu-id="b34b2-114">Requirement</span></span> | <span data-ttu-id="b34b2-115">值</span><span class="sxs-lookup"><span data-stu-id="b34b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34b2-116">標頭</span><span class="sxs-lookup"><span data-stu-id="b34b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b34b2-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b34b2-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b34b2-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="b34b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="b34b2-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b34b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b34b2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b34b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34b2-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="b34b2-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




