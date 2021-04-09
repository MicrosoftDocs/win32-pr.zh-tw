---
description: 本節說明 Windows 中的技術，可讓您在 C 或 c + + 型 Microsoft Win32 應用程式中支援國際市場的許多文化特性和書寫語言。
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Windows 應用程式的國際化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f6e4952c94af3b14dc0e8f4f135c1cc0cebafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690844"
---
# <a name="internationalization-for-windows-applications"></a><span data-ttu-id="4a356-103">Windows 應用程式的國際化</span><span class="sxs-lookup"><span data-stu-id="4a356-103">Internationalization for Windows Applications</span></span>

<span data-ttu-id="4a356-104">之前稱為「國際支援」 () </span><span class="sxs-lookup"><span data-stu-id="4a356-104">(Formerly titled "International Support")</span></span>

<span data-ttu-id="4a356-105">本節說明 Windows 中的技術，可讓您在 C 或 c + + 型 Microsoft Win32 應用程式中支援國際市場的許多文化特性和書寫語言。</span><span class="sxs-lookup"><span data-stu-id="4a356-105">This section describes the technologies in Windows that enable you to support the many cultures and written languages of the international marketplace in your C or C++ based Microsoft Win32 application.</span></span>

<span data-ttu-id="4a356-106">Windows 已成為全球客戶的基本平臺。</span><span class="sxs-lookup"><span data-stu-id="4a356-106">Windows has become an essential platform for customers worldwide.</span></span> <span data-ttu-id="4a356-107">國際使用者期待的解決方案是針對其在世界各地的語言和區域進行調整。</span><span class="sxs-lookup"><span data-stu-id="4a356-107">International users expect solutions that are adapted to their languages and regions around the world.</span></span> <span data-ttu-id="4a356-108">在本節中，您將找到開發多語系、多重文化和多網站解決方案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a356-108">In this section, you will find the information you need to develop multilanguage, multicultural, and multi-site solutions.</span></span> <span data-ttu-id="4a356-109">Windows 內建的國際支援可讓您以比以往更少的工程額外負荷來實行許多案例。</span><span class="sxs-lookup"><span data-stu-id="4a356-109">The international support built into Windows empowers you to implement many scenarios with less engineering overhead than ever before.</span></span>

<span data-ttu-id="4a356-110">開發全球化應用程式需要使用許多服務和工具。</span><span class="sxs-lookup"><span data-stu-id="4a356-110">The development of world-ready applications requires the use of many services and tools.</span></span> <span data-ttu-id="4a356-111">Windows 包含的功能可讓您開發下列解決方案：</span><span class="sxs-lookup"><span data-stu-id="4a356-111">Windows contains features that enable you to develop solutions that:</span></span>

- <span data-ttu-id="4a356-112">支援世界各地使用者的不同語言特定和地區設定特有的需求 (包括特製化文字支援、排序行為、日期和時間格式，以及鍵盤配置) 。</span><span class="sxs-lookup"><span data-stu-id="4a356-112">Support the different language-specific and locale-specific needs of users around the world (including specialized text support, sorting behavior, date and time formatting, and keyboard layouts).</span></span> <span data-ttu-id="4a356-113"> (需詳細資訊，請參閱 [國家語言支援知識中心](./national-language-support-reference.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="4a356-113">(For more information, see [National Language Support Knowledge Center](./national-language-support-reference.md).)</span></span>
- <span data-ttu-id="4a356-114">全球化 (可從單一二進位影像部署) ，而且可以當地語系化 (可以針對特定的當地市場) 進行調整。</span><span class="sxs-lookup"><span data-stu-id="4a356-114">Are globalized (can be deployed worldwide from a single binary image) and can be localized (able to be adapted for specific local markets).</span></span> <span data-ttu-id="4a356-115"> (需詳細資訊，請參閱 [多語系消費者介面](./multilingual-user-interface.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="4a356-115">(For more information, see [Multilingual User Interface](./multilingual-user-interface.md).)</span></span>
- <span data-ttu-id="4a356-116">顯示國際字型和文字，並允許使用者指定所需的字型。</span><span class="sxs-lookup"><span data-stu-id="4a356-116">Display international fonts and text, and allow users to specify the font they want.</span></span> <span data-ttu-id="4a356-117"> (需詳細資訊，請參閱 [Windows 中的腳本與字型支援](/globalization/input/font-support)) 。</span><span class="sxs-lookup"><span data-stu-id="4a356-117">(For more information, see [Script and Font Support in Windows](/globalization/input/font-support).)</span></span>
- <span data-ttu-id="4a356-118">允許使用者使用標準鍵盤輸入複雜的字元和符號。</span><span class="sxs-lookup"><span data-stu-id="4a356-118">Permit the user to enter complex characters and symbols with a standard keyboard.</span></span>
- <span data-ttu-id="4a356-119">透過 Unicode 和傳統字元集，提供許多不同書寫語言的支援。</span><span class="sxs-lookup"><span data-stu-id="4a356-119">Provide support for many different written languages through Unicode and traditional character sets.</span></span>
- <span data-ttu-id="4a356-120">探索使用者的語言輸入，並量身打造您的應用程式所提供的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="4a356-120">Discover the language input by a user, and tailor the user experience provided by your application.</span></span> <span data-ttu-id="4a356-121"> (需詳細資訊，請參閱 [在 windows 中撰寫可供世界用的應用程式： windows 中的擴充語言服務](./using-extended-linguistic-services.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="4a356-121">(For more information, see [Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md).)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4a356-122">本章節內容</span><span class="sxs-lookup"><span data-stu-id="4a356-122">In this Section</span></span>

<span data-ttu-id="4a356-123">本章節記載了下列國際支援技術。</span><span class="sxs-lookup"><span data-stu-id="4a356-123">The following international support technologies are documented in this section.</span></span> <span data-ttu-id="4a356-124">這些應用程式可使用這些主要案例來列出它們。</span><span class="sxs-lookup"><span data-stu-id="4a356-124">They are listed with some key scenarios for which they can be used.</span></span>

- [<span data-ttu-id="4a356-125">使用國際 Windows 開發開始使用</span><span class="sxs-lookup"><span data-stu-id="4a356-125">Getting Started with International Windows Development</span></span>](getting-started-with-international-development.md)

    <span data-ttu-id="4a356-126">說明如何開始建立可供使用的全球應用程式，並提供教學課程來說明撰寫全域軟體的一般工作。</span><span class="sxs-lookup"><span data-stu-id="4a356-126">Describes how to get started creating world-ready applications, and provides a tutorial illustrating a common task in writing global software.</span></span>

    <span data-ttu-id="4a356-127">常見案例：</span><span class="sxs-lookup"><span data-stu-id="4a356-127">Common Scenarios:</span></span>

    - <span data-ttu-id="4a356-128">判斷要採取的途徑，以瞭解如何開發國際軟體。</span><span class="sxs-lookup"><span data-stu-id="4a356-128">Determine a path to take to learn how to develop international software.</span></span>
    - <span data-ttu-id="4a356-129">探索 Microsoft Windows 軟體開發套件 (SDK) 提供的國際化技術。</span><span class="sxs-lookup"><span data-stu-id="4a356-129">Discover the internationalization technologies available in the Microsoft Windows Software Development Kit (SDK).</span></span>
    - <span data-ttu-id="4a356-130">遵循採用現有單一語言應用程式的教學課程，並新增其他語言的支援。</span><span class="sxs-lookup"><span data-stu-id="4a356-130">Follow a tutorial that takes an existing monolingual application and adds support for additional languages.</span></span>

- [<span data-ttu-id="4a356-131">全球化服務</span><span class="sxs-lookup"><span data-stu-id="4a356-131">Globalization Services</span></span>](globalization-services.md)

    <span data-ttu-id="4a356-132">描述 [ (ELS) 的擴充語言服務 ](extended-linguistic-services.md)，這可讓您探索撰寫文字和使用者輸入的語言，以及 [ (NLS) 的國家語言支援 ](national-language-support.md)，這可讓應用程式使用地區設定資訊來顯示區分文化特性的資訊 (例如時間、日期和貨幣) ，以及正確地排序字串。</span><span class="sxs-lookup"><span data-stu-id="4a356-132">Describes [Extended Linguistic Services (ELS)](extended-linguistic-services.md), which enable you to discover the language in which text and user input is written, and [National Language Support (NLS)](national-language-support.md), which enables an application to use locale information to display culture-sensitive information (such as time, dates, and currency) and properly sort strings.</span></span>

    <span data-ttu-id="4a356-133">常見案例：</span><span class="sxs-lookup"><span data-stu-id="4a356-133">Common Scenarios:</span></span>

    - <span data-ttu-id="4a356-134">探索使用者輸入的語言，以便能以可理解的語言來顯示說明內容。</span><span class="sxs-lookup"><span data-stu-id="4a356-134">Discover the language of the user's input, so that help content can be displayed in an understandable language.</span></span>
    - <span data-ttu-id="4a356-135">探索要顯示之文字中所使用的腳本。</span><span class="sxs-lookup"><span data-stu-id="4a356-135">Discover the script used in text that is to be displayed.</span></span> <span data-ttu-id="4a356-136">如果是簡體或繁體中文，請提供使用者將文字從一個文字轉譯成另一個的選項。</span><span class="sxs-lookup"><span data-stu-id="4a356-136">If it is Simplified or Traditional Chinese, offer the user the option to have the text transliterated from one to the other.</span></span>
    - <span data-ttu-id="4a356-137">允許使用者選取地區設定 () 的語言相關使用者喜好設定資訊的集合。</span><span class="sxs-lookup"><span data-stu-id="4a356-137">Permit the user to select a locale (a collection of language-related user preference information).</span></span>
    - <span data-ttu-id="4a356-138">以適當的語言和格式顯示時間、日期、行事曆資訊、貨幣和其他許多文化特性相依物件。</span><span class="sxs-lookup"><span data-stu-id="4a356-138">Display times, dates, calendar information, currency, and many other culture-dependent objects in appropriate languages and formats.</span></span>
    - <span data-ttu-id="4a356-139">依給定地區設定的使用者所預期的順序來排序字串。</span><span class="sxs-lookup"><span data-stu-id="4a356-139">Sort strings into the order expected by the user of a given locale.</span></span>

- [<span data-ttu-id="4a356-140">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="4a356-140">Input Method Manager</span></span>](input-method-manager.md)

    <span data-ttu-id="4a356-141">描述應用程式用來與輸入方法編輯器通訊的技術 (IME) 。</span><span class="sxs-lookup"><span data-stu-id="4a356-141">Describes the technology used by an application to communicate with an input method editor (IME).</span></span> <span data-ttu-id="4a356-142">IME 可讓電腦使用者使用標準鍵盤來輸入複雜的字元和符號。</span><span class="sxs-lookup"><span data-stu-id="4a356-142">The IME allows computer users to enter complex characters and symbols by using a standard keyboard.</span></span>

    <span data-ttu-id="4a356-143">常見案例：</span><span class="sxs-lookup"><span data-stu-id="4a356-143">Common Scenario:</span></span>

    - <span data-ttu-id="4a356-144">允許使用者使用標準鍵盤來輸入日文中文字元。</span><span class="sxs-lookup"><span data-stu-id="4a356-144">Permit the user to use a standard keyboard to enter Japanese kanji characters.</span></span>

- [<span data-ttu-id="4a356-145">國際字型和文字顯示</span><span class="sxs-lookup"><span data-stu-id="4a356-145">International Fonts and Text Display</span></span>](international-fonts-and-text-display.md)

    <span data-ttu-id="4a356-146">描述 Windows 平臺針對國際字型提供的支援、國際文字，以及精細的印刷樣式。</span><span class="sxs-lookup"><span data-stu-id="4a356-146">Describes the support provided by the Windows platform for international fonts, international text, and fine typography.</span></span>

    <span data-ttu-id="4a356-147">常見案例：</span><span class="sxs-lookup"><span data-stu-id="4a356-147">Common Scenarios:</span></span>

    - <span data-ttu-id="4a356-148">允許使用者根據字元集選取國際字型。</span><span class="sxs-lookup"><span data-stu-id="4a356-148">Allow the user to select international fonts based on character set.</span></span>
    - <span data-ttu-id="4a356-149">顯示國際文字。</span><span class="sxs-lookup"><span data-stu-id="4a356-149">Display international text.</span></span>
    - <span data-ttu-id="4a356-150">處理複雜的腳本，包括雙向轉譯、內容成形，以及連 (Uniscribe) 的連字。</span><span class="sxs-lookup"><span data-stu-id="4a356-150">Process complex scripts, including bidirectional rendering, contextual shaping, and ligatures (Uniscribe).</span></span>
    - <span data-ttu-id="4a356-151">針對精細的印刷樣式， (Uniscribe) 提供高度的控制。</span><span class="sxs-lookup"><span data-stu-id="4a356-151">Allow a high degree of control for fine typography (Uniscribe).</span></span>

- [<span data-ttu-id="4a356-152">多語系使用者介面</span><span class="sxs-lookup"><span data-stu-id="4a356-152">Multilingual User Interface</span></span>](multilingual-user-interface.md)

    <span data-ttu-id="4a356-153">描述應用程式如何將語言相依的資源與語言中立的程式碼分開，以提供支援的使用者介面語言。</span><span class="sxs-lookup"><span data-stu-id="4a356-153">Describes how applications can separate language-dependent resources from language-neutral code for supported user interface languages.</span></span>

    <span data-ttu-id="4a356-154">常見案例：</span><span class="sxs-lookup"><span data-stu-id="4a356-154">Common Scenarios:</span></span>

    - <span data-ttu-id="4a356-155">建立應用程式的區域或全球單一部署映射。</span><span class="sxs-lookup"><span data-stu-id="4a356-155">Create regional or worldwide single deployment images of an application.</span></span>
    - <span data-ttu-id="4a356-156">藉由更新應用程式資源來當地語系化方案，而不需要變更應用程式原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="4a356-156">Localize a solution by updating application resources with no change to application source code.</span></span>
    - <span data-ttu-id="4a356-157">允許使用者在執行時間從某個 UI 語言切換至另一種語言。</span><span class="sxs-lookup"><span data-stu-id="4a356-157">Permit users to switch from one UI language to another at run time.</span></span>

- [<span data-ttu-id="4a356-158">Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="4a356-158">Unicode and Character Sets</span></span>](unicode-and-character-sets.md)

    <span data-ttu-id="4a356-159">描述應用程式如何利用 Unicode，也就是使用16位程式碼值的全球字元編碼標準，來代表新式運算中使用的所有字元，包括用於發佈的技術符號和特殊字元。</span><span class="sxs-lookup"><span data-stu-id="4a356-159">Describes how applications can take advantage of Unicode, the worldwide character-encoding standard that uses 16-bit code values to represent all the characters used in modern computing, including technical symbols and special characters used in publishing.</span></span>

    <span data-ttu-id="4a356-160">常見案例：</span><span class="sxs-lookup"><span data-stu-id="4a356-160">Common Scenarios:</span></span>

    - <span data-ttu-id="4a356-161">透過 Unicode 支援國際 marketplace 的許多不同語言。</span><span class="sxs-lookup"><span data-stu-id="4a356-161">Support the many different languages of the international marketplace through Unicode.</span></span>
    - <span data-ttu-id="4a356-162">必要時，將 Unicode 字元轉換成其他字元集或從中轉換。</span><span class="sxs-lookup"><span data-stu-id="4a356-162">Convert Unicode characters to and from other character sets, when necessary.</span></span>

- [<span data-ttu-id="4a356-163">安全性考慮：國際功能</span><span class="sxs-lookup"><span data-stu-id="4a356-163">Security Considerations: International Features</span></span>](security-considerations--international-features.md)

    <span data-ttu-id="4a356-164">提供與國際開發支援功能相關之安全性考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a356-164">Provides information about security considerations related to international development support features.</span></span>

    <span data-ttu-id="4a356-165">安全性資訊適用于所有案例。</span><span class="sxs-lookup"><span data-stu-id="4a356-165">The security information pertains to all scenarios.</span></span>

## <a name="related-international-technologies"></a><span data-ttu-id="4a356-166">相關的國際技術</span><span class="sxs-lookup"><span data-stu-id="4a356-166">Related International Technologies</span></span>

<span data-ttu-id="4a356-167">國際開發支援也適用于以 managed 程式碼撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4a356-167">International development support is also available for applications written in managed code.</span></span> <span data-ttu-id="4a356-168">如果您正在針對 .NET Framework 進行開發，您將需要下列部分或全部：</span><span class="sxs-lookup"><span data-stu-id="4a356-168">If you are developing for the .NET Framework, you will need some or all of these:</span></span>

- <span data-ttu-id="4a356-169">「 [全球化」命名空間](/dotnet/api/system.globalization) 包含類別，這些類別會定義與文化特性相關的資訊，並提供先進的全球化函數。</span><span class="sxs-lookup"><span data-stu-id="4a356-169">The [System.Globalization Namespace](/dotnet/api/system.globalization) contains classes that define culture-related information and provide advanced globalization functions.</span></span>
- <span data-ttu-id="4a356-170">System.string [命名空間](/dotnet/api/system.text) 包含代表字元編碼、轉換字元區塊，以及操作和格式化字串物件的類別。</span><span class="sxs-lookup"><span data-stu-id="4a356-170">The [System.Text Namespace](/dotnet/api/system.text) contains classes that represent character encodings, convert blocks of characters, and manipulate and format String objects.</span></span>
