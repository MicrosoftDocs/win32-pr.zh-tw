---
description: 本主題提供建立支援多個市場之程式碼所採取的動作。 當您評估組建時，請將這些語句視為程式碼設計和計量的指南。
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: 國際化檢查清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b18ef8cf88efa8d496d19c0b66208cd44abaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847688"
---
# <a name="internationalization-checklist"></a><span data-ttu-id="a5472-104">國際化檢查清單</span><span class="sxs-lookup"><span data-stu-id="a5472-104">Internationalization Checklist</span></span>

<span data-ttu-id="a5472-105">本主題提供建立支援多個市場之程式碼所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="a5472-105">This topic provides actions to take to create code that supports multiple markets.</span></span> <span data-ttu-id="a5472-106">當您評估組建時，請將這些語句視為程式碼設計和計量的指南。</span><span class="sxs-lookup"><span data-stu-id="a5472-106">Consider these statements as a guide during code design, and as metrics when you evaluate the builds.</span></span>

-   <span data-ttu-id="a5472-107">建立可考慮從一開始就進行國際考慮的程式規格。</span><span class="sxs-lookup"><span data-stu-id="a5472-107">Create program specifications that account for international considerations from the outset.</span></span>
    -   <span data-ttu-id="a5472-108">將圖示和點陣圖設計成有意義且不具冒犯性的目標市場，且不包含文字。</span><span class="sxs-lookup"><span data-stu-id="a5472-108">Design icons and bitmaps to be meaningful and not offensive in your target markets, and to not contain text.</span></span>
    -   <span data-ttu-id="a5472-109">設計功能表和對話方塊，以留出空間供文字展開之用。</span><span class="sxs-lookup"><span data-stu-id="a5472-109">Design menus and dialog boxes to leave room for text expansion.</span></span> <span data-ttu-id="a5472-110">例如，英文字串在轉譯成德文或荷蘭文時，通常會擴展40%。</span><span class="sxs-lookup"><span data-stu-id="a5472-110">For example, English strings often expand by 40% when translated into German or Dutch.</span></span>
    -   <span data-ttu-id="a5472-111">請勿在 UI 元素或訊息中使用俚語或特定文化特性的參考。</span><span class="sxs-lookup"><span data-stu-id="a5472-111">Do not use slang or culturally-specific references in UI elements or messages.</span></span>
    -   <span data-ttu-id="a5472-112">建立可在國際鍵盤上存取的快捷方式按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="a5472-112">Create shortcut key combinations that are accessible on international keyboards.</span></span> <span data-ttu-id="a5472-113">例如，請避免使用標點符號字元索引鍵做為快速鍵，因為它們不一定會出現在國際鍵盤上或由使用者輕鬆產生。</span><span class="sxs-lookup"><span data-stu-id="a5472-113">For example, avoid using punctuation character keys as shortcut keys because they are not always found on international keyboards or easily produced by the user.</span></span> <span data-ttu-id="a5472-114">如需鍵盤配置的範例，請參閱 [Windows 鍵盤佈局](https://msdn.microsoft.com/goglobal/bb964651.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a5472-114">For examples of keyboard layouts, see [Windows Keyboard Layouts](https://msdn.microsoft.com/goglobal/bb964651.aspx).</span></span>
    -   <span data-ttu-id="a5472-115">考慮影響功能設計的當地法律，例如政府機構購買軟體以支援多種官方語言的需求。</span><span class="sxs-lookup"><span data-stu-id="a5472-115">Consider local laws affecting feature designs, such as requirements that government entities purchase software that supports multiple official languages.</span></span>
    -   <span data-ttu-id="a5472-116">開發可支援貴組織國際 UI 標準和設計決策的協力廠商協定。</span><span class="sxs-lookup"><span data-stu-id="a5472-116">Develop third-party agreements that support your organization's international UI standards and design decisions.</span></span>
    -   <span data-ttu-id="a5472-117">在必須翻譯的使用者介面字串中使用一致的術語。</span><span class="sxs-lookup"><span data-stu-id="a5472-117">Use consistent terminology in user interface strings that must be translated.</span></span>

<!-- -->

-   <span data-ttu-id="a5472-118">建立與地區設定無關的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5472-118">Create code that is independent of locale.</span></span>
    -   <span data-ttu-id="a5472-119">請勿將字串串連成表單句子。</span><span class="sxs-lookup"><span data-stu-id="a5472-119">Don't concatenate strings to form sentences.</span></span>
    -   <span data-ttu-id="a5472-120">請勿在多個內容中使用指定的字串變數，例如在不同的訊息和提示中重複使用句子片段，因為這類字串可能不容易轉譯。</span><span class="sxs-lookup"><span data-stu-id="a5472-120">Don't use a given string variable in more than one context, such as reusing a sentence fragment in different messages and prompts, because such strings may not be easy to translate.</span></span>
    -   <span data-ttu-id="a5472-121">使用批註的檔字串來提供翻譯人員的內容，並清楚地標示不應當地語系化的字串或字元。</span><span class="sxs-lookup"><span data-stu-id="a5472-121">Document strings using comments to provide context for translators, and clearly mark strings or characters that should not be localized.</span></span>
    -   <span data-ttu-id="a5472-122">請勿使用採用特定語言的硬式編碼字元常數、數值常數、螢幕位置、檔案名或路徑。</span><span class="sxs-lookup"><span data-stu-id="a5472-122">Don't use hard-coded character constants, numeric constants, screen positions, filenames, or pathnames that presume a particular language.</span></span>
    -   <span data-ttu-id="a5472-123">讓緩衝區夠大以容納轉譯的字串。</span><span class="sxs-lookup"><span data-stu-id="a5472-123">Make buffers large enough to hold translated strings.</span></span>
    -   <span data-ttu-id="a5472-124">允許資料的輸入格式會因地區設定而異，例如日期、時間和貨幣。</span><span class="sxs-lookup"><span data-stu-id="a5472-124">Allow the input of data with formats that vary by locale, such as dates, times, and currencies.</span></span>
    -   <span data-ttu-id="a5472-125">使用適用于特定地區設定的紙張大小、信封大小和其他預設值。</span><span class="sxs-lookup"><span data-stu-id="a5472-125">Use paper size, envelope size, and other defaults that are appropriate to a given locale.</span></span>
    -   <span data-ttu-id="a5472-126">確定每個語言版本都可以讀取其他版本所建立的檔。</span><span class="sxs-lookup"><span data-stu-id="a5472-126">Ensure that each language edition can read documents created by the other editions.</span></span>
    -   <span data-ttu-id="a5472-127">如有必要，請提供地區設定特定硬體的支援。</span><span class="sxs-lookup"><span data-stu-id="a5472-127">Provide support for locale-specific hardware, if necessary.</span></span>
    -   <span data-ttu-id="a5472-128">將不會套用至國際市場的功能設定為可輕鬆停用的實作為選項。</span><span class="sxs-lookup"><span data-stu-id="a5472-128">Configure features that don't apply to international markets as implementation options that can be disabled easily.</span></span>

<!-- -->

-   <span data-ttu-id="a5472-129">建立利用 Microsoft Windows 所提供之國際功能的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5472-129">Create code that takes advantage of international functionality offered by Microsoft Windows.</span></span>
    -   <span data-ttu-id="a5472-130">使用系統所攜帶的國際資訊 (國語言支援) 。</span><span class="sxs-lookup"><span data-stu-id="a5472-130">Use international information carried by the system (National Language Support).</span></span>
    -   <span data-ttu-id="a5472-131">使用系統函數進行排序、案例轉換和字串對應。</span><span class="sxs-lookup"><span data-stu-id="a5472-131">Use system functions for sorting, case conversion, and string mapping.</span></span>
    -   <span data-ttu-id="a5472-132">使用一般文字版面配置函數。</span><span class="sxs-lookup"><span data-stu-id="a5472-132">Use generic text layout functions.</span></span>
    -   <span data-ttu-id="a5472-133">在主控台中回應國際設定的變更。</span><span class="sxs-lookup"><span data-stu-id="a5472-133">Respond to changes to international settings in Control Panel.</span></span>
    -   <span data-ttu-id="a5472-134">處理 WM \_ INPUTLANGCHANGEREQUEST 訊息。</span><span class="sxs-lookup"><span data-stu-id="a5472-134">Handle the WM\_INPUTLANGCHANGEREQUEST message.</span></span>
    -   <span data-ttu-id="a5472-135">在東亞版中支援輸入方法編輯器、垂直文字和分行規則。</span><span class="sxs-lookup"><span data-stu-id="a5472-135">Support input method editors, vertical text, and line-breaking rules in East Asian editions.</span></span>

<!-- -->

-   <span data-ttu-id="a5472-136">從一組來源檔案編譯器的所有國際版本。</span><span class="sxs-lookup"><span data-stu-id="a5472-136">Compile all international editions of the program from one set of source files.</span></span>
    -   <span data-ttu-id="a5472-137">最小化或消除需要針對不同語言版本重新編譯程式碼的機制。</span><span class="sxs-lookup"><span data-stu-id="a5472-137">Minimize or eliminate mechanisms that require code to be recompiled for different language editions.</span></span>
    -   <span data-ttu-id="a5472-138">在 Windows 資源檔中儲存可當地語系化的專案，例如字串和圖示。</span><span class="sxs-lookup"><span data-stu-id="a5472-138">Store localizable items, such as strings and icons, in Windows resource files.</span></span>
    -   <span data-ttu-id="a5472-139">使用相同的檔案格式，將檔儲存在所有語言版本中。</span><span class="sxs-lookup"><span data-stu-id="a5472-139">Store documents in all language editions using the same file format.</span></span>

<!-- -->

-   <span data-ttu-id="a5472-140">支援不同的字元集，而不只是拉丁字母1字碼頁，數位1252。</span><span class="sxs-lookup"><span data-stu-id="a5472-140">Support different character sets, not just the Latin 1 code page, number 1252.</span></span>
    -   <span data-ttu-id="a5472-141">程式支援網路環境，在此環境中，電腦會使用不同的預設字碼頁來執行作業系統。</span><span class="sxs-lookup"><span data-stu-id="a5472-141">Program supports network environments in which computers run operating systems with different default code pages.</span></span>
    -   <span data-ttu-id="a5472-142">使用 GetCPInfoEx 來取出東亞字碼頁的前導位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="a5472-142">Use GetCPInfoEx to retrieve lead-byte ranges for East Asian code pages.</span></span>
    -   <span data-ttu-id="a5472-143">剖析東亞語言應用程式中的雙位元組字元，除非程式碼是以 Unicode 為基礎。</span><span class="sxs-lookup"><span data-stu-id="a5472-143">Parse double-byte characters in East Asian–language applications unless the code is based on Unicode.</span></span>
    -   <span data-ttu-id="a5472-144">支援 Unicode 或 Unicode 和本機字碼頁之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="a5472-144">Support Unicode or conversion between Unicode and the local code page.</span></span>
    -   <span data-ttu-id="a5472-145">請勿假設所有字元都是8位或16位。</span><span class="sxs-lookup"><span data-stu-id="a5472-145">Don't assume that all characters are 8-bit or 16-bit.</span></span>
    -   <span data-ttu-id="a5472-146">使用泛型資料類型和泛型函數原型。</span><span class="sxs-lookup"><span data-stu-id="a5472-146">Use generic data types and generic function prototypes.</span></span>
    -   <span data-ttu-id="a5472-147">使用 [字型字元集] 屬性，它會呼叫 EnumFontFamiliesEx 和 ChooseFont 通用對話方塊函式。</span><span class="sxs-lookup"><span data-stu-id="a5472-147">Use the font charset property, which calls EnumFontFamiliesEx and the ChooseFont common dialog function.</span></span>
    -   <span data-ttu-id="a5472-148">使用適用于地區設定的字型來顯示和列印文字。</span><span class="sxs-lookup"><span data-stu-id="a5472-148">Display and print text using the fonts that are appropriate for the locale.</span></span>

<!-- -->

-   <span data-ttu-id="a5472-149">測試程式的國際功能。</span><span class="sxs-lookup"><span data-stu-id="a5472-149">Test the international features of the program.</span></span>
    -   <span data-ttu-id="a5472-150">翻譯文字應符合原生喇叭的標準。</span><span class="sxs-lookup"><span data-stu-id="a5472-150">Translated text should meet the standards of native speakers.</span></span>
    -   <span data-ttu-id="a5472-151">對話方塊應適當調整大小，並在顯示不同的語言時，適當地將文字放在適當的字元上。</span><span class="sxs-lookup"><span data-stu-id="a5472-151">Dialog boxes should resize properly, and text should be hyphenated appropriately, when different languages are displayed.</span></span>
    -   <span data-ttu-id="a5472-152">針對所有翻譯語言，對話方塊、狀態列、工具列和功能表都應該放在畫面上，並在顯示的解析度設定不同的解析度時讀取 legibly。</span><span class="sxs-lookup"><span data-stu-id="a5472-152">Dialog boxes, status bars, toolbars, and menus should fit on the screen and read legibly when the display is set at different resolutions, for all translated languages.</span></span>
    -   <span data-ttu-id="a5472-153">功能表和對話方塊加速器應該是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a5472-153">Menu and dialog-box accelerators should be unique.</span></span>
    -   <span data-ttu-id="a5472-154">使用者應該能夠將非歐洲腳本的字元輸入檔、對話方塊和檔案名。</span><span class="sxs-lookup"><span data-stu-id="a5472-154">Users should be able to type characters from non-European scripts into documents, dialog boxes, and filenames.</span></span>
    -   <span data-ttu-id="a5472-155">使用者應該能夠順利剪下、貼上、儲存和列印非歐洲腳本的字元。</span><span class="sxs-lookup"><span data-stu-id="a5472-155">Users should be able to cut, paste, save, and print characters from non-European scripts successfully.</span></span>
    -   <span data-ttu-id="a5472-156">針對不同的地區設定，排序和大小寫轉換應該是正確的。</span><span class="sxs-lookup"><span data-stu-id="a5472-156">Sorting and case conversion should be accurate for different locales.</span></span>
    -   <span data-ttu-id="a5472-157">應用程式應該在 Windows 的當地語系化版本上正確運作。</span><span class="sxs-lookup"><span data-stu-id="a5472-157">The application should work correctly on localized editions of Windows.</span></span>

 

 



