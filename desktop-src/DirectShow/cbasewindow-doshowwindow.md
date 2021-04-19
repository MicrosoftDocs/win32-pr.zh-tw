---
description: DoShowWindow 方法會設定視窗的顯示狀態。
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: 'CBaseWindow. DoShowWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992918"
---
# <a name="cbasewindowdoshowwindow-method"></a><span data-ttu-id="c9a56-103">CBaseWindow. DoShowWindow 方法</span><span class="sxs-lookup"><span data-stu-id="c9a56-103">CBaseWindow.DoShowWindow method</span></span>

<span data-ttu-id="c9a56-104">**DoShowWindow** 方法會設定視窗的顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="c9a56-104">The **DoShowWindow** method sets the window's show state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a56-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9a56-105">Syntax</span></span>


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c9a56-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a56-107">*ShowCmd*</span><span class="sxs-lookup"><span data-stu-id="c9a56-107">*ShowCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a56-108">指定視窗顯示方式的旗標。</span><span class="sxs-lookup"><span data-stu-id="c9a56-108">Flag that specifies how the window is to be shown.</span></span> <span data-ttu-id="c9a56-109">值可以是針對 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數所定義的任何常數。</span><span class="sxs-lookup"><span data-stu-id="c9a56-109">The value can be any constant defined for the *nCmdShow* parameter of the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a56-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9a56-110">Return value</span></span>

<span data-ttu-id="c9a56-111">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c9a56-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9a56-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9a56-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a56-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9a56-113">Requirements</span></span>



| <span data-ttu-id="c9a56-114">需求</span><span class="sxs-lookup"><span data-stu-id="c9a56-114">Requirement</span></span> | <span data-ttu-id="c9a56-115">值</span><span class="sxs-lookup"><span data-stu-id="c9a56-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a56-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c9a56-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c9a56-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c9a56-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9a56-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9a56-118">Library</span></span><br/> | <dl> <span data-ttu-id="c9a56-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c9a56-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a56-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9a56-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a56-121">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="c9a56-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

