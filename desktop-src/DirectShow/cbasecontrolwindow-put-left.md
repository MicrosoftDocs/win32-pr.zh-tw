---
description: Put \_ left 方法會設定視窗的左座標。
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: 'CBaseControlWindow.put_Left 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987913"
---
# <a name="cbasecontrolwindowput_left-method"></a><span data-ttu-id="f80f1-103">CBaseControlWindow，put \_ 方法</span><span class="sxs-lookup"><span data-stu-id="f80f1-103">CBaseControlWindow.put\_Left method</span></span>

<span data-ttu-id="f80f1-104">`put_Left`方法會設定視窗的左座標。</span><span class="sxs-lookup"><span data-stu-id="f80f1-104">The `put_Left` method sets the left coordinate for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f80f1-105">語法</span><span class="sxs-lookup"><span data-stu-id="f80f1-105">Syntax</span></span>


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a><span data-ttu-id="f80f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f80f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f80f1-107">*離開*</span><span class="sxs-lookup"><span data-stu-id="f80f1-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="f80f1-108">新的左座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f80f1-108">New left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f80f1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f80f1-109">Return value</span></span>

<span data-ttu-id="f80f1-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f80f1-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f80f1-111">備註</span><span class="sxs-lookup"><span data-stu-id="f80f1-111">Remarks</span></span>

<span data-ttu-id="f80f1-112">視窗具有桌面上的位置。</span><span class="sxs-lookup"><span data-stu-id="f80f1-112">The window has a position on the desktop.</span></span> <span data-ttu-id="f80f1-113">這是以圖元為單位來表示， (左、上、右和下) 。</span><span class="sxs-lookup"><span data-stu-id="f80f1-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="f80f1-114">OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是用於 DirectShow 的慣例。</span><span class="sxs-lookup"><span data-stu-id="f80f1-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="f80f1-115">所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。</span><span class="sxs-lookup"><span data-stu-id="f80f1-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="f80f1-116">設定左方或上座標會分別將視窗向左或上移動;這些座標不會影響視窗的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="f80f1-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="f80f1-117">同樣地，設定寬度和高度並不會影響左邊和上座標。</span><span class="sxs-lookup"><span data-stu-id="f80f1-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f80f1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f80f1-118">Requirements</span></span>



| <span data-ttu-id="f80f1-119">需求</span><span class="sxs-lookup"><span data-stu-id="f80f1-119">Requirement</span></span> | <span data-ttu-id="f80f1-120">值</span><span class="sxs-lookup"><span data-stu-id="f80f1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f80f1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f80f1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f80f1-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f80f1-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f80f1-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f80f1-123">Library</span></span><br/> | <dl> <span data-ttu-id="f80f1-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f80f1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f80f1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f80f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f80f1-126">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="f80f1-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




