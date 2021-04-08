---
description: 用來定義私用訊息以供私用視窗類別使用，通常是以 WM 使用者 + x 形式來使用， \_ 其中 x 是整數值。
ms.assetid: 4115c587-fcb4-4170-9948-fe33bcb8742a
title: 'WM_USER (Winuser) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1efd6f2e79180b7dc627281829539d20f5fa74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026185"
---
# <a name="wm_user"></a><span data-ttu-id="c5c35-103">WM \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="c5c35-103">WM\_USER</span></span>

<span data-ttu-id="c5c35-104">用來定義私用訊息以供私用視窗類別使用，通常是以 **WM \_ 使用者** x 形式來使用， + 其中 *x* 是整數值。</span><span class="sxs-lookup"><span data-stu-id="c5c35-104">Used to define private messages for use by private window classes, usually of the form **WM\_USER**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                         0x0400
```

## <a name="remarks"></a><span data-ttu-id="c5c35-105">備註</span><span class="sxs-lookup"><span data-stu-id="c5c35-105">Remarks</span></span>

<span data-ttu-id="c5c35-106">以下是訊息編號的範圍。</span><span class="sxs-lookup"><span data-stu-id="c5c35-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="c5c35-107">範圍</span><span class="sxs-lookup"><span data-stu-id="c5c35-107">Range</span></span>                                                        | <span data-ttu-id="c5c35-108">意義</span><span class="sxs-lookup"><span data-stu-id="c5c35-108">Meaning</span></span>                                                        |
|--------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c5c35-109">0到 **WM \_ 使用者** -1</span><span class="sxs-lookup"><span data-stu-id="c5c35-109">0 through **WM\_USER** –1</span></span><br/>                         | <span data-ttu-id="c5c35-110">保留供系統使用的訊息。</span><span class="sxs-lookup"><span data-stu-id="c5c35-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="c5c35-111">**WM \_使用者** 透過0x7FFF</span><span class="sxs-lookup"><span data-stu-id="c5c35-111">**WM\_USER** through 0x7FFF</span></span><br/>                       | <span data-ttu-id="c5c35-112">私用視窗類別使用的整數訊息。</span><span class="sxs-lookup"><span data-stu-id="c5c35-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="c5c35-113">[**WM \_應用程式**](wm-app.md) (0x8000) 至0xBFFF</span><span class="sxs-lookup"><span data-stu-id="c5c35-113">[**WM\_APP**](wm-app.md) (0x8000) through 0xBFFF</span></span><br/> | <span data-ttu-id="c5c35-114">應用程式可使用的訊息。</span><span class="sxs-lookup"><span data-stu-id="c5c35-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="c5c35-115">0xC000 至0xFFFF</span><span class="sxs-lookup"><span data-stu-id="c5c35-115">0xC000 through 0xFFFF</span></span><br/>                             | <span data-ttu-id="c5c35-116">應用程式所使用的字串訊息。</span><span class="sxs-lookup"><span data-stu-id="c5c35-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="c5c35-117">大於0xFFFF</span><span class="sxs-lookup"><span data-stu-id="c5c35-117">Greater than 0xFFFF</span></span><br/>                               | <span data-ttu-id="c5c35-118">由系統所保留。</span><span class="sxs-lookup"><span data-stu-id="c5c35-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="c5c35-119">第一個範圍中的訊息編號 (0 到 **WM \_ 使用者** -1) 是由系統所定義。</span><span class="sxs-lookup"><span data-stu-id="c5c35-119">Message numbers in the first range (0 through **WM\_USER** –1) are defined by the system.</span></span> <span data-ttu-id="c5c35-120">此範圍中未明確定義的值是由系統所保留。</span><span class="sxs-lookup"><span data-stu-id="c5c35-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="c5c35-121">第二個範圍中的訊息編號 (**WM \_ 使用者** 透過 0x7FFF) 可以由應用程式定義和使用，以在私用視窗類別內傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="c5c35-121">Message numbers in the second range (**WM\_USER** through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="c5c35-122">這些值不能用來定義整個應用程式中有意義的訊息，因為某些預先定義的視窗類別已經在這個範圍中定義值。</span><span class="sxs-lookup"><span data-stu-id="c5c35-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="c5c35-123">例如，[ **按鈕**]、[ **編輯**]、[ **LISTBOX**] 和 [ **COMBOBOX** ] 等預先定義的控制項類別，都可能會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="c5c35-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="c5c35-124">除非應用程式已設計為交換訊息，並將相同意義附加至訊息編號，否則不應將此範圍中的訊息傳送至其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="c5c35-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="c5c35-125">第三個範圍中的訊息編號 (0x8000 到 0xBFFF) 可供應用程式用來作為私用訊息。</span><span class="sxs-lookup"><span data-stu-id="c5c35-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="c5c35-126">此範圍內的訊息不會與系統訊息發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c5c35-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="c5c35-127">第四個範圍內的訊息編號 (0xC000 至 0xFFFF) 是在執行時間定義，而應用程式會呼叫 [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) 函式來取得字串的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="c5c35-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="c5c35-128">所有註冊相同字串的應用程式都可以使用相關聯的訊息編號來交換訊息。</span><span class="sxs-lookup"><span data-stu-id="c5c35-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="c5c35-129">不過，實際的訊息編號不是常數，而且在不同的會話之間不能假設是相同的。</span><span class="sxs-lookup"><span data-stu-id="c5c35-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="c5c35-130">系統會保留第五個範圍 (大於 0xFFFF) 的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="c5c35-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c35-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5c35-131">Requirements</span></span>



| <span data-ttu-id="c5c35-132">需求</span><span class="sxs-lookup"><span data-stu-id="c5c35-132">Requirement</span></span> | <span data-ttu-id="c5c35-133">值</span><span class="sxs-lookup"><span data-stu-id="c5c35-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c35-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5c35-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c35-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5c35-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c5c35-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5c35-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c35-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5c35-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5c35-138">標頭</span><span class="sxs-lookup"><span data-stu-id="c5c35-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c35-139"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c5c35-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c35-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5c35-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5c35-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="c5c35-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5c35-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="c5c35-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="c5c35-143">**WM \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="c5c35-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="c5c35-144">**概念**</span><span class="sxs-lookup"><span data-stu-id="c5c35-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5c35-145">訊息和訊息佇列</span><span class="sxs-lookup"><span data-stu-id="c5c35-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
