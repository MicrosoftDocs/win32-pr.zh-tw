---
description: 取得 \_ 寬度方法會抓取目前的視窗寬度。
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: 'CBaseControlWindow.get_Width 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999693"
---
# <a name="cbasecontrolwindowget_width-method"></a><span data-ttu-id="16cda-103">CBaseControlWindow. 取得 \_ 寬度方法</span><span class="sxs-lookup"><span data-stu-id="16cda-103">CBaseControlWindow.get\_Width method</span></span>

<span data-ttu-id="16cda-104">方法會抓取 `get_Width` 目前的視窗寬度。</span><span class="sxs-lookup"><span data-stu-id="16cda-104">The `get_Width` method retrieves the current window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cda-105">語法</span><span class="sxs-lookup"><span data-stu-id="16cda-105">Syntax</span></span>


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a><span data-ttu-id="16cda-106">參數</span><span class="sxs-lookup"><span data-stu-id="16cda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16cda-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="16cda-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="16cda-108">視窗寬度的指標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="16cda-108">Pointer to the window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16cda-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="16cda-109">Return value</span></span>

<span data-ttu-id="16cda-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="16cda-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16cda-111">備註</span><span class="sxs-lookup"><span data-stu-id="16cda-111">Remarks</span></span>

<span data-ttu-id="16cda-112">視窗具有桌面上的位置。</span><span class="sxs-lookup"><span data-stu-id="16cda-112">The window has a position on the desktop.</span></span> <span data-ttu-id="16cda-113">這是以圖元為單位來表示， (左、上、右和下) 。</span><span class="sxs-lookup"><span data-stu-id="16cda-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="16cda-114">OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是用於 DirectShow 的慣例。</span><span class="sxs-lookup"><span data-stu-id="16cda-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="16cda-115">所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。</span><span class="sxs-lookup"><span data-stu-id="16cda-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="16cda-116">設定左方或上座標會分別將視窗向左或上移動;這些座標不會影響視窗的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="16cda-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="16cda-117">同樣地，設定寬度和高度並不會影響左邊和上座標。</span><span class="sxs-lookup"><span data-stu-id="16cda-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="16cda-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="16cda-118">Requirements</span></span>



| <span data-ttu-id="16cda-119">需求</span><span class="sxs-lookup"><span data-stu-id="16cda-119">Requirement</span></span> | <span data-ttu-id="16cda-120">值</span><span class="sxs-lookup"><span data-stu-id="16cda-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16cda-121">標頭</span><span class="sxs-lookup"><span data-stu-id="16cda-121">Header</span></span><br/>  | <dl> <span data-ttu-id="16cda-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="16cda-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="16cda-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="16cda-123">Library</span></span><br/> | <dl> <span data-ttu-id="16cda-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="16cda-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16cda-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16cda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16cda-126">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="16cda-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




