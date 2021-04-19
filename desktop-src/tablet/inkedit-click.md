---
description: 發生于使用者按一下 InkEdit 控制項時。
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: 'InkEdit： Click event (筆跡) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997568"
---
# <a name="inkeditclick-event"></a><span data-ttu-id="33437-103">InkEdit。按一下事件</span><span class="sxs-lookup"><span data-stu-id="33437-103">InkEdit.Click event</span></span>

<span data-ttu-id="33437-104">發生于使用者按一下 [InkEdit](inkedit-control-reference.md) 控制項時。</span><span class="sxs-lookup"><span data-stu-id="33437-104">Occurs when a user clicks the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="33437-105">語法</span><span class="sxs-lookup"><span data-stu-id="33437-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="33437-106">參數</span><span class="sxs-lookup"><span data-stu-id="33437-106">Parameters</span></span>

<span data-ttu-id="33437-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="33437-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33437-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="33437-108">Return value</span></span>

<span data-ttu-id="33437-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33437-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33437-110">備註</span><span class="sxs-lookup"><span data-stu-id="33437-110">Remarks</span></span>

<span data-ttu-id="33437-111">按一下控制項除了按一下事件之外，還會產生 [**MouseDown**](inkedit-mousedown.md) 和 [**MouseUp**](inkedit-mouseup.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="33437-111">Clicking a control generates [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="33437-112">若要區分左、右和中間的按鍵，請使用 [**MouseDown**](inkedit-mousedown.md) 和 [**MouseUp**](inkedit-mouseup.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="33437-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span>

 

<span data-ttu-id="33437-113">如果 **click** 事件中有程式碼，則 [**DblClick**](inkedit-dblclick.md) 事件永遠不會觸發，因為 **click** 事件是在兩者之間觸發的第一個事件。</span><span class="sxs-lookup"><span data-stu-id="33437-113">If there is code in the **Click** event, the [**DblClick**](inkedit-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="33437-114">如此一來，滑鼠點擊就會被 **click** 事件攔截，因此不會發生 **DblClick** 事件。</span><span class="sxs-lookup"><span data-stu-id="33437-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="33437-115">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="33437-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="33437-116">**\_ IInkEditEvents** 介面會以 **DISPID \_ IeeClick** 的識別碼來實作為 IDispatch 介面。</span><span class="sxs-lookup"><span data-stu-id="33437-116">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33437-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="33437-117">Requirements</span></span>



| <span data-ttu-id="33437-118">需求</span><span class="sxs-lookup"><span data-stu-id="33437-118">Requirement</span></span> | <span data-ttu-id="33437-119">值</span><span class="sxs-lookup"><span data-stu-id="33437-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33437-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33437-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33437-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33437-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33437-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33437-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33437-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="33437-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="33437-124">標頭</span><span class="sxs-lookup"><span data-stu-id="33437-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33437-125"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="33437-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33437-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="33437-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="33437-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33437-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="33437-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33437-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33437-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="33437-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




