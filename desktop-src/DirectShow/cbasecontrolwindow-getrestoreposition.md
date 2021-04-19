---
description: 當視窗未最大化或最小化時，GetRestorePosition 方法會抓取要還原的位置。
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: 'CBaseControlWindow. GetRestorePosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995741"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a><span data-ttu-id="71080-103">CBaseControlWindow. GetRestorePosition 方法</span><span class="sxs-lookup"><span data-stu-id="71080-103">CBaseControlWindow.GetRestorePosition method</span></span>

<span data-ttu-id="71080-104">`GetRestorePosition`當視窗未最大化或最小化時，此方法會抓取要還原的位置。</span><span class="sxs-lookup"><span data-stu-id="71080-104">The `GetRestorePosition` method retrieves the position to which the window will be restored when it is not maximized or minimized.</span></span>

## <a name="syntax"></a><span data-ttu-id="71080-105">語法</span><span class="sxs-lookup"><span data-stu-id="71080-105">Syntax</span></span>


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="71080-106">參數</span><span class="sxs-lookup"><span data-stu-id="71080-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71080-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="71080-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="71080-108">最左邊座標值的指標。</span><span class="sxs-lookup"><span data-stu-id="71080-108">Pointer to the value for leftmost coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="71080-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="71080-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="71080-110">視窗頂端值的指標。</span><span class="sxs-lookup"><span data-stu-id="71080-110">Pointer to the value for top of the window.</span></span>

</dd> <dt>

<span data-ttu-id="71080-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="71080-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="71080-112">視窗寬度值的指標。</span><span class="sxs-lookup"><span data-stu-id="71080-112">Pointer to the value for width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="71080-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="71080-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="71080-114">視窗高度值的指標。</span><span class="sxs-lookup"><span data-stu-id="71080-114">Pointer to the value for height of window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71080-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="71080-115">Return value</span></span>

<span data-ttu-id="71080-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="71080-116">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71080-117">備註</span><span class="sxs-lookup"><span data-stu-id="71080-117">Remarks</span></span>

<span data-ttu-id="71080-118">當視窗未最大化或最小化時，這與 [**CBaseControlWindow：： GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) 函數所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="71080-118">This is the same as the values returned by the [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) function when the window is neither maximized nor minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="71080-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="71080-119">Requirements</span></span>



| <span data-ttu-id="71080-120">需求</span><span class="sxs-lookup"><span data-stu-id="71080-120">Requirement</span></span> | <span data-ttu-id="71080-121">值</span><span class="sxs-lookup"><span data-stu-id="71080-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71080-122">標頭</span><span class="sxs-lookup"><span data-stu-id="71080-122">Header</span></span><br/>  | <dl> <span data-ttu-id="71080-123"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="71080-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71080-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="71080-124">Library</span></span><br/> | <dl> <span data-ttu-id="71080-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="71080-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71080-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71080-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71080-127">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="71080-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




