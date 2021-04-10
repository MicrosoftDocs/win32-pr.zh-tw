---
title: 關於 IP 位址控制項
description: 網際網路通訊協定 (IP) 位址控制可讓使用者以容易理解的格式輸入 IP 位址。
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8cf39400c97d211d83b5496067fe6d4772e1e7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933644"
---
# <a name="about-ip-address-controls"></a><span data-ttu-id="83532-103">關於 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="83532-103">About IP Address Controls</span></span>

<span data-ttu-id="83532-104">網際網路通訊協定 (IP) 位址控制可讓使用者以容易理解的格式輸入 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="83532-104">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span> <span data-ttu-id="83532-105">此控制項也可讓應用程式以數值格式（而不是文字格式）取得位址。</span><span class="sxs-lookup"><span data-stu-id="83532-105">This control also allows the application to obtain the address in numeric form rather than in text form.</span></span>

-   [<span data-ttu-id="83532-106">關於 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="83532-106">About IP Address Controls</span></span>](#about-ip-address-controls)
-   [<span data-ttu-id="83532-107">建立 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="83532-107">Creating an IP Address Control</span></span>](#creating-an-ip-address-control)
-   [<span data-ttu-id="83532-108">IP 位址是否可以控制編輯控制項？</span><span class="sxs-lookup"><span data-stu-id="83532-108">Is an IP Address Control an Edit Control?</span></span>](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a><span data-ttu-id="83532-109">關於 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="83532-109">About IP Address Controls</span></span>

<span data-ttu-id="83532-110">Windows Internet Explorer 4.0 版引進了 IP 位址控制項，這是一個新的控制項，類似于編輯控制項，可讓使用者輸入網際網路通訊協定中的數位位址， (IP) 格式。</span><span class="sxs-lookup"><span data-stu-id="83532-110">Windows Internet Explorer Version 4.0 introduces the IP address control, a new control similar to an edit control that allows the user to enter a numeric address in Internet protocol (IP) format.</span></span> <span data-ttu-id="83532-111">此格式包含 4 3 位數的欄位。</span><span class="sxs-lookup"><span data-stu-id="83532-111">This format consists of four three-digit fields.</span></span> <span data-ttu-id="83532-112">每個欄位都會個別處理;欄位號碼是以零為基底，並從左至右繼續，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="83532-112">Each field is treated individually; the field numbers are zero-based and proceed from left to right as shown in this figure.</span></span>

![顯示 ip 位址控制項四個欄位中各項值的圖表](images/ipa-scrn.png)

<span data-ttu-id="83532-114">控制項只允許在每個欄位中輸入數位文字。</span><span class="sxs-lookup"><span data-stu-id="83532-114">The control allows only numeric text to be entered in each of the fields.</span></span> <span data-ttu-id="83532-115">一旦在指定的欄位中輸入三個數字，鍵盤焦點就會自動移至下一個欄位。</span><span class="sxs-lookup"><span data-stu-id="83532-115">Once three digits have been entered in a given field, keyboard focus is automatically moved to the next field.</span></span> <span data-ttu-id="83532-116">如果應用程式不需要填滿整個欄位，使用者可以輸入少於三位數。</span><span class="sxs-lookup"><span data-stu-id="83532-116">If filling the entire field is not required by the application, the user can enter fewer than three digits.</span></span> <span data-ttu-id="83532-117">例如，如果欄位只應包含第二十個數字，輸入 "21" 並按下按鍵，就會將使用者帶到下一個欄位。</span><span class="sxs-lookup"><span data-stu-id="83532-117">For example, if the field should only contain the number twenty-one, typing "21" and pressing the key will take the user to the next field.</span></span>

<span data-ttu-id="83532-118">每個欄位的預設範圍是0到255，但應用程式可以將範圍設定為這些限制與 [**IPM \_ SETRANGE**](ipm-setrange.md) 訊息之間的任何值。</span><span class="sxs-lookup"><span data-stu-id="83532-118">The default range for each field is 0 to 255, but the application can set the range to any values between those limits with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="83532-119">IP 位址控制是在 Comctl32.dll 4.71 版和更新版本中執行。</span><span class="sxs-lookup"><span data-stu-id="83532-119">The IP address control is implemented in version 4.71 and later of Comctl32.dll.</span></span>

 

## <a name="creating-an-ip-address-control"></a><span data-ttu-id="83532-120">建立 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="83532-120">Creating an IP Address Control</span></span>

<span data-ttu-id="83532-121">建立 IP 位址控制項之前，請使用 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **dwICC** 成員中設定的「 **ICC \_ 網際網路 \_ 類別**」旗標來呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 。</span><span class="sxs-lookup"><span data-stu-id="83532-121">Before creating an IP address control, call [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) with the **ICC\_INTERNET\_CLASSES** flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="83532-122">使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立 IP 位址控制項。</span><span class="sxs-lookup"><span data-stu-id="83532-122">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an IP address control.</span></span> <span data-ttu-id="83532-123">控制項的類別名稱是 [**WC \_ IPADDRESS**](common-control-window-classes.md)，定義于 Commctrl 中。</span><span class="sxs-lookup"><span data-stu-id="83532-123">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="83532-124">沒有任何 IP 位址控制特定樣式存在;不過，因為這是子控制項，所以請至少使用 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 系樣式。</span><span class="sxs-lookup"><span data-stu-id="83532-124">No IP address control-specific styles exist; however, because this is a child control, use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style as a minimum.</span></span>

## <a name="is-an-ip-address-control-an-edit-control"></a><span data-ttu-id="83532-125">IP 位址是否可以控制編輯控制項？</span><span class="sxs-lookup"><span data-stu-id="83532-125">Is an IP Address Control an Edit Control?</span></span>

<span data-ttu-id="83532-126">IP 位址控制項不是編輯控制項，也不會回應 EM \_ 訊息。</span><span class="sxs-lookup"><span data-stu-id="83532-126">An IP address control is not an edit control and it will not respond to EM\_ messages.</span></span> <span data-ttu-id="83532-127">不過，它會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，將下列編輯控制項通知傳送給擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="83532-127">It will, however, send the owner window the following edit control notifications through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="83532-128">請注意，IP 位址控制也會 \_ 透過 [**WM \_ 通知**](wm-notify.md) 訊息傳送私用 IPN 通知。</span><span class="sxs-lookup"><span data-stu-id="83532-128">Note that the IP address control will also send private IPN\_ notifications through the [**WM\_NOTIFY**](wm-notify.md) message.</span></span>



|                                   |                                                                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83532-129">**通知**</span><span class="sxs-lookup"><span data-stu-id="83532-129">**Notification**</span></span>                  | <span data-ttu-id="83532-130">**通知的原因**</span><span class="sxs-lookup"><span data-stu-id="83532-130">**Reason for notification**</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="83532-131">EN \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="83532-131">EN\_SETFOCUS</span></span>](en-setfocus.md)   | <span data-ttu-id="83532-132">在 IP 位址控制取得鍵盤焦點時傳送。</span><span class="sxs-lookup"><span data-stu-id="83532-132">Sent when the IP address control gains the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="83532-133">EN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="83532-133">EN\_KILLFOCUS</span></span>](en-killfocus.md) | <span data-ttu-id="83532-134">在 IP 位址控制項失去鍵盤焦點時傳送。</span><span class="sxs-lookup"><span data-stu-id="83532-134">Sent when the IP address control loses the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="83532-135">EN \_ 變更</span><span class="sxs-lookup"><span data-stu-id="83532-135">EN\_CHANGE</span></span>](en-change.md)       | <span data-ttu-id="83532-136">在 IP 位址控制項中的任何欄位變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="83532-136">Sent when any field in the IP address control changes.</span></span> <span data-ttu-id="83532-137">就像來自標準編輯控制項的 [EN \_ 變更](en-change.md) 通知一樣，此通知會在螢幕更新之後收到。</span><span class="sxs-lookup"><span data-stu-id="83532-137">Like the [EN\_CHANGE](en-change.md) notification from a standard edit control, this notification is received after the screen has been updated.</span></span> |



 

 

 