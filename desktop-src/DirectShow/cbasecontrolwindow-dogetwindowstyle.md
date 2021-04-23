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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909816"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="cd947-103">CBaseControlWindow. DoGetWindowStyle 方法</span><span class="sxs-lookup"><span data-stu-id="cd947-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="cd947-104">方法會抓取 `DoGetWindowStyle` 目前的一般或擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="cd947-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd947-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd947-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="cd947-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd947-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="cd947-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="cd947-108">接收樣式資訊之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="cd947-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="cd947-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="cd947-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="cd947-110">值，指定要取出的樣式。</span><span class="sxs-lookup"><span data-stu-id="cd947-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="cd947-111">必須是下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="cd947-111">Must be one of the following:</span></span>



| <span data-ttu-id="cd947-112">標籤</span><span class="sxs-lookup"><span data-stu-id="cd947-112">Label</span></span> | <span data-ttu-id="cd947-113">值</span><span class="sxs-lookup"><span data-stu-id="cd947-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="cd947-114">GWL \_ 樣式</span><span class="sxs-lookup"><span data-stu-id="cd947-114">GWL\_STYLE</span></span>   | <span data-ttu-id="cd947-115">取出視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="cd947-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="cd947-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="cd947-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="cd947-117">取出擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="cd947-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd947-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd947-118">Return value</span></span>

<span data-ttu-id="cd947-119">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cd947-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd947-120">備註</span><span class="sxs-lookup"><span data-stu-id="cd947-120">Remarks</span></span>

<span data-ttu-id="cd947-121">此成員函式會呼叫 Win32 **GetWindowLong** 函式，以取得視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="cd947-121">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="cd947-122">它是由 [**CBaseControlWindow：： get \_ System.windows.window.windowstyle**](cbasecontrolwindow-get-windowstyle.md) 和 [**CBaseControlWindow：： get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) 成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="cd947-122">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd947-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd947-123">Requirements</span></span>



| <span data-ttu-id="cd947-124">需求</span><span class="sxs-lookup"><span data-stu-id="cd947-124">Requirement</span></span> | <span data-ttu-id="cd947-125">值</span><span class="sxs-lookup"><span data-stu-id="cd947-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd947-126">標頭</span><span class="sxs-lookup"><span data-stu-id="cd947-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cd947-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cd947-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd947-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd947-128">Library</span></span><br/> | <dl> <span data-ttu-id="cd947-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cd947-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd947-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd947-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd947-131">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="cd947-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




