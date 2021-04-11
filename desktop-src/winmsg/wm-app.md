---
description: 用來定義私用訊息（通常是以 WM \_ 應用程式 + x 形式），其中 x 是整數值。
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: 'WM_APP (Winuser) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193707"
---
# <a name="wm_app"></a><span data-ttu-id="c31da-103">WM \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="c31da-103">WM\_APP</span></span>

<span data-ttu-id="c31da-104">用來定義私用訊息（通常是以 **WM \_ 應用程式** x 形式）， + 其中 *x* 是整數值。</span><span class="sxs-lookup"><span data-stu-id="c31da-104">Used to define private messages, usually of the form **WM\_APP**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a><span data-ttu-id="c31da-105">備註</span><span class="sxs-lookup"><span data-stu-id="c31da-105">Remarks</span></span>

<span data-ttu-id="c31da-106">**WM \_ 應用程式** 常數可用來區分保留給系統使用的訊息值，以及可供應用程式用來在私用視窗類別內傳送訊息的值。</span><span class="sxs-lookup"><span data-stu-id="c31da-106">The **WM\_APP** constant is used to distinguish between message values that are reserved for use by the system and values that can be used by an application to send messages within a private window class.</span></span> <span data-ttu-id="c31da-107">以下是可用的訊息編號範圍。</span><span class="sxs-lookup"><span data-stu-id="c31da-107">The following are the ranges of message numbers available.</span></span>



| <span data-ttu-id="c31da-108">範圍</span><span class="sxs-lookup"><span data-stu-id="c31da-108">Range</span></span>                                                 | <span data-ttu-id="c31da-109">意義</span><span class="sxs-lookup"><span data-stu-id="c31da-109">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c31da-110">0到 [**WM \_ 使用者**](wm-user.md) -1</span><span class="sxs-lookup"><span data-stu-id="c31da-110">0 through [**WM\_USER**](wm-user.md) –1</span></span><br/>   | <span data-ttu-id="c31da-111">保留供系統使用的訊息。</span><span class="sxs-lookup"><span data-stu-id="c31da-111">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="c31da-112">[**WM \_使用者**](wm-user.md) 透過0x7FFF</span><span class="sxs-lookup"><span data-stu-id="c31da-112">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="c31da-113">私用視窗類別使用的整數訊息。</span><span class="sxs-lookup"><span data-stu-id="c31da-113">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="c31da-114">**WM \_** 透過0xBFFF 的應用程式</span><span class="sxs-lookup"><span data-stu-id="c31da-114">**WM\_APP** through 0xBFFF</span></span><br/>                 | <span data-ttu-id="c31da-115">應用程式可使用的訊息。</span><span class="sxs-lookup"><span data-stu-id="c31da-115">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="c31da-116">0xC000 至0xFFFF</span><span class="sxs-lookup"><span data-stu-id="c31da-116">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="c31da-117">應用程式所使用的字串訊息。</span><span class="sxs-lookup"><span data-stu-id="c31da-117">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="c31da-118">大於0xFFFF</span><span class="sxs-lookup"><span data-stu-id="c31da-118">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="c31da-119">由系統所保留。</span><span class="sxs-lookup"><span data-stu-id="c31da-119">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="c31da-120">第一個範圍中的訊息編號 (0 到 [**WM \_ 使用者**](wm-user.md) -1) 是由系統所定義。</span><span class="sxs-lookup"><span data-stu-id="c31da-120">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md) –1) are defined by the system.</span></span> <span data-ttu-id="c31da-121">此範圍中未明確定義的值是由系統所保留。</span><span class="sxs-lookup"><span data-stu-id="c31da-121">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="c31da-122">第二個範圍中的訊息編號 ([**WM \_ 使用者**](wm-user.md) 透過 0x7FFF) 可以由應用程式定義和使用，以在私用視窗類別內傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="c31da-122">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="c31da-123">這些值不能用來定義整個應用程式中有意義的訊息，因為某些預先定義的視窗類別已經在這個範圍中定義值。</span><span class="sxs-lookup"><span data-stu-id="c31da-123">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="c31da-124">例如，[ **按鈕**]、[ **編輯**]、[ **LISTBOX**] 和 [ **COMBOBOX** ] 等預先定義的控制項類別，都可能會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="c31da-124">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="c31da-125">除非應用程式已設計為交換訊息，並將相同意義附加至訊息編號，否則不應將此範圍中的訊息傳送至其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="c31da-125">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="c31da-126">第三個範圍中的訊息編號 (0x8000 到 0xBFFF) 可供應用程式用來作為私用訊息。</span><span class="sxs-lookup"><span data-stu-id="c31da-126">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="c31da-127">此範圍內的訊息不會與系統訊息發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c31da-127">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="c31da-128">第四個範圍內的訊息編號 (0xC000 至 0xFFFF) 是在執行時間定義，而應用程式會呼叫 [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) 函式來取得字串的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="c31da-128">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="c31da-129">所有註冊相同字串的應用程式都可以使用相關聯的訊息編號來交換訊息。</span><span class="sxs-lookup"><span data-stu-id="c31da-129">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="c31da-130">不過，實際的訊息編號不是常數，而且在不同的會話之間不能假設是相同的。</span><span class="sxs-lookup"><span data-stu-id="c31da-130">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="c31da-131">系統會保留第五個範圍 (大於 0xFFFF) 的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="c31da-131">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="c31da-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c31da-132">Requirements</span></span>



| <span data-ttu-id="c31da-133">需求</span><span class="sxs-lookup"><span data-stu-id="c31da-133">Requirement</span></span> | <span data-ttu-id="c31da-134">值</span><span class="sxs-lookup"><span data-stu-id="c31da-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c31da-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c31da-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c31da-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c31da-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c31da-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c31da-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c31da-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c31da-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c31da-139">標頭</span><span class="sxs-lookup"><span data-stu-id="c31da-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c31da-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c31da-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c31da-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c31da-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="c31da-142">**參考**</span><span class="sxs-lookup"><span data-stu-id="c31da-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c31da-143">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="c31da-143">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="c31da-144">**WM \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="c31da-144">**WM\_USER**</span></span>](wm-user.md)
</dt> <dt>

<span data-ttu-id="c31da-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="c31da-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c31da-146">訊息和訊息佇列</span><span class="sxs-lookup"><span data-stu-id="c31da-146">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
