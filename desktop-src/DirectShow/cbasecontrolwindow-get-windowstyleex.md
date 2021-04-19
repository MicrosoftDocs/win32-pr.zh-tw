---
description: Get \_ WindowStyleEx 方法會抓取擴充的視窗樣式。
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: 'CBaseControlWindow.get_WindowStyleEx 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996461"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a><span data-ttu-id="7c303-103">CBaseControlWindow. 取得 \_ WindowStyleEx 方法</span><span class="sxs-lookup"><span data-stu-id="7c303-103">CBaseControlWindow.get\_WindowStyleEx method</span></span>

<span data-ttu-id="7c303-104">方法會抓取 `get_WindowStyleEx` 擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="7c303-104">The `get_WindowStyleEx` method retrieves the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c303-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c303-105">Syntax</span></span>


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="7c303-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c303-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c303-107">*pWindowStyleEx*</span><span class="sxs-lookup"><span data-stu-id="7c303-107">*pWindowStyleEx*</span></span> 
</dt> <dd>

<span data-ttu-id="7c303-108">延伸視窗樣式的指標。</span><span class="sxs-lookup"><span data-stu-id="7c303-108">Pointer to extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c303-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c303-109">Return value</span></span>

<span data-ttu-id="7c303-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7c303-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c303-111">備註</span><span class="sxs-lookup"><span data-stu-id="7c303-111">Remarks</span></span>

<span data-ttu-id="7c303-112">此成員函式會抓取擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="7c303-112">This member function retrieves the extended window styles.</span></span> <span data-ttu-id="7c303-113">它會呼叫 [**CBaseControlWindow：:D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="7c303-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c303-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c303-114">Requirements</span></span>



| <span data-ttu-id="7c303-115">需求</span><span class="sxs-lookup"><span data-stu-id="7c303-115">Requirement</span></span> | <span data-ttu-id="7c303-116">值</span><span class="sxs-lookup"><span data-stu-id="7c303-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c303-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7c303-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7c303-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7c303-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c303-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c303-119">Library</span></span><br/> | <dl> <span data-ttu-id="7c303-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7c303-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c303-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c303-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c303-122">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="7c303-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




