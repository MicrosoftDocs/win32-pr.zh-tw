---
description: Put \_ WindowStyleEx 方法會設定擴充的視窗樣式。
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: 'CBaseControlWindow.put_WindowStyleEx 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991244"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a><span data-ttu-id="ede47-103">CBaseControlWindow. put \_ WindowStyleEx 方法</span><span class="sxs-lookup"><span data-stu-id="ede47-103">CBaseControlWindow.put\_WindowStyleEx method</span></span>

<span data-ttu-id="ede47-104">`put_WindowStyleEx`方法會設定擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="ede47-104">The `put_WindowStyleEx` method sets the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede47-105">語法</span><span class="sxs-lookup"><span data-stu-id="ede47-105">Syntax</span></span>


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="ede47-106">參數</span><span class="sxs-lookup"><span data-stu-id="ede47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede47-107">*WindowStyleEx* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ede47-107">*WindowStyleEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede47-108">值，指定控制項視窗的樣式。</span><span class="sxs-lookup"><span data-stu-id="ede47-108">Value that specifies the style of the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede47-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ede47-109">Return value</span></span>

<span data-ttu-id="ede47-110">傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。</span><span class="sxs-lookup"><span data-stu-id="ede47-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede47-111">備註</span><span class="sxs-lookup"><span data-stu-id="ede47-111">Remarks</span></span>

<span data-ttu-id="ede47-112">這個方法會使用擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="ede47-112">This method uses extended window styles.</span></span> <span data-ttu-id="ede47-113">如需延伸視窗樣式的完整清單，請參閱 Microsoft Win32 **CreateWindowEx** 函數。</span><span class="sxs-lookup"><span data-stu-id="ede47-113">For a complete list of extended window styles, see the Microsoft Win32 **CreateWindowEx** function.</span></span> <span data-ttu-id="ede47-114">若要變更視窗樣式，請取出目前的視窗樣式，然後加入或移除必要的位欄位。</span><span class="sxs-lookup"><span data-stu-id="ede47-114">To change the window style, retrieve the current window style, and then add or remove the necessary bit fields.</span></span>

<span data-ttu-id="ede47-115">請勿使用下列視窗樣式，因為它們不會經過驗證。</span><span class="sxs-lookup"><span data-stu-id="ede47-115">Do not use the following window styles because they are not validated.</span></span>

-   <span data-ttu-id="ede47-116">WS \_ 已停用</span><span class="sxs-lookup"><span data-stu-id="ede47-116">WS\_DISABLED</span></span>
-   <span data-ttu-id="ede47-117">WS \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="ede47-117">WS\_HSCROLL</span></span>
-   <span data-ttu-id="ede47-118">WS \_ ICONIC</span><span class="sxs-lookup"><span data-stu-id="ede47-118">WS\_ICONIC</span></span>
-   <span data-ttu-id="ede47-119">WS \_ 最大化</span><span class="sxs-lookup"><span data-stu-id="ede47-119">WS\_MAXIMIZE</span></span>
-   <span data-ttu-id="ede47-120">WS \_ 最小化</span><span class="sxs-lookup"><span data-stu-id="ede47-120">WS\_MINIMIZE</span></span>
-   <span data-ttu-id="ede47-121">WS \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="ede47-121">WS\_VSCROLL</span></span>

<span data-ttu-id="ede47-122">有一些例外狀況 (記下) ，可接受的旗標與 Win32 **CreateWindow** 函數所允許的旗標相同。</span><span class="sxs-lookup"><span data-stu-id="ede47-122">With some exceptions (noted here), the acceptable flags are the same as those allowed by the Win32 **CreateWindow** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ede47-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ede47-123">Requirements</span></span>



| <span data-ttu-id="ede47-124">需求</span><span class="sxs-lookup"><span data-stu-id="ede47-124">Requirement</span></span> | <span data-ttu-id="ede47-125">值</span><span class="sxs-lookup"><span data-stu-id="ede47-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ede47-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ede47-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ede47-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ede47-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ede47-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="ede47-128">Library</span></span><br/> | <dl> <span data-ttu-id="ede47-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ede47-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede47-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ede47-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede47-131">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="ede47-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




