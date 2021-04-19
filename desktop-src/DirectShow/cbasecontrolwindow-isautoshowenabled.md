---
description: IsAutoShowEnabled 方法會抓取當轉譯篩選暫停或執行時，是否會自動顯示影片視窗的相關資訊。
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: 'CBaseControlWindow. IsAutoShowEnabled 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990261"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a><span data-ttu-id="d92cb-103">CBaseControlWindow. IsAutoShowEnabled 方法</span><span class="sxs-lookup"><span data-stu-id="d92cb-103">CBaseControlWindow.IsAutoShowEnabled method</span></span>

<span data-ttu-id="d92cb-104">`IsAutoShowEnabled`方法會抓取當轉譯篩選暫停或執行時，是否會自動顯示影片視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d92cb-104">The `IsAutoShowEnabled` method retrieves information about whether the video window automatically appears when the rendering filter pauses or runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="d92cb-105">Syntax</span></span>


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a><span data-ttu-id="d92cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="d92cb-106">Parameters</span></span>

<span data-ttu-id="d92cb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d92cb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d92cb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d92cb-108">Return value</span></span>

<span data-ttu-id="d92cb-109">如果 **m \_ bAutoShow** 成員設為1，則傳回 **TRUE** ，如果設定為0，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d92cb-109">Returns **TRUE** if the **m\_bAutoShow** member is set to  1 or **FALSE** if it is set to 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92cb-110">備註</span><span class="sxs-lookup"><span data-stu-id="d92cb-110">Remarks</span></span>

<span data-ttu-id="d92cb-111">如果在隱藏的影片視窗上， **m \_ bAutoShow** 成員設為1，當篩選暫停或執行時，視窗就會變成可見。</span><span class="sxs-lookup"><span data-stu-id="d92cb-111">If the **m\_bAutoShow** member is set to  1 on a video window that is hidden, the window becomes visible when the filter pauses or runs.</span></span> <span data-ttu-id="d92cb-112">如果這個成員設定為0，則只有在您使用 [**CBaseControlWindow：:p ui \_ Visible**](cbasecontrolwindow-put-visible.md) 或 [**CBaseControlWindow：:p 的 \_ system.windows.window.windowstate**](cbasecontrolwindow-put-windowstate.md) 成員函式搭配適當的參數時，才會出現此視窗。</span><span class="sxs-lookup"><span data-stu-id="d92cb-112">If this member is set to 0, the window will appear only if you use the [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) member function with the appropriate parameters.</span></span>

<span data-ttu-id="d92cb-113">此成員函式會抓取 **m \_ bAutoShow** 成員設定，並具有與使用 [**IVideoWindow：： get 自動完成 \_**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) 方法相同的結果。</span><span class="sxs-lookup"><span data-stu-id="d92cb-113">This member function retrieves the **m\_bAutoShow** member setting and has the same result as using the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92cb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d92cb-114">Requirements</span></span>



| <span data-ttu-id="d92cb-115">需求</span><span class="sxs-lookup"><span data-stu-id="d92cb-115">Requirement</span></span> | <span data-ttu-id="d92cb-116">值</span><span class="sxs-lookup"><span data-stu-id="d92cb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d92cb-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d92cb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d92cb-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d92cb-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d92cb-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d92cb-119">Library</span></span><br/> | <dl> <span data-ttu-id="d92cb-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d92cb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d92cb-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d92cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92cb-122">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="d92cb-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




