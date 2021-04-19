---
title: 關於游標
description: 本主題討論游標。
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- 資源，游標
- 游標，移除
- 閃爍線
- 閃爍的區塊
- 閃爍的點陣圖
- 游標，可見度
- 游標，閃爍時間
- 閃爍時間
- 游標，職位
- 移除游標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969102"
---
# <a name="about-carets"></a><span data-ttu-id="b2f1c-113">關於游標</span><span class="sxs-lookup"><span data-stu-id="b2f1c-113">About Carets</span></span>

<span data-ttu-id="b2f1c-114">系統會為每個訊息佇列提供一個插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-114">The system provides one caret per message queue.</span></span> <span data-ttu-id="b2f1c-115">只有當視窗具有鍵盤焦點或作用中時，才會建立插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-115">A window should create a caret only when it has the keyboard focus or is active.</span></span> <span data-ttu-id="b2f1c-116">在失去鍵盤焦點或變成非使用中之前，視窗應該會終結插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-116">The window should destroy the caret before losing the keyboard focus or becoming inactive.</span></span> <span data-ttu-id="b2f1c-117">如需鍵盤輸入的詳細資訊，請參閱 [鍵盤輸入](/windows/desktop/inputdev/keyboard-input)。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-117">For more information on keyboard input, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="b2f1c-118">您可以使用 [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) 函式來指定插入號的參數。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-118">Use the [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) function to specify the parameters for a caret.</span></span> <span data-ttu-id="b2f1c-119">系統會將插入號的位置、寬度和高度所指定的矩形內的圖元色彩反轉，藉以形成插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-119">The system forms a caret by inverting the pixel color within the rectangle specified by the caret's position, width, and height.</span></span> <span data-ttu-id="b2f1c-120">寬度和高度是以邏輯單元指定;因此，插入點的外觀會受限於視窗的對應模式。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-120">The width and height are specified in logical units; therefore, the appearance of a caret is subject to the window's mapping mode.</span></span>

<span data-ttu-id="b2f1c-121">本節將討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-121">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="b2f1c-122">插入號可見度</span><span class="sxs-lookup"><span data-stu-id="b2f1c-122">Caret Visibility</span></span>](#caret-visibility)
-   [<span data-ttu-id="b2f1c-123">插入號閃爍時間</span><span class="sxs-lookup"><span data-stu-id="b2f1c-123">Caret Blink Time</span></span>](#caret-blink-time)
-   [<span data-ttu-id="b2f1c-124">插入號位置</span><span class="sxs-lookup"><span data-stu-id="b2f1c-124">Caret Position</span></span>](#caret-position)
-   [<span data-ttu-id="b2f1c-125">移除插入號</span><span class="sxs-lookup"><span data-stu-id="b2f1c-125">Removing a Caret</span></span>](#removing-a-caret)

## <a name="caret-visibility"></a><span data-ttu-id="b2f1c-126">插入號可見度</span><span class="sxs-lookup"><span data-stu-id="b2f1c-126">Caret Visibility</span></span>

<span data-ttu-id="b2f1c-127">在定義插入號之後，請使用 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 函式讓插入號變成可見。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-127">After the caret is defined, use the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function to make the caret visible.</span></span> <span data-ttu-id="b2f1c-128">當插入號出現時，它會自動開始閃爍。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-128">When the caret appears, it automatically begins flashing.</span></span> <span data-ttu-id="b2f1c-129">為了顯示實線的插入號，系統會反轉矩形中的每個圖元;為了顯示灰色的插入號，系統會反轉每個其他圖元;為了顯示點陣圖插入號，系統只會反轉點陣圖的白色位。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-129">To display a solid caret, the system inverts every pixel in the rectangle; to display a gray caret, the system inverts every other pixel; to display a bitmap caret, the system inverts only the white bits of the bitmap.</span></span>

## <a name="caret-blink-time"></a><span data-ttu-id="b2f1c-130">插入號閃爍時間</span><span class="sxs-lookup"><span data-stu-id="b2f1c-130">Caret Blink Time</span></span>

<span data-ttu-id="b2f1c-131">反轉插入號所需的經過時間（以毫秒為單位）稱為 *閃爍時間*。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-131">The elapsed time, in milliseconds, required to invert the caret is called the *blink time*.</span></span> <span data-ttu-id="b2f1c-132">只要擁有訊息佇列的執行緒有訊息抽取處理訊息，插入號就會閃爍。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-132">The caret will blink as long as the thread that owns the message queue has a message pump processing the messages.</span></span>

<span data-ttu-id="b2f1c-133">使用者可以使用主控台設定插入號的閃爍時間，而應用程式應該遵守使用者所選擇的設定。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-133">The user can set the blink time of the caret using the Control Panel and applications should respect the settings that the user has chosen.</span></span> <span data-ttu-id="b2f1c-134">應用程式可以使用 [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) 函數來判斷插入號的閃爍時間。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-134">An application can determine the caret's blink time by using the [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) function.</span></span> <span data-ttu-id="b2f1c-135">如果您要撰寫可讓使用者調整閃爍時間的應用程式（例如主控台小程式），請使用 [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) 函數將閃爍時間的速率設定為指定的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-135">If you are writing an application that allows the user to adjust the blink time, such as a Control Panel applet, use the [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function to set the rate of the blink time to a specified number of milliseconds.</span></span>

<span data-ttu-id="b2f1c-136">*Flash time* 是顯示、反轉和還原插入號的顯示所需的經過時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-136">The *flash time* is the elapsed time, in milliseconds, required to display, invert, and restore the caret's display.</span></span> <span data-ttu-id="b2f1c-137">插入號的閃爍時間與閃爍時間最多兩倍。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-137">The flash time of a caret is twice as much as the blink time.</span></span>

## <a name="caret-position"></a><span data-ttu-id="b2f1c-138">插入號位置</span><span class="sxs-lookup"><span data-stu-id="b2f1c-138">Caret Position</span></span>

<span data-ttu-id="b2f1c-139">您可以使用 [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) 函數來判斷插入號的位置。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-139">You can determine the position of the caret using the [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) function.</span></span> <span data-ttu-id="b2f1c-140">在用戶端座標中的位置會複製到 **GetCaretPos** 中參數所指定的結構。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-140">The position, in client coordinates, is copied to a structure specified by a parameter in **GetCaretPos**.</span></span> <span data-ttu-id="b2f1c-141">應用程式可以使用 [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) 函數，在視窗中移動插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-141">An application can move a caret in a window by using the [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) function.</span></span> <span data-ttu-id="b2f1c-142">只有當視窗已經擁有插入點時，才可以移動插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-142">A window can move a caret only if it already owns the caret.</span></span> <span data-ttu-id="b2f1c-143">**SetCaretPos** 可以移動插入號（不論是否為可見）。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-143">**SetCaretPos** can move the caret whether it is visible or not.</span></span>

## <a name="removing-a-caret"></a><span data-ttu-id="b2f1c-144">移除插入號</span><span class="sxs-lookup"><span data-stu-id="b2f1c-144">Removing a Caret</span></span>

<span data-ttu-id="b2f1c-145">您可以藉由隱藏插入號來暫時移除它，也可以藉由終結插入號來永久移除插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-145">You can temporarily remove a caret by hiding it, or you can permanently remove the caret by destroying it.</span></span> <span data-ttu-id="b2f1c-146">若要隱藏插入號，請使用 [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) 函數。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-146">To hide the caret, use the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function.</span></span> <span data-ttu-id="b2f1c-147">當您的應用程式必須在處理訊息時重繪畫面，但必須讓插入號離開時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-147">This is useful when your application must redraw the screen while processing a message, but must keep the caret out of the way.</span></span> <span data-ttu-id="b2f1c-148">當應用程式完成繪圖時，可以使用 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 函式再次顯示插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-148">When the application finishes drawing, it can display the caret again by using the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function.</span></span> <span data-ttu-id="b2f1c-149">隱藏插入號不會終結其形狀或使插入點失效。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-149">Hiding the caret does not destroy its shape or invalidate the insertion point.</span></span> <span data-ttu-id="b2f1c-150">隱藏插入號是累計的;也就是，如果應用程式呼叫 **HideCaret** 五次，它也必須呼叫 **ShowCaret** 五次，插入號才會再次出現。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-150">Hiding the caret is cumulative; that is, if the application calls **HideCaret** five times, it must also call **ShowCaret** five times before the caret will reappear.</span></span>

<span data-ttu-id="b2f1c-151">若要從畫面中移除插入號並終結其圖形，請使用 [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) 函式。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-151">To remove the caret from the screen and destroy its shape, use using the [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) function.</span></span> <span data-ttu-id="b2f1c-152">只有當目前工作的相關視窗擁有插入號時， **DestroyCaret** 才會終結插入號。</span><span class="sxs-lookup"><span data-stu-id="b2f1c-152">**DestroyCaret** destroys the caret only if the window involved in the current task owns the caret.</span></span>

 

 