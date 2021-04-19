---
description: PerformanceAlignWindow 方法會將視窗位置對齊 DWORD 界限，以獲得最大效能。
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: 'CBaseWindow. PerformanceAlignWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979566"
---
# <a name="cbasewindowperformancealignwindow-method"></a><span data-ttu-id="0f6eb-103">CBaseWindow. PerformanceAlignWindow 方法</span><span class="sxs-lookup"><span data-stu-id="0f6eb-103">CBaseWindow.PerformanceAlignWindow method</span></span>

<span data-ttu-id="0f6eb-104">方法會將 `PerformanceAlignWindow` 視窗位置對齊 **DWORD** 界限，以獲得最大效能。</span><span class="sxs-lookup"><span data-stu-id="0f6eb-104">The `PerformanceAlignWindow` method aligns the window position to **DWORD** boundaries, for maximum performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f6eb-105">Syntax</span></span>


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a><span data-ttu-id="0f6eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f6eb-106">Parameters</span></span>

<span data-ttu-id="0f6eb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0f6eb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f6eb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f6eb-108">Return value</span></span>

<span data-ttu-id="0f6eb-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0f6eb-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6eb-110">備註</span><span class="sxs-lookup"><span data-stu-id="0f6eb-110">Remarks</span></span>

<span data-ttu-id="0f6eb-111">這個方法會將視窗的左邊和上邊緣對齊 DWORD 界限，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="0f6eb-111">This method aligns the left and top edges of the window to DWORD boundaries, which can improve performance.</span></span> <span data-ttu-id="0f6eb-112">如果視窗有父代，則此方法會傳回 \_ [確定]，但會執行對齊。</span><span class="sxs-lookup"><span data-stu-id="0f6eb-112">If the window has a parent, the method returns S\_OK but does perform the alignment.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6eb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f6eb-113">Requirements</span></span>



| <span data-ttu-id="0f6eb-114">需求</span><span class="sxs-lookup"><span data-stu-id="0f6eb-114">Requirement</span></span> | <span data-ttu-id="0f6eb-115">值</span><span class="sxs-lookup"><span data-stu-id="0f6eb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6eb-116">標頭</span><span class="sxs-lookup"><span data-stu-id="0f6eb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0f6eb-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0f6eb-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f6eb-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f6eb-118">Library</span></span><br/> | <dl> <span data-ttu-id="0f6eb-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0f6eb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6eb-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f6eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6eb-121">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="0f6eb-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




