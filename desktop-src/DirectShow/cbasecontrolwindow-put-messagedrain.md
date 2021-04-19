---
description: Put \_ MessageDrain 方法會設定視窗，以接收傳送至影片轉譯器的視窗訊息。
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: 'CBaseControlWindow.put_MessageDrain 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981392"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a><span data-ttu-id="58af9-103">CBaseControlWindow. put \_ MessageDrain 方法</span><span class="sxs-lookup"><span data-stu-id="58af9-103">CBaseControlWindow.put\_MessageDrain method</span></span>

<span data-ttu-id="58af9-104">`put_MessageDrain`方法會將視窗設定為接收傳送至影片轉譯器的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="58af9-104">The `put_MessageDrain` method sets the window to receive window messages sent to the video renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="58af9-105">語法</span><span class="sxs-lookup"><span data-stu-id="58af9-105">Syntax</span></span>


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a><span data-ttu-id="58af9-106">參數</span><span class="sxs-lookup"><span data-stu-id="58af9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58af9-107">*清空*</span><span class="sxs-lookup"><span data-stu-id="58af9-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="58af9-108">要張貼訊息的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="58af9-108">Window to post messages to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58af9-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="58af9-109">Return value</span></span>

<span data-ttu-id="58af9-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="58af9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58af9-111">備註</span><span class="sxs-lookup"><span data-stu-id="58af9-111">Remarks</span></span>

<span data-ttu-id="58af9-112">傳送至影片轉譯器篩選器的訊息可以張貼至另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="58af9-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="58af9-113">此成員函式會註冊視窗以接收這些訊息。</span><span class="sxs-lookup"><span data-stu-id="58af9-113">This member function registers the window to receive these messages.</span></span> <span data-ttu-id="58af9-114">不同于 [**CBaseControlWindow：:p ui \_ 擁有**](cbasecontrolwindow-put-owner.md) 者成員函式，此成員函式不會讓影片視窗成為另一個視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="58af9-114">Unlike the [**CBaseControlWindow::put\_Owner**](cbasecontrolwindow-put-owner.md) member function, this member function does not make the video window a child of another window.</span></span> <span data-ttu-id="58af9-115">它特別適用于全螢幕的影片轉譯器，它不能是子視窗。</span><span class="sxs-lookup"><span data-stu-id="58af9-115">It is particularly useful for full-screen video renderers, which cannot be child windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="58af9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="58af9-116">Requirements</span></span>



| <span data-ttu-id="58af9-117">需求</span><span class="sxs-lookup"><span data-stu-id="58af9-117">Requirement</span></span> | <span data-ttu-id="58af9-118">值</span><span class="sxs-lookup"><span data-stu-id="58af9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58af9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="58af9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="58af9-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="58af9-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="58af9-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="58af9-121">Library</span></span><br/> | <dl> <span data-ttu-id="58af9-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="58af9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58af9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58af9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58af9-124">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="58af9-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




