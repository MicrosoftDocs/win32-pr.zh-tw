---
description: Get \_ MessageDrain 方法會抓取目前的訊息清空。
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: 'CBaseControlWindow.get_MessageDrain 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001514"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a><span data-ttu-id="577ab-103">CBaseControlWindow. 取得 \_ MessageDrain 方法</span><span class="sxs-lookup"><span data-stu-id="577ab-103">CBaseControlWindow.get\_MessageDrain method</span></span>

<span data-ttu-id="577ab-104">方法會抓取 `get_MessageDrain` 目前的訊息清空。</span><span class="sxs-lookup"><span data-stu-id="577ab-104">The `get_MessageDrain` method retrieves the current message drain.</span></span>

## <a name="syntax"></a><span data-ttu-id="577ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="577ab-105">Syntax</span></span>


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a><span data-ttu-id="577ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="577ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577ab-107">*清空*</span><span class="sxs-lookup"><span data-stu-id="577ab-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="577ab-108">目前視窗的指標，接收視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="577ab-108">Pointer to the current window receiving window messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577ab-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="577ab-109">Return value</span></span>

<span data-ttu-id="577ab-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="577ab-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="577ab-111">備註</span><span class="sxs-lookup"><span data-stu-id="577ab-111">Remarks</span></span>

<span data-ttu-id="577ab-112">傳送至影片轉譯器篩選器的訊息可以張貼至另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="577ab-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="577ab-113">使用 **CBaseControlWindow：： get \_ MessageDrain** 成員函式註冊來接收這些訊息 (的視窗) 是目前的訊息清空。</span><span class="sxs-lookup"><span data-stu-id="577ab-113">The window registered to receive these messages (using the **CBaseControlWindow::get\_MessageDrain** member function) is the current message drain.</span></span>

## <a name="requirements"></a><span data-ttu-id="577ab-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="577ab-114">Requirements</span></span>



| <span data-ttu-id="577ab-115">需求</span><span class="sxs-lookup"><span data-stu-id="577ab-115">Requirement</span></span> | <span data-ttu-id="577ab-116">值</span><span class="sxs-lookup"><span data-stu-id="577ab-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="577ab-117">標頭</span><span class="sxs-lookup"><span data-stu-id="577ab-117">Header</span></span><br/>  | <dl> <span data-ttu-id="577ab-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="577ab-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="577ab-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="577ab-119">Library</span></span><br/> | <dl> <span data-ttu-id="577ab-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="577ab-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577ab-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="577ab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577ab-122">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="577ab-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




