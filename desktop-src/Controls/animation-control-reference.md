---
title: 動畫控制項
description: 本章節包含與動畫控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463793"
---
# <a name="animation-control"></a><span data-ttu-id="6286c-103">動畫控制項</span><span class="sxs-lookup"><span data-stu-id="6286c-103">Animation Control</span></span>

<span data-ttu-id="6286c-104">本章節包含與動畫控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6286c-104">This section contains information about the programming elements used with animation controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="6286c-105">概觀</span><span class="sxs-lookup"><span data-stu-id="6286c-105">Overviews</span></span>



| <span data-ttu-id="6286c-106">主題</span><span class="sxs-lookup"><span data-stu-id="6286c-106">Topic</span></span>                                                      | <span data-ttu-id="6286c-107">目錄</span><span class="sxs-lookup"><span data-stu-id="6286c-107">Contents</span></span>                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6286c-108">關於動畫控制項</span><span class="sxs-lookup"><span data-stu-id="6286c-108">About Animation Controls</span></span>](animation-control-overview.md) | <span data-ttu-id="6286c-109">*動畫控制項* 是顯示 Audio-Video 交錯 (AVI) 剪輯的視窗。</span><span class="sxs-lookup"><span data-stu-id="6286c-109">An *animation control* is a window that displays an Audio-Video Interleaved (AVI) clip.</span></span> <span data-ttu-id="6286c-110">AVI 剪輯是一系列的點陣圖框架，例如電影。</span><span class="sxs-lookup"><span data-stu-id="6286c-110">An AVI clip is a series of bitmap frames like a movie.</span></span> <span data-ttu-id="6286c-111">動畫控制項只能顯示不包含音訊的 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-111">Animation controls can only display AVI clips that do not contain audio.</span></span><br/> |
| [<span data-ttu-id="6286c-112">使用動畫控制項</span><span class="sxs-lookup"><span data-stu-id="6286c-112">Using Animation Controls</span></span>](using-animation-control.md)    | <span data-ttu-id="6286c-113">本節提供動畫控制項的執行詳細資料與範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="6286c-113">This section gives implementation details and example code for animation controls.</span></span><br/>                                                                                                                                      |



 

### <a name="macros"></a><span data-ttu-id="6286c-114">巨集</span><span class="sxs-lookup"><span data-stu-id="6286c-114">Macros</span></span>



| <span data-ttu-id="6286c-115">主題</span><span class="sxs-lookup"><span data-stu-id="6286c-115">Topic</span></span>                                           | <span data-ttu-id="6286c-116">目錄</span><span class="sxs-lookup"><span data-stu-id="6286c-116">Contents</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6286c-117">**動畫 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="6286c-117">**Animate\_Close**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | <span data-ttu-id="6286c-118">關閉 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-118">Closes an AVI clip.</span></span> <span data-ttu-id="6286c-119">您可以使用這個宏，或明確地傳送未傳遞的 [**\_ 開啟**](acm-open.md) 訊息，傳遞 **Null** 參數。</span><span class="sxs-lookup"><span data-stu-id="6286c-119">You can use this macro or send the [**ACM\_OPEN**](acm-open.md) message explicitly, passing in **NULL** parameters.</span></span> <br/>                                                                                                              |
| [<span data-ttu-id="6286c-120">**\_建立動畫**</span><span class="sxs-lookup"><span data-stu-id="6286c-120">**Animate\_Create**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | <span data-ttu-id="6286c-121">建立動畫控制項。</span><span class="sxs-lookup"><span data-stu-id="6286c-121">Creates an animation control.</span></span> <span data-ttu-id="6286c-122">[**動畫 \_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) 會呼叫 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函數來建立動畫控制項。</span><span class="sxs-lookup"><span data-stu-id="6286c-122">[**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) calls the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create the animation control.</span></span> <br/>                                                                                   |
| [<span data-ttu-id="6286c-123">**動畫 \_ >isplaying**</span><span class="sxs-lookup"><span data-stu-id="6286c-123">**Animate\_IsPlaying**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | <span data-ttu-id="6286c-124">檢查是否現正播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-124">Checks to see if an AVI clip is playing.</span></span> <span data-ttu-id="6286c-125">您可以使用此宏或傳送進行中的 [**\_ >isplaying**](acm-isplaying.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6286c-125">You can use this macro or send an [**ACM\_ISPLAYING**](acm-isplaying.md) message.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="6286c-126">**\_開啟動畫**</span><span class="sxs-lookup"><span data-stu-id="6286c-126">**Animate\_Open**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | <span data-ttu-id="6286c-127">開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="6286c-127">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="6286c-128">您可以使用這個宏，或明確地傳送未執行的 [**\_ 開啟**](acm-open.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6286c-128">You can use this macro or send the [**ACM\_OPEN**](acm-open.md) message explicitly.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="6286c-129">**動畫 \_ OpenEx**</span><span class="sxs-lookup"><span data-stu-id="6286c-129">**Animate\_OpenEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | <span data-ttu-id="6286c-130">從指定模組中的資源開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="6286c-130">Opens an AVI clip from a resource in a specified module and displays its first frame in an animation control.</span></span> <span data-ttu-id="6286c-131">您可以使用這個宏，或明確地傳送未執行的 [**\_ 開啟**](acm-open.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6286c-131">You can use this macro or send the [**ACM\_OPEN**](acm-open.md) message explicitly.</span></span> <br/>                                                    |
| [<span data-ttu-id="6286c-132">**動畫 \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="6286c-132">**Animate\_Play**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | <span data-ttu-id="6286c-133">在動畫控制項中播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-133">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="6286c-134">當執行緒繼續執行時，控制項會在背景中播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-134">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="6286c-135">您可以使用這個宏，或明確地傳送未執行的 [**\_ 播放**](acm-play.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6286c-135">You can use this macro or send the [**ACM\_PLAY**](acm-play.md) message explicitly.</span></span> <br/>                                    |
| [<span data-ttu-id="6286c-136">**建立 \_ 搜尋動畫**</span><span class="sxs-lookup"><span data-stu-id="6286c-136">**Animate\_Seek**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | <span data-ttu-id="6286c-137">指示動畫控制項顯示 AVI 剪輯的特定框架。</span><span class="sxs-lookup"><span data-stu-id="6286c-137">Directs an animation control to display a particular frame of an AVI clip.</span></span> <span data-ttu-id="6286c-138">當執行緒繼續執行時，控制項會在背景中顯示剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-138">The control displays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="6286c-139">您可以使用這個宏，或明確地傳送未執行的 [**\_ 播放**](acm-play.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="6286c-139">You can use this macro or send the [**ACM\_PLAY**](acm-play.md) message explicitly.</span></span> <br/> |
| [<span data-ttu-id="6286c-140">**動畫 \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="6286c-140">**Animate\_Stop**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | <span data-ttu-id="6286c-141">停止在動畫控制項中播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-141">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="6286c-142">您可以使用這個宏，或明確地傳送未進行的「執行的 [**\_ 停止**](acm-stop.md) 」訊息。</span><span class="sxs-lookup"><span data-stu-id="6286c-142">You can use this macro or send the [**ACM\_STOP**](acm-stop.md) message explicitly.</span></span> <br/>                                                                                                               |



 

### <a name="messages"></a><span data-ttu-id="6286c-143">訊息</span><span class="sxs-lookup"><span data-stu-id="6286c-143">Messages</span></span>



| <span data-ttu-id="6286c-144">主題</span><span class="sxs-lookup"><span data-stu-id="6286c-144">Topic</span></span>                                   | <span data-ttu-id="6286c-145">目錄</span><span class="sxs-lookup"><span data-stu-id="6286c-145">Contents</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6286c-146">**\_>ISPLAYING**</span><span class="sxs-lookup"><span data-stu-id="6286c-146">**ACM\_ISPLAYING**</span></span>](acm-isplaying.md) | <span data-ttu-id="6286c-147">檢查是否現正播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-147">Checks whether an AVI clip is playing.</span></span> <span data-ttu-id="6286c-148">您可以明確地傳送此訊息，或使用 [**動畫 \_ >isplaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) 宏。</span><span class="sxs-lookup"><span data-stu-id="6286c-148">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span><br/>                                                                                   |
| [<span data-ttu-id="6286c-149">**\_開啟的狀態**</span><span class="sxs-lookup"><span data-stu-id="6286c-149">**ACM\_OPEN**</span></span>](acm-open.md)           | <span data-ttu-id="6286c-150">開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="6286c-150">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="6286c-151">您可以明確地傳送此訊息，或使用 [**動畫 \_ 開啟**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) 或 [**\_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) 宏的動畫。</span><span class="sxs-lookup"><span data-stu-id="6286c-151">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <br/>              |
| [<span data-ttu-id="6286c-152">**未通過的 \_ PLAY**</span><span class="sxs-lookup"><span data-stu-id="6286c-152">**ACM\_PLAY**</span></span>](acm-play.md)           | <span data-ttu-id="6286c-153">在動畫控制項中播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-153">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="6286c-154">當執行緒繼續執行時，控制項會在背景中播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-154">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="6286c-155">您可以明確地傳送此訊息，或使用 [**動畫 \_ 播放**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) 宏。</span><span class="sxs-lookup"><span data-stu-id="6286c-155">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span><br/> |
| [<span data-ttu-id="6286c-156">**進行中的 \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="6286c-156">**ACM\_STOP**</span></span>](acm-stop.md)           | <span data-ttu-id="6286c-157">停止在動畫控制項中播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6286c-157">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="6286c-158">您可以明確地傳送此訊息，或使用 [**動畫 \_ 停**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) 用宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="6286c-158">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span><br/>                                                                            |



 

### <a name="notifications"></a><span data-ttu-id="6286c-159">通知</span><span class="sxs-lookup"><span data-stu-id="6286c-159">Notifications</span></span>



| <span data-ttu-id="6286c-160">主題</span><span class="sxs-lookup"><span data-stu-id="6286c-160">Topic</span></span>                           | <span data-ttu-id="6286c-161">目錄</span><span class="sxs-lookup"><span data-stu-id="6286c-161">Contents</span></span>                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6286c-162">**ACN \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="6286c-162">**ACN\_START**</span></span>](acn-start.md) | <span data-ttu-id="6286c-163">通知動畫控制項的父視窗，相關聯的 AVI 剪輯已開始播放。</span><span class="sxs-lookup"><span data-stu-id="6286c-163">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="6286c-164">此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6286c-164">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <br/>      |
| [<span data-ttu-id="6286c-165">**ACN \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="6286c-165">**ACN\_STOP**</span></span>](acn-stop.md)   | <span data-ttu-id="6286c-166">通知動畫控制項的父視窗，相關聯的 AVI 剪輯已停止播放。</span><span class="sxs-lookup"><span data-stu-id="6286c-166">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="6286c-167">此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6286c-167">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <br/> |



 

### <a name="constants"></a><span data-ttu-id="6286c-168">常數</span><span class="sxs-lookup"><span data-stu-id="6286c-168">Constants</span></span>



| <span data-ttu-id="6286c-169">主題</span><span class="sxs-lookup"><span data-stu-id="6286c-169">Topic</span></span>                                                        | <span data-ttu-id="6286c-170">目錄</span><span class="sxs-lookup"><span data-stu-id="6286c-170">Contents</span></span>                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="6286c-171">**動畫控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="6286c-171">**Animation Control Styles**</span></span>](animation-control-styles.md) | <span data-ttu-id="6286c-172">此區段會列出與動畫控制項搭配使用的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="6286c-172">This section lists the window styles used with animation controls.</span></span><br/> |



 

 

