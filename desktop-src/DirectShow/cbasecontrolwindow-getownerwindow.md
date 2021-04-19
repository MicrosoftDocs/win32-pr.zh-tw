---
description: GetOwnerWindow 方法會抓取擁有的視窗控制碼 m \_ hwndOwner。
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: 'CBaseControlWindow. GetOwnerWindow 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990627"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a><span data-ttu-id="ee523-103">CBaseControlWindow. GetOwnerWindow 方法</span><span class="sxs-lookup"><span data-stu-id="ee523-103">CBaseControlWindow.GetOwnerWindow method</span></span>

<span data-ttu-id="ee523-104">方法會抓取 `GetOwnerWindow` 擁有的視窗控制碼（ **m \_ hwndOwner**）。</span><span class="sxs-lookup"><span data-stu-id="ee523-104">The `GetOwnerWindow` method retrieves the owning window handle, **m\_hwndOwner**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee523-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee523-105">Syntax</span></span>


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a><span data-ttu-id="ee523-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee523-106">Parameters</span></span>

<span data-ttu-id="ee523-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ee523-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee523-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee523-108">Return value</span></span>

<span data-ttu-id="ee523-109">傳回擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="ee523-109">Returns the owner window.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee523-110">備註</span><span class="sxs-lookup"><span data-stu-id="ee523-110">Remarks</span></span>

<span data-ttu-id="ee523-111">在不呼叫介面方法的情況下，抓取擁有視窗。</span><span class="sxs-lookup"><span data-stu-id="ee523-111">Retrieves the owning window without calling the interface method.</span></span> <span data-ttu-id="ee523-112">使用這個成員函式，而不是 [**CBaseControlWindow：： get \_ owner**](cbasecontrolwindow-get-owner.md)，除非您是透過 [**IVideoWindow：： get \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) 方法在外部呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="ee523-112">Use this member function instead of [**CBaseControlWindow::get\_Owner**](cbasecontrolwindow-get-owner.md), unless you are calling this externally through the [**IVideoWindow::get\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee523-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee523-113">Requirements</span></span>



| <span data-ttu-id="ee523-114">需求</span><span class="sxs-lookup"><span data-stu-id="ee523-114">Requirement</span></span> | <span data-ttu-id="ee523-115">值</span><span class="sxs-lookup"><span data-stu-id="ee523-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee523-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ee523-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ee523-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ee523-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee523-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee523-118">Library</span></span><br/> | <dl> <span data-ttu-id="ee523-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ee523-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee523-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee523-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee523-121">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="ee523-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




