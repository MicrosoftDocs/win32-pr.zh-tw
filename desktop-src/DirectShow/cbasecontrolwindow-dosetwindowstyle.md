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
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909806"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="b9736-103">CBaseControlWindow. DoSetWindowStyle 方法</span><span class="sxs-lookup"><span data-stu-id="b9736-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="b9736-104">`DoSetWindowStyle`方法會變更典型或延伸的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="b9736-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9736-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9736-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="b9736-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9736-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9736-107">*Style*</span><span class="sxs-lookup"><span data-stu-id="b9736-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="b9736-108">適當的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="b9736-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="b9736-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="b9736-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="b9736-110">值，指定要設定的樣式。</span><span class="sxs-lookup"><span data-stu-id="b9736-110">Value specifying which styles to set.</span></span> <span data-ttu-id="b9736-111">必須是下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="b9736-111">Must be one of the following:</span></span>



| <span data-ttu-id="b9736-112">標籤</span><span class="sxs-lookup"><span data-stu-id="b9736-112">Label</span></span> | <span data-ttu-id="b9736-113">值</span><span class="sxs-lookup"><span data-stu-id="b9736-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="b9736-114">GWL \_ 樣式</span><span class="sxs-lookup"><span data-stu-id="b9736-114">GWL\_STYLE</span></span>   | <span data-ttu-id="b9736-115">取出視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="b9736-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="b9736-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="b9736-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="b9736-117">取出擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="b9736-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9736-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9736-118">Return value</span></span>

<span data-ttu-id="b9736-119">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b9736-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9736-120">備註</span><span class="sxs-lookup"><span data-stu-id="b9736-120">Remarks</span></span>

<span data-ttu-id="b9736-121">這個成員函式會呼叫 Win32 **SetWindowLong** 函式來設定視窗樣式，然後在目前的位置重新配置視窗。</span><span class="sxs-lookup"><span data-stu-id="b9736-121">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="b9736-122">這個成員函式是由 [**CBaseControlWindow：:p 的 \_ System.windows.window.windowstyle**](cbasecontrolwindow-put-windowstyle.md) 和 [**CBaseControlWindow：:p 的工作 \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) 成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="b9736-122">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9736-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9736-123">Requirements</span></span>



| <span data-ttu-id="b9736-124">需求</span><span class="sxs-lookup"><span data-stu-id="b9736-124">Requirement</span></span> | <span data-ttu-id="b9736-125">值</span><span class="sxs-lookup"><span data-stu-id="b9736-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9736-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b9736-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b9736-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b9736-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9736-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9736-128">Library</span></span><br/> | <dl> <span data-ttu-id="b9736-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b9736-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9736-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9736-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9736-131">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="b9736-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




