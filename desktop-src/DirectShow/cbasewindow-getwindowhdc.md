---
description: GetWindowHDC 方法會 (DC) 抓取視窗的裝置內容控制碼。
ms.assetid: 35ee2a66-ee56-44dc-ad59-fd467bb4aa63
title: 'CBaseWindow. GetWindowHDC 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetWindowHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16c2502b3a9de587e91ff43ddc45a84ae08492db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989601"
---
# <a name="cbasewindowgetwindowhdc-method"></a><span data-ttu-id="10d84-103">CBaseWindow. GetWindowHDC 方法</span><span class="sxs-lookup"><span data-stu-id="10d84-103">CBaseWindow.GetWindowHDC method</span></span>

<span data-ttu-id="10d84-104">`GetWindowHDC`方法會 (DC) 抓取視窗的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d84-104">The `GetWindowHDC` method retrieves a handle to the window's device context (DC).</span></span>

## <a name="syntax"></a><span data-ttu-id="10d84-105">語法</span><span class="sxs-lookup"><span data-stu-id="10d84-105">Syntax</span></span>


```C++
HDC GetWindowHDC();
```



## <a name="parameters"></a><span data-ttu-id="10d84-106">參數</span><span class="sxs-lookup"><span data-stu-id="10d84-106">Parameters</span></span>

<span data-ttu-id="10d84-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="10d84-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10d84-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="10d84-108">Return value</span></span>

<span data-ttu-id="10d84-109">傳回 DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d84-109">Returns a handle to the DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d84-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="10d84-110">Requirements</span></span>



| <span data-ttu-id="10d84-111">需求</span><span class="sxs-lookup"><span data-stu-id="10d84-111">Requirement</span></span> | <span data-ttu-id="10d84-112">值</span><span class="sxs-lookup"><span data-stu-id="10d84-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d84-113">標頭</span><span class="sxs-lookup"><span data-stu-id="10d84-113">Header</span></span><br/>  | <dl> <span data-ttu-id="10d84-114"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="10d84-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10d84-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="10d84-115">Library</span></span><br/> | <dl> <span data-ttu-id="10d84-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="10d84-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d84-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10d84-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d84-118">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="10d84-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




