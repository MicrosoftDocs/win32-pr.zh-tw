---
description: 取得邊框 \_ 型方法會抓取目前的框線色彩。
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: 'CBaseControlWindow.get_BorderColor 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994599"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a><span data-ttu-id="7dc60-103">CBaseControlWindow. 取得 \_ 邊框方法</span><span class="sxs-lookup"><span data-stu-id="7dc60-103">CBaseControlWindow.get\_BorderColor method</span></span>

<span data-ttu-id="7dc60-104">方法會抓取 `get_BorderColor` 目前的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="7dc60-104">The `get_BorderColor` method retrieves the current border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc60-105">語法</span><span class="sxs-lookup"><span data-stu-id="7dc60-105">Syntax</span></span>


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a><span data-ttu-id="7dc60-106">參數</span><span class="sxs-lookup"><span data-stu-id="7dc60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc60-107">*色彩*</span><span class="sxs-lookup"><span data-stu-id="7dc60-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc60-108">目前框線色彩的指標。</span><span class="sxs-lookup"><span data-stu-id="7dc60-108">Pointer to the current border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc60-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dc60-109">Return value</span></span>

<span data-ttu-id="7dc60-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7dc60-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc60-111">備註</span><span class="sxs-lookup"><span data-stu-id="7dc60-111">Remarks</span></span>

<span data-ttu-id="7dc60-112">應用程式可以設定應該顯示影片的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="7dc60-112">An application can set a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="7dc60-113">這個矩形相對於視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="7dc60-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="7dc60-114">如果這樣做 (預設為一律繪製整個視窗) ，則會在影片周圍加上框線。</span><span class="sxs-lookup"><span data-stu-id="7dc60-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="7dc60-115">這個屬性會影響框線所使用的色彩。</span><span class="sxs-lookup"><span data-stu-id="7dc60-115">This property affects the color used by the border.</span></span> <span data-ttu-id="7dc60-116">雖然參數指定為 **LONG** 類型，但其實是 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="7dc60-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

<span data-ttu-id="7dc60-117">此成員函式的目的是要透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面呼叫外部物件，因此會鎖定重要區段以與相關聯的篩選進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="7dc60-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="7dc60-118">呼叫 [**CBaseControlWindow：： GetBorderColour**](cbasecontrolwindow-getbordercolour.md) 成員函式，以取得此屬性（如果不是從外部物件呼叫）。</span><span class="sxs-lookup"><span data-stu-id="7dc60-118">Call the [**CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc60-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dc60-119">Requirements</span></span>



| <span data-ttu-id="7dc60-120">需求</span><span class="sxs-lookup"><span data-stu-id="7dc60-120">Requirement</span></span> | <span data-ttu-id="7dc60-121">值</span><span class="sxs-lookup"><span data-stu-id="7dc60-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc60-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7dc60-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7dc60-123"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7dc60-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7dc60-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="7dc60-124">Library</span></span><br/> | <dl> <span data-ttu-id="7dc60-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7dc60-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc60-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dc60-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc60-127">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="7dc60-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




