---
title: 靜態控制項
description: 本章節包含與靜態控制項搭配使用之程式設計項目的相關資訊。 靜態控制項是一種控制項，可讓應用程式為使用者提供通常不需要回應的資訊文字和圖形。
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024178"
---
# <a name="static-control"></a><span data-ttu-id="c04e0-104">靜態控制項</span><span class="sxs-lookup"><span data-stu-id="c04e0-104">Static Control</span></span>

<span data-ttu-id="c04e0-105">本章節包含與靜態控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c04e0-105">This section contains information about the programming elements used with static controls.</span></span> <span data-ttu-id="c04e0-106">*靜態控制項* 是一種控制項，可讓應用程式為使用者提供通常不需要回應的資訊文字和圖形。</span><span class="sxs-lookup"><span data-stu-id="c04e0-106">A *static control* is a control that enables an application to provide the user with informational text and graphics that typically require no response.</span></span>

### <a name="overviews"></a><span data-ttu-id="c04e0-107">概觀</span><span class="sxs-lookup"><span data-stu-id="c04e0-107">Overviews</span></span>



| <span data-ttu-id="c04e0-108">主題</span><span class="sxs-lookup"><span data-stu-id="c04e0-108">Topic</span></span>                                              | <span data-ttu-id="c04e0-109">目錄</span><span class="sxs-lookup"><span data-stu-id="c04e0-109">Contents</span></span>                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c04e0-110">關於靜態控制項</span><span class="sxs-lookup"><span data-stu-id="c04e0-110">About Static Controls</span></span>](about-static-controls.md) | <span data-ttu-id="c04e0-111">本主題討論如何使用靜態控制項。</span><span class="sxs-lookup"><span data-stu-id="c04e0-111">This topic discusses how static controls are used.</span></span><br/>         |
| [<span data-ttu-id="c04e0-112">靜態控制項樣式</span><span class="sxs-lookup"><span data-stu-id="c04e0-112">Static Control Styles</span></span>](static-control-styles.md) |                                                                       |
| [<span data-ttu-id="c04e0-113">使用靜態控制項</span><span class="sxs-lookup"><span data-stu-id="c04e0-113">Using Static Controls</span></span>](using-static-controls.md) | <span data-ttu-id="c04e0-114">本主題提供使用靜態控制項的範例。</span><span class="sxs-lookup"><span data-stu-id="c04e0-114">This topic provides an example that uses a static control.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="c04e0-115">訊息</span><span class="sxs-lookup"><span data-stu-id="c04e0-115">Messages</span></span>



| <span data-ttu-id="c04e0-116">主題</span><span class="sxs-lookup"><span data-stu-id="c04e0-116">Topic</span></span>                                 | <span data-ttu-id="c04e0-117">目錄</span><span class="sxs-lookup"><span data-stu-id="c04e0-117">Contents</span></span>                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c04e0-118">**STM \_ GETICON**</span><span class="sxs-lookup"><span data-stu-id="c04e0-118">**STM\_GETICON**</span></span>](stm-geticon.md)   | <span data-ttu-id="c04e0-119">應用程式會傳送 [**STM \_ GETICON**](stm-geticon.md) 訊息，以抓取與具有 SS 圖示樣式之靜態控制項相關聯的圖示控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c04e0-119">An application sends the [**STM\_GETICON**](stm-geticon.md) message to retrieve a handle to the icon associated with a static control that has the SS\_ICON style.</span></span> <br/> |
| [<span data-ttu-id="c04e0-120">**STM \_ GETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="c04e0-120">**STM\_GETIMAGE**</span></span>](stm-getimage.md) | <span data-ttu-id="c04e0-121">應用程式會傳送 [**STM \_ GETIMAGE**](stm-getimage.md) 訊息，以抓取與靜態控制項相關聯之影像的控制碼 (圖示或點陣圖) 。</span><span class="sxs-lookup"><span data-stu-id="c04e0-121">An application sends an [**STM\_GETIMAGE**](stm-getimage.md) message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span> <br/>          |
| [<span data-ttu-id="c04e0-122">**STM \_ SETICON**</span><span class="sxs-lookup"><span data-stu-id="c04e0-122">**STM\_SETICON**</span></span>](stm-seticon.md)   | <span data-ttu-id="c04e0-123">應用程式會傳送 [**STM \_ SETICON**](stm-seticon.md) 訊息，以將圖示與圖示控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c04e0-123">An application sends the [**STM\_SETICON**](stm-seticon.md) message to associate an icon with an icon control.</span></span> <br/>                                                     |
| [<span data-ttu-id="c04e0-124">**STM \_ SETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="c04e0-124">**STM\_SETIMAGE**</span></span>](stm-setimage.md) | <span data-ttu-id="c04e0-125">應用程式會傳送 [**STM \_ SETIMAGE**](stm-setimage.md) 訊息，以將新的映射與靜態控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c04e0-125">An application sends an [**STM\_SETIMAGE**](stm-setimage.md) message to associate a new image with a static control.</span></span><br/>                                                |



 

### <a name="notifications"></a><span data-ttu-id="c04e0-126">通知</span><span class="sxs-lookup"><span data-stu-id="c04e0-126">Notifications</span></span>



| <span data-ttu-id="c04e0-127">主題</span><span class="sxs-lookup"><span data-stu-id="c04e0-127">Topic</span></span>                                           | <span data-ttu-id="c04e0-128">目錄</span><span class="sxs-lookup"><span data-stu-id="c04e0-128">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c04e0-129">STN \_ 按一下</span><span class="sxs-lookup"><span data-stu-id="c04e0-129">STN\_CLICKED</span></span>](stn-clicked.md)                 | <span data-ttu-id="c04e0-130">當使用者按一下具有 [**SS \_ 通知**](static-control-styles.md)樣式的靜態控制項時，會傳送 [STN \_ 點擊](stn-clicked.md)通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-130">The [STN\_CLICKED](stn-clicked.md) notification code is sent when the user clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="c04e0-131">控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-131">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="c04e0-132">STN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="c04e0-132">STN\_DBLCLK</span></span>](stn-dblclk.md)                   | <span data-ttu-id="c04e0-133">當使用者按兩下具有 **SS \_ 通知** 樣式的靜態控制項時，會傳送 [STN \_ DBLCLK](stn-dblclk.md)通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-133">The [STN\_DBLCLK](stn-dblclk.md) notification code is sent when the user double-clicks a static control that has the **SS\_NOTIFY** style.</span></span> <span data-ttu-id="c04e0-134">控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-134">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span><br/>                                                                                                                                                                                          |
| [<span data-ttu-id="c04e0-135">STN \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="c04e0-135">STN\_DISABLE</span></span>](stn-disable.md)                 | <span data-ttu-id="c04e0-136">停用靜態控制項時，會傳送 [STN \_ 停](stn-disable.md) 用通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-136">The [STN\_DISABLE](stn-disable.md) notification code is sent when a static control is disabled.</span></span> <span data-ttu-id="c04e0-137">靜態控制項必須具有 **SS \_ 通知** 樣式才能接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-137">The static control must have the **SS\_NOTIFY** style to receive this notification code.</span></span> <span data-ttu-id="c04e0-138">控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-138">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="c04e0-139">STN \_ 啟用</span><span class="sxs-lookup"><span data-stu-id="c04e0-139">STN\_ENABLE</span></span>](stn-enable.md)                   | <span data-ttu-id="c04e0-140">啟用靜態控制項時，會傳送 [STN \_ 啟用](stn-enable.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-140">The [STN\_ENABLE](stn-enable.md) notification code is sent when a static control is enabled.</span></span> <span data-ttu-id="c04e0-141">靜態控制項必須具有 **SS \_ 通知** 樣式才能接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-141">The static control must have the **SS\_NOTIFY** style to receive this notification code.</span></span> <span data-ttu-id="c04e0-142">控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c04e0-142">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="c04e0-143">**WM \_ CTLCOLORSTATIC**</span><span class="sxs-lookup"><span data-stu-id="c04e0-143">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md) | <span data-ttu-id="c04e0-144">靜態控制項，或是唯讀或停用的編輯控制項，會在即將繪製控制項時，將 [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) 訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="c04e0-144">A static control, or an edit control that is read-only or disabled, sends the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="c04e0-145">藉由回應此訊息，父視窗可使用指定的裝置內容控制碼來設定靜態控制項的文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="c04e0-145">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the static control.</span></span> <br/> <span data-ttu-id="c04e0-146">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="c04e0-146">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <br/> |



 

 

