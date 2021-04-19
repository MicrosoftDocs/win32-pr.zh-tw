---
description: PossiblyEatMessage 方法可讓衍生類別將訊息轉送到另一個視窗。
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: 'CBaseWindow. PossiblyEatMessage 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998736"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a><span data-ttu-id="fb912-103">CBaseWindow. PossiblyEatMessage 方法</span><span class="sxs-lookup"><span data-stu-id="fb912-103">CBaseWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="fb912-104">`PossiblyEatMessage`方法可讓衍生類別將訊息轉送到另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="fb912-104">The `PossiblyEatMessage` method enables a derived class to forward messages to another window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb912-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb912-105">Syntax</span></span>


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="fb912-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb912-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="fb912-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="fb912-108">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb912-108">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="fb912-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb912-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb912-110">第一個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="fb912-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fb912-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb912-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb912-112">第二個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="fb912-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb912-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb912-113">Return value</span></span>

<span data-ttu-id="fb912-114">如果轉寄訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fb912-114">Returns **TRUE** if the message was forwarded, or **FALSE** otherwise.</span></span> <span data-ttu-id="fb912-115">基類會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fb912-115">The base class returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb912-116">備註</span><span class="sxs-lookup"><span data-stu-id="fb912-116">Remarks</span></span>

<span data-ttu-id="fb912-117">在 [**CBaseWindow：： OnReceiveMessage**](cbasewindow-onreceivemessage.md) 方法處理訊息之前，它會呼叫 `PossiblyEatMessage` 。</span><span class="sxs-lookup"><span data-stu-id="fb912-117">Before the [**CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) method handles a message, it calls `PossiblyEatMessage`.</span></span> <span data-ttu-id="fb912-118">如果 `PossiblyEatMessage` 傳回 **TRUE，則** **OnReceiveMessage** 會忽略該訊息。</span><span class="sxs-lookup"><span data-stu-id="fb912-118">If `PossiblyEatMessage` returns **TRUE**, **OnReceiveMessage** ignores the message.</span></span> <span data-ttu-id="fb912-119">衍生的類別可以覆寫， `PossiblyEatMessage` 以便將某些訊息轉送至擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="fb912-119">A derived class can override `PossiblyEatMessage` so that it forwards some messages to an owner window.</span></span> <span data-ttu-id="fb912-120">例如，衍生自 **CBaseWindow** 的 [**CBaseControlWindow**](cbasecontrolwindow.md)類別會轉送鍵盤和滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="fb912-120">For example, the [**CBaseControlWindow**](cbasecontrolwindow.md) class, which derives from **CBaseWindow**, forwards keyboard and mouse messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb912-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb912-121">Requirements</span></span>



| <span data-ttu-id="fb912-122">需求</span><span class="sxs-lookup"><span data-stu-id="fb912-122">Requirement</span></span> | <span data-ttu-id="fb912-123">值</span><span class="sxs-lookup"><span data-stu-id="fb912-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb912-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fb912-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb912-125"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fb912-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb912-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb912-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb912-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fb912-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb912-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb912-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb912-129">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="fb912-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




