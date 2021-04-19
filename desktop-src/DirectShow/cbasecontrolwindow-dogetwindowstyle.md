---
description: DoGetWindowStyle 方法會抓取目前的一般或擴充的視窗樣式。
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: 'CBaseControlWindow. DoGetWindowStyle 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976076"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="1c34e-103">CBaseControlWindow. DoGetWindowStyle 方法</span><span class="sxs-lookup"><span data-stu-id="1c34e-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="1c34e-104">方法會抓取 `DoGetWindowStyle` 目前的一般或擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="1c34e-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c34e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c34e-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="1c34e-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c34e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c34e-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="1c34e-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="1c34e-108">接收樣式資訊之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="1c34e-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="1c34e-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="1c34e-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="1c34e-110">值，指定要取出的樣式。</span><span class="sxs-lookup"><span data-stu-id="1c34e-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="1c34e-111">必須是下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="1c34e-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="1c34e-112">GWL \_ 樣式</span><span class="sxs-lookup"><span data-stu-id="1c34e-112">GWL\_STYLE</span></span>   | <span data-ttu-id="1c34e-113">取出視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="1c34e-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="1c34e-114">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="1c34e-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="1c34e-115">取出擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="1c34e-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c34e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c34e-116">Return value</span></span>

<span data-ttu-id="1c34e-117">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1c34e-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c34e-118">備註</span><span class="sxs-lookup"><span data-stu-id="1c34e-118">Remarks</span></span>

<span data-ttu-id="1c34e-119">此成員函式會呼叫 Win32 **GetWindowLong** 函式，以取得視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="1c34e-119">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="1c34e-120">它是由 [**CBaseControlWindow：： get \_ System.windows.window.windowstyle**](cbasecontrolwindow-get-windowstyle.md) 和 [**CBaseControlWindow：： get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) 成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="1c34e-120">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c34e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c34e-121">Requirements</span></span>



| <span data-ttu-id="1c34e-122">需求</span><span class="sxs-lookup"><span data-stu-id="1c34e-122">Requirement</span></span> | <span data-ttu-id="1c34e-123">值</span><span class="sxs-lookup"><span data-stu-id="1c34e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c34e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1c34e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1c34e-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1c34e-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c34e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c34e-126">Library</span></span><br/> | <dl> <span data-ttu-id="1c34e-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1c34e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c34e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c34e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c34e-129">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="1c34e-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




