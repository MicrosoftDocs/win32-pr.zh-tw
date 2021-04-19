---
description: Get \_ system.windows.window.windowstyle 方法會抓取標準的視窗樣式。
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: 'CBaseControlWindow.get_WindowStyle 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987933"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a><span data-ttu-id="10b72-103">CBaseControlWindow. 取得 \_ system.windows.window.windowstyle 方法</span><span class="sxs-lookup"><span data-stu-id="10b72-103">CBaseControlWindow.get\_WindowStyle method</span></span>

<span data-ttu-id="10b72-104">方法會抓取 `get_WindowStyle` 標準的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="10b72-104">The `get_WindowStyle` method retrieves the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b72-105">語法</span><span class="sxs-lookup"><span data-stu-id="10b72-105">Syntax</span></span>


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="10b72-106">參數</span><span class="sxs-lookup"><span data-stu-id="10b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b72-107">*pWindowStyle*</span><span class="sxs-lookup"><span data-stu-id="10b72-107">*pWindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="10b72-108">視窗樣式的指標。</span><span class="sxs-lookup"><span data-stu-id="10b72-108">Pointer to window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b72-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="10b72-109">Return value</span></span>

<span data-ttu-id="10b72-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="10b72-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b72-111">備註</span><span class="sxs-lookup"><span data-stu-id="10b72-111">Remarks</span></span>

<span data-ttu-id="10b72-112">此成員函式會傳回標準視窗樣式，例如 WS \_ CHILD 和 ws \_ 。</span><span class="sxs-lookup"><span data-stu-id="10b72-112">This member function returns the standard window styles, such as WS\_CHILD and WS\_VISIBLE.</span></span> <span data-ttu-id="10b72-113">它會呼叫 [**CBaseControlWindow：:D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="10b72-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b72-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="10b72-114">Requirements</span></span>



| <span data-ttu-id="10b72-115">需求</span><span class="sxs-lookup"><span data-stu-id="10b72-115">Requirement</span></span> | <span data-ttu-id="10b72-116">值</span><span class="sxs-lookup"><span data-stu-id="10b72-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b72-117">標頭</span><span class="sxs-lookup"><span data-stu-id="10b72-117">Header</span></span><br/>  | <dl> <span data-ttu-id="10b72-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="10b72-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10b72-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="10b72-119">Library</span></span><br/> | <dl> <span data-ttu-id="10b72-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="10b72-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b72-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10b72-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b72-122">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="10b72-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




