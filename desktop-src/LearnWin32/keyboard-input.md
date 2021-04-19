---
title: 使用 Win32 和 c + +) 開始的鍵盤輸入 (
description: 鍵盤輸入
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "106986002"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a><span data-ttu-id="9a525-103">使用 Win32 和 c + +) 開始的鍵盤輸入 (</span><span class="sxs-lookup"><span data-stu-id="9a525-103">Keyboard Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="9a525-104">鍵盤用於數種不同類型的輸入，包括：</span><span class="sxs-lookup"><span data-stu-id="9a525-104">The keyboard is used for several distinct types of input, including:</span></span>

-   <span data-ttu-id="9a525-105">字元輸入。</span><span class="sxs-lookup"><span data-stu-id="9a525-105">Character input.</span></span> <span data-ttu-id="9a525-106">使用者在檔或編輯方塊中輸入的文字。</span><span class="sxs-lookup"><span data-stu-id="9a525-106">Text that the user types into a document or edit box.</span></span>
-   <span data-ttu-id="9a525-107">鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="9a525-107">Keyboard shortcuts.</span></span> <span data-ttu-id="9a525-108">叫用應用程式函式的按鍵筆觸;例如，CTRL + O 表示開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="9a525-108">Key strokes that invoke application functions; for example, CTRL + O to open a file.</span></span>
-   <span data-ttu-id="9a525-109">系統命令。</span><span class="sxs-lookup"><span data-stu-id="9a525-109">System commands.</span></span> <span data-ttu-id="9a525-110">叫用系統函數的按鍵筆觸;例如，ALT + TAB 可以切換視窗。</span><span class="sxs-lookup"><span data-stu-id="9a525-110">Key strokes that invoke system functions; for example, ALT + TAB to switch windows.</span></span>

<span data-ttu-id="9a525-111">考慮鍵盤輸入時，請務必記住，按鍵筆劃與字元不同。</span><span class="sxs-lookup"><span data-stu-id="9a525-111">When thinking about keyboard input, it is important to remember that a key stroke is not the same as a character.</span></span> <span data-ttu-id="9a525-112">例如，按下按鍵可能會產生下列任何字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-112">For example, pressing the A key could result in any of the following characters.</span></span>

-   <span data-ttu-id="9a525-113">a</span><span class="sxs-lookup"><span data-stu-id="9a525-113">a</span></span>
-   <span data-ttu-id="9a525-114">A</span><span class="sxs-lookup"><span data-stu-id="9a525-114">A</span></span>
-   <span data-ttu-id="9a525-115">× (鍵盤是否支援合併字元符號) </span><span class="sxs-lookup"><span data-stu-id="9a525-115">á (if the keyboard supports combining diacritics)</span></span>

<span data-ttu-id="9a525-116">此外，如果按住 ALT 鍵，則按下鍵會產生 ALT + A，而系統完全不會將它視為一個字元，而是系統命令。</span><span class="sxs-lookup"><span data-stu-id="9a525-116">Further, if the ALT key is held down, pressing the A key produces ALT+A, which the system does not treat as a character at all, but rather as a system command.</span></span>

## <a name="key-codes"></a><span data-ttu-id="9a525-117">金鑰碼</span><span class="sxs-lookup"><span data-stu-id="9a525-117">Key Codes</span></span>

<span data-ttu-id="9a525-118">當您按下按鍵時，硬體會產生 *掃描程式碼*。</span><span class="sxs-lookup"><span data-stu-id="9a525-118">When you press a key, the hardware generates a *scan code*.</span></span> <span data-ttu-id="9a525-119">掃描程式碼會依下一個鍵盤而有所不同，而且有個別的掃描碼可用於按鍵和關鍵事件。</span><span class="sxs-lookup"><span data-stu-id="9a525-119">Scan codes vary from one keyboard to the next, and there are separate scan codes for key-up and key-down events.</span></span> <span data-ttu-id="9a525-120">您幾乎不會在意掃描代碼。</span><span class="sxs-lookup"><span data-stu-id="9a525-120">You will almost never care about scan codes.</span></span> <span data-ttu-id="9a525-121">鍵盤驅動程式會將掃描碼轉譯為 *虛擬金鑰代碼*。</span><span class="sxs-lookup"><span data-stu-id="9a525-121">The keyboard driver translates scan codes into *virtual-key codes*.</span></span> <span data-ttu-id="9a525-122">虛擬金鑰碼與裝置無關。</span><span class="sxs-lookup"><span data-stu-id="9a525-122">Virtual-key codes are device-independent.</span></span> <span data-ttu-id="9a525-123">在任何鍵盤上按下按鍵會產生相同的虛擬按鍵程式碼。</span><span class="sxs-lookup"><span data-stu-id="9a525-123">Pressing the A key on any keyboard generates the same virtual-key code.</span></span>

<span data-ttu-id="9a525-124">一般而言，虛擬機器碼不會對應到 ASCII 碼或任何其他字元編碼標準。</span><span class="sxs-lookup"><span data-stu-id="9a525-124">In general, virtual-key codes do not correspond to ASCII codes or any other character-encoding standard.</span></span> <span data-ttu-id="9a525-125">如果您想要的話，這是很明顯的，因為相同的索引鍵可以產生不同的字元 (a、×) ，而某些按鍵（例如函式索引鍵）不會對應到任何字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-125">This is obvious if you think about it, because the same key can generate different characters (a, A, á), and some keys, such as function keys, do not correspond to any character.</span></span>

<span data-ttu-id="9a525-126">也就是說，下列虛擬機器碼會對應到 ASCII 對等專案：</span><span class="sxs-lookup"><span data-stu-id="9a525-126">That said, the following virtual-key codes do map to ASCII equivalents:</span></span>

-   <span data-ttu-id="9a525-127">0到9個索引鍵 = ASCII ' 0 ' – ' 9 ' (0x30< – 0x39) </span><span class="sxs-lookup"><span data-stu-id="9a525-127">0 through 9 keys = ASCII '0' – '9' (0x30 – 0x39)</span></span>
-   <span data-ttu-id="9a525-128">A 到 Z 的按鍵 = ASCII ' A ' – ' Z ' (0x41 向– 0x5A) </span><span class="sxs-lookup"><span data-stu-id="9a525-128">A through Z keys = ASCII 'A' – 'Z' (0x41 – 0x5A)</span></span>

<span data-ttu-id="9a525-129">在某些方面，這個對應很不幸，因為您絕對不應該將虛擬金鑰碼視為字元，因為這是討論的原因。</span><span class="sxs-lookup"><span data-stu-id="9a525-129">In some respects this mapping is unfortunate, because you should never think of virtual-key codes as characters, for the reasons discussed.</span></span>

<span data-ttu-id="9a525-130">標頭檔 WinUser 會定義大部分虛擬金鑰程式碼的常數。</span><span class="sxs-lookup"><span data-stu-id="9a525-130">The header file WinUser.h defines constants for most of the virtual-key codes.</span></span> <span data-ttu-id="9a525-131">例如，向左箭號鍵的虛擬按鍵程式碼會 **VK \_ left** (0x25) 。</span><span class="sxs-lookup"><span data-stu-id="9a525-131">For example, the virtual-key code for the LEFT ARROW key is **VK\_LEFT** (0x25).</span></span> <span data-ttu-id="9a525-132">如需完整的虛擬金鑰程式代碼清單，請參閱虛擬機器碼 [**程式碼**](/windows/desktop/inputdev/virtual-key-codes)。</span><span class="sxs-lookup"><span data-stu-id="9a525-132">For the complete list of virtual-key codes, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="9a525-133">不會針對符合 ASCII 值的虛擬金鑰碼定義常數。</span><span class="sxs-lookup"><span data-stu-id="9a525-133">No constants are defined for the virtual-key codes that match ASCII values.</span></span> <span data-ttu-id="9a525-134">例如，索引鍵的虛擬金鑰程式碼為0x41 向，但沒有名為 **VK \_ 的** 常數。</span><span class="sxs-lookup"><span data-stu-id="9a525-134">For example, the virtual-key code for the A key is 0x41, but there is no constant named **VK\_A**.</span></span> <span data-ttu-id="9a525-135">相反地，只使用數值。</span><span class="sxs-lookup"><span data-stu-id="9a525-135">Instead, just use the numeric value.</span></span>

## <a name="key-down-and-key-up-messages"></a><span data-ttu-id="9a525-136">Key-Down 和 Key-Up 訊息</span><span class="sxs-lookup"><span data-stu-id="9a525-136">Key-Down and Key-Up Messages</span></span>

<span data-ttu-id="9a525-137">當您按下按鍵時，具有鍵盤焦點的視窗就會收到下列其中一則訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-137">When you press a key, the window that has keyboard focus receives one of the following messages.</span></span>

-   [<span data-ttu-id="9a525-138">**WM \_ SYSKEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="9a525-138">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
-   [<span data-ttu-id="9a525-139">**WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="9a525-139">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)

<span data-ttu-id="9a525-140">[**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)訊息表示 *系統金鑰*，也就是叫用系統命令的按鍵筆觸。</span><span class="sxs-lookup"><span data-stu-id="9a525-140">The [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message indicates a *system key*, which is a key stroke that invokes a system command.</span></span> <span data-ttu-id="9a525-141">系統金鑰有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="9a525-141">There are two types of system key:</span></span>

-   <span data-ttu-id="9a525-142">ALT + 任何按鍵</span><span class="sxs-lookup"><span data-stu-id="9a525-142">ALT + any key</span></span>
-   <span data-ttu-id="9a525-143">F10</span><span class="sxs-lookup"><span data-stu-id="9a525-143">F10</span></span>

<span data-ttu-id="9a525-144">F10 鍵會啟用視窗的功能表列。</span><span class="sxs-lookup"><span data-stu-id="9a525-144">The F10 key activates the menu bar of a window.</span></span> <span data-ttu-id="9a525-145">不同的 ALT 鍵組合會叫用系統命令。</span><span class="sxs-lookup"><span data-stu-id="9a525-145">Various ALT-key combinations invoke system commands.</span></span> <span data-ttu-id="9a525-146">例如，ALT + TAB 會切換至新的視窗。</span><span class="sxs-lookup"><span data-stu-id="9a525-146">For example, ALT + TAB switches to a new window.</span></span> <span data-ttu-id="9a525-147">此外，如果視窗有功能表，則可以使用 ALT 鍵來啟動功能表項目。</span><span class="sxs-lookup"><span data-stu-id="9a525-147">In addition, if a window has a menu, the ALT key can be used to activate menu items.</span></span> <span data-ttu-id="9a525-148">某些 ALT 按鍵組合不會進行任何動作。</span><span class="sxs-lookup"><span data-stu-id="9a525-148">Some ALT key combinations do not do anything.</span></span>

<span data-ttu-id="9a525-149">所有其他的按鍵筆劃會被視為非系統金鑰，並產生 [**WM 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-149">All other key strokes are considered nonsystem keys and produce the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span> <span data-ttu-id="9a525-150">這包括 F10 以外的函式索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9a525-150">This includes the function keys other than F10.</span></span>

<span data-ttu-id="9a525-151">當您釋放金鑰時，系統會傳送對應的索引鍵訊息：</span><span class="sxs-lookup"><span data-stu-id="9a525-151">When you release a key, the system sends a corresponding key-up message:</span></span>

-   [<span data-ttu-id="9a525-152">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="9a525-152">**WM\_KEYUP**</span></span>](/windows/desktop/inputdev/wm-keyup)
-   [<span data-ttu-id="9a525-153">**WM \_ SYSKEYUP**</span><span class="sxs-lookup"><span data-stu-id="9a525-153">**WM\_SYSKEYUP**</span></span>](/windows/desktop/inputdev/wm-syskeyup)

<span data-ttu-id="9a525-154">如果您將按鍵的時間夠長，以啟動鍵盤的重複功能，系統會傳送多個關鍵的訊息，後面接著單一的按鍵訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-154">If you hold down a key long enough to start the keyboard's repeat feature, the system sends multiple key-down messages, followed by a single key-up message.</span></span>

<span data-ttu-id="9a525-155">在截至目前為止所討論的四個鍵盤訊息中， *wParam* 參數包含金鑰的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="9a525-155">In all four of the keyboard messages discussed so far, the *wParam* parameter contains the virtual-key code of the key.</span></span> <span data-ttu-id="9a525-156">*LParam* 參數包含封裝成32位的一些其他資訊。</span><span class="sxs-lookup"><span data-stu-id="9a525-156">The *lParam* parameter contains some miscellaneous information packed into 32 bits.</span></span> <span data-ttu-id="9a525-157">您通常不需要 *lParam* 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="9a525-157">You typically do not need the information in *lParam*.</span></span> <span data-ttu-id="9a525-158">有一個可能有用的旗標是 bit 30，也就是「先前的金鑰狀態」旗標，它會設定為1，以重複的索引鍵關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-158">One flag that might be useful is bit 30, the "previous key state" flag, which is set to 1 for repeated key-down messages.</span></span>

<span data-ttu-id="9a525-159">顧名思義，系統金鑰筆劃主要是供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="9a525-159">As the name implies, system key strokes are primarily intended for use by the operating system.</span></span> <span data-ttu-id="9a525-160">如果您攔截了 [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) 訊息，請在之後呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 。</span><span class="sxs-lookup"><span data-stu-id="9a525-160">If you intercept the [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message, call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afterward.</span></span> <span data-ttu-id="9a525-161">否則，您將會封鎖作業系統來處理命令。</span><span class="sxs-lookup"><span data-stu-id="9a525-161">Otherwise, you will block the operating system from handling the command.</span></span>

## <a name="character-messages"></a><span data-ttu-id="9a525-162">字元訊息</span><span class="sxs-lookup"><span data-stu-id="9a525-162">Character Messages</span></span>

<span data-ttu-id="9a525-163">[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式會將按鍵筆劃轉換成字元，我們會先在 [課程模組 1](your-first-windows-program.md)中看到此功能。</span><span class="sxs-lookup"><span data-stu-id="9a525-163">Key strokes are converted into characters by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function, which we first saw in [Module 1](your-first-windows-program.md).</span></span> <span data-ttu-id="9a525-164">此函式會檢查索引鍵下的訊息，並將其轉譯為字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-164">This function examines key-down messages and translates them into characters.</span></span> <span data-ttu-id="9a525-165">**TranslateMessage** 函式會針對每個產生的字元，將 [**Wm \_ CHAR**](/windows/desktop/inputdev/wm-char)或 [**wm \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)訊息放在視窗的訊息佇列上。</span><span class="sxs-lookup"><span data-stu-id="9a525-165">For each character that is produced, the **TranslateMessage** function puts a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) or [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message on the message queue of the window.</span></span> <span data-ttu-id="9a525-166">訊息的 *wParam* 參數包含 utf-16 字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-166">The *wParam* parameter of the message contains the UTF-16 character.</span></span>

<span data-ttu-id="9a525-167">您可能會猜到，wm 的 [**\_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息是從 [**wm 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息產生，而 [**wm \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) 訊息是從 [**wm \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) 訊息產生的。</span><span class="sxs-lookup"><span data-stu-id="9a525-167">As you might guess, [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages are generated from [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, while [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) messages are generated from [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) messages.</span></span> <span data-ttu-id="9a525-168">例如，假設使用者按下 SHIFT 鍵，然後按下鍵。</span><span class="sxs-lookup"><span data-stu-id="9a525-168">For example, suppose the user presses the SHIFT key followed by the A key.</span></span> <span data-ttu-id="9a525-169">假設有標準鍵盤佈局，您會收到下列一連串的訊息：</span><span class="sxs-lookup"><span data-stu-id="9a525-169">Assuming a standard keyboard layout, you would get the following sequence of messages:</span></span>

<span data-ttu-id="9a525-170">**WM \_KEYDOWN**： SHIFT</span><span class="sxs-lookup"><span data-stu-id="9a525-170">**WM\_KEYDOWN**: SHIFT</span></span>  
<span data-ttu-id="9a525-171">**WM \_KEYDOWN**： A</span><span class="sxs-lookup"><span data-stu-id="9a525-171">**WM\_KEYDOWN**: A</span></span>  
<span data-ttu-id="9a525-172">**WM \_CHAR**： ' A '</span><span class="sxs-lookup"><span data-stu-id="9a525-172">**WM\_CHAR**: 'A'</span></span>  


<span data-ttu-id="9a525-173">另一方面，ALT + P 的組合會產生：</span><span class="sxs-lookup"><span data-stu-id="9a525-173">On the other hand, the combination ALT + P would generate:</span></span>

 <span data-ttu-id="9a525-174">**WM \_SYSKEYDOWN**： VK \_ 功能表</span><span class="sxs-lookup"><span data-stu-id="9a525-174">**WM\_SYSKEYDOWN**: VK\_MENU</span></span>  
<span data-ttu-id="9a525-175">**WM \_SYSKEYDOWN**：0x50</span><span class="sxs-lookup"><span data-stu-id="9a525-175">**WM\_SYSKEYDOWN**: 0x50</span></span>  
<span data-ttu-id="9a525-176">**WM \_SYSCHAR**： ' p '</span><span class="sxs-lookup"><span data-stu-id="9a525-176">**WM\_SYSCHAR**: 'p'</span></span>  
<span data-ttu-id="9a525-177">**WM \_SYSKEYUP**：0x50</span><span class="sxs-lookup"><span data-stu-id="9a525-177">**WM\_SYSKEYUP**: 0x50</span></span>  
<span data-ttu-id="9a525-178">**WM \_KEYUP**： VK \_ 功能表</span><span class="sxs-lookup"><span data-stu-id="9a525-178">**WM\_KEYUP**: VK\_MENU</span></span>  


<span data-ttu-id="9a525-179">基於歷史原因， (ALT 鍵的虛擬按鍵程式碼名稱為 VK \_ 功能表。 ) </span><span class="sxs-lookup"><span data-stu-id="9a525-179">(The virtual-key code for the ALT key is named VK\_MENU for historical reasons.)</span></span>

<span data-ttu-id="9a525-180">[**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)訊息表示系統字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-180">The [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message indicates a system character.</span></span> <span data-ttu-id="9a525-181">如同使用 [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)，您通常應該將此訊息直接傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="9a525-181">As with [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), you should generally pass this message directly to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="9a525-182">否則，您可能會干擾標準系統命令。</span><span class="sxs-lookup"><span data-stu-id="9a525-182">Otherwise, you may interfere with standard system commands.</span></span> <span data-ttu-id="9a525-183">尤其是，請勿將 **WM \_ SYSCHAR** 視為使用者所輸入的文字。</span><span class="sxs-lookup"><span data-stu-id="9a525-183">In particular, do not treat **WM\_SYSCHAR** as text that the user has typed.</span></span>

<span data-ttu-id="9a525-184">您通常會將 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息視為字元輸入。</span><span class="sxs-lookup"><span data-stu-id="9a525-184">The [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message is what you normally think of as character input.</span></span> <span data-ttu-id="9a525-185">字元的資料類型為 **wchar \_ t**，代表 utf-16 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-185">The data type for the character is **wchar\_t**, representing a UTF-16 Unicode character.</span></span> <span data-ttu-id="9a525-186">字元輸入可以包含 ASCII 範圍以外的字元，尤其是在美國以外的鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="9a525-186">Character input can include characters outside the ASCII range, especially with keyboard layouts that are commonly used outside of the United States.</span></span> <span data-ttu-id="9a525-187">您可以使用 [螢幕小鍵盤] 功能來安裝區域鍵盤，以嘗試不同的鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="9a525-187">You can try different keyboard layouts by installing a regional keyboard and then using the On-Screen Keyboard feature.</span></span>

<span data-ttu-id="9a525-188">使用者也可以使用標準鍵盤， (IME) 輸入複雜的腳本（例如日文字元），以安裝輸入方法編輯器。</span><span class="sxs-lookup"><span data-stu-id="9a525-188">Users can also install an Input Method Editor (IME) to enter complex scripts, such as Japanese characters, with a standard keyboard.</span></span> <span data-ttu-id="9a525-189">例如，使用日文 IME 輸入片假名字元カ (ka) ，您可能會收到下列訊息：</span><span class="sxs-lookup"><span data-stu-id="9a525-189">For example, using a Japanese IME to enter the katakana character カ (ka), you might get the following messages:</span></span>

<span data-ttu-id="9a525-190">**WM \_KEYDOWN**： VK \_ PROCESSKEY (IME 處理按鍵) </span><span class="sxs-lookup"><span data-stu-id="9a525-190">**WM\_KEYDOWN**: VK\_PROCESSKEY (the IME PROCESS key)</span></span>  
<span data-ttu-id="9a525-191">**WM \_KEYUP**：0x4B</span><span class="sxs-lookup"><span data-stu-id="9a525-191">**WM\_KEYUP**: 0x4B</span></span>  
<span data-ttu-id="9a525-192">**WM \_KEYDOWN**： VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="9a525-192">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="9a525-193">**WM \_KEYUP**：0x41 向</span><span class="sxs-lookup"><span data-stu-id="9a525-193">**WM\_KEYUP**: 0x41</span></span>  
<span data-ttu-id="9a525-194">**WM \_KEYDOWN**： VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="9a525-194">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="9a525-195">**WM \_CHAR**：カ</span><span class="sxs-lookup"><span data-stu-id="9a525-195">**WM\_CHAR**: カ</span></span>  
<span data-ttu-id="9a525-196">**WM \_KEYUP**： VK \_ RETURN</span><span class="sxs-lookup"><span data-stu-id="9a525-196">**WM\_KEYUP**: VK\_RETURN</span></span>  


<span data-ttu-id="9a525-197">有些 CTRL 按鍵組合會轉譯成 ASCII 控制字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-197">Some CTRL key combinations are translated into ASCII control characters.</span></span> <span data-ttu-id="9a525-198">例如，CTRL + A 會轉譯成 ASCII CTRL-A (SOH) 字元 (ASCII 值 0x01) 。</span><span class="sxs-lookup"><span data-stu-id="9a525-198">For example, CTRL+A is translated to the ASCII ctrl-A (SOH) character (ASCII value 0x01).</span></span> <span data-ttu-id="9a525-199">針對文字輸入，您通常應該篩選出控制字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-199">For text input, you should generally filter out the control characters.</span></span> <span data-ttu-id="9a525-200">此外，請避免使用 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 來執行鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="9a525-200">Also, avoid using [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) to implement keyboard shortcuts.</span></span> <span data-ttu-id="9a525-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span><span class="sxs-lookup"><span data-stu-id="9a525-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span></span> <span data-ttu-id="9a525-202">快速鍵對應表將在下一個主題（ [快速鍵對應表](accelerator-tables.md)）中描述。</span><span class="sxs-lookup"><span data-stu-id="9a525-202">Accelerator tables are described in the next topic, [Accelerator Tables](accelerator-tables.md).</span></span>

<span data-ttu-id="9a525-203">下列程式碼會在偵錯工具中顯示主要鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-203">The following code displays the main keyboard messages in the debugger.</span></span> <span data-ttu-id="9a525-204">請嘗試使用不同的按鍵組合來播放，並查看所產生的訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-204">Try playing with different keystroke combinations and see what messages are generated.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a><span data-ttu-id="9a525-205">其他鍵盤訊息</span><span class="sxs-lookup"><span data-stu-id="9a525-205">Miscellaneous Keyboard Messages</span></span>

<span data-ttu-id="9a525-206">大部分的應用程式都可以安全地忽略一些其他的鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-206">Some other keyboard messages can safely be ignored by most applications.</span></span>

-   <span data-ttu-id="9a525-207">會針對組合索引鍵傳送 [**WM \_ DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) 訊息，例如「變音符號」。</span><span class="sxs-lookup"><span data-stu-id="9a525-207">The [**WM\_DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) message is sent for a combining key, such as a diacritic.</span></span> <span data-ttu-id="9a525-208">例如，在西班牙文語言鍵盤上，輸入輔符號 ( ' ) 後面接著 E 會產生日字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-208">For example, on a Spanish language keyboard, typing accent (') followed by E produces the character é.</span></span> <span data-ttu-id="9a525-209">會為輔色字元傳送 **WM \_ DEADCHAR** 。</span><span class="sxs-lookup"><span data-stu-id="9a525-209">The **WM\_DEADCHAR** is sent for the accent character.</span></span>
-   <span data-ttu-id="9a525-210">[**WM \_ 則 unichar 會**](/windows/desktop/inputdev/wm-unichar)訊息已過時。</span><span class="sxs-lookup"><span data-stu-id="9a525-210">The [**WM\_UNICHAR**](/windows/desktop/inputdev/wm-unichar) message is obsolete.</span></span> <span data-ttu-id="9a525-211">它可讓 ANSI 程式接收 Unicode 字元輸入。</span><span class="sxs-lookup"><span data-stu-id="9a525-211">It enables ANSI programs to receive Unicode character input.</span></span>
-   <span data-ttu-id="9a525-212">當 IME 將按鍵順序轉譯為字元時，會傳送 [**WM \_ ime \_**](/windows/desktop/Intl/wm-ime-char) 字元字元。</span><span class="sxs-lookup"><span data-stu-id="9a525-212">The [**WM\_IME\_CHAR**](/windows/desktop/Intl/wm-ime-char) character is sent when an IME translates a keystroke sequence into characters.</span></span> <span data-ttu-id="9a525-213">除了一般的 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息之外，還會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9a525-213">It is sent in addition to the usual [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>

## <a name="keyboard-state"></a><span data-ttu-id="9a525-214">鍵盤狀態</span><span class="sxs-lookup"><span data-stu-id="9a525-214">Keyboard State</span></span>

<span data-ttu-id="9a525-215">鍵盤訊息是由事件驅動。</span><span class="sxs-lookup"><span data-stu-id="9a525-215">The keyboard messages are event-driven.</span></span> <span data-ttu-id="9a525-216">也就是說，當發生有趣的問題（例如按鍵）時，您會收到訊息，而訊息會告訴您發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="9a525-216">That is, you get a message when something interesting happens, such as a key press, and the message tells you what just happened.</span></span> <span data-ttu-id="9a525-217">但是，您也可以藉由呼叫 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 函式，隨時測試索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="9a525-217">But you can also test the state of a key at any time, by calling the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function.</span></span>

<span data-ttu-id="9a525-218">例如，請考慮您要如何偵測滑鼠左鍵按一下 + ALT 鍵的組合。</span><span class="sxs-lookup"><span data-stu-id="9a525-218">For example, consider how would you detect the combination of left mouse click + ALT key.</span></span> <span data-ttu-id="9a525-219">您可以藉由接聽按鍵筆劃訊息和儲存旗標來追蹤 ALT 鍵的狀態，但 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 可節省您的麻煩。</span><span class="sxs-lookup"><span data-stu-id="9a525-219">You could track the state of the ALT key by listening for key-stroke messages and storing a flag, but [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) saves you the trouble.</span></span> <span data-ttu-id="9a525-220">當您收到 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息時，只要呼叫 **GetKeyState** ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9a525-220">When you receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, just call **GetKeyState** as follows:</span></span>


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



<span data-ttu-id="9a525-221">[**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate)訊息會採用虛擬金鑰程式碼作為輸入，並傳回一組位旗標， (實際上只有兩個旗標) 。</span><span class="sxs-lookup"><span data-stu-id="9a525-221">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) message takes a virtual-key code as input and returns a set of bit flags (actually just two flags).</span></span> <span data-ttu-id="9a525-222">0x8000 值包含位旗標，可測試是否目前已按下金鑰。</span><span class="sxs-lookup"><span data-stu-id="9a525-222">The value 0x8000 contains the bit flag that tests whether the key is currently pressed.</span></span>

<span data-ttu-id="9a525-223">大部分鍵盤都有兩個 ALT 鍵：左邊和右邊。</span><span class="sxs-lookup"><span data-stu-id="9a525-223">Most keyboards have two ALT keys, left and right.</span></span> <span data-ttu-id="9a525-224">上述範例會測試是否已按下其中一個。</span><span class="sxs-lookup"><span data-stu-id="9a525-224">The previous example tests whether either of them of pressed.</span></span> <span data-ttu-id="9a525-225">您也可以使用 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 來區分 ALT、SHIFT 或 CTRL 鍵的左和右實例。</span><span class="sxs-lookup"><span data-stu-id="9a525-225">You can also use [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) to distinguish between the left and right instances of the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="9a525-226">例如，下列程式碼會測試是否按下右邊的 ALT 鍵。</span><span class="sxs-lookup"><span data-stu-id="9a525-226">For example, the following code tests if the right ALT key is pressed.</span></span>


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



<span data-ttu-id="9a525-227">[**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate)函數很有趣，因為它會報告 *虛擬* 鍵盤狀態。</span><span class="sxs-lookup"><span data-stu-id="9a525-227">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function is interesting because it reports a *virtual* keyboard state.</span></span> <span data-ttu-id="9a525-228">此虛擬狀態是以訊息佇列的內容為基礎，當您從佇列中移除訊息時就會更新。</span><span class="sxs-lookup"><span data-stu-id="9a525-228">This virtual state is based on the contents of your message queue, and gets updated as you remove messages from the queue.</span></span> <span data-ttu-id="9a525-229">當您的程式處理視窗訊息時， **GetKeyState** 會在每個訊息排入佇列時，提供鍵盤的快照。</span><span class="sxs-lookup"><span data-stu-id="9a525-229">As your program processes window messages, **GetKeyState** gives you a snapshot of the keyboard at the time that each message was queued.</span></span> <span data-ttu-id="9a525-230">例如，如果佇列上的最後一個訊息是 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)， **GetKeyState** 就會在使用者按下滑鼠按鍵時報告鍵盤狀態。</span><span class="sxs-lookup"><span data-stu-id="9a525-230">For example, if the last message on the queue was [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** reports the keyboard state at the moment when the user clicked the mouse button.</span></span>

<span data-ttu-id="9a525-231">因為 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 是以您的訊息佇列為基礎，所以它也會忽略傳送至另一個程式的鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="9a525-231">Because [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) is based on your message queue, it also ignores keyboard input that was sent to another program.</span></span> <span data-ttu-id="9a525-232">如果使用者切換到其他程式， **GetKeyState** 會忽略傳送至該程式的任何按鍵動作。</span><span class="sxs-lookup"><span data-stu-id="9a525-232">If the user switches to another program, any key presses that are sent to that program are ignored by **GetKeyState**.</span></span> <span data-ttu-id="9a525-233">如果您真的想要知道鍵盤的立即實體狀態，有一個函式可用於： [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)。</span><span class="sxs-lookup"><span data-stu-id="9a525-233">If you really want to know the immediate physical state of the keyboard, there is a function for that: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span> <span data-ttu-id="9a525-234">但是針對大部分的 UI 程式碼，正確的函式是 **GetKeyState**。</span><span class="sxs-lookup"><span data-stu-id="9a525-234">For most UI code, however, the correct function is **GetKeyState**.</span></span>

## <a name="next"></a><span data-ttu-id="9a525-235">下一個</span><span class="sxs-lookup"><span data-stu-id="9a525-235">Next</span></span>

[<span data-ttu-id="9a525-236">快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="9a525-236">Accelerator Tables</span></span>](accelerator-tables.md)

 

 
