---
title: Up-Down 控制項
description: 本章節包含與上下按鈕控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021285"
---
# <a name="up-down-control"></a><span data-ttu-id="f7533-103">Up-Down 控制項</span><span class="sxs-lookup"><span data-stu-id="f7533-103">Up-Down Control</span></span>

<span data-ttu-id="f7533-104">本章節包含與上下按鈕控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f7533-104">This section contains information about the programming elements used with up-down controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="f7533-105">概觀</span><span class="sxs-lookup"><span data-stu-id="f7533-105">Overviews</span></span>



| <span data-ttu-id="f7533-106">主題</span><span class="sxs-lookup"><span data-stu-id="f7533-106">Topic</span></span>                                    | <span data-ttu-id="f7533-107">目錄</span><span class="sxs-lookup"><span data-stu-id="f7533-107">Contents</span></span>                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7533-108">上下控制項</span><span class="sxs-lookup"><span data-stu-id="f7533-108">Up-Down Controls</span></span>](up-down-controls.md) | <span data-ttu-id="f7533-109">由上而下的控制項是一組箭號按鈕，使用者可以按一下來遞增或遞減值，例如在附屬控制項中顯示的捲軸位置或數位， (稱為「合作者視窗) 。</span><span class="sxs-lookup"><span data-stu-id="f7533-109">An up-down control is a pair of arrow buttons that the user can click to increment or decrement a value, such as a scroll position or a number displayed in a companion control (called a buddy window).</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="f7533-110">函式</span><span class="sxs-lookup"><span data-stu-id="f7533-110">Functions</span></span>



| <span data-ttu-id="f7533-111">主題</span><span class="sxs-lookup"><span data-stu-id="f7533-111">Topic</span></span>                                              | <span data-ttu-id="f7533-112">目錄</span><span class="sxs-lookup"><span data-stu-id="f7533-112">Contents</span></span>                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7533-113">**CreateUpDownControl**</span><span class="sxs-lookup"><span data-stu-id="f7533-113">**CreateUpDownControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | <span data-ttu-id="f7533-114">建立上下按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="f7533-114">Creates an up-down control.</span></span> <span data-ttu-id="f7533-115">注意：此函式已過時。</span><span class="sxs-lookup"><span data-stu-id="f7533-115">Note: This function is obsolete.</span></span> <span data-ttu-id="f7533-116">它是16位函式，而且無法處理範圍和位置的32位值。</span><span class="sxs-lookup"><span data-stu-id="f7533-116">It is a 16 bit function and cannot handle 32 bit values for range and position.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="f7533-117">訊息</span><span class="sxs-lookup"><span data-stu-id="f7533-117">Messages</span></span>



| <span data-ttu-id="f7533-118">主題</span><span class="sxs-lookup"><span data-stu-id="f7533-118">Topic</span></span>                                                 | <span data-ttu-id="f7533-119">目錄</span><span class="sxs-lookup"><span data-stu-id="f7533-119">Contents</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7533-120">**UDM \_ GETACCEL**</span><span class="sxs-lookup"><span data-stu-id="f7533-120">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)                 | <span data-ttu-id="f7533-121">抓取上下按鈕控制項的加速資訊。</span><span class="sxs-lookup"><span data-stu-id="f7533-121">Retrieves acceleration information for an up-down control.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="f7533-122">**UDM \_ GETBASE**</span><span class="sxs-lookup"><span data-stu-id="f7533-122">**UDM\_GETBASE**</span></span>](udm-getbase.md)                   | <span data-ttu-id="f7533-123">抓取目前的基本基底基底 (也就是上下按鈕控制項的基底10或 16) 。</span><span class="sxs-lookup"><span data-stu-id="f7533-123">Retrieves the current radix base (that is, either base 10 or 16) for an up-down control.</span></span> <br/>                                                                                                                                   |
| [<span data-ttu-id="f7533-124">**UDM \_ GETBUDDY**</span><span class="sxs-lookup"><span data-stu-id="f7533-124">**UDM\_GETBUDDY**</span></span>](udm-getbuddy.md)                 | <span data-ttu-id="f7533-125">抓取目前好友視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7533-125">Retrieves the handle to the current buddy window.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="f7533-126">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="f7533-126">**UDM\_GETPOS**</span></span>](udm-getpos.md)                     | <span data-ttu-id="f7533-127">抓取具有16位精確度之上下按鈕控制項的目前位置。</span><span class="sxs-lookup"><span data-stu-id="f7533-127">Retrieves the current position of an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="f7533-128">**UDM \_ GETPOS32**</span><span class="sxs-lookup"><span data-stu-id="f7533-128">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)                 | <span data-ttu-id="f7533-129">傳回上下按鈕控制項的32位位置。</span><span class="sxs-lookup"><span data-stu-id="f7533-129">Returns the 32-bit position of an up-down control.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="f7533-130">**UDM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="f7533-130">**UDM\_GETRANGE**</span></span>](udm-getrange.md)                 | <span data-ttu-id="f7533-131">抓取上下按鈕 (範圍) 的最小和最大位置。</span><span class="sxs-lookup"><span data-stu-id="f7533-131">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="f7533-132">**UDM \_ GETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="f7533-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)             | <span data-ttu-id="f7533-133">抓取上下按鈕控制項的32位範圍。</span><span class="sxs-lookup"><span data-stu-id="f7533-133">Retrieves the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="f7533-134">**UDM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="f7533-134">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md) | <span data-ttu-id="f7533-135">抓取控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="f7533-135">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                                                               |
| [<span data-ttu-id="f7533-136">**UDM \_ SETACCEL**</span><span class="sxs-lookup"><span data-stu-id="f7533-136">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)                 | <span data-ttu-id="f7533-137">設定上下按鈕控制項的加速。</span><span class="sxs-lookup"><span data-stu-id="f7533-137">Sets the acceleration for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="f7533-138">**UDM \_ SETBASE**</span><span class="sxs-lookup"><span data-stu-id="f7533-138">**UDM\_SETBASE**</span></span>](udm-setbase.md)                   | <span data-ttu-id="f7533-139">設定上下按鈕控制項的基本基底。</span><span class="sxs-lookup"><span data-stu-id="f7533-139">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="f7533-140">基底值會決定合作者視窗是否以十進位或十六進位數字顯示數位。</span><span class="sxs-lookup"><span data-stu-id="f7533-140">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="f7533-141">十六進位數位一律不帶正負號，而且會簽署十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7533-141">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span> <br/> |
| [<span data-ttu-id="f7533-142">**UDM \_ SETBUDDY**</span><span class="sxs-lookup"><span data-stu-id="f7533-142">**UDM\_SETBUDDY**</span></span>](udm-setbuddy.md)                 | <span data-ttu-id="f7533-143">設定上下按鈕控制項的合作者視窗。</span><span class="sxs-lookup"><span data-stu-id="f7533-143">Sets the buddy window for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="f7533-144">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="f7533-144">**UDM\_SETPOS**</span></span>](udm-setpos.md)                     | <span data-ttu-id="f7533-145">設定具有16位精確度之上下按鈕控制項的目前位置。</span><span class="sxs-lookup"><span data-stu-id="f7533-145">Sets the current position for an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                    |
| [<span data-ttu-id="f7533-146">**UDM \_ SETPOS32**</span><span class="sxs-lookup"><span data-stu-id="f7533-146">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)                 | <span data-ttu-id="f7533-147">設定具有32位精確度的上下按鈕控制項的位置。</span><span class="sxs-lookup"><span data-stu-id="f7533-147">Sets the position of an up-down control with 32-bit precision.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="f7533-148">**UDM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="f7533-148">**UDM\_SETRANGE**</span></span>](udm-setrange.md)                 | <span data-ttu-id="f7533-149">設定上下按鈕 (範圍) 的最小和最大位置。</span><span class="sxs-lookup"><span data-stu-id="f7533-149">Sets the minimum and maximum positions (range) for an up-down control.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="f7533-150">**UDM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="f7533-150">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)             | <span data-ttu-id="f7533-151">設定上下按鈕控制項的32位範圍。</span><span class="sxs-lookup"><span data-stu-id="f7533-151">Sets the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                               |
| [<span data-ttu-id="f7533-152">**UDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="f7533-152">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md) | <span data-ttu-id="f7533-153">設定控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="f7533-153">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="f7533-154">此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。</span><span class="sxs-lookup"><span data-stu-id="f7533-154">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/>                                   |



 

### <a name="notifications"></a><span data-ttu-id="f7533-155">通知</span><span class="sxs-lookup"><span data-stu-id="f7533-155">Notifications</span></span>



| <span data-ttu-id="f7533-156">主題</span><span class="sxs-lookup"><span data-stu-id="f7533-156">Topic</span></span>                                                            | <span data-ttu-id="f7533-157">目錄</span><span class="sxs-lookup"><span data-stu-id="f7533-157">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7533-158">NM \_ RELEASEDCAPTURE (上下) </span><span class="sxs-lookup"><span data-stu-id="f7533-158">NM\_RELEASEDCAPTURE (up-down)</span></span>](nm-releasedcapture-up-down-.md) | <span data-ttu-id="f7533-159">通知上下控制項的父視窗，控制項正在釋放滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="f7533-159">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="f7533-160">此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f7533-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                                                                                                                                       |
| [<span data-ttu-id="f7533-161">UDN \_ DELTAPOS</span><span class="sxs-lookup"><span data-stu-id="f7533-161">UDN\_DELTAPOS</span></span>](udn-deltapos.md)                                | <span data-ttu-id="f7533-162">當控制項的位置即將變更時，作業系統會將其傳送至上下按鈕控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="f7533-162">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="f7533-163">當使用者按下控制項的向上或向下箭號時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="f7533-163">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="f7533-164">[UDN \_ DELTAPOS](udn-deltapos.md)訊息會以 [**WM \_ 通知**](wm-notify.md)訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f7533-164">The [UDN\_DELTAPOS](udn-deltapos.md) message is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="f7533-165">結構</span><span class="sxs-lookup"><span data-stu-id="f7533-165">Structures</span></span>



| <span data-ttu-id="f7533-166">主題</span><span class="sxs-lookup"><span data-stu-id="f7533-166">Topic</span></span>                        | <span data-ttu-id="f7533-167">目錄</span><span class="sxs-lookup"><span data-stu-id="f7533-167">Contents</span></span>                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7533-168">**NMUPDOWN**</span><span class="sxs-lookup"><span data-stu-id="f7533-168">**NMUPDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | <span data-ttu-id="f7533-169">包含由上而下控制通知訊息的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="f7533-169">Contains information specific to up-down control notification messages.</span></span> <span data-ttu-id="f7533-170">它等同于並取代 **NM \_ 上下按鈕** 結構。</span><span class="sxs-lookup"><span data-stu-id="f7533-170">It is identical to and replaces the **NM\_UPDOWN** structure.</span></span> <br/> |
| [<span data-ttu-id="f7533-171">**UDACCEL**</span><span class="sxs-lookup"><span data-stu-id="f7533-171">**UDACCEL**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | <span data-ttu-id="f7533-172">包含上下按鈕控制項的加速資訊。</span><span class="sxs-lookup"><span data-stu-id="f7533-172">Contains acceleration information for an up-down control.</span></span> <br/>                                                                             |



 

### <a name="constants"></a><span data-ttu-id="f7533-173">常數</span><span class="sxs-lookup"><span data-stu-id="f7533-173">Constants</span></span>



| <span data-ttu-id="f7533-174">主題</span><span class="sxs-lookup"><span data-stu-id="f7533-174">Topic</span></span>                                                | <span data-ttu-id="f7533-175">目錄</span><span class="sxs-lookup"><span data-stu-id="f7533-175">Contents</span></span>                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="f7533-176">上下控制項樣式</span><span class="sxs-lookup"><span data-stu-id="f7533-176">Up-Down Control Styles</span></span>](up-down-control-styles.md) | <span data-ttu-id="f7533-177">本節列出建立上下控制項時所使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="f7533-177">This section lists the styles used when creating up-down controls.</span></span><br/> |



 

 

 





