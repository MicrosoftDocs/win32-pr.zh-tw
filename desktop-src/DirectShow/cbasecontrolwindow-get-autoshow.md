---
description: Get 自動完成方法會抓取 \_ 目前的自動完成狀態旗標。
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: 'CBaseControlWindow.get_AutoShow 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982536"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a><span data-ttu-id="928cb-103">CBaseControlWindow。取得自動完成 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="928cb-103">CBaseControlWindow.get\_AutoShow method</span></span>

<span data-ttu-id="928cb-104">方法會抓取 `get_AutoShow` 目前的自動中狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="928cb-104">The `get_AutoShow` method retrieves the current AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="928cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="928cb-105">Syntax</span></span>


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="928cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="928cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928cb-107">*自動*</span><span class="sxs-lookup"><span data-stu-id="928cb-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="928cb-108">自動化布林值旗標的指標 (0 是 off，1是) 。</span><span class="sxs-lookup"><span data-stu-id="928cb-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928cb-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="928cb-109">Return value</span></span>

<span data-ttu-id="928cb-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="928cb-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="928cb-111">備註</span><span class="sxs-lookup"><span data-stu-id="928cb-111">Remarks</span></span>

<span data-ttu-id="928cb-112">此成員函式會實 [**IVideoWindow：： \_ get**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) 自動完成方法。</span><span class="sxs-lookup"><span data-stu-id="928cb-112">This member function implements the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span> <span data-ttu-id="928cb-113">這個屬性可簡化應用程式的視窗顯示存取。</span><span class="sxs-lookup"><span data-stu-id="928cb-113">This property simplifies window display access for applications.</span></span> <span data-ttu-id="928cb-114">如果這是在) 上設定為 1 (，則在篩選暫停或執行時，通常會隱藏的視窗（通常會在篩選連接之後隱藏）。</span><span class="sxs-lookup"><span data-stu-id="928cb-114">If this is set to  1 (on), the window, which is typically hidden after connection of the filter, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="928cb-115">不過，當篩選準則停止時，不應該隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="928cb-115">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="928cb-116">如果此參數設定為 0 (off) ，則只有當應用程式呼叫 CBaseControlWindow 時，才會顯示此視窗 [**： \_ :p**](cbasecontrolwindow-put-visible.md) 的 Ui 可見或 [**CBaseControlWindow \_ ：:p**](cbasecontrolwindow-put-windowstate.md) 不適當的參數 system.windows.window.windowstate。</span><span class="sxs-lookup"><span data-stu-id="928cb-116">If this parameter is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

<span data-ttu-id="928cb-117">此成員函式的目的是要透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面呼叫外部物件，因此會鎖定重要區段以與相關聯的篩選進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="928cb-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="928cb-118">如果您不是從外部物件呼叫，請呼叫 [**CBaseControlWindow：： IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) 成員函式，以取得此屬性。</span><span class="sxs-lookup"><span data-stu-id="928cb-118">Call the [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) member function to retrieve this property if you are not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="928cb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="928cb-119">Requirements</span></span>



| <span data-ttu-id="928cb-120">需求</span><span class="sxs-lookup"><span data-stu-id="928cb-120">Requirement</span></span> | <span data-ttu-id="928cb-121">值</span><span class="sxs-lookup"><span data-stu-id="928cb-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="928cb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="928cb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="928cb-123"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="928cb-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="928cb-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="928cb-124">Library</span></span><br/> | <dl> <span data-ttu-id="928cb-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="928cb-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="928cb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="928cb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="928cb-127">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="928cb-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




