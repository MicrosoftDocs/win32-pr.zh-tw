---
description: GetBorderColour 方法會抓取目前的視窗框線色彩 m \_ BorderColour。
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: 'CBaseControlWindow. GetBorderColour 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994340"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a><span data-ttu-id="80d2f-103">CBaseControlWindow. GetBorderColour 方法</span><span class="sxs-lookup"><span data-stu-id="80d2f-103">CBaseControlWindow.GetBorderColour method</span></span>

<span data-ttu-id="80d2f-104">方法會抓取 `GetBorderColour` 目前的視窗框線色彩 **m \_ BorderColour**。</span><span class="sxs-lookup"><span data-stu-id="80d2f-104">The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d2f-105">語法</span><span class="sxs-lookup"><span data-stu-id="80d2f-105">Syntax</span></span>


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a><span data-ttu-id="80d2f-106">參數</span><span class="sxs-lookup"><span data-stu-id="80d2f-106">Parameters</span></span>

<span data-ttu-id="80d2f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="80d2f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80d2f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="80d2f-108">Return value</span></span>

<span data-ttu-id="80d2f-109">傳回框線的色彩。</span><span class="sxs-lookup"><span data-stu-id="80d2f-109">Returns the color of the border.</span></span>

## <a name="remarks"></a><span data-ttu-id="80d2f-110">備註</span><span class="sxs-lookup"><span data-stu-id="80d2f-110">Remarks</span></span>

<span data-ttu-id="80d2f-111">應用程式可以設定目的地矩形來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="80d2f-111">An application can set a destination rectangle to display the video.</span></span> <span data-ttu-id="80d2f-112">這個矩形應該相對於視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="80d2f-112">This rectangle should be relative to the client area for the window.</span></span> <span data-ttu-id="80d2f-113">如果這樣做 (預設為一律繪製整個視窗) ，則會有一個圍繞影片的區域;亦即框線。</span><span class="sxs-lookup"><span data-stu-id="80d2f-113">If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border.</span></span> <span data-ttu-id="80d2f-114">框線色彩可透過 [**CBaseControlWindow：:p 的 ui \_ 邊框**](cbasecontrolwindow-put-bordercolor.md) 型成員函式來設定。</span><span class="sxs-lookup"><span data-stu-id="80d2f-114">The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function.</span></span> <span data-ttu-id="80d2f-115">這個屬性會影響框線的色彩。</span><span class="sxs-lookup"><span data-stu-id="80d2f-115">This property affects the color of the border.</span></span> <span data-ttu-id="80d2f-116">除非您是透過 [**IVideoWindow：： get \_**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) CBaseControlWindow，否則請使用此成員函式，而不是使用 [**：： get \_ 邊框**](cbasecontrolwindow-get-bordercolor.md)式。</span><span class="sxs-lookup"><span data-stu-id="80d2f-116">Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="80d2f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="80d2f-117">Requirements</span></span>



| <span data-ttu-id="80d2f-118">需求</span><span class="sxs-lookup"><span data-stu-id="80d2f-118">Requirement</span></span> | <span data-ttu-id="80d2f-119">值</span><span class="sxs-lookup"><span data-stu-id="80d2f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80d2f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="80d2f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="80d2f-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="80d2f-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80d2f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="80d2f-122">Library</span></span><br/> | <dl> <span data-ttu-id="80d2f-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="80d2f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80d2f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80d2f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d2f-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="80d2f-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




