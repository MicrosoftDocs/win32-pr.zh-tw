---
description: 回呼，會通知主機 assocaited 要求所傳回的圖元歷程記錄交集資訊。
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryCallback2：： IntersectionsCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109064"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span data-ttu-id="53619-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2：： IntersectionsCallback 方法</span><span class="sxs-lookup"><span data-stu-id="53619-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2::IntersectionsCallback method</span></span>

<span data-ttu-id="53619-104">回呼，會通知主機 assocaited 要求所傳回的圖元歷程記錄交集資訊。</span><span class="sxs-lookup"><span data-stu-id="53619-104">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="53619-105">語法</span><span class="sxs-lookup"><span data-stu-id="53619-105">Syntax</span></span>


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a><span data-ttu-id="53619-106">參數</span><span class="sxs-lookup"><span data-stu-id="53619-106">Parameters</span></span>

<span data-ttu-id="53619-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="53619-107">*count* </span></span>  
<span data-ttu-id="53619-108">圖元歷程記錄交集的數目。</span><span class="sxs-lookup"><span data-stu-id="53619-108">The number of pixel history intersections.</span></span>

<span data-ttu-id="53619-109">*count0 \_ 交集* </span><span class="sxs-lookup"><span data-stu-id="53619-109">*count0\_intersections* </span></span>  
<span data-ttu-id="53619-110">圖元歷程記錄交集。</span><span class="sxs-lookup"><span data-stu-id="53619-110">The pixel history intersections.</span></span>

## <a name="return-value"></a><span data-ttu-id="53619-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="53619-111">Return value</span></span>

<span data-ttu-id="53619-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="53619-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53619-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53619-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53619-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="53619-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="53619-115">標頭</span><span class="sxs-lookup"><span data-stu-id="53619-115">Header</span></span></p></td><td><span data-ttu-id="53619-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="53619-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="53619-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="53619-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="53619-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="53619-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
