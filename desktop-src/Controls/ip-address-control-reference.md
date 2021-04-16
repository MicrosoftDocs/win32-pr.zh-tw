---
title: IP 位址控制
description: 本章節包含與 IP 位址控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462121"
---
# <a name="ip-address-control"></a><span data-ttu-id="f0d29-103">IP 位址控制</span><span class="sxs-lookup"><span data-stu-id="f0d29-103">IP Address Control</span></span>

<span data-ttu-id="f0d29-104">本章節包含與 IP 位址控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0d29-104">This section contains information about the programming elements used with IP address controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="f0d29-105">概觀</span><span class="sxs-lookup"><span data-stu-id="f0d29-105">Overviews</span></span>



| <span data-ttu-id="f0d29-106">主題</span><span class="sxs-lookup"><span data-stu-id="f0d29-106">Topic</span></span>                                          | <span data-ttu-id="f0d29-107">目錄</span><span class="sxs-lookup"><span data-stu-id="f0d29-107">Contents</span></span>                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0d29-108">IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="f0d29-108">IP Address Controls</span></span>](ip-address-controls.md) | <span data-ttu-id="f0d29-109">網際網路通訊協定 (IP) 位址控制可讓使用者以容易理解的格式輸入 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f0d29-109">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span><br/> |



 

### <a name="macros"></a><span data-ttu-id="f0d29-110">巨集</span><span class="sxs-lookup"><span data-stu-id="f0d29-110">Macros</span></span>



| <span data-ttu-id="f0d29-111">主題</span><span class="sxs-lookup"><span data-stu-id="f0d29-111">Topic</span></span>                                         | <span data-ttu-id="f0d29-112">目錄</span><span class="sxs-lookup"><span data-stu-id="f0d29-112">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0d29-113">**第一個 \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-113">**FIRST\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | <span data-ttu-id="f0d29-114">從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息取出的已壓縮 IP 位址中，解壓縮 [欄位 0] 值。</span><span class="sxs-lookup"><span data-stu-id="f0d29-114">Extracts the field 0 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="f0d29-115">**第四個 \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-115">**FOURTH\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | <span data-ttu-id="f0d29-116">從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息取出的已壓縮 IP 位址中，解壓縮 [欄位 3] 值。</span><span class="sxs-lookup"><span data-stu-id="f0d29-116">Extracts the field 3 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="f0d29-117">**MAKEIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-117">**MAKEIPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | <span data-ttu-id="f0d29-118">將四個位元組值封裝成適合與 [**IPM \_ SETADDRESS**](ipm-setaddress.md) 訊息搭配使用的單一 LPARAM。</span><span class="sxs-lookup"><span data-stu-id="f0d29-118">Packs four byte-values into a single LPARAM suitable for use with the [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span> <br/>  |
| [<span data-ttu-id="f0d29-119">**MAKEIPRANGE**</span><span class="sxs-lookup"><span data-stu-id="f0d29-119">**MAKEIPRANGE**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | <span data-ttu-id="f0d29-120">將兩個位元組值封裝成適合與 [**IPM \_ SETRANGE**](ipm-setrange.md) 訊息搭配使用的單一 LPARAM。</span><span class="sxs-lookup"><span data-stu-id="f0d29-120">Packs two byte-values into a single LPARAM suitable for use with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span> <br/>       |
| [<span data-ttu-id="f0d29-121">**第二個 \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-121">**SECOND\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | <span data-ttu-id="f0d29-122">從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息取出的已壓縮 IP 位址中，解壓縮欄位1值。</span><span class="sxs-lookup"><span data-stu-id="f0d29-122">Extracts the field 1 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="f0d29-123">**第三個 \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-123">**THIRD\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | <span data-ttu-id="f0d29-124">從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息抓取的封裝 IP 位址中，解壓縮 [欄位 2] 值。</span><span class="sxs-lookup"><span data-stu-id="f0d29-124">Extracts the field 2 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |



 

### <a name="messages"></a><span data-ttu-id="f0d29-125">訊息</span><span class="sxs-lookup"><span data-stu-id="f0d29-125">Messages</span></span>



| <span data-ttu-id="f0d29-126">主題</span><span class="sxs-lookup"><span data-stu-id="f0d29-126">Topic</span></span>                                         | <span data-ttu-id="f0d29-127">目錄</span><span class="sxs-lookup"><span data-stu-id="f0d29-127">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0d29-128">**IPM \_ CLEARADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-128">**IPM\_CLEARADDRESS**</span></span>](ipm-clearaddress.md) | <span data-ttu-id="f0d29-129">清除 IP 位址控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="f0d29-129">Clears the contents of the IP address control.</span></span> <br/>                                                                            |
| [<span data-ttu-id="f0d29-130">**IPM \_ GETADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-130">**IPM\_GETADDRESS**</span></span>](ipm-getaddress.md)     | <span data-ttu-id="f0d29-131">取得 IP 位址控制項中所有四個欄位的位址值。</span><span class="sxs-lookup"><span data-stu-id="f0d29-131">Gets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="f0d29-132">**IPM \_ ISBLANK**</span><span class="sxs-lookup"><span data-stu-id="f0d29-132">**IPM\_ISBLANK**</span></span>](ipm-isblank.md)           | <span data-ttu-id="f0d29-133">判斷 IP 位址控制項中的所有欄位是否為空白。</span><span class="sxs-lookup"><span data-stu-id="f0d29-133">Determines if all fields in the IP address control are blank.</span></span> <br/>                                                             |
| [<span data-ttu-id="f0d29-134">**IPM \_ SETADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-134">**IPM\_SETADDRESS**</span></span>](ipm-setaddress.md)     | <span data-ttu-id="f0d29-135">在 IP 位址控制項中設定所有四個欄位的位址值。</span><span class="sxs-lookup"><span data-stu-id="f0d29-135">Sets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="f0d29-136">**IPM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-136">**IPM\_SETFOCUS**</span></span>](ipm-setfocus.md)         | <span data-ttu-id="f0d29-137">將鍵盤焦點設定為 IP 位址控制項中的指定欄位。</span><span class="sxs-lookup"><span data-stu-id="f0d29-137">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="f0d29-138">將會選取該欄位中的所有文字。</span><span class="sxs-lookup"><span data-stu-id="f0d29-138">All of the text in that field will be selected.</span></span> <br/> |
| [<span data-ttu-id="f0d29-139">**IPM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="f0d29-139">**IPM\_SETRANGE**</span></span>](ipm-setrange.md)         | <span data-ttu-id="f0d29-140">在 IP 位址控制項中，設定指定之欄位的有效範圍。</span><span class="sxs-lookup"><span data-stu-id="f0d29-140">Sets the valid range for the specified field in the IP address control.</span></span> <br/>                                                   |



 

### <a name="notifications"></a><span data-ttu-id="f0d29-141">通知</span><span class="sxs-lookup"><span data-stu-id="f0d29-141">Notifications</span></span>



| <span data-ttu-id="f0d29-142">主題</span><span class="sxs-lookup"><span data-stu-id="f0d29-142">Topic</span></span>                                     | <span data-ttu-id="f0d29-143">目錄</span><span class="sxs-lookup"><span data-stu-id="f0d29-143">Contents</span></span>                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0d29-144">IPN \_ FIELDCHANGED</span><span class="sxs-lookup"><span data-stu-id="f0d29-144">IPN\_FIELDCHANGED</span></span>](ipn-fieldchanged.md) | <span data-ttu-id="f0d29-145">當使用者變更控制項中的欄位，或從某個欄位移至另一個欄位時傳送。</span><span class="sxs-lookup"><span data-stu-id="f0d29-145">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="f0d29-146">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f0d29-146">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="f0d29-147">結構</span><span class="sxs-lookup"><span data-stu-id="f0d29-147">Structures</span></span>



| <span data-ttu-id="f0d29-148">主題</span><span class="sxs-lookup"><span data-stu-id="f0d29-148">Topic</span></span>                              | <span data-ttu-id="f0d29-149">目錄</span><span class="sxs-lookup"><span data-stu-id="f0d29-149">Contents</span></span>                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0d29-150">**NMIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f0d29-150">**NMIPADDRESS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | <span data-ttu-id="f0d29-151">包含 [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) 通知碼的資訊。</span><span class="sxs-lookup"><span data-stu-id="f0d29-151">Contains information for the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification code.</span></span> <br/> |



 

 

 





