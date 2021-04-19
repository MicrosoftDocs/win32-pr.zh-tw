---
description: GetWindowPosition 方法會抓取視窗目前的座標。
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: 'CBaseControlWindow. GetWindowPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979435"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a><span data-ttu-id="86490-103">CBaseControlWindow. GetWindowPosition 方法</span><span class="sxs-lookup"><span data-stu-id="86490-103">CBaseControlWindow.GetWindowPosition method</span></span>

<span data-ttu-id="86490-104">方法會抓取 `GetWindowPosition` 視窗目前的座標。</span><span class="sxs-lookup"><span data-stu-id="86490-104">The `GetWindowPosition` method retrieves the current coordinates for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="86490-105">語法</span><span class="sxs-lookup"><span data-stu-id="86490-105">Syntax</span></span>


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="86490-106">參數</span><span class="sxs-lookup"><span data-stu-id="86490-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86490-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="86490-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="86490-108">左邊座標的指標，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="86490-108">Pointer to the left coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="86490-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="86490-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="86490-110">頂端座標的指標，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="86490-110">Pointer to the top coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="86490-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="86490-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="86490-112">視窗寬度的指標，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="86490-112">Pointer to the window width, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="86490-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="86490-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="86490-114">視窗高度的指標（以螢幕座標表示）。</span><span class="sxs-lookup"><span data-stu-id="86490-114">Pointer to the window height, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86490-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="86490-115">Return value</span></span>

<span data-ttu-id="86490-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="86490-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="86490-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="86490-117">Requirements</span></span>



| <span data-ttu-id="86490-118">需求</span><span class="sxs-lookup"><span data-stu-id="86490-118">Requirement</span></span> | <span data-ttu-id="86490-119">值</span><span class="sxs-lookup"><span data-stu-id="86490-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86490-120">標頭</span><span class="sxs-lookup"><span data-stu-id="86490-120">Header</span></span><br/>  | <dl> <span data-ttu-id="86490-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="86490-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="86490-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="86490-122">Library</span></span><br/> | <dl> <span data-ttu-id="86490-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="86490-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86490-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86490-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86490-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="86490-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




