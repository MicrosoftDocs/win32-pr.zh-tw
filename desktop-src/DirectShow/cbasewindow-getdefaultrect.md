---
description: GetDefaultRect 方法會抓取工作區的預設大小。
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: 'CBaseWindow. GetDefaultRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977708"
---
# <a name="cbasewindowgetdefaultrect-method"></a><span data-ttu-id="ff951-103">CBaseWindow. GetDefaultRect 方法</span><span class="sxs-lookup"><span data-stu-id="ff951-103">CBaseWindow.GetDefaultRect method</span></span>

<span data-ttu-id="ff951-104">方法會抓取 `GetDefaultRect` 工作區的預設大小。</span><span class="sxs-lookup"><span data-stu-id="ff951-104">The `GetDefaultRect` method retrieves the default size of the client area.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff951-105">語法</span><span class="sxs-lookup"><span data-stu-id="ff951-105">Syntax</span></span>


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a><span data-ttu-id="ff951-106">參數</span><span class="sxs-lookup"><span data-stu-id="ff951-106">Parameters</span></span>

<span data-ttu-id="ff951-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ff951-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff951-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff951-108">Return value</span></span>

<span data-ttu-id="ff951-109">傳回預設的矩形。</span><span class="sxs-lookup"><span data-stu-id="ff951-109">Returns the default rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff951-110">備註</span><span class="sxs-lookup"><span data-stu-id="ff951-110">Remarks</span></span>

<span data-ttu-id="ff951-111">當視窗啟動時，物件會呼叫這個方法來判斷視窗的工作區應該要有多大。</span><span class="sxs-lookup"><span data-stu-id="ff951-111">When the window is activated, the object calls this method to determine how large it should make the window's client area.</span></span> <span data-ttu-id="ff951-112">在基類中，此方法會傳回其高度和寬度是定義的常數 DEFHEIGHT 和 DEFWIDTH 的矩形。</span><span class="sxs-lookup"><span data-stu-id="ff951-112">In the base class, this method returns a rectangle whose height and width are the defined constants DEFHEIGHT and DEFWIDTH.</span></span> <span data-ttu-id="ff951-113">衍生類別應該覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ff951-113">A derived class should override this method.</span></span> <span data-ttu-id="ff951-114">若為影片轉譯器，衍生類別通常會傳回原生影片影像的大小。</span><span class="sxs-lookup"><span data-stu-id="ff951-114">For a video renderer, the derived class will typically return the size of the native video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff951-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff951-115">Requirements</span></span>



| <span data-ttu-id="ff951-116">需求</span><span class="sxs-lookup"><span data-stu-id="ff951-116">Requirement</span></span> | <span data-ttu-id="ff951-117">值</span><span class="sxs-lookup"><span data-stu-id="ff951-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff951-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ff951-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ff951-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ff951-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff951-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff951-120">Library</span></span><br/> | <dl> <span data-ttu-id="ff951-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ff951-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff951-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff951-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff951-123">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="ff951-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




