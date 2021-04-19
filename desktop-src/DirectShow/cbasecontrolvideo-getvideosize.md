---
description: GetVideoSize 方法會抓取原生影片的寬度和高度。
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: 'CBaseControlVideo. GetVideoSize 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990793"
---
# <a name="cbasecontrolvideogetvideosize-method"></a><span data-ttu-id="867f5-103">CBaseControlVideo. GetVideoSize 方法</span><span class="sxs-lookup"><span data-stu-id="867f5-103">CBaseControlVideo.GetVideoSize method</span></span>

<span data-ttu-id="867f5-104">方法會抓取 `GetVideoSize` 原生影片的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="867f5-104">The `GetVideoSize` method retrieves the native video's width and height.</span></span>

## <a name="syntax"></a><span data-ttu-id="867f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="867f5-105">Syntax</span></span>


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="867f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="867f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="867f5-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="867f5-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="867f5-108">影片寬度的指標。</span><span class="sxs-lookup"><span data-stu-id="867f5-108">Pointer to the video width.</span></span>

</dd> <dt>

<span data-ttu-id="867f5-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="867f5-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="867f5-110">影片高度的指標。</span><span class="sxs-lookup"><span data-stu-id="867f5-110">Pointer to the video height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="867f5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="867f5-111">Return value</span></span>

<span data-ttu-id="867f5-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="867f5-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="867f5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="867f5-113">Requirements</span></span>



| <span data-ttu-id="867f5-114">需求</span><span class="sxs-lookup"><span data-stu-id="867f5-114">Requirement</span></span> | <span data-ttu-id="867f5-115">值</span><span class="sxs-lookup"><span data-stu-id="867f5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="867f5-116">標頭</span><span class="sxs-lookup"><span data-stu-id="867f5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="867f5-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="867f5-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="867f5-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="867f5-118">Library</span></span><br/> | <dl> <span data-ttu-id="867f5-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="867f5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="867f5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="867f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="867f5-121">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="867f5-121">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




