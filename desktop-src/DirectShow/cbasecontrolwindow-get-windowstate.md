---
description: Get \_ system.windows.window.windowstate 方法會抓取目前的視窗狀態。
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: 'CBaseControlWindow.get_WindowState 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999494"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a><span data-ttu-id="04d9f-103">CBaseControlWindow. 取得 \_ system.windows.window.windowstate 方法</span><span class="sxs-lookup"><span data-stu-id="04d9f-103">CBaseControlWindow.get\_WindowState method</span></span>

<span data-ttu-id="04d9f-104">方法會抓取 `get_WindowState` 目前的視窗狀態。</span><span class="sxs-lookup"><span data-stu-id="04d9f-104">The `get_WindowState` method retrieves the current window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d9f-105">語法</span><span class="sxs-lookup"><span data-stu-id="04d9f-105">Syntax</span></span>


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a><span data-ttu-id="04d9f-106">參數</span><span class="sxs-lookup"><span data-stu-id="04d9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d9f-107">*pWindowState*</span><span class="sxs-lookup"><span data-stu-id="04d9f-107">*pWindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="04d9f-108">視窗狀態的指標。</span><span class="sxs-lookup"><span data-stu-id="04d9f-108">Pointer to the window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d9f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="04d9f-109">Return value</span></span>

<span data-ttu-id="04d9f-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="04d9f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d9f-111">備註</span><span class="sxs-lookup"><span data-stu-id="04d9f-111">Remarks</span></span>

<span data-ttu-id="04d9f-112">此成員函式會傳回 Microsoft Win32 **ShowWindow** 函數的參數子集。</span><span class="sxs-lookup"><span data-stu-id="04d9f-112">This member function returns a subset of the parameters of the Microsoft Win32 **ShowWindow** function.</span></span> <span data-ttu-id="04d9f-113">尤其是，它會 \_ 根據目前的視窗可見度，傳回軟體顯示和軟體 \_ 隱藏。</span><span class="sxs-lookup"><span data-stu-id="04d9f-113">In particular, it returns SW\_SHOW and SW\_HIDE, depending on the current visibility of the window.</span></span> <span data-ttu-id="04d9f-114">它也會傳回 SW \_ 最小化和 \_ 最大化軟體，取決於視窗是圖示或展開。</span><span class="sxs-lookup"><span data-stu-id="04d9f-114">It also returns SW\_MINIMIZE and SW\_MAXIMIZE, depending on whether the window is an icon or is expanded.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d9f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="04d9f-115">Requirements</span></span>



| <span data-ttu-id="04d9f-116">需求</span><span class="sxs-lookup"><span data-stu-id="04d9f-116">Requirement</span></span> | <span data-ttu-id="04d9f-117">值</span><span class="sxs-lookup"><span data-stu-id="04d9f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d9f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="04d9f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="04d9f-119"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="04d9f-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04d9f-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="04d9f-120">Library</span></span><br/> | <dl> <span data-ttu-id="04d9f-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="04d9f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d9f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04d9f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d9f-123">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="04d9f-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




