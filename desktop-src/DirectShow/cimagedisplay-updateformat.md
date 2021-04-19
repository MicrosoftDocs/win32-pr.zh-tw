---
description: UpdateFormat 方法會填入 VIDEOINFO 結構的一些選擇性成員。
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: 'CImageDisplay. UpdateFormat 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977726"
---
# <a name="cimagedisplayupdateformat-method"></a><span data-ttu-id="ed91b-103">CImageDisplay. UpdateFormat 方法</span><span class="sxs-lookup"><span data-stu-id="ed91b-103">CImageDisplay.UpdateFormat method</span></span>

<span data-ttu-id="ed91b-104">`UpdateFormat`方法會填入 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構的一些選擇性成員。</span><span class="sxs-lookup"><span data-stu-id="ed91b-104">The `UpdateFormat` method fills in some optional members of the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed91b-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed91b-105">Syntax</span></span>


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ed91b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed91b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed91b-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="ed91b-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ed91b-108">**VIDEOINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ed91b-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed91b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed91b-109">Return value</span></span>

<span data-ttu-id="ed91b-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ed91b-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed91b-111">備註</span><span class="sxs-lookup"><span data-stu-id="ed91b-111">Remarks</span></span>

<span data-ttu-id="ed91b-112">這個方法會將 **biClrUsed**、 **biClrImportant** 和 **biSizeImage** 成員設定為正確的值，並清除來源和目標矩形。</span><span class="sxs-lookup"><span data-stu-id="ed91b-112">This method sets the **biClrUsed**, **biClrImportant**, and **biSizeImage** members to the correct values, and clears the source and target rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed91b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed91b-113">Requirements</span></span>



| <span data-ttu-id="ed91b-114">需求</span><span class="sxs-lookup"><span data-stu-id="ed91b-114">Requirement</span></span> | <span data-ttu-id="ed91b-115">值</span><span class="sxs-lookup"><span data-stu-id="ed91b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed91b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ed91b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ed91b-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ed91b-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed91b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed91b-118">Library</span></span><br/> | <dl> <span data-ttu-id="ed91b-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ed91b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed91b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed91b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed91b-121">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="ed91b-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




