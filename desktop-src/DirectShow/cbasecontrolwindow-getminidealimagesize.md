---
description: GetMinIdealImageSize 方法會抓取最小的理想影像大小。
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: 'CBaseControlWindow. GetMinIdealImageSize 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993499"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a><span data-ttu-id="1ae85-103">CBaseControlWindow. GetMinIdealImageSize 方法</span><span class="sxs-lookup"><span data-stu-id="1ae85-103">CBaseControlWindow.GetMinIdealImageSize method</span></span>

<span data-ttu-id="1ae85-104">方法會抓取 `GetMinIdealImageSize` 最小的理想影像大小。</span><span class="sxs-lookup"><span data-stu-id="1ae85-104">The `GetMinIdealImageSize` method retrieves the minimum ideal image size.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae85-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ae85-105">Syntax</span></span>


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="1ae85-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ae85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae85-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="1ae85-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae85-108">最小理想寬度的指標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1ae85-108">Pointer to the minimum ideal width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1ae85-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="1ae85-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae85-110">最小理想高度（以圖元為單位）的指標。</span><span class="sxs-lookup"><span data-stu-id="1ae85-110">Pointer to the minimum ideal height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae85-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ae85-111">Return value</span></span>

<span data-ttu-id="1ae85-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1ae85-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae85-113">備註</span><span class="sxs-lookup"><span data-stu-id="1ae85-113">Remarks</span></span>

<span data-ttu-id="1ae85-114">各種轉譯器對於可顯示的影像大小都有其效能限制。</span><span class="sxs-lookup"><span data-stu-id="1ae85-114">Various renderers have performance restrictions on the size of images they can display.</span></span> <span data-ttu-id="1ae85-115">雖然當要求顯示的影像大於指定的最大值時，仍可正常運作，但轉譯器可以透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面提名最小和最大的理想大小。</span><span class="sxs-lookup"><span data-stu-id="1ae85-115">Although they should still function properly when requested to display images larger than the specified maximum, renderers can nominate the minimum and maximum ideal sizes through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="1ae85-116">只有在篩選圖形暫停或正在執行時，才可以呼叫這個介面，因為它不會等到配置資源，而且轉譯器可以辨識其限制。</span><span class="sxs-lookup"><span data-stu-id="1ae85-116">This interface can be called only when the filter graph is paused or running, because it is not until then that resources are allocated and the renderer can recognize its restrictions.</span></span> <span data-ttu-id="1ae85-117">如果沒有任何限制，轉譯器會以原生影片維度填入 *pWidth* 和 *pHeight* 參數，並傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="1ae85-117">If no restrictions exist, the renderer fills in the *pWidth* and *pHeight* parameters with the native video dimensions and returns S\_FALSE.</span></span> <span data-ttu-id="1ae85-118">如果有限制，則會輸入限制的寬度和高度，而且成員函式會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1ae85-118">If restrictions do exist, the restricted width and height are entered, and the member function returns S\_OK.</span></span>

<span data-ttu-id="1ae85-119">這些維度會套用至目的地影片的大小，而不會套用到整體視窗大小。</span><span class="sxs-lookup"><span data-stu-id="1ae85-119">The dimensions apply to the size of the destination video and not to the overall window size.</span></span> <span data-ttu-id="1ae85-120">因此，在計算要設定之視窗的大小時，請考慮目前的視窗樣式 (例如，WS \_ 標題和 ws \_ 框線) 。</span><span class="sxs-lookup"><span data-stu-id="1ae85-120">So, when calculating the size of the window to set, account for the current window styles (for example, WS\_CAPTION and WS\_BORDER).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae85-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ae85-121">Requirements</span></span>



| <span data-ttu-id="1ae85-122">需求</span><span class="sxs-lookup"><span data-stu-id="1ae85-122">Requirement</span></span> | <span data-ttu-id="1ae85-123">值</span><span class="sxs-lookup"><span data-stu-id="1ae85-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae85-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1ae85-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1ae85-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1ae85-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ae85-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ae85-126">Library</span></span><br/> | <dl> <span data-ttu-id="1ae85-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1ae85-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae85-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ae85-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae85-129">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="1ae85-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




