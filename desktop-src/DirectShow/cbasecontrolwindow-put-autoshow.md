---
description: Put 自動輸入 \_ 方法會設定自動建立狀態旗標。
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: 'CBaseControlWindow.put_AutoShow 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992887"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a><span data-ttu-id="c715c-103">CBaseControlWindow，put 的 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="c715c-103">CBaseControlWindow.put\_AutoShow method</span></span>

<span data-ttu-id="c715c-104">`put_AutoShow`方法會設定自動中的狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="c715c-104">The `put_AutoShow` method sets the AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="c715c-105">語法</span><span class="sxs-lookup"><span data-stu-id="c715c-105">Syntax</span></span>


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="c715c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c715c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c715c-107">*自動*</span><span class="sxs-lookup"><span data-stu-id="c715c-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="c715c-108">自動化布林值旗標 (0 是 off，1是) 。</span><span class="sxs-lookup"><span data-stu-id="c715c-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c715c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c715c-109">Return value</span></span>

<span data-ttu-id="c715c-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c715c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c715c-111">備註</span><span class="sxs-lookup"><span data-stu-id="c715c-111">Remarks</span></span>

<span data-ttu-id="c715c-112">這個屬性可簡化應用程式的視窗顯示存取。</span><span class="sxs-lookup"><span data-stu-id="c715c-112">This property simplifies window display access for applications.</span></span> <span data-ttu-id="c715c-113">如果這是在) 上設定為 1 (，則當篩選暫停或執行時，通常會隱藏的視窗（通常是在連接篩選之後隱藏）。</span><span class="sxs-lookup"><span data-stu-id="c715c-113">If this is set to  1 (on), the window, which is typically hidden after the filter is connected, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="c715c-114">不過，當篩選準則停止時，不應該隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="c715c-114">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="c715c-115">如果此設定為 0 (關閉) ，只有當應用程式呼叫 CBaseControlWindow 時，才會顯示視窗 [**：:p 的 ui \_ 可見**](cbasecontrolwindow-put-visible.md) 或 [**CBaseControlWindow：:p \_**](cbasecontrolwindow-put-windowstate.md) 不適當的參數 system.windows.window.windowstate。</span><span class="sxs-lookup"><span data-stu-id="c715c-115">If this is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c715c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c715c-116">Requirements</span></span>



| <span data-ttu-id="c715c-117">需求</span><span class="sxs-lookup"><span data-stu-id="c715c-117">Requirement</span></span> | <span data-ttu-id="c715c-118">值</span><span class="sxs-lookup"><span data-stu-id="c715c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c715c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c715c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c715c-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c715c-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c715c-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="c715c-121">Library</span></span><br/> | <dl> <span data-ttu-id="c715c-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c715c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c715c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c715c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c715c-124">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="c715c-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




