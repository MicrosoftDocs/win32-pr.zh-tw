---
description: 發生于使用者按一下 InkPicture 控制項時。
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: 'InkPicture： Click event (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851612"
---
# <a name="inkpictureclick-event"></a><span data-ttu-id="2e01c-103">InkPicture。按一下事件</span><span class="sxs-lookup"><span data-stu-id="2e01c-103">InkPicture.Click event</span></span>

<span data-ttu-id="2e01c-104">發生于使用者按一下 [InkPicture](inkpicture-control-reference.md) 控制項時。</span><span class="sxs-lookup"><span data-stu-id="2e01c-104">Occurs when a user clicks the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e01c-105">語法</span><span class="sxs-lookup"><span data-stu-id="2e01c-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="2e01c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e01c-106">Parameters</span></span>

<span data-ttu-id="2e01c-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2e01c-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e01c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e01c-108">Return value</span></span>

<span data-ttu-id="2e01c-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2e01c-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e01c-110">備註</span><span class="sxs-lookup"><span data-stu-id="2e01c-110">Remarks</span></span>

<span data-ttu-id="2e01c-111">按一下控制項除了按一下事件之外，還會產生 [**MouseDown**](inkpicture-mousedown.md) 和 [**MouseUp**](inkpicture-mouseup.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="2e01c-111">Clicking a control generates [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="2e01c-112">若要區分左、右和中間的按鍵，請使用 [**MouseDown**](inkpicture-mousedown.md) 和 [**MouseUp**](inkpicture-mouseup.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="2e01c-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span>

 

<span data-ttu-id="2e01c-113">如果 **click** 事件中有程式碼，則 [**DblClick**](inkpicture-dblclick.md) 事件永遠不會觸發，因為 **click** 事件是在兩者之間觸發的第一個事件。</span><span class="sxs-lookup"><span data-stu-id="2e01c-113">If there is code in the **Click** event, the [**DblClick**](inkpicture-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="2e01c-114">如此一來，滑鼠點擊就會被 **click** 事件攔截，因此不會發生 **DblClick** 事件。</span><span class="sxs-lookup"><span data-stu-id="2e01c-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="2e01c-115">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="2e01c-115">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="2e01c-116">**\_ IInkPictureEvents** 介面會以 **DISPID \_ IPEClick** 的識別碼來實作為 IDispatch 介面。</span><span class="sxs-lookup"><span data-stu-id="2e01c-116">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e01c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e01c-117">Requirements</span></span>



| <span data-ttu-id="2e01c-118">需求</span><span class="sxs-lookup"><span data-stu-id="2e01c-118">Requirement</span></span> | <span data-ttu-id="2e01c-119">值</span><span class="sxs-lookup"><span data-stu-id="2e01c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e01c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e01c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e01c-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e01c-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2e01c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e01c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e01c-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="2e01c-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2e01c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2e01c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e01c-125"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="2e01c-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2e01c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e01c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e01c-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e01c-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2e01c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e01c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e01c-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="2e01c-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




