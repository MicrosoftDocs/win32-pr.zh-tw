---
title: 在遊戲中使用輸入法編輯器
description: 本文說明如何在全螢幕 Microsoft DirectX 應用程式中，執行基本的 IME 編輯控制項。
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "103946026"
---
# <a name="using-an-input-method-editor-in-a-game"></a><span data-ttu-id="166a3-103">在遊戲中使用輸入法編輯器</span><span class="sxs-lookup"><span data-stu-id="166a3-103">Using an Input Method Editor in a Game</span></span>

> [!Note]  
> <span data-ttu-id="166a3-104">本文詳細說明如何使用 Windows XP 輸入法編輯器 (IME) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-104">This article details working with the Windows XP Input Method Editor (IME).</span></span> <span data-ttu-id="166a3-105">針對 Windows Vista 的 IME 進行了變更，但這篇文章並未完整詳述。</span><span class="sxs-lookup"><span data-stu-id="166a3-105">Changes were made to the IME for Windows Vista that are not fully detailed in this article.</span></span> <span data-ttu-id="166a3-106">如需 Windows Vista 的輸入法變更的詳細資訊，請參閱 Windows Vista 中的 [輸入法編輯器 (ime) ](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) -Microsoft 全球開發和運算入口網站上的 [國際化 Ever-Expanding 視圖](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-106">For more info about changes to the IME for Windows Vista, see [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal.</span></span>

 

<span data-ttu-id="166a3-107">輸入法編輯器 (IME) 是一種程式，可讓您使用標準鍵盤（例如中文、日文、韓文及其他語言的複雜字元）輕鬆地輸入文字。</span><span class="sxs-lookup"><span data-stu-id="166a3-107">An input method editor (IME) is a program that allows easy text entry using a standard keyboard for East Asian languages such as Chinese, Japanese, Korean, and other languages with complex characters.</span></span> <span data-ttu-id="166a3-108">例如，在使用者輸入 Ime 的情況下，使用者可以在文字處理器中輸入複雜字元，或大量多人遊戲線上遊戲的玩家可以用複雜的字元與朋友聊天。</span><span class="sxs-lookup"><span data-stu-id="166a3-108">For example, with IMEs a user can type complex characters in a word processor, or a player of a massive multiplayer online game can chat with friends in complex characters.</span></span>

<span data-ttu-id="166a3-109">本文說明如何在全螢幕 Microsoft DirectX 應用程式中，執行基本的 IME 編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="166a3-109">This article explains how you can implement a basic IME edit control in a full-screen Microsoft DirectX application.</span></span> <span data-ttu-id="166a3-110">利用 DXUT 的應用程式會自動取得輸入法功能。</span><span class="sxs-lookup"><span data-stu-id="166a3-110">Applications that take advantage of DXUT automatically get IME functionality.</span></span> <span data-ttu-id="166a3-111">針對未使用架構的應用程式，本文將說明如何在編輯控制項中新增 IME 支援。</span><span class="sxs-lookup"><span data-stu-id="166a3-111">For applications that do not make use of the framework, this article describes how to add IME support to an edit control.</span></span>

<span data-ttu-id="166a3-112">內容: </span><span class="sxs-lookup"><span data-stu-id="166a3-112">Contents:</span></span>

-   [<span data-ttu-id="166a3-113">預設 IME 行為</span><span class="sxs-lookup"><span data-stu-id="166a3-113">Default IME Behavior</span></span>](#default-ime-behavior)
-   [<span data-ttu-id="166a3-114">搭配使用 Ime 與 DXUT</span><span class="sxs-lookup"><span data-stu-id="166a3-114">Using IMEs with DXUT</span></span>](#using-imes-with-dxut)
-   [<span data-ttu-id="166a3-115">覆寫預設的 IME 行為</span><span class="sxs-lookup"><span data-stu-id="166a3-115">Overriding the Default IME Behavior</span></span>](#overriding-the-default-ime-behavior)
-   [<span data-ttu-id="166a3-116">函數</span><span class="sxs-lookup"><span data-stu-id="166a3-116">Functions</span></span>](#functions)
-   [<span data-ttu-id="166a3-117">訊息</span><span class="sxs-lookup"><span data-stu-id="166a3-117">Messages</span></span>](#ime-messages)
-   [<span data-ttu-id="166a3-118">範例</span><span class="sxs-lookup"><span data-stu-id="166a3-118">Examples</span></span>](#examples)
    -   [<span data-ttu-id="166a3-119">CHT IME 4.2、4.3 和4.4 版</span><span class="sxs-lookup"><span data-stu-id="166a3-119">CHT IME version 4.2, 4.3 and 4.4</span></span>](#cht-ime-version-42-43-and-44)
    -   [<span data-ttu-id="166a3-120">CHT IME 5.0 版</span><span class="sxs-lookup"><span data-stu-id="166a3-120">CHT IME version 5.0</span></span>](#cht-ime-version-50)
    -   [<span data-ttu-id="166a3-121">CHT IME 5.1、5.2 和 CHS IME 版本5。3</span><span class="sxs-lookup"><span data-stu-id="166a3-121">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [<span data-ttu-id="166a3-122">CHS IME 4.1 版</span><span class="sxs-lookup"><span data-stu-id="166a3-122">CHS IME version 4.1</span></span>](#chs-ime-version-41)
    -   [<span data-ttu-id="166a3-123">CHS IME 4.2 版</span><span class="sxs-lookup"><span data-stu-id="166a3-123">CHS IME version 4.2</span></span>](#chs-ime-version-42)
-   [<span data-ttu-id="166a3-124">輸入法訊息</span><span class="sxs-lookup"><span data-stu-id="166a3-124">IME Messages</span></span>](#ime-messages)
    -   [<span data-ttu-id="166a3-125">WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="166a3-125">WM\_INPUTLANGCHANGE</span></span>](#wm_inputlangchange)
    -   [<span data-ttu-id="166a3-126">WM \_ IME \_ STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="166a3-126">WM\_IME\_STARTCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="166a3-127">WM \_ IME \_ 組合</span><span class="sxs-lookup"><span data-stu-id="166a3-127">WM\_IME\_COMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="166a3-128">WM \_ IME \_ ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="166a3-128">WM\_IME\_ENDCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="166a3-129">WM \_ 輸入法 \_ 通知</span><span class="sxs-lookup"><span data-stu-id="166a3-129">WM\_IME\_NOTIFY</span></span>](/windows)
-   [<span data-ttu-id="166a3-130">轉譯</span><span class="sxs-lookup"><span data-stu-id="166a3-130">Rendering</span></span>](#rendering)
    -   [<span data-ttu-id="166a3-131">輸入地區設定指標</span><span class="sxs-lookup"><span data-stu-id="166a3-131">Input Locale Indicator</span></span>](#input-locale-indicator)
    -   [<span data-ttu-id="166a3-132">撰寫視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-132">Composition Window</span></span>](#composition-window)
    -   [<span data-ttu-id="166a3-133">讀取和候選視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-133">Reading and Candidate Windows</span></span>](#reading-and-candidate-windows)
-   [<span data-ttu-id="166a3-134">限制</span><span class="sxs-lookup"><span data-stu-id="166a3-134">Limitations</span></span>](#limitations)
-   [<span data-ttu-id="166a3-135">登錄資訊</span><span class="sxs-lookup"><span data-stu-id="166a3-135">Registry Information</span></span>](#registry-information)
-   [<span data-ttu-id="166a3-136">附錄 A：每個作業系統的 CHT 版本</span><span class="sxs-lookup"><span data-stu-id="166a3-136">Appendix A: CHT Versions per Operating System</span></span>](#appendix-a-cht-versions-per-operating-system)
-   [<span data-ttu-id="166a3-137">詳細資訊</span><span class="sxs-lookup"><span data-stu-id="166a3-137">Further Information</span></span>](#further-information)
-   [<span data-ttu-id="166a3-138">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="166a3-138">GetReadingString</span></span>](#getreadingstring)
-   [<span data-ttu-id="166a3-139">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="166a3-139">ShowReadingWindow</span></span>](#showreadingwindow)

## <a name="default-ime-behavior"></a><span data-ttu-id="166a3-140">預設 IME 行為</span><span class="sxs-lookup"><span data-stu-id="166a3-140">Default IME Behavior</span></span>

<span data-ttu-id="166a3-141">Ime 會將鍵盤輸入對應至所選語言特定的語音元件或其他語言元素。</span><span class="sxs-lookup"><span data-stu-id="166a3-141">IMEs map keyboard input to phonetic components or other language elements specific to a selected language.</span></span> <span data-ttu-id="166a3-142">在一般案例中，使用者會輸入代表複雜字元發音的按鍵。</span><span class="sxs-lookup"><span data-stu-id="166a3-142">In a typical scenario, the user types keys that represent pronunciation of a complex character.</span></span> <span data-ttu-id="166a3-143">如果 IME 將發音辨識為有效，則會向使用者顯示一份單字或片語候選人清單，讓使用者可以從中選取最後的選項。</span><span class="sxs-lookup"><span data-stu-id="166a3-143">If the IME recognizes the pronunciation as valid, it presents the user with a list of word or phrase candidates from which the user can select a final choice.</span></span> <span data-ttu-id="166a3-144">選擇的單字接著會透過一系列 Microsoft Windows [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-144">The chosen word is then sent to the application through a series of Microsoft Windows [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span> <span data-ttu-id="166a3-145">因為 IME 會在應用程式下方的某個層級上運作，藉由攔截鍵盤輸入，因此，IME 是否存在於應用程式中是透明的。</span><span class="sxs-lookup"><span data-stu-id="166a3-145">Because the IME works at a level below the application by intercepting keyboard input, the presence of an IME is transparent to the application.</span></span> <span data-ttu-id="166a3-146">幾乎所有 Windows 應用程式都可以立即利用 Ime，而不需要知道它們是否存在，也不需要特殊的編碼。</span><span class="sxs-lookup"><span data-stu-id="166a3-146">Almost all Windows applications can readily take advantage of IMEs without being aware of their existence and without requiring special coding.</span></span>

<span data-ttu-id="166a3-147">一般的 IME 會顯示數個視窗，以引導使用者完成字元輸入，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="166a3-147">A typical IME displays several windows to guide the user through character entry, as shown in the following examples.</span></span>

![ime 會顯示數個視窗](images/ime-elements.png)

| <span data-ttu-id="166a3-149">視窗類型</span><span class="sxs-lookup"><span data-stu-id="166a3-149">Window Type</span></span>                                       | <span data-ttu-id="166a3-150">Description</span><span class="sxs-lookup"><span data-stu-id="166a3-150">Description</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="166a3-151">IME 輸出</span><span class="sxs-lookup"><span data-stu-id="166a3-151">IME Output</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="166a3-152">A.</span><span class="sxs-lookup"><span data-stu-id="166a3-152">A.</span></span> <span data-ttu-id="166a3-153">讀取視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-153">Reading Window</span></span>                                 | <span data-ttu-id="166a3-154">包含鍵盤的按鍵;通常會在每次擊鍵之後變更。</span><span class="sxs-lookup"><span data-stu-id="166a3-154">Contains keystrokes from the keyboard; typically changes after each keystroke.</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="166a3-155">讀取字串</span><span class="sxs-lookup"><span data-stu-id="166a3-155">reading string</span></span>                               |
| <span data-ttu-id="166a3-156">B.</span><span class="sxs-lookup"><span data-stu-id="166a3-156">B.</span></span> <span data-ttu-id="166a3-157">撰寫視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-157">Composition Window</span></span>                             | <span data-ttu-id="166a3-158">包含使用者使用 IME 所撰寫的字元集合。</span><span class="sxs-lookup"><span data-stu-id="166a3-158">Contains the collection of characters that the user has composed with the IME.</span></span> <span data-ttu-id="166a3-159">這些字元是由應用程式頂端的 IME 所繪製。</span><span class="sxs-lookup"><span data-stu-id="166a3-159">These characters are drawn by the IME on top of the application.</span></span> <span data-ttu-id="166a3-160">當使用者將組合字元串通知給 IME 時，IME 接著會透過一系列的 WM 字元訊息，將撰寫字串傳送給應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="166a3-160">When the user notifies the IME that the composition string is satisfactory, the IME then sends the composition string to the application via a series of WM\_CHAR messages.</span></span> | <span data-ttu-id="166a3-161">組合字元串</span><span class="sxs-lookup"><span data-stu-id="166a3-161">composition string</span></span>                           |
| <span data-ttu-id="166a3-162">C.</span><span class="sxs-lookup"><span data-stu-id="166a3-162">C.</span></span> <span data-ttu-id="166a3-163">候選視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-163">Candidate Window</span></span>                               | <span data-ttu-id="166a3-164">當使用者輸入有效的發音時，IME 會顯示所有符合指定發音的候選字元清單。</span><span class="sxs-lookup"><span data-stu-id="166a3-164">When the user has entered a valid pronunciation, the IME displays a list of candidate characters that all match the given pronunciation.</span></span> <span data-ttu-id="166a3-165">然後，使用者從這份清單中選取想要的字元，並將此字元加入至組合視窗顯示中。</span><span class="sxs-lookup"><span data-stu-id="166a3-165">The user then selects the intended character from this list, and the IME adds this character to the Composition Window display.</span></span>                                                    | <span data-ttu-id="166a3-166">組合字元串中的下一個字元</span><span class="sxs-lookup"><span data-stu-id="166a3-166">the next character in the composition string</span></span> |
| <span data-ttu-id="166a3-167">D.</span><span class="sxs-lookup"><span data-stu-id="166a3-167">D.</span></span> <span data-ttu-id="166a3-168">[輸入地區](/windows/desktop/Intl/nls-terminology) 設定指標</span><span class="sxs-lookup"><span data-stu-id="166a3-168">[Input Locale](/windows/desktop/Intl/nls-terminology) indicator</span></span> | <span data-ttu-id="166a3-169">顯示使用者為鍵盤輸入選取的語言。</span><span class="sxs-lookup"><span data-stu-id="166a3-169">Shows the language the user has selected for keyboard input.</span></span> <span data-ttu-id="166a3-170">此指標內嵌于 Windows 工作列中。</span><span class="sxs-lookup"><span data-stu-id="166a3-170">This indicator is embedded in the Windows taskbar.</span></span> <span data-ttu-id="166a3-171">開啟 [地區及語言選項] 主控台然後按一下 [語言] 索引標籤上的 [詳細資料]，即可選取輸入語言。</span><span class="sxs-lookup"><span data-stu-id="166a3-171">The input language can be selected by opening the Regional and Language Options Control Panel and then clicking Details on the Languages tab.</span></span>                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a><span data-ttu-id="166a3-172">搭配使用 Ime 與 DXUT</span><span class="sxs-lookup"><span data-stu-id="166a3-172">Using IMEs with DXUT</span></span>

<span data-ttu-id="166a3-173">在 DXUT 中，CDXUTIMEEditBox 類別會實作為 IME 功能。</span><span class="sxs-lookup"><span data-stu-id="166a3-173">In DXUT, the CDXUTIMEEditBox class implements IME functionality.</span></span> <span data-ttu-id="166a3-174">這個類別衍生自 CDXUTEditBox 類別，此為架構所提供的基本編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="166a3-174">This class is derived from the CDXUTEditBox class, the basic edit control provided by the framework.</span></span> <span data-ttu-id="166a3-175">CDXUTIMEEditBox 會藉由覆寫 CDXUTIMEEditBox 方法，擴充該編輯控制項以支援 Ime。</span><span class="sxs-lookup"><span data-stu-id="166a3-175">CDXUTIMEEditBox extends that edit control to support IMEs by overriding the CDXUTIMEEditBox methods.</span></span> <span data-ttu-id="166a3-176">這些類別是以這種方式設計，可協助開發人員瞭解他們需要從架構中取得的內容，以在自己的編輯控制項中執行 IME 支援。</span><span class="sxs-lookup"><span data-stu-id="166a3-176">The classes are designed this way to help developers learn what they need to take from the framework to implement IME support in their own edit controls.</span></span> <span data-ttu-id="166a3-177">本主題的其餘部分將說明架構和 CDXUTIMEEditBox 如何覆寫基本編輯控制項以執行 IME 功能。</span><span class="sxs-lookup"><span data-stu-id="166a3-177">The rest of this topic explains how the framework, and CDXUTIMEEditBox in particular, overrides a basic edit control to implement IME functionality.</span></span>

<span data-ttu-id="166a3-178">CDXUTIMEEditBox 中大部分的輸入法特定變數都會宣告為靜態，因為許多輸入的緩衝區和狀態都是進程特有的。</span><span class="sxs-lookup"><span data-stu-id="166a3-178">Most of the IME-specific variables in CDXUTIMEEditBox are declared as static, because many IME buffers and states are specific to the process.</span></span> <span data-ttu-id="166a3-179">比方說，進程的組合字元串只有一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="166a3-179">For instance, a process has only one buffer for the composition string.</span></span> <span data-ttu-id="166a3-180">即使進程有十個編輯控制項，它們全都會共用相同的組合字元串緩衝區。</span><span class="sxs-lookup"><span data-stu-id="166a3-180">Even if the process has ten edit controls, they will all be sharing the same composition string buffer.</span></span> <span data-ttu-id="166a3-181">因此，CDXUTIMEEditBox 的組合字元串緩衝區是靜態的，可防止應用程式佔用不必要的記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="166a3-181">The composition string buffer for CDXUTIMEEditBox is therefore static, preventing the application from taking up unnecessary memory space.</span></span>

<span data-ttu-id="166a3-182">CDXUTIMEEditBox 會在下列 DXUT 程式碼中執行：</span><span class="sxs-lookup"><span data-stu-id="166a3-182">CDXUTIMEEditBox is implemented in the following DXUT code:</span></span>

<span data-ttu-id="166a3-183"> (SDK 根) \\ 範例 \\ c + + \\ Common \\ DXUTgui .cpp</span><span class="sxs-lookup"><span data-stu-id="166a3-183">(SDK root)\\Samples\\C++\\Common\\DXUTgui.cpp</span></span>

## <a name="overriding-the-default-ime-behavior"></a><span data-ttu-id="166a3-184">覆寫預設的 IME 行為</span><span class="sxs-lookup"><span data-stu-id="166a3-184">Overriding the Default IME Behavior</span></span>

<span data-ttu-id="166a3-185">輸入法通常會使用標準的 Windows 程式來建立視窗 (請參閱 [使用 Windows](/windows/desktop/winmsg/using-windows)) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-185">Normally an IME uses standard Windows procedures to create a window (see [Using Windows](/windows/desktop/winmsg/using-windows)).</span></span> <span data-ttu-id="166a3-186">在正常情況下，這會產生令人滿意的結果。</span><span class="sxs-lookup"><span data-stu-id="166a3-186">Under normal circumstances, this produces satisfactory results.</span></span> <span data-ttu-id="166a3-187">不過，當應用程式在全螢幕模式下呈現時（如同遊戲的常見），標準 windows 將不再運作，而且可能不會顯示在應用程式的最上層。</span><span class="sxs-lookup"><span data-stu-id="166a3-187">However, when the application presents in full-screen mode, as is common for games, standard windows no longer work and may not display on top of the application.</span></span> <span data-ttu-id="166a3-188">若要解決這個問題，應用程式必須繪製 IME 視窗本身，而不是依賴 Windows 來執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="166a3-188">To overcome this issue, the application must draw the IME windows itself instead of relying on Windows to perform this task.</span></span>

<span data-ttu-id="166a3-189">當預設的 IME 視窗建立行為未提供應用程式所需的行為時，應用程式可以覆寫 IME 視窗處理。</span><span class="sxs-lookup"><span data-stu-id="166a3-189">When the default IME window creation behavior does not provide what an application requires, the application can override the IME window handling.</span></span> <span data-ttu-id="166a3-190">應用程式可以藉由處理輸入法相關的訊息，並呼叫 [輸入方法管理員](/windows/desktop/Intl/input-method-manager) (IMM) API 來達到此目的。</span><span class="sxs-lookup"><span data-stu-id="166a3-190">An application can achieve this by processing IME-related messages and calling the [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM) API.</span></span>

<span data-ttu-id="166a3-191">當使用者與 IME 互動以輸入複雜字元時，輸出會將訊息傳送至應用程式，以通知它有重要事件，例如開始撰寫或顯示候選視窗。</span><span class="sxs-lookup"><span data-stu-id="166a3-191">When a user interacts with an IME to input complex characters, the IMM sends messages to the application to notify it of important events, such as starting a composition or showing the candidate window.</span></span> <span data-ttu-id="166a3-192">應用程式通常會忽略這些訊息，並將它們傳遞至預設的訊息處理常式，以使 IME 處理這些訊息。</span><span class="sxs-lookup"><span data-stu-id="166a3-192">An application typically ignores these messages and passes them to the default message handler, which causes the IME to handle them.</span></span> <span data-ttu-id="166a3-193">當應用程式（而不是預設處理常式）處理訊息時，它會完全控制每個 IME 事件所發生的情況。</span><span class="sxs-lookup"><span data-stu-id="166a3-193">When the application, instead of the default handler, handles the messages, it controls exactly what happens at each of the IME events.</span></span> <span data-ttu-id="166a3-194">訊息處理常式通常會呼叫 IMM API 來抓取各種 IME 視窗的內容。</span><span class="sxs-lookup"><span data-stu-id="166a3-194">Often the message handler retrieves the content of the various IME windows by calling the IMM API.</span></span> <span data-ttu-id="166a3-195">一旦應用程式擁有這種資訊之後，它就可以在需要呈現給顯示器時，適當地繪製 IME 視窗本身。</span><span class="sxs-lookup"><span data-stu-id="166a3-195">Once the application has this information, it can properly draw the IME windows itself when it needs to render to the display.</span></span>

## <a name="functions"></a><span data-ttu-id="166a3-196">函式</span><span class="sxs-lookup"><span data-stu-id="166a3-196">Functions</span></span>

<span data-ttu-id="166a3-197">輸入法需要取得讀取字串、隱藏讀取視窗，以及取得閱讀視窗的方向。</span><span class="sxs-lookup"><span data-stu-id="166a3-197">An IME needs to get the reading string, hide the reading window, and get the orientation of reading window.</span></span> <span data-ttu-id="166a3-198">下表顯示每個 IME 版本的功能：</span><span class="sxs-lookup"><span data-stu-id="166a3-198">This table shows the functionalities per IME version:</span></span>



|                    | <span data-ttu-id="166a3-199">取得讀取字串</span><span class="sxs-lookup"><span data-stu-id="166a3-199">Getting reading string</span></span>                                                | <span data-ttu-id="166a3-200">隱藏讀取視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-200">Hiding reading window</span></span>                       | <span data-ttu-id="166a3-201">讀取視窗的方向</span><span class="sxs-lookup"><span data-stu-id="166a3-201">Orientation of reading window</span></span>                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="166a3-202">在6.0 版之前</span><span class="sxs-lookup"><span data-stu-id="166a3-202">Before version 6.0</span></span> | <span data-ttu-id="166a3-203">A.</span><span class="sxs-lookup"><span data-stu-id="166a3-203">A.</span></span> <span data-ttu-id="166a3-204">直接讀取視窗存取 IME 私用資料。</span><span class="sxs-lookup"><span data-stu-id="166a3-204">Reading Window Access IME private data directly.</span></span> <span data-ttu-id="166a3-205">請參閱「4結構」</span><span class="sxs-lookup"><span data-stu-id="166a3-205">See "4 Structure"</span></span> | <span data-ttu-id="166a3-206">陷阱 IME 私用訊息。</span><span class="sxs-lookup"><span data-stu-id="166a3-206">Trap IME private messages.</span></span> <span data-ttu-id="166a3-207">請參閱「3個訊息」</span><span class="sxs-lookup"><span data-stu-id="166a3-207">See "3 Messages"</span></span> | <span data-ttu-id="166a3-208">檢查登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="166a3-208">Examine registry information.</span></span> <span data-ttu-id="166a3-209">請參閱 "5 Registry Information"</span><span class="sxs-lookup"><span data-stu-id="166a3-209">See "5 Registry Information"</span></span> |
| <span data-ttu-id="166a3-210">6.0 版之後</span><span class="sxs-lookup"><span data-stu-id="166a3-210">After version 6.0</span></span>  | [<span data-ttu-id="166a3-211">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="166a3-211">GetReadingString</span></span>](#getreadingstring)                                 | [<span data-ttu-id="166a3-212">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="166a3-212">ShowReadingWindow</span></span>](#showreadingwindow)     | [<span data-ttu-id="166a3-213">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="166a3-213">GetReadingString</span></span>](#getreadingstring)                      |



 

## <a name="messages"></a><span data-ttu-id="166a3-214">訊息</span><span class="sxs-lookup"><span data-stu-id="166a3-214">Messages</span></span>

<span data-ttu-id="166a3-215">下列訊息不需要針對執行 [ShowReadingWindow](#showreadingwindow) () 的較新 IME 進行處理。</span><span class="sxs-lookup"><span data-stu-id="166a3-215">The following messages don't have to be processed for newer IME that implements [ShowReadingWindow](#showreadingwindow)().</span></span>

<span data-ttu-id="166a3-216">下列訊息是由應用程式訊息處理常式所攔截 (也就是它們不會傳遞至 DefWindowProc) 以防止讀取視窗顯示。</span><span class="sxs-lookup"><span data-stu-id="166a3-216">The following messages are trapped by application message handler (i.e. they are not passed to DefWindowProc) to prevent the reading window from showing up.</span></span>

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a><span data-ttu-id="166a3-217">範例</span><span class="sxs-lookup"><span data-stu-id="166a3-217">Examples</span></span>

<span data-ttu-id="166a3-218">下列範例說明如何從沒有 GetReadingString () 的舊版輸入法讀取字串資訊。</span><span class="sxs-lookup"><span data-stu-id="166a3-218">The following examples illustrate how to get reading string information from older IME that doesn't have GetReadingString().</span></span> <span data-ttu-id="166a3-219">此程式碼會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="166a3-219">The code generates the following outputs:</span></span>



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="166a3-220">DWORD dwlen</span><span class="sxs-lookup"><span data-stu-id="166a3-220">DWORD dwlen</span></span>  | <span data-ttu-id="166a3-221">讀取字串的長度</span><span class="sxs-lookup"><span data-stu-id="166a3-221">Length of the reading string</span></span>                                                          |
| <span data-ttu-id="166a3-222">DWORD dwerr</span><span class="sxs-lookup"><span data-stu-id="166a3-222">DWORD dwerr</span></span>  | <span data-ttu-id="166a3-223">錯誤 char 的索引</span><span class="sxs-lookup"><span data-stu-id="166a3-223">Index of error char</span></span>                                                                   |
| <span data-ttu-id="166a3-224">LPWSTR wstr</span><span class="sxs-lookup"><span data-stu-id="166a3-224">LPWSTR wstr</span></span>  | <span data-ttu-id="166a3-225">讀取字串的指標</span><span class="sxs-lookup"><span data-stu-id="166a3-225">Pointer to the reading string</span></span>                                                         |
| <span data-ttu-id="166a3-226">BOOL unicode</span><span class="sxs-lookup"><span data-stu-id="166a3-226">BOOL unicode</span></span> | <span data-ttu-id="166a3-227">若為 true，則表示讀取字串採用 Unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="166a3-227">If true, the reading string is in Unicode format.</span></span> <span data-ttu-id="166a3-228">否則會是多位元組格式。</span><span class="sxs-lookup"><span data-stu-id="166a3-228">Otherwise it's in multibyte format.</span></span> |



 

### <a name="cht-ime-version-42-43-and-44"></a><span data-ttu-id="166a3-229">CHT IME 4.2、4.3 和4.4 版</span><span class="sxs-lookup"><span data-stu-id="166a3-229">CHT IME version 4.2, 4.3 and 4.4</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a><span data-ttu-id="166a3-230">CHT IME 5.0 版</span><span class="sxs-lookup"><span data-stu-id="166a3-230">CHT IME version 5.0</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a><span data-ttu-id="166a3-231">CHT IME 5.1、5.2 和 CHS IME 版本5。3</span><span class="sxs-lookup"><span data-stu-id="166a3-231">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a><span data-ttu-id="166a3-232">CHS IME 4.1 版</span><span class="sxs-lookup"><span data-stu-id="166a3-232">CHS IME version 4.1</span></span>

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a><span data-ttu-id="166a3-233">CHS IME 4.2 版</span><span class="sxs-lookup"><span data-stu-id="166a3-233">CHS IME version 4.2</span></span>

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a><span data-ttu-id="166a3-234">輸入法訊息</span><span class="sxs-lookup"><span data-stu-id="166a3-234">IME Messages</span></span>

<span data-ttu-id="166a3-235">全螢幕應用程式必須適當地處理下列與 IME 相關的訊息：</span><span class="sxs-lookup"><span data-stu-id="166a3-235">A full-screen application must properly handle the following IME-related messages:</span></span>

### <a name="wm_inputlangchange"></a><span data-ttu-id="166a3-236">WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="166a3-236">WM\_INPUTLANGCHANGE</span></span>

<span data-ttu-id="166a3-237">\_當使用者以按鍵組合變更輸入地區設定之後，輸出會將 WM INPUTLANGCHANGE 訊息傳送至應用程式的使用中視窗， (通常是 ALT + SHIFT) ，或使用工作列或語言列上的輸入地區設定指標。</span><span class="sxs-lookup"><span data-stu-id="166a3-237">The IMM sends a WM\_INPUTLANGCHANGE message to the active window of an application after the input locale has been changed by the user with a key combination (usually ALT+SHIFT), or with the input locale indicator on the taskbar or language bar.</span></span> <span data-ttu-id="166a3-238">語言列是螢幕上的控制項，使用者可以用它來設定文字服務。</span><span class="sxs-lookup"><span data-stu-id="166a3-238">The language bar is an on-screen control with which the user can configure a text service.</span></span> <span data-ttu-id="166a3-239"> (參閱 [如何顯示語言](/windows/desktop/TSF/how-to-set-up-tsf)列。 ) 下列螢幕擷取畫面顯示當使用者按一下地區設定指標時所顯示的語言挑選清單。</span><span class="sxs-lookup"><span data-stu-id="166a3-239">(See [How to show the language bar](/windows/desktop/TSF/how-to-set-up-tsf).) The following screen shot shows a language selection list that is displayed when the user clicks on the locale indicator.</span></span>

![當使用者按一下地區設定指標時所顯示的語言挑選清單](images/ime-langselection.png)

<span data-ttu-id="166a3-241">當 IMM 傳送 WM \_ INPUTLANGCHANGE 訊息時，CDXUTIMEEditBox 必須執行幾項重要工作：</span><span class="sxs-lookup"><span data-stu-id="166a3-241">When the IMM sends a WM\_INPUTLANGCHANGE message, CDXUTIMEEditBox must perform several important tasks:</span></span>

1.  <span data-ttu-id="166a3-242">呼叫 GetKeyboardLayout 方法，以傳回應用程式執行緒 (識別碼) 的輸入地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="166a3-242">The GetKeyboardLayout method is called to return the input locale identifier (ID) for the application thread.</span></span> <span data-ttu-id="166a3-243">CDXUTIMEEditBox 類別會將此識別碼儲存在其靜態成員變數 s \_ hklCurrent 中，以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="166a3-243">The CDXUTIMEEditBox class saves this ID in its static member variable s\_hklCurrent for later use.</span></span> <span data-ttu-id="166a3-244">應用程式必須知道目前的輸入地區設定是很重要的，因為每種語言的 IME 都有自己的獨特行為。</span><span class="sxs-lookup"><span data-stu-id="166a3-244">It is important for the application to know the current input locale, because the IME for each language has its own distinct behavior.</span></span> <span data-ttu-id="166a3-245">開發人員可能需要針對不同的輸入地區設定提供不同的程式碼。</span><span class="sxs-lookup"><span data-stu-id="166a3-245">The developer may need to provide different code for different input locales.</span></span>
2.  <span data-ttu-id="166a3-246">CDXUTIMEEditBox 會初始化要顯示在編輯方塊語言指標中的字串。</span><span class="sxs-lookup"><span data-stu-id="166a3-246">CDXUTIMEEditBox initializes a string to display in the edit box language indicator.</span></span> <span data-ttu-id="166a3-247">當應用程式在全螢幕模式下執行，而且沒有看到工作列或語言列時，此指標可以顯示作用中的輸入語言。</span><span class="sxs-lookup"><span data-stu-id="166a3-247">This indicator can display the active input language when the application is running in full-screen mode and neither the taskbar nor language bar is visible.</span></span>
3.  <span data-ttu-id="166a3-248">呼叫 ImmGetConversionStatus 方法，以指出輸入地區設定是否為原生或非原生轉換模式。</span><span class="sxs-lookup"><span data-stu-id="166a3-248">The ImmGetConversionStatus method is called to indicate whether the input locale is in native or non-native conversion mode.</span></span> <span data-ttu-id="166a3-249">原生轉換模式可讓使用者以選擇的語言輸入文字。</span><span class="sxs-lookup"><span data-stu-id="166a3-249">Native conversion mode lets the user enter text in the chosen language.</span></span> <span data-ttu-id="166a3-250">非原生轉換模式讓鍵盤成為標準的英文鍵盤。</span><span class="sxs-lookup"><span data-stu-id="166a3-250">Non-native conversion mode makes the keyboard act as a standard English keyboard.</span></span> <span data-ttu-id="166a3-251">請務必為使用者提供視覺提示，指出輸入法在何種類型的轉換模式中，如此一來，使用者就能在叫用按鍵時輕鬆知道預期的字元。</span><span class="sxs-lookup"><span data-stu-id="166a3-251">It is important to give the user a visual cue as to what type of conversion mode the IME is in, so that the user can easily know what characters to expect when hitting a key.</span></span> <span data-ttu-id="166a3-252">CDXUTIMEEditBox 會以語言指標色彩提供此視覺提示。</span><span class="sxs-lookup"><span data-stu-id="166a3-252">CDXUTIMEEditBox provides this visual cue with a language indicator color.</span></span> <span data-ttu-id="166a3-253">當輸入地區設定使用具有原生轉換模式的輸入法時，CDXUTIMEEditBox 類別會使用 m IndicatorImeColor 參數所定義的色彩來繪製指標文字 \_ 。</span><span class="sxs-lookup"><span data-stu-id="166a3-253">When the input locale uses an IME with native conversion mode, the CDXUTIMEEditBox class draws the indicator text with the color defined by the m\_IndicatorImeColor parameter.</span></span> <span data-ttu-id="166a3-254">當 IME 處於非原生轉換模式，或完全沒有使用任何輸入法時，類別會使用 m IndicatorEngColor 參數所定義的色彩來繪製指標文字 \_ 。</span><span class="sxs-lookup"><span data-stu-id="166a3-254">When the IME is in non-native conversion mode, or no IME is used at all, the class draws the indicator text with the color defined by the m\_IndicatorEngColor parameter.</span></span>
4.  <span data-ttu-id="166a3-255">CDXUTIMEEditBox 會檢查輸入地區設定，並將韓文的靜態成員變數 s bInsertOnType 設定為 TRUE，並將 \_ 所有其他語言設定為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="166a3-255">CDXUTIMEEditBox checks the input locale and sets the static member variable s\_bInsertOnType to TRUE for Korean and FALSE for all other languages.</span></span> <span data-ttu-id="166a3-256">因為韓文 Ime 和所有其他 Ime 的行為不同，所以需要此旗標。</span><span class="sxs-lookup"><span data-stu-id="166a3-256">This flag is required because of the different behaviors of Korean IMEs and all other IMEs.</span></span> <span data-ttu-id="166a3-257">以韓文以外的語言輸入字元時，使用者輸入的文字會顯示在組合視窗中，使用者可以自由變更組合字元串的內容。</span><span class="sxs-lookup"><span data-stu-id="166a3-257">When entering characters in languages other than Korean, the user-entered text is displayed in the composition window, and the user can freely change the content of the composition string.</span></span> <span data-ttu-id="166a3-258">當您滿意組合字元串時，使用者按下 ENTER 鍵，然後將組合字元串以一系列的 WM 字元訊息傳送至應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="166a3-258">The user presses the ENTER key when satisfied with the composition string, and the composition string is sent to the application as a series of WM\_CHAR messages.</span></span> <span data-ttu-id="166a3-259">不過，在韓文 Ime 中，當使用者按下按鍵來輸入文字時，會立即將字元傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-259">In Korean IMEs, however, when a user presses a key to enter text, a character is immediately sent to the application.</span></span> <span data-ttu-id="166a3-260">當使用者後續按更多按鍵來修改該初始字元時，編輯方塊中的字元會變更，以反映使用者的其他輸入。</span><span class="sxs-lookup"><span data-stu-id="166a3-260">When the user subsequently presses more keys to modify that initial character, the character in the edit box changes to reflect additional input from the user.</span></span> <span data-ttu-id="166a3-261">基本上，使用者是在編輯方塊中撰寫字元。</span><span class="sxs-lookup"><span data-stu-id="166a3-261">Essentially, the user is composing characters in the edit box.</span></span> <span data-ttu-id="166a3-262">這兩種行為不同，CDXUTIMEEditBox 必須特別為每個行為編寫程式碼。</span><span class="sxs-lookup"><span data-stu-id="166a3-262">These two behaviors are different enough that CDXUTIMEEditBox must code for each of them specifically.</span></span>
5.  <span data-ttu-id="166a3-263">呼叫靜態成員方法 SetupImeApi 時，會從 IME 模組取得兩個函式的位址： GetReadingString 和 ShowReadingWindow。</span><span class="sxs-lookup"><span data-stu-id="166a3-263">The static member method SetupImeApi is called to retrieve addresses of two functions from the IME module: GetReadingString and ShowReadingWindow.</span></span> <span data-ttu-id="166a3-264">如果這些函式存在，則會呼叫 ShowReadingWindow 來隱藏此 IME 的預設讀取視窗。</span><span class="sxs-lookup"><span data-stu-id="166a3-264">If these functions exist, ShowReadingWindow is called to hide the default reading window for this IME.</span></span> <span data-ttu-id="166a3-265">由於應用程式會轉譯讀取視窗本身，因此它會通知 IME 停用繪製預設的讀取視窗，使其不會干擾全螢幕呈現。</span><span class="sxs-lookup"><span data-stu-id="166a3-265">Because the application renders the reading window itself, it notifies the IME to disable drawing the default reading window so that it will not interfere with full-screen rendering.</span></span>

<span data-ttu-id="166a3-266">\_ \_ 當應用程式的視窗啟用時，IMM 會傳送 WM IME SETCONTEXT 訊息。</span><span class="sxs-lookup"><span data-stu-id="166a3-266">The IMM sends a WM\_IME\_SETCONTEXT message when a window of the application is activated.</span></span> <span data-ttu-id="166a3-267">此訊息的 lParam 參數所包含的旗標，會向 IME 指出應該繪製的視窗，以及不應該使用的參數。</span><span class="sxs-lookup"><span data-stu-id="166a3-267">The lParam parameter of this message contains a flag that indicates to the IME which windows should get drawn and which should not.</span></span> <span data-ttu-id="166a3-268">因為應用程式會處理所有繪圖，所以不需要 IME 來繪製任何 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="166a3-268">Because the application is handling all of the drawing, it does not need the IME to draw any of the IME windows.</span></span> <span data-ttu-id="166a3-269">因此，應用程式的訊息處理常式只會將 lParam 設定為0，並傳回。</span><span class="sxs-lookup"><span data-stu-id="166a3-269">Therefore, the application's message handler simply sets lParam to 0 and returns.</span></span>

<span data-ttu-id="166a3-270">為了讓應用程式支援 IME，IME 相關訊息 WM ime SETCONTEXT 需要進行特殊處理 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="166a3-270">In order for applications to support IME, special processing is needed for the IME-related message WM\_IME\_SETCONTEXT.</span></span> <span data-ttu-id="166a3-271">因為 Windows 通常會在呼叫 PanoramaInitialize () 方法之前將此訊息傳送至應用程式，所以全景沒有機會處理 UI 來顯示候選清單視窗。</span><span class="sxs-lookup"><span data-stu-id="166a3-271">Since Windows typically sends this message to the application prior to calling the PanoramaInitialize() method, Panorama doesn't have a chance to process the UI for showing candidate list windows.</span></span>

<span data-ttu-id="166a3-272">下列程式碼片段會將 Windows 應用程式指定為不顯示任何與候選清單視窗相關聯的 UI，讓全景可以明確地處理這個 UI。</span><span class="sxs-lookup"><span data-stu-id="166a3-272">The following code snippet specifies to Windows applications not to display any UI associated with the candidate list window, allowing Panorama to specifically handle this UI.</span></span>

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a><span data-ttu-id="166a3-273">WM \_ IME \_ STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="166a3-273">WM\_IME\_STARTCOMPOSITION</span></span>

<span data-ttu-id="166a3-274">\_ \_ 當 IME 組合即將從使用者擊鍵的結果開始時，輸出會將 WM ime STARTCOMPOSITION 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-274">The IMM sends a WM\_IME\_STARTCOMPOSITION message to the application when an IME composition is about to begin as a result of keystrokes by the user.</span></span> <span data-ttu-id="166a3-275">如果 IME 使用撰寫視窗，則會在組合視窗中顯示目前的組合字元串。</span><span class="sxs-lookup"><span data-stu-id="166a3-275">If the IME uses the composition window, it displays the current composition string in a composition window.</span></span> <span data-ttu-id="166a3-276">CDXUTIMEEditBox 會執行兩個工作來處理此訊息：</span><span class="sxs-lookup"><span data-stu-id="166a3-276">CDXUTIMEEditBox handles this message by performing two tasks:</span></span>

1.  <span data-ttu-id="166a3-277">CDXUTIMEEditBox 會清除組合字元串緩衝區和屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="166a3-277">CDXUTIMEEditBox clears the composition string buffer and attribute buffer.</span></span> <span data-ttu-id="166a3-278">這些緩衝區是 CDXUTIMEEditBox 的靜態成員。</span><span class="sxs-lookup"><span data-stu-id="166a3-278">These buffers are static members of CDXUTIMEEditBox.</span></span>
2.  <span data-ttu-id="166a3-279">CDXUTIMEEditBox 會將 s \_ bHideCaret 靜態成員變數設為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="166a3-279">CDXUTIMEEditBox sets the s\_bHideCaret static member variable to TRUE.</span></span> <span data-ttu-id="166a3-280">這個成員定義在基底 CDXUTEditBox 類別中，可控制是否要在編輯方塊時繪製編輯方塊中的游標。</span><span class="sxs-lookup"><span data-stu-id="166a3-280">This member, defined in the base CDXUTEditBox class, controls whether the cursor in the edit box should be drawn when the edit box is rendered.</span></span> <span data-ttu-id="166a3-281">組合視窗的功能類似于具有文字和游標的編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="166a3-281">The composition window functions similarly to an edit box with text and cursor.</span></span> <span data-ttu-id="166a3-282">為了避免在組合視窗可見時產生混淆，編輯方塊會隱藏其資料指標，因此一次只會顯示一個資料指標。</span><span class="sxs-lookup"><span data-stu-id="166a3-282">To avoid confusion when the composition window is visible, the edit box hides its cursor so that only one cursor is visible at a time.</span></span>

### <a name="wm_ime_composition"></a><span data-ttu-id="166a3-283">WM \_ IME \_ 組合</span><span class="sxs-lookup"><span data-stu-id="166a3-283">WM\_IME\_COMPOSITION</span></span>

<span data-ttu-id="166a3-284">\_ \_ 當使用者輸入按鍵來變更組合字元串時，IMM 會將 WM IME 組合訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-284">The IMM sends a WM\_IME\_COMPOSITION message to the application when the user enters a keystroke to change the composition string.</span></span> <span data-ttu-id="166a3-285">LParam 的值表示應用程式可以從輸入方法管理員 (的 IMM) 中取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="166a3-285">The value of lParam indicates what type of information the application can retrieve from the Input Method Manager (IMM).</span></span> <span data-ttu-id="166a3-286">應用程式應該藉由呼叫 [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) 來取得可用的資訊，然後應該將資訊儲存在其私用緩衝區中，以便稍後可以轉譯 IME 元素。</span><span class="sxs-lookup"><span data-stu-id="166a3-286">The application should retrieve the available information by calling [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) and then should save the information in its private buffer so that it can render the IME elements later.</span></span>

<span data-ttu-id="166a3-287">CDXUTIMEEditBox 會檢查並抓取下列組合字元串資料：</span><span class="sxs-lookup"><span data-stu-id="166a3-287">CDXUTIMEEditBox checks for and retrieves the following composition string data:</span></span>



| <span data-ttu-id="166a3-288">[**WM \_IME \_ 組合**](/windows/desktop/Intl/wm-ime-composition) lParam 旗標值</span><span class="sxs-lookup"><span data-stu-id="166a3-288">[**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam Flag Value</span></span> | <span data-ttu-id="166a3-289">資料</span><span class="sxs-lookup"><span data-stu-id="166a3-289">Data</span></span>                           | <span data-ttu-id="166a3-290">描述</span><span class="sxs-lookup"><span data-stu-id="166a3-290">Description</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="166a3-291">GC \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="166a3-291">GCS\_COMPATTR</span></span>                                                         | <span data-ttu-id="166a3-292">組合屬性</span><span class="sxs-lookup"><span data-stu-id="166a3-292">Composition Attribute</span></span>          | <span data-ttu-id="166a3-293">這個屬性所包含的資訊，像是組合字元串中每個字元的狀態 (例如，已轉換或非轉換的) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-293">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="166a3-294">這項資訊是必要的，因為 CDXUTIMEEditBox 會根據其屬性，以不同的方式來色彩撰寫字串字元。</span><span class="sxs-lookup"><span data-stu-id="166a3-294">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span>                                                                                   |
| <span data-ttu-id="166a3-295">GC \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="166a3-295">GCS\_COMPCLAUSE</span></span>                                                       | <span data-ttu-id="166a3-296">撰寫子句資訊</span><span class="sxs-lookup"><span data-stu-id="166a3-296">Composition Clause Information</span></span> | <span data-ttu-id="166a3-297">當日文 IME 為使用中時，會使用這個子句資訊。</span><span class="sxs-lookup"><span data-stu-id="166a3-297">This clause information is used when the Japanese IME is active.</span></span> <span data-ttu-id="166a3-298">轉換日文組合字元串時，可以將字元群組在一起，成為轉換成單一實體的子句。</span><span class="sxs-lookup"><span data-stu-id="166a3-298">When a Japanese composition string is converted, characters may be grouped together as a clause that gets converted to a single entity.</span></span> <span data-ttu-id="166a3-299">當使用者移動游標時，CDXUTIMEEditBox 會使用這項資訊來反白顯示整個子句，而不只是子句內的單一字元。</span><span class="sxs-lookup"><span data-stu-id="166a3-299">When the user moves the cursor, CDXUTIMEEditBox uses this information to highlight the entire clause, instead of just a single character within the clause.</span></span> |
| <span data-ttu-id="166a3-300">GC \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="166a3-300">GCS\_COMPSTR</span></span>                                                          | <span data-ttu-id="166a3-301">組合字元串</span><span class="sxs-lookup"><span data-stu-id="166a3-301">Composition String</span></span>             | <span data-ttu-id="166a3-302">這個字串是由使用者組成的最新字串。</span><span class="sxs-lookup"><span data-stu-id="166a3-302">This string is the up-to-date string being composed by the user.</span></span> <span data-ttu-id="166a3-303">這也是顯示在組合視窗中的字串。</span><span class="sxs-lookup"><span data-stu-id="166a3-303">This is also the string displayed in the composition window.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="166a3-304">GC \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="166a3-304">GCS\_CURSORPOS</span></span>                                                        | <span data-ttu-id="166a3-305">組合游標位置</span><span class="sxs-lookup"><span data-stu-id="166a3-305">Composition Cursor Position</span></span>    | <span data-ttu-id="166a3-306">組合視窗會實作為游標，類似于編輯方塊中的游標。</span><span class="sxs-lookup"><span data-stu-id="166a3-306">The composition window implements a cursor, similar to the cursor in an edit box.</span></span> <span data-ttu-id="166a3-307">應用程式可以在處理 WM IME 組合訊息時取出游標位置，以便 \_ \_ 適當地繪製資料指標。</span><span class="sxs-lookup"><span data-stu-id="166a3-307">The application can retrieve the cursor position when processing the WM\_IME\_COMPOSITION message in order to draw the cursor properly.</span></span>                                                                                                                                            |
| <span data-ttu-id="166a3-308">GC \_ RESULTSTR</span><span class="sxs-lookup"><span data-stu-id="166a3-308">GCS\_RESULTSTR</span></span>                                                        | <span data-ttu-id="166a3-309">結果字串</span><span class="sxs-lookup"><span data-stu-id="166a3-309">Result String</span></span>                  | <span data-ttu-id="166a3-310">當使用者即將完成撰寫程式時，就可以使用結果字串。</span><span class="sxs-lookup"><span data-stu-id="166a3-310">The result string is available when the user is about to complete the composition process.</span></span> <span data-ttu-id="166a3-311">應抓取這個字串，並將字元傳送至編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="166a3-311">This string should be retrieved and the characters should be sent to the edit box.</span></span>                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a><span data-ttu-id="166a3-312">WM \_ IME \_ ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="166a3-312">WM\_IME\_ENDCOMPOSITION</span></span>

<span data-ttu-id="166a3-313">\_ \_ 當 IME 組合作業結束時，IMM 會將 WM ime ENDCOMPOSITION 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-313">The IMM sends a WM\_IME\_ENDCOMPOSITION message to the application when the IME composition operation is ending.</span></span> <span data-ttu-id="166a3-314">當使用者按下 ENTER 鍵核准組合字元串，或是按 ESC 鍵取消群組時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="166a3-314">This can occur when the user presses the ENTER key to approve the composition string, or the ESC key to cancel the composition.</span></span> <span data-ttu-id="166a3-315">CDXUTIMEEditBox 會藉由將組合字元串緩衝區設定為空白來處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="166a3-315">CDXUTIMEEditBox handles this message by setting the composition string buffer to be empty.</span></span> <span data-ttu-id="166a3-316">然後，它會將 \_ bHideCaret 設定為 FALSE，因為組合視窗已關閉，而編輯方塊中的游標應該會再次顯示。</span><span class="sxs-lookup"><span data-stu-id="166a3-316">It then sets s\_bHideCaret to FALSE because the composition window is closed and the cursor in the edit box should again be visible.</span></span>

<span data-ttu-id="166a3-317">CDXUTIMEEditBox 訊息處理常式也會將 \_ bShowReadingWindow 設定為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="166a3-317">The CDXUTIMEEditBox message handler also sets s\_bShowReadingWindow to FALSE.</span></span> <span data-ttu-id="166a3-318">此旗標會控制當編輯方塊本身呈現時，類別是否繪製讀取視窗，因此在組合結束時必須將它設定為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="166a3-318">This flag controls whether the class draws the reading window when the edit box renders itself, so it must be set to FALSE when a composition ends.</span></span>

### <a name="wm_ime_notify"></a><span data-ttu-id="166a3-319">WM \_ 輸入法 \_ 通知</span><span class="sxs-lookup"><span data-stu-id="166a3-319">WM\_IME\_NOTIFY</span></span>

<span data-ttu-id="166a3-320">\_ \_ 每當輸入法視窗變更時，IMM 都會將 WM ime 通知訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-320">The IMM sends a WM\_IME\_NOTIFY message to the application whenever an IME window changes.</span></span> <span data-ttu-id="166a3-321">處理 IME 視窗繪圖的應用程式應該處理此訊息，讓它知道視窗內容的任何更新。</span><span class="sxs-lookup"><span data-stu-id="166a3-321">An application that handles the drawing of the IME windows should process this message so that it is aware of any update to the content of the window.</span></span> <span data-ttu-id="166a3-322">WParam 指出正在進行的命令或變更。</span><span class="sxs-lookup"><span data-stu-id="166a3-322">The wParam indicates the command or the change that is taking place.</span></span> <span data-ttu-id="166a3-323">CDXUTIMEEditBox 會處理下列命令：</span><span class="sxs-lookup"><span data-stu-id="166a3-323">CDXUTIMEEditBox handles the following commands:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="166a3-324">IME 命令</span><span class="sxs-lookup"><span data-stu-id="166a3-324">IME Command</span></span></th>
<th><span data-ttu-id="166a3-325">Description</span><span class="sxs-lookup"><span data-stu-id="166a3-325">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="166a3-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="166a3-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span></span></td>
<td><span data-ttu-id="166a3-327">這個屬性所包含的資訊，像是組合字元串中每個字元的狀態 (例如，已轉換或非轉換的) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-327">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="166a3-328">這項資訊是必要的，因為 CDXUTIMEEditBox 會根據其屬性，以不同的方式來色彩撰寫字串字元。</span><span class="sxs-lookup"><span data-stu-id="166a3-328">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="166a3-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="166a3-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span></span></td>
<td><span data-ttu-id="166a3-330">在即將開啟或更新候選視窗時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-330">Sent to the application when the candidate window is about to be opened or updated, respectively.</span></span> <span data-ttu-id="166a3-331">當使用者想要變更轉換的文字選擇時，就會開啟候選視窗。</span><span class="sxs-lookup"><span data-stu-id="166a3-331">The candidate window opens when a user wishes to change the converted text choice.</span></span> <span data-ttu-id="166a3-332">當使用者移動選取指標或變更頁面時，會更新視窗。</span><span class="sxs-lookup"><span data-stu-id="166a3-332">The window is updated when a user moves the selection indicator or changes the page.</span></span> <span data-ttu-id="166a3-333">CDXUTIMEEditBox 會針對這兩個命令使用一個訊息處理常式，因為所需的工作完全相同：</span><span class="sxs-lookup"><span data-stu-id="166a3-333">CDXUTIMEEditBox uses one message handler for both of these commands because the tasks required are exactly the same:</span></span><br/>
<ol>
<li><span data-ttu-id="166a3-334">CDXUTIMEEditBox 會將候選清單結構的 bShowWindow 成員 s_CandList 設定為 TRUE，表示需要在畫面格轉譯期間繪製候選視窗。</span><span class="sxs-lookup"><span data-stu-id="166a3-334">CDXUTIMEEditBox sets the bShowWindow member of the candidate list structure s_CandList to TRUE to indicate that the candidate window needs to be drawn during frame rendering.</span></span></li>
<li><span data-ttu-id="166a3-335">CDXUTIMEEditBox 會藉由呼叫 <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>，先取得所需的緩衝區大小，然後再取得實際的資料，以抓取候選清單。</span><span class="sxs-lookup"><span data-stu-id="166a3-335">CDXUTIMEEditBox retrieves the candidate list by calling <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, first to get the required buffer size, and then again to get the actual data.</span></span></li>
<li><span data-ttu-id="166a3-336">私用候選清單結構 s_CandList 會以抓取的候選資料進行初始化。</span><span class="sxs-lookup"><span data-stu-id="166a3-336">The private candidate list structure s_CandList is initialized with the retrieved candidate data.</span></span></li>
<li><span data-ttu-id="166a3-337">候選字串會儲存為字串陣列。</span><span class="sxs-lookup"><span data-stu-id="166a3-337">The candidate strings are stored as an array of strings.</span></span></li>
<li><span data-ttu-id="166a3-338">所選取專案的索引和頁面索引都會儲存起來。</span><span class="sxs-lookup"><span data-stu-id="166a3-338">The index of the selected entry, as well as the page index, is saved.</span></span></li>
<li><span data-ttu-id="166a3-339">CDXUTIMEEditBox 會檢查候選視窗樣式是垂直或水準。</span><span class="sxs-lookup"><span data-stu-id="166a3-339">CDXUTIMEEditBox checks whether the candidate window style is vertical or horizontal.</span></span> <span data-ttu-id="166a3-340">如果視窗樣式是水準的，則額外的字串緩衝區（s_CandList 的 HoriCand 成員）必須使用所有的候選字串來初始化，並在所有相鄰字串之間插入空白字元。</span><span class="sxs-lookup"><span data-stu-id="166a3-340">If the window style is horizontal, an additional string buffer, the HoriCand member of s_CandList, must be initialized with all of the candidate strings, with space characters inserted between all adjacent strings.</span></span> <span data-ttu-id="166a3-341">轉譯垂直候選視窗時，會一次繪製一個候選字串，其中每個字串的 y 座標都會遞增。</span><span class="sxs-lookup"><span data-stu-id="166a3-341">When rendering a vertical candidate window, the individual candidate strings are drawn one at a time, with the y coordinates incremented for each string.</span></span> <span data-ttu-id="166a3-342">不過，轉譯水準候選視窗時應該使用這個 HoriCand 字串，因為空白字元是在同一行上分隔兩個相鄰字串的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="166a3-342">However, this HoriCand string should be used when rendering a horizontal candidate window, because the space character is the best way to separate two adjacent strings on the same line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="166a3-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="166a3-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span></span></td>
<td><span data-ttu-id="166a3-344">當候選視窗即將關閉時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-344">Sent to the application when a candidate window is about to close.</span></span> <span data-ttu-id="166a3-345">當使用者從候選清單進行選取時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="166a3-345">This happens when a user has made a selection from the candidate list.</span></span> <span data-ttu-id="166a3-346">CDXUTIMEEditBox 會藉由將候選視窗的可見旗標設定為 FALSE，然後清除候選字串緩衝區，來處理此命令。</span><span class="sxs-lookup"><span data-stu-id="166a3-346">CDXUTIMEEditBox handles this command by setting the visible flag of the candidate window to FALSE and then clearing the candidate string buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="166a3-347">IMN_PRI加值稅E</span><span class="sxs-lookup"><span data-stu-id="166a3-347">IMN_PRIVATE</span></span></td>
<td><span data-ttu-id="166a3-348">當 IME 將其讀取字串更新為使用者鍵入或移除字元的結果時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="166a3-348">Sent to the application when the IME has updated its reading string as a result of the user typing or removing characters.</span></span> <span data-ttu-id="166a3-349">應用程式應該取出讀取字串，並加以儲存以供呈現。</span><span class="sxs-lookup"><span data-stu-id="166a3-349">The application should retrieve the reading string and save it for rendering.</span></span> <span data-ttu-id="166a3-350">CDXUTIMEEditBox 有兩個方法可根據 IME 中的讀取字串支援方式來取出讀取字串：</span><span class="sxs-lookup"><span data-stu-id="166a3-350">CDXUTIMEEditBox has two methods to retrieve the reading string, based upon how reading strings are supported in the IME:</span></span> <br/>
<ul>
<li><span data-ttu-id="166a3-351">如果 IME 支援 GetReadingString 函式，就會呼叫 GetReadingString 來取出讀取字串。</span><span class="sxs-lookup"><span data-stu-id="166a3-351">If the IME supports the GetReadingString function, GetReadingString is called to retrieve the reading string.</span></span></li>
<li><span data-ttu-id="166a3-352">如果 IME 未執行 GetReadingString，CDXUTIMEEditBox 會從輸入內容內容中抓取讀取字串。</span><span class="sxs-lookup"><span data-stu-id="166a3-352">If the IME does not implement GetReadingString, CDXUTIMEEditBox retrieves the reading string from the input context content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a><span data-ttu-id="166a3-353">轉譯</span><span class="sxs-lookup"><span data-stu-id="166a3-353">Rendering</span></span>

<span data-ttu-id="166a3-354">IME 元素和視窗的轉譯很簡單。</span><span class="sxs-lookup"><span data-stu-id="166a3-354">Rendering of the IME elements and windows is straightforward.</span></span> <span data-ttu-id="166a3-355">CDXUTIMEEditBox 可讓基類先轉譯，因為 IME 視窗應該會出現在編輯控制項的上方。</span><span class="sxs-lookup"><span data-stu-id="166a3-355">CDXUTIMEEditBox lets the base class render first because IME windows should appear on top of the edit control.</span></span> <span data-ttu-id="166a3-356">在基底編輯方塊呈現之後，CDXUTIMEEditBox 會檢查每個輸入視窗的可見度旗標 (指標、撰寫、候選和讀取視窗) 並繪製視窗（如果應該顯示的話）。</span><span class="sxs-lookup"><span data-stu-id="166a3-356">After the base edit box is rendered, CDXUTIMEEditBox checks the visibility flag of each IME window (indicator, composition, candidate, and reading window) and draws the window if it should be visible.</span></span> <span data-ttu-id="166a3-357">如需不同 IME 視窗類型的說明，請參閱預設的輸入法行為。</span><span class="sxs-lookup"><span data-stu-id="166a3-357">See Default IME Behavior for descriptions of the different IME window types.</span></span>

### <a name="input-locale-indicator"></a><span data-ttu-id="166a3-358">輸入地區設定指標</span><span class="sxs-lookup"><span data-stu-id="166a3-358">Input Locale Indicator</span></span>

<span data-ttu-id="166a3-359">輸入地區設定指標會在任何其他 IME 視窗之前轉譯，因為它是永遠顯示的元素。</span><span class="sxs-lookup"><span data-stu-id="166a3-359">The input locale indicator is rendered before any other IME windows because it is an element that is always displayed.</span></span> <span data-ttu-id="166a3-360">因此，它應該會出現在其他的 IME 視窗底下。</span><span class="sxs-lookup"><span data-stu-id="166a3-360">It should therefore appear below other IME windows.</span></span> <span data-ttu-id="166a3-361">CDXUTIMEEditBox 會藉由呼叫 RenderIndicator 方法來轉譯指標，其中指標字型色彩是藉由檢查 s \_ ImeState 靜態變數（反映目前的 IME 轉換模式）來決定。</span><span class="sxs-lookup"><span data-stu-id="166a3-361">CDXUTIMEEditBox renders the indicator by calling the RenderIndicator method, in which the indicator font color is determined by examining the s\_ImeState static variable, which reflects the current IME conversion mode.</span></span> <span data-ttu-id="166a3-362">啟用 IME 且原生轉換為使用中時，此方法會使用 m \_ IndicatorImeColor 做為指標色彩。</span><span class="sxs-lookup"><span data-stu-id="166a3-362">When the IME is enabled and native conversion is active, the method uses m\_IndicatorImeColor as the indicator color.</span></span> <span data-ttu-id="166a3-363">如果 IME 已停用或處於非原生轉換模式， \_ 則會使用 m IndicatorImeColor 來繪製指標文字。</span><span class="sxs-lookup"><span data-stu-id="166a3-363">If the IME is disabled or is in non-native conversion mode, m\_IndicatorImeColor is used to draw the indicator text.</span></span> <span data-ttu-id="166a3-364">根據預設，指標視窗本身會繪製在編輯方塊的右邊。</span><span class="sxs-lookup"><span data-stu-id="166a3-364">By default, the indicator window itself is drawn to the right of the edit box.</span></span> <span data-ttu-id="166a3-365">應用程式可以藉由覆寫 RenderIndicator 方法來變更此行為。</span><span class="sxs-lookup"><span data-stu-id="166a3-365">Applications can change this behavior by overriding the RenderIndicator method.</span></span>

<span data-ttu-id="166a3-366">下圖顯示英文的輸入地區設定指標的不同外觀、英數位元轉換模式的日文，以及日文的原生轉換模式：</span><span class="sxs-lookup"><span data-stu-id="166a3-366">The following figure shows the different appearances of an input locale indicator for English, Japanese in alphanumeric conversion mode, and Japanese in native conversion mode:</span></span>

![英文和日文輸入地區設定指標的不同外觀](images/ime-indicator.png)

### <a name="composition-window"></a><span data-ttu-id="166a3-368">撰寫視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-368">Composition Window</span></span>

<span data-ttu-id="166a3-369">撰寫視窗的繪圖是在 CDXUTIMEEditBox 的 RenderComposition 方法中處理。</span><span class="sxs-lookup"><span data-stu-id="166a3-369">The drawing of the composition window is handled in the RenderComposition method of CDXUTIMEEditBox.</span></span> <span data-ttu-id="166a3-370">撰寫視窗會浮動在編輯方塊上方。</span><span class="sxs-lookup"><span data-stu-id="166a3-370">The composition window floats above the edit box.</span></span> <span data-ttu-id="166a3-371">它應該繪製在基礎編輯控制項的游標位置。</span><span class="sxs-lookup"><span data-stu-id="166a3-371">It should be drawn at the cursor position of the underlying edit control.</span></span> <span data-ttu-id="166a3-372">CDXUTIMEEditBox 會處理轉譯，如下所示：</span><span class="sxs-lookup"><span data-stu-id="166a3-372">CDXUTIMEEditBox handles the rendering as follows:</span></span>

1.  <span data-ttu-id="166a3-373">整個組合字元串是使用預設的組合字元串色彩來繪製。</span><span class="sxs-lookup"><span data-stu-id="166a3-373">The entire composition string is drawn using the default composition string colors.</span></span>
2.  <span data-ttu-id="166a3-374">具有特定特殊屬性的字元應以不同的色彩繪製，因此 CDXUTIMEEditBox 會審核組合字元串的字元，並檢查字串屬性。</span><span class="sxs-lookup"><span data-stu-id="166a3-374">Characters with certain special attributes should be drawn in different colors, so CDXUTIMEEditBox reviews the characters of the composition string and inspects the string attribute.</span></span> <span data-ttu-id="166a3-375">如果屬性呼叫不同的色彩，則會使用適當的色彩再次繪製該字元。</span><span class="sxs-lookup"><span data-stu-id="166a3-375">If the attribute calls for different colors, the character is drawn again with the appropriate colors.</span></span>
3.  <span data-ttu-id="166a3-376">繪製組合視窗的游標以完成轉譯。</span><span class="sxs-lookup"><span data-stu-id="166a3-376">The cursor of the composition window is drawn to complete the rendering.</span></span>

<span data-ttu-id="166a3-377">資料指標應針對韓文 Ime 閃爍，但不應該用於其他 Ime。</span><span class="sxs-lookup"><span data-stu-id="166a3-377">The cursor should blink for Korean IMEs, but it should not for other IMEs.</span></span> <span data-ttu-id="166a3-378">RenderComposition 會根據使用韓文 IME 時的計時器值，決定是否要顯示資料指標。</span><span class="sxs-lookup"><span data-stu-id="166a3-378">RenderComposition determines whether the cursor should be visible based upon timer values when the Korean IME is used.</span></span>

### <a name="reading-and-candidate-windows"></a><span data-ttu-id="166a3-379">讀取和候選視窗</span><span class="sxs-lookup"><span data-stu-id="166a3-379">Reading and Candidate Windows</span></span>

<span data-ttu-id="166a3-380">讀取和候選視窗都是由相同的 CDXUTIMEEditBox 方法 RenderCandidateReadingWindow 所呈現。</span><span class="sxs-lookup"><span data-stu-id="166a3-380">The reading and candidate windows are rendered by the same CDXUTIMEEditBox method, RenderCandidateReadingWindow.</span></span> <span data-ttu-id="166a3-381">這兩個視窗都包含垂直配置的字串陣列，或是水準配置時的單一字串。</span><span class="sxs-lookup"><span data-stu-id="166a3-381">Both windows contain an array of strings for vertical layout, or a single string in the case of horizontal layout.</span></span> <span data-ttu-id="166a3-382">RenderCandidateReadingWindow 中的大部分程式碼都是用來放置視窗，讓視窗中的部分不會落在應用程式視窗之外，而且會被裁剪。</span><span class="sxs-lookup"><span data-stu-id="166a3-382">The bulk of the code in RenderCandidateReadingWindow is used to position the window so that no part of the window falls outside the application window and gets clipped.</span></span>

## <a name="limitations"></a><span data-ttu-id="166a3-383">限制</span><span class="sxs-lookup"><span data-stu-id="166a3-383">Limitations</span></span>

<span data-ttu-id="166a3-384">Ime 有時包含增強的功能，可改善輸入文字的便利性。</span><span class="sxs-lookup"><span data-stu-id="166a3-384">IMEs sometimes contain advanced features to improve the ease of inputting text.</span></span> <span data-ttu-id="166a3-385">下圖顯示一些在較新的 Ime 中找到的功能。</span><span class="sxs-lookup"><span data-stu-id="166a3-385">Some of the features found in newer IMEs are shown in the following figures.</span></span> <span data-ttu-id="166a3-386">這些 advanced 功能不存在於 DXUT 中。</span><span class="sxs-lookup"><span data-stu-id="166a3-386">These advanced features are not present in DXUT.</span></span> <span data-ttu-id="166a3-387">由於未定義介面可從 Ime 取得必要的資訊，因此針對這些先進的功能執行支援可能會很困難。</span><span class="sxs-lookup"><span data-stu-id="166a3-387">Implementing support for these advanced features can be challenging because there is no interface defined to obtain the necessary information from the IMEs.</span></span>

<span data-ttu-id="166a3-388">先進的繁體中文 IME 與擴充的候選清單：</span><span class="sxs-lookup"><span data-stu-id="166a3-388">Advanced Traditional Chinese IME with expanded candidate list:</span></span>

![具有展開候選清單的 advanced 繁體中文 ime](images/ime-advanced1.png)

<span data-ttu-id="166a3-390">具有一些候選項目的 Advanced 日文 IME，其中包含可描述其意義的其他文字：</span><span class="sxs-lookup"><span data-stu-id="166a3-390">Advanced Japanese IME with some candidate entries that contain additional text to describe their meanings:</span></span>

![具有某些候選項目的 advanced 日文 ime，其中包含用來描述其意義的其他文字](images/ime-advanced2.png)

<span data-ttu-id="166a3-392">包含手寫辨識系統的 Advanced 韓文 IME：</span><span class="sxs-lookup"><span data-stu-id="166a3-392">Advanced Korean IME that includes a handwriting recognition system:</span></span>

![包含手寫辨識系統的 advanced 韓文 ime](images/ime-advanced3.png)

## <a name="registry-information"></a><span data-ttu-id="166a3-394">登錄資訊</span><span class="sxs-lookup"><span data-stu-id="166a3-394">Registry Information</span></span>

<span data-ttu-id="166a3-395">當目前的 IME 較舊 CHT 不會執行 GetReadingString () 的新語音時，會檢查下列登錄資訊以決定閱讀視窗的方向。</span><span class="sxs-lookup"><span data-stu-id="166a3-395">The following registry information is checked to determine the orientation of the reading window, when the current IME is older CHT New Phonetic that doesn't implement GetReadingString().</span></span>



| <span data-ttu-id="166a3-396">Key</span><span class="sxs-lookup"><span data-stu-id="166a3-396">Key</span></span>                                                           | <span data-ttu-id="166a3-397">值</span><span class="sxs-lookup"><span data-stu-id="166a3-397">Value</span></span>            |
|---------------------------------------------------------------|------------------|
| <span data-ttu-id="166a3-398">HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="166a3-398">HKCU\\software\\microsoft\\windows\\currentversion\\IME\_Name</span></span> | <span data-ttu-id="166a3-399">鍵盤對應</span><span class="sxs-lookup"><span data-stu-id="166a3-399">keyboard mapping</span></span> |



 

<span data-ttu-id="166a3-400">其中： \_ 如果 ime 檔案版本是5.1 或更新版本，則會 MSTCIPH ime 名稱; 否則輸入 \_ 名稱為 TINTLGNT。</span><span class="sxs-lookup"><span data-stu-id="166a3-400">Where: IME\_Name is MSTCIPH if the IME file version is 5.1 or later; otherwise IME\_Name is TINTLGNT.</span></span>

<span data-ttu-id="166a3-401">讀取視窗的方向是水準的，如果其中一個：</span><span class="sxs-lookup"><span data-stu-id="166a3-401">The orientation of reading window is horizontal if either:</span></span>

-   <span data-ttu-id="166a3-402">IME 是版本5.0，而鍵盤對應值為0x22 或0x23</span><span class="sxs-lookup"><span data-stu-id="166a3-402">The IME is version 5.0 and keyboard mapping value is 0x22 or 0x23</span></span>
-   <span data-ttu-id="166a3-403">IME 是版本5.1 或5.2 版，而鍵盤對應值為0x22、0x23 或0x24。</span><span class="sxs-lookup"><span data-stu-id="166a3-403">The IME is version 5.1 or version 5.2 and keyboard mapping value is 0x22, 0x23 or 0x24.</span></span>

<span data-ttu-id="166a3-404">如果兩個條件都不符合，讀取視窗會垂直。</span><span class="sxs-lookup"><span data-stu-id="166a3-404">If neither condition is met, the reading window is vertical.</span></span>

## <a name="appendix-a-cht-versions-per-operating-system"></a><span data-ttu-id="166a3-405">附錄 A：每個作業系統的 CHT 版本</span><span class="sxs-lookup"><span data-stu-id="166a3-405">Appendix A: CHT Versions per Operating System</span></span>



| <span data-ttu-id="166a3-406">作業系統</span><span class="sxs-lookup"><span data-stu-id="166a3-406">Operating System</span></span>           | <span data-ttu-id="166a3-407">CHT IME 版本</span><span class="sxs-lookup"><span data-stu-id="166a3-407">CHT IME Version</span></span> |
|----------------------------|-----------------|
| <span data-ttu-id="166a3-408">Windows 98</span><span class="sxs-lookup"><span data-stu-id="166a3-408">Windows 98</span></span>                 | <span data-ttu-id="166a3-409">4.2</span><span class="sxs-lookup"><span data-stu-id="166a3-409">4.2</span></span>             |
| <span data-ttu-id="166a3-410">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="166a3-410">Windows 2000</span></span>               | <span data-ttu-id="166a3-411">4.3</span><span class="sxs-lookup"><span data-stu-id="166a3-411">4.3</span></span>             |
| <span data-ttu-id="166a3-412">未知</span><span class="sxs-lookup"><span data-stu-id="166a3-412">unknown</span></span>                    | <span data-ttu-id="166a3-413">4.4</span><span class="sxs-lookup"><span data-stu-id="166a3-413">4.4</span></span>             |
| <span data-ttu-id="166a3-414">Windows ME</span><span class="sxs-lookup"><span data-stu-id="166a3-414">Windows ME</span></span>                 | <span data-ttu-id="166a3-415">5.0</span><span class="sxs-lookup"><span data-stu-id="166a3-415">5.0</span></span>             |
| <span data-ttu-id="166a3-416">Office XP</span><span class="sxs-lookup"><span data-stu-id="166a3-416">Office XP</span></span>                  | <span data-ttu-id="166a3-417">5.1</span><span class="sxs-lookup"><span data-stu-id="166a3-417">5.1</span></span>             |
| <span data-ttu-id="166a3-418">Windows XP</span><span class="sxs-lookup"><span data-stu-id="166a3-418">Windows XP</span></span>                 | <span data-ttu-id="166a3-419">5.2</span><span class="sxs-lookup"><span data-stu-id="166a3-419">5.2</span></span>             |
| <span data-ttu-id="166a3-420">獨立 web 可下載檔案</span><span class="sxs-lookup"><span data-stu-id="166a3-420">Standalone web downloadble</span></span> | <span data-ttu-id="166a3-421">6.0</span><span class="sxs-lookup"><span data-stu-id="166a3-421">6.0</span></span>             |



 

## <a name="further-information"></a><span data-ttu-id="166a3-422">詳細資訊</span><span class="sxs-lookup"><span data-stu-id="166a3-422">Further Information</span></span>

<span data-ttu-id="166a3-423">如需相關資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="166a3-423">For additional information, see the following:</span></span>

-   [<span data-ttu-id="166a3-424">安裝和使用輸入法編輯器</span><span class="sxs-lookup"><span data-stu-id="166a3-424">Installing and Using Input Method Editors</span></span>](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [<span data-ttu-id="166a3-425">國際文字顯示</span><span class="sxs-lookup"><span data-stu-id="166a3-425">International Text Display</span></span>](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [<span data-ttu-id="166a3-426">Unicode 協會</span><span class="sxs-lookup"><span data-stu-id="166a3-426">The Unicode Consortium</span></span>](https://www.unicode.org/)
-   <span data-ttu-id="166a3-427">開發國際軟體。</span><span class="sxs-lookup"><span data-stu-id="166a3-427">Developing International Software.</span></span> <span data-ttu-id="166a3-428">Dr. 國際化。</span><span class="sxs-lookup"><span data-stu-id="166a3-428">Dr. International.</span></span> <span data-ttu-id="166a3-429">第 2 ed。</span><span class="sxs-lookup"><span data-stu-id="166a3-429">2nd ed.</span></span> <span data-ttu-id="166a3-430">華盛頓州 Redmond，WA： Microsoft 按下，2003。</span><span class="sxs-lookup"><span data-stu-id="166a3-430">Redmond, WA: Microsoft Press, 2003.</span></span>

## <a name="getreadingstring"></a><span data-ttu-id="166a3-431">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="166a3-431">GetReadingString</span></span>

<span data-ttu-id="166a3-432">取得讀取字串資訊。</span><span class="sxs-lookup"><span data-stu-id="166a3-432">Gets reading string information.</span></span>

<span data-ttu-id="166a3-433">**參數**</span><span class="sxs-lookup"><span data-stu-id="166a3-433">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="166a3-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="166a3-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="166a3-435">\[在 [ \] 輸入內容] 中。</span><span class="sxs-lookup"><span data-stu-id="166a3-435">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span><span class="sxs-lookup"><span data-stu-id="166a3-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span></span>
</dt> <dd>

<span data-ttu-id="166a3-437">\[在 \] WCHAR 中的 lpwReadingBuf 長度。</span><span class="sxs-lookup"><span data-stu-id="166a3-437">\[in\] Length of lpwReadingBuf, in WCHAR.</span></span> <span data-ttu-id="166a3-438">如果是零，則表示查詢讀取緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="166a3-438">If it is zero, it means query reading buffer length.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span><span class="sxs-lookup"><span data-stu-id="166a3-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span></span> 
</dt> <dd>

<span data-ttu-id="166a3-440">\[out 傳回 \] 讀取字串 (不是零的結束) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-440">\[out\] Return reading string (not zero end).</span></span>

</dd> <dt>

<span data-ttu-id="166a3-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span><span class="sxs-lookup"><span data-stu-id="166a3-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="166a3-442">\[\]如果有的話，會傳回讀取字串中錯誤字元的索引。</span><span class="sxs-lookup"><span data-stu-id="166a3-442">\[out\] Return index of error character in the reading string if there is.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span><span class="sxs-lookup"><span data-stu-id="166a3-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span></span> 
</dt> <dd>

<span data-ttu-id="166a3-444">\[\]如果是 TRUE，則讀取 UI 是垂直的。</span><span class="sxs-lookup"><span data-stu-id="166a3-444">\[out\] If it is TRUE, reading UI is vertical.</span></span> <span data-ttu-id="166a3-445">否則，水準 puMaxReadingLen。</span><span class="sxs-lookup"><span data-stu-id="166a3-445">Otherwise, horizontal puMaxReadingLen.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span><span class="sxs-lookup"><span data-stu-id="166a3-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span></span> 
</dt> <dd>

<span data-ttu-id="166a3-447">\[\]讀取 UI 長度。</span><span class="sxs-lookup"><span data-stu-id="166a3-447">\[out\] The reading UI length.</span></span> <span data-ttu-id="166a3-448">最大讀取長度不是固定的;它不僅取決於鍵盤配置，也取決於輸入模式 (例如，內部程式碼、代理輸入) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-448">The max reading length is not fixed; it depends not only on keyboard layout, but also on input mode (for example, internal code, surrogate input).</span></span>

</dd> </dl>

<span data-ttu-id="166a3-449">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="166a3-449">**Return Values**</span></span>

<span data-ttu-id="166a3-450">讀取字串長度。</span><span class="sxs-lookup"><span data-stu-id="166a3-450">The reading string length.</span></span>

<span data-ttu-id="166a3-451">**備註**</span><span class="sxs-lookup"><span data-stu-id="166a3-451">**Remarks**</span></span>

<span data-ttu-id="166a3-452">如果傳回值大於 uReadingBufLen 的值，則所有輸出參數都是未定義的。</span><span class="sxs-lookup"><span data-stu-id="166a3-452">If the return value is greater than the value of uReadingBufLen, then all output parameters are undefined.</span></span>

<span data-ttu-id="166a3-453">此函式會在 CHT IME 6.0 或更新版本中執行，並可在輸入法模組控制碼上以 GetProcAddress 方式取得。ImmGetIMEFileName 和 LoadLibrary 可以取得輸入法模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="166a3-453">This function is implemented in CHT IME 6.0 or later, and can be acquired by GetProcAddress on an IME module handle; the IME module handle can be acquired by ImmGetIMEFileName and LoadLibrary.</span></span>

<span data-ttu-id="166a3-454">**需求**</span><span class="sxs-lookup"><span data-stu-id="166a3-454">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="166a3-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**頭**</span><span class="sxs-lookup"><span data-stu-id="166a3-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="166a3-456">宣告于 Imm. h 中。</span><span class="sxs-lookup"><span data-stu-id="166a3-456">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**匯入程式庫**</span><span class="sxs-lookup"><span data-stu-id="166a3-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="166a3-458">使用 Imm。</span><span class="sxs-lookup"><span data-stu-id="166a3-458">Use Imm.lib.</span></span>

</dd> </dl>

## <a name="showreadingwindow"></a><span data-ttu-id="166a3-459">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="166a3-459">ShowReadingWindow</span></span>

<span data-ttu-id="166a3-460">顯示 (或隱藏讀取視窗) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-460">Show (or hide) the reading window.</span></span>

<span data-ttu-id="166a3-461">**參數**</span><span class="sxs-lookup"><span data-stu-id="166a3-461">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="166a3-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="166a3-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="166a3-463">\[在 [ \] 輸入內容] 中。</span><span class="sxs-lookup"><span data-stu-id="166a3-463">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="166a3-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span></span> 
</dt> <dd>

<span data-ttu-id="166a3-465">\[\]將設定為 TRUE 以顯示閱讀視窗 (或 FALSE，將它隱藏) 。</span><span class="sxs-lookup"><span data-stu-id="166a3-465">\[in\] Set to TRUE to show the reading window (or FALSE to hide it).</span></span>

</dd> </dl>

<span data-ttu-id="166a3-466">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="166a3-466">**Return Values**</span></span>

<span data-ttu-id="166a3-467">**備註**</span><span class="sxs-lookup"><span data-stu-id="166a3-467">**Remarks**</span></span>

<span data-ttu-id="166a3-468">如果成功則傳回 TRUE，否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="166a3-468">Return TRUE if successful or FALSE if otherwise.</span></span>

<span data-ttu-id="166a3-469">**需求**</span><span class="sxs-lookup"><span data-stu-id="166a3-469">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="166a3-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**頭**</span><span class="sxs-lookup"><span data-stu-id="166a3-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="166a3-471">宣告于 Imm. h 中。</span><span class="sxs-lookup"><span data-stu-id="166a3-471">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="166a3-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**匯入程式庫**</span><span class="sxs-lookup"><span data-stu-id="166a3-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="166a3-473">使用 Imm。</span><span class="sxs-lookup"><span data-stu-id="166a3-473">Use Imm.lib.</span></span>

</dd> </dl>