---
description: DoSetWindowStyle 方法會變更典型或延伸的視窗樣式。
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: 'CBaseControlWindow. DoSetWindowStyle 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989713"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="8b2e3-103">CBaseControlWindow. DoSetWindowStyle 方法</span><span class="sxs-lookup"><span data-stu-id="8b2e3-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="8b2e3-104">`DoSetWindowStyle`方法會變更典型或延伸的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b2e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="8b2e3-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="8b2e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="8b2e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2e3-107">*Style*</span><span class="sxs-lookup"><span data-stu-id="8b2e3-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2e3-108">適當的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="8b2e3-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="8b2e3-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="8b2e3-110">值，指定要設定的樣式。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-110">Value specifying which styles to set.</span></span> <span data-ttu-id="8b2e3-111">必須是下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="8b2e3-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="8b2e3-112">GWL \_ 樣式</span><span class="sxs-lookup"><span data-stu-id="8b2e3-112">GWL\_STYLE</span></span>   | <span data-ttu-id="8b2e3-113">取出視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="8b2e3-114">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="8b2e3-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="8b2e3-115">取出擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2e3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b2e3-116">Return value</span></span>

<span data-ttu-id="8b2e3-117">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b2e3-118">備註</span><span class="sxs-lookup"><span data-stu-id="8b2e3-118">Remarks</span></span>

<span data-ttu-id="8b2e3-119">這個成員函式會呼叫 Win32 **SetWindowLong** 函式來設定視窗樣式，然後在目前的位置重新配置視窗。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-119">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="8b2e3-120">這個成員函式是由 [**CBaseControlWindow：:p 的 \_ System.windows.window.windowstyle**](cbasecontrolwindow-put-windowstyle.md) 和 [**CBaseControlWindow：:p 的工作 \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) 成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="8b2e3-120">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b2e3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b2e3-121">Requirements</span></span>



| <span data-ttu-id="8b2e3-122">需求</span><span class="sxs-lookup"><span data-stu-id="8b2e3-122">Requirement</span></span> | <span data-ttu-id="8b2e3-123">值</span><span class="sxs-lookup"><span data-stu-id="8b2e3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2e3-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8b2e3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8b2e3-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8b2e3-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b2e3-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8b2e3-126">Library</span></span><br/> | <dl> <span data-ttu-id="8b2e3-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8b2e3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b2e3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b2e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b2e3-129">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="8b2e3-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




