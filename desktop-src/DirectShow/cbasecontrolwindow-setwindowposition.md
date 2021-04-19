---
description: SetWindowPosition 方法會設定桌面上的視窗位置。
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: 'CBaseControlWindow. SetWindowPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995360"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a><span data-ttu-id="ed78f-103">CBaseControlWindow. SetWindowPosition 方法</span><span class="sxs-lookup"><span data-stu-id="ed78f-103">CBaseControlWindow.SetWindowPosition method</span></span>

<span data-ttu-id="ed78f-104">`SetWindowPosition`方法會在桌面上設定視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="ed78f-104">The `SetWindowPosition` method sets the window position on the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed78f-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed78f-105">Syntax</span></span>


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="ed78f-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed78f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed78f-107">*離開*</span><span class="sxs-lookup"><span data-stu-id="ed78f-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="ed78f-108">新的左座標。</span><span class="sxs-lookup"><span data-stu-id="ed78f-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="ed78f-109">*前幾個*</span><span class="sxs-lookup"><span data-stu-id="ed78f-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="ed78f-110">新的上方座標。</span><span class="sxs-lookup"><span data-stu-id="ed78f-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="ed78f-111">*寬度*</span><span class="sxs-lookup"><span data-stu-id="ed78f-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="ed78f-112">視窗的寬度。</span><span class="sxs-lookup"><span data-stu-id="ed78f-112">Width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="ed78f-113">*高度*</span><span class="sxs-lookup"><span data-stu-id="ed78f-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="ed78f-114">視窗的高度。</span><span class="sxs-lookup"><span data-stu-id="ed78f-114">Height of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed78f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed78f-115">Return value</span></span>

<span data-ttu-id="ed78f-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ed78f-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed78f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed78f-117">Requirements</span></span>



| <span data-ttu-id="ed78f-118">需求</span><span class="sxs-lookup"><span data-stu-id="ed78f-118">Requirement</span></span> | <span data-ttu-id="ed78f-119">值</span><span class="sxs-lookup"><span data-stu-id="ed78f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed78f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ed78f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ed78f-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ed78f-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed78f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed78f-122">Library</span></span><br/> | <dl> <span data-ttu-id="ed78f-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ed78f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed78f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed78f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed78f-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="ed78f-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




