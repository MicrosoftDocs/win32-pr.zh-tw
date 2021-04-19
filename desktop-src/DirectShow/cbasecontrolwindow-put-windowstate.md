---
description: Put \_ system.windows.window.windowstate 方法會設定視窗狀態。
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: 'CBaseControlWindow.put_WindowState 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984757"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a><span data-ttu-id="120d6-103">CBaseControlWindow. put \_ system.windows.window.windowstate 方法</span><span class="sxs-lookup"><span data-stu-id="120d6-103">CBaseControlWindow.put\_WindowState method</span></span>

<span data-ttu-id="120d6-104">`put_WindowState`方法會設定視窗狀態。</span><span class="sxs-lookup"><span data-stu-id="120d6-104">The `put_WindowState` method sets the window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="120d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="120d6-105">Syntax</span></span>


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a><span data-ttu-id="120d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="120d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120d6-107">*System.windows.window.windowstate*</span><span class="sxs-lookup"><span data-stu-id="120d6-107">*WindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="120d6-108">新的視窗狀態。</span><span class="sxs-lookup"><span data-stu-id="120d6-108">New window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="120d6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="120d6-109">Return value</span></span>

<span data-ttu-id="120d6-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="120d6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="120d6-111">備註</span><span class="sxs-lookup"><span data-stu-id="120d6-111">Remarks</span></span>

<span data-ttu-id="120d6-112">此成員函式會採用與 Microsoft Win32 **ShowWindow** 函式相同的參數 (例如，ws \_ SHOWNORMAL、WS \_ SHOWMINNOACTI加值稅E 和 ws \_ SHOWMAXIMIZED) 。</span><span class="sxs-lookup"><span data-stu-id="120d6-112">This member function takes the same parameters as the Microsoft Win32 **ShowWindow** function (for example, WS\_SHOWNORMAL, WS\_SHOWMINNOACTIVATE, and WS\_SHOWMAXIMIZED).</span></span>

## <a name="requirements"></a><span data-ttu-id="120d6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="120d6-113">Requirements</span></span>



| <span data-ttu-id="120d6-114">需求</span><span class="sxs-lookup"><span data-stu-id="120d6-114">Requirement</span></span> | <span data-ttu-id="120d6-115">值</span><span class="sxs-lookup"><span data-stu-id="120d6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="120d6-116">標頭</span><span class="sxs-lookup"><span data-stu-id="120d6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="120d6-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="120d6-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="120d6-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="120d6-118">Library</span></span><br/> | <dl> <span data-ttu-id="120d6-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="120d6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120d6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="120d6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120d6-121">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="120d6-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




