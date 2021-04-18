---
description: GetDisplayFormat 方法會抓取描述目前顯示模式的影片格式。
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: 'CImageDisplay. GetDisplayFormat 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976192"
---
# <a name="cimagedisplaygetdisplayformat-method"></a><span data-ttu-id="55e42-103">CImageDisplay. GetDisplayFormat 方法</span><span class="sxs-lookup"><span data-stu-id="55e42-103">CImageDisplay.GetDisplayFormat method</span></span>

<span data-ttu-id="55e42-104">`GetDisplayFormat`方法會抓取描述目前顯示模式的影片格式。</span><span class="sxs-lookup"><span data-stu-id="55e42-104">The `GetDisplayFormat` method retrieves a video format that describes the current display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e42-105">語法</span><span class="sxs-lookup"><span data-stu-id="55e42-105">Syntax</span></span>


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a><span data-ttu-id="55e42-106">參數</span><span class="sxs-lookup"><span data-stu-id="55e42-106">Parameters</span></span>

<span data-ttu-id="55e42-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="55e42-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55e42-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="55e42-108">Return value</span></span>

<span data-ttu-id="55e42-109">傳回 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="55e42-109">Returns a pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e42-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="55e42-110">Requirements</span></span>



| <span data-ttu-id="55e42-111">需求</span><span class="sxs-lookup"><span data-stu-id="55e42-111">Requirement</span></span> | <span data-ttu-id="55e42-112">值</span><span class="sxs-lookup"><span data-stu-id="55e42-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e42-113">標頭</span><span class="sxs-lookup"><span data-stu-id="55e42-113">Header</span></span><br/>  | <dl> <span data-ttu-id="55e42-114"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="55e42-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55e42-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="55e42-115">Library</span></span><br/> | <dl> <span data-ttu-id="55e42-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="55e42-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e42-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55e42-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e42-118">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="55e42-118">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




