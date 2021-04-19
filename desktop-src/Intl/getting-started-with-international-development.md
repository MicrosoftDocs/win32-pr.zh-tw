---
description: 本主題將協助您開始建立可供使用的應用程式，方法是指定必要條件、摘要技術，以及引入入門教學課程。
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: 使用國際 Windows 開發開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc77a86b652f1b713b29517b513cddc26ed801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992484"
---
# <a name="getting-started-with-international-windows-development"></a><span data-ttu-id="6e093-103">使用國際 Windows 開發開始使用</span><span class="sxs-lookup"><span data-stu-id="6e093-103">Getting Started with International Windows Development</span></span>

<span data-ttu-id="6e093-104">本主題將協助您開始建立可供使用的應用程式，方法是指定必要條件、摘要技術，以及引入入門教學課程。</span><span class="sxs-lookup"><span data-stu-id="6e093-104">This topic helps you get started creating world-ready applications, by specifying prerequisites, summarizing technologies, and introducing a getting-started tutorial.</span></span>

## <a name="getting-started"></a><span data-ttu-id="6e093-105">開始使用</span><span class="sxs-lookup"><span data-stu-id="6e093-105">Getting Started</span></span>

<span data-ttu-id="6e093-106">如果您為使用者撰寫單一地區設定的應用程式，即使您使用地區設定特定的假設來設計這些應用程式，也可以成功，例如以特定格式呈現日期，或以特定順序排序字串。</span><span class="sxs-lookup"><span data-stu-id="6e093-106">If you write applications for users in a single locale, those applications can be successful even if you design them with locale-specific assumptions, such as presenting dates in a particular format, or sorting strings in a particular sequence.</span></span> <span data-ttu-id="6e093-107">但現在您必須確保應用程式可以在多個國家（地區）使用不同語言和不同文化特性的使用者使用。</span><span class="sxs-lookup"><span data-stu-id="6e093-107">But now you have to ensure that your applications can be used in multiple countries, by users who have different languages and different cultures.</span></span> <span data-ttu-id="6e093-108">若要在多個地區設定中成功，應用程式必須調整為執行所在的地區設定。</span><span class="sxs-lookup"><span data-stu-id="6e093-108">To succeed in multiple locales, the applications need to adjust to the locale in which they run.</span></span> <span data-ttu-id="6e093-109">無論您是將它新增至現有的應用程式，或是將它設計成新的應用程式，這種彈性都很重要。</span><span class="sxs-lookup"><span data-stu-id="6e093-109">This flexibility is important whether you add it to an existing application, or you design it into a new application.</span></span>

<span data-ttu-id="6e093-110">本節可協助您開始進行國際開發。</span><span class="sxs-lookup"><span data-stu-id="6e093-110">This section helps you get started in international development.</span></span> <span data-ttu-id="6e093-111">其中提供的主題連結可提供國際化的先決條件。</span><span class="sxs-lookup"><span data-stu-id="6e093-111">It presents links to topics that provide prerequisite overviews of internationalization.</span></span> <span data-ttu-id="6e093-112">其中摘要說明 SDK 提供的技術，以支援全球客戶。</span><span class="sxs-lookup"><span data-stu-id="6e093-112">It summarizes the technologies that the SDK offers for support of worldwide customers.</span></span> <span data-ttu-id="6e093-113">最後，本節提供的範例應用程式可解決您在撰寫全域軟體時經常遇到的問題。</span><span class="sxs-lookup"><span data-stu-id="6e093-113">Finally, this section provides a sample application that solves a problem that you often encounter when writing global software.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6e093-114">必要條件</span><span class="sxs-lookup"><span data-stu-id="6e093-114">Prerequisites</span></span>

<span data-ttu-id="6e093-115">您應該熟悉開發 Windows 的國際軟體所產生的問題。</span><span class="sxs-lookup"><span data-stu-id="6e093-115">You should become familiar with the issues that arise in developing international software for Windows.</span></span> <span data-ttu-id="6e093-116">請從這些總覽著手。</span><span class="sxs-lookup"><span data-stu-id="6e093-116">Start with these overviews.</span></span>

-   <span data-ttu-id="6e093-117">[瞭解國際化](understanding-internationalization.md) 可解釋開發全球化應用程式的額外困難，並定義重要詞彙。</span><span class="sxs-lookup"><span data-stu-id="6e093-117">[Understanding Internationalization](understanding-internationalization.md) explains the added difficulty of developing world-ready applications, and defines key terms.</span></span>
-   <span data-ttu-id="6e093-118">「 [取得全球可用](https://msdn.microsoft.com/goglobal/bb895995.aspx) 」主題將引導您瞭解您可以流覽的指導方針和最佳作法，或視需要深入探討。</span><span class="sxs-lookup"><span data-stu-id="6e093-118">The [Get World-Ready](https://msdn.microsoft.com/goglobal/bb895995.aspx) topic leads you to guidelines and best practices that you can skim through or delve into as needed.</span></span>
-   <span data-ttu-id="6e093-119">[國際化檢查清單](internationalization-checklist.md)摘要說明建立全球化應用程式所應採取的動作。</span><span class="sxs-lookup"><span data-stu-id="6e093-119">The [Internationalization Checklist](internationalization-checklist.md) summarizes the actions you should take to create a world-ready application.</span></span>
-   <span data-ttu-id="6e093-120">安全性一直是軟體發展的問題，但是您必須在開發國際軟體時考慮其他問題。</span><span class="sxs-lookup"><span data-stu-id="6e093-120">Security is always an issue in software development, but you need to consider additional issues when developing international software.</span></span> <span data-ttu-id="6e093-121">請參閱 [安全性考慮：國際功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="6e093-121">Take a look at [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

<span data-ttu-id="6e093-122">也請留意更廣泛的文章，請參閱全球[化逐步](https://msdn.microsoft.com/globalization/mt642951)章節的「[全球開發人員中心](https://msdn.microsoft.com/globalization/mt613165)」。</span><span class="sxs-lookup"><span data-stu-id="6e093-122">Also be aware of the more extensive articles that can be found at the [Go Global Developer Center](https://msdn.microsoft.com/globalization/mt613165) in the [Globalization Step-by-Step](https://msdn.microsoft.com/globalization/mt642951) section.</span></span> <span data-ttu-id="6e093-123">當您開發國際軟體時，您會想要查閱可在該處找到的其他總覽和詳細文章。</span><span class="sxs-lookup"><span data-stu-id="6e093-123">As you develop international software, you will want to consult the additional overviews and detailed articles that can be found there.</span></span>

## <a name="learning-paths"></a><span data-ttu-id="6e093-124">學習路徑</span><span class="sxs-lookup"><span data-stu-id="6e093-124">Learning Paths</span></span>

<span data-ttu-id="6e093-125">您接下來在學習中建立國際軟體時所遵循的路徑，取決於您所面對的案例。</span><span class="sxs-lookup"><span data-stu-id="6e093-125">The path you follow next in learning to create international software depends on the scenarios you face.</span></span> <span data-ttu-id="6e093-126">下列案例是以主要區段主題（ [適用于 Windows 應用程式的國際化](international-support.md)）中引進的案例為基礎。</span><span class="sxs-lookup"><span data-stu-id="6e093-126">The following scenarios are based on those introduced in the main section topic, [Internationalization for Windows Applications](international-support.md).</span></span>

-   <span data-ttu-id="6e093-127">**建立可部署至多個語言之多個區域的應用程式。**</span><span class="sxs-lookup"><span data-stu-id="6e093-127">**Create applications that can be deployed to multiple regions in multiple languages.**</span></span>

    <span data-ttu-id="6e093-128">挑戰在於開發不需要針對每種語言或文化特性重寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e093-128">The challenge is to develop an application that does not have to be rewritten for each language or culture.</span></span>

    -   <span data-ttu-id="6e093-129">請參閱 [瞭解多語系消費者介面 (MUI) ](./about-multilingual-user-interface.md)的文章。</span><span class="sxs-lookup"><span data-stu-id="6e093-129">Read the article [Understanding Multilingual User Interface (MUI)](./about-multilingual-user-interface.md).</span></span>
    -   <span data-ttu-id="6e093-130">探索 [多語系消費者介面](multilingual-user-interface.md)的檔。</span><span class="sxs-lookup"><span data-stu-id="6e093-130">Explore the documentation for [Multilingual User Interface](multilingual-user-interface.md).</span></span>
    -   <span data-ttu-id="6e093-131">開始使用 [HELLO MUI](#the-hello-mui-application) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e093-131">Get started with the [Hello MUI](#the-hello-mui-application) application.</span></span>

-   <span data-ttu-id="6e093-132">**支援不同語言、字元集和字型的輸入和顯示。**</span><span class="sxs-lookup"><span data-stu-id="6e093-132">**Support the input and display of different languages, character sets, and fonts.**</span></span>

    <span data-ttu-id="6e093-133">您的應用程式可能需要支援多個字元集、支援複雜的腳本 (例如，用來代表希伯來文、阿拉伯文、泰文和印度文的語言) 、允許使用者從國際字型中選取，或允許使用者使用標準鍵盤來輸入字元和符號，例如日文漢字。</span><span class="sxs-lookup"><span data-stu-id="6e093-133">Your application may need to support multiple character sets, support complex scripts (such as those used to represent Hebrew, Arabic, Thai, and Indic languages), permit the user to select from international fonts, or allow the user to enter characters and symbols, such as Japanese kanji, for other languages by using a standard keyboard.</span></span>

    -   <span data-ttu-id="6e093-134">閱讀下列文章：</span><span class="sxs-lookup"><span data-stu-id="6e093-134">Read the articles:</span></span>

        -   [<span data-ttu-id="6e093-135">Windows 中的腳本與字型支援</span><span class="sxs-lookup"><span data-stu-id="6e093-135">Script and Font Support in Windows</span></span>](https://msdn.microsoft.com/globalization/mt791278)
        -   [<span data-ttu-id="6e093-136">輸入語言：鍵盤和 Ime</span><span class="sxs-lookup"><span data-stu-id="6e093-136">Input Language: Keyboards and IMEs</span></span>](https://msdn.microsoft.com/globalization/mt662332)

    -   <span data-ttu-id="6e093-137">探索以下檔：</span><span class="sxs-lookup"><span data-stu-id="6e093-137">Explore the documentation for:</span></span>

        -   [<span data-ttu-id="6e093-138">Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="6e093-138">Unicode and Character Sets</span></span>](unicode-and-character-sets.md)
        -   [<span data-ttu-id="6e093-139">國際字型和文字顯示</span><span class="sxs-lookup"><span data-stu-id="6e093-139">International Fonts and Text Display</span></span>](international-fonts-and-text-display.md)
        -   [<span data-ttu-id="6e093-140">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="6e093-140">Input Method Manager</span></span>](input-method-manager.md)

-   <span data-ttu-id="6e093-141">**以適當的格式顯示文化特性相依物件。**</span><span class="sxs-lookup"><span data-stu-id="6e093-141">**Display culture-dependent objects in appropriate formats.**</span></span>

    <span data-ttu-id="6e093-142">國際應用程式應該使用地區設定來正確地排序字串，以及顯示區分文化特性的資訊，例如時間、日期和貨幣。</span><span class="sxs-lookup"><span data-stu-id="6e093-142">International applications should use locale settings to properly sort strings, and to display culture-sensitive information, such as time, dates, and currency.</span></span>

    -   <span data-ttu-id="6e093-143">探索「 [國家語言支援知識中心](./national-language-support-reference.md)」。</span><span class="sxs-lookup"><span data-stu-id="6e093-143">Explore the [National Language Support Knowledge Center](./national-language-support-reference.md).</span></span>
    -   <span data-ttu-id="6e093-144">查看 [ (NLS) 的國家語言支援 ](national-language-support.md)檔。</span><span class="sxs-lookup"><span data-stu-id="6e093-144">Examine the documentation for [National Language Support (NLS)](national-language-support.md).</span></span>

-   <span data-ttu-id="6e093-145">**探索使用者使用的語言或腳本，並將其套用至應用程式的其他服務。**</span><span class="sxs-lookup"><span data-stu-id="6e093-145">**Discover the language or script used by the user, and apply it to the other services of the application.**</span></span>

    <span data-ttu-id="6e093-146">如果您的應用程式可以決定撰寫文字和使用者輸入的語言，它可以在可理解的語言中顯示提示或協助等內容。</span><span class="sxs-lookup"><span data-stu-id="6e093-146">If your application can determine the language in which text and user input is written, it can display content such as prompts or help in an understandable language.</span></span>

    -   <span data-ttu-id="6e093-147">閱讀在 [windows 中撰寫全球可用應用程式的文章： windows 中的擴充語言服務](./using-extended-linguistic-services.md)。</span><span class="sxs-lookup"><span data-stu-id="6e093-147">Read the article [Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md).</span></span>
    -   <span data-ttu-id="6e093-148">探索 [ (ELS) 擴充語言服務 ](extended-linguistic-services.md)的檔。</span><span class="sxs-lookup"><span data-stu-id="6e093-148">Explore the documentation for [Extended Linguistic Services (ELS)](extended-linguistic-services.md).</span></span>

## <a name="internationalization-technologies-in-the-sdk"></a><span data-ttu-id="6e093-149">SDK 中的國際化技術</span><span class="sxs-lookup"><span data-stu-id="6e093-149">Internationalization Technologies in the SDK</span></span>

<span data-ttu-id="6e093-150">SDK 的國際開發支援區段提供可讓應用程式列舉語言、地區設定和地區設定特定格式的技術。</span><span class="sxs-lookup"><span data-stu-id="6e093-150">The International Development Support section of the SDK provides technologies that permit the application to enumerate languages, locales, and locale-specific formats.</span></span> <span data-ttu-id="6e093-151">您可以在使用 C 或 c + + 撰寫的 Microsoft Win32 應用程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="6e093-151">You can use them in Microsoft Win32 applications that you write in C or C++ .</span></span>

<span data-ttu-id="6e093-152">[擴充的語言服務](extended-linguistic-services.md)會提供 Microsoft 專利技術，以文字識別語言和腳本。</span><span class="sxs-lookup"><span data-stu-id="6e093-152">The [Extended Linguistic Services](extended-linguistic-services.md) offer Microsoft-patented technology for the identification of languages and scripts in text.</span></span> <span data-ttu-id="6e093-153">您的應用程式可以根據類別以及輸入和輸出語言、腳本和內容類型，判斷可用的服務。</span><span class="sxs-lookup"><span data-stu-id="6e093-153">Your application can determine the services available based on category as well as on input and output language, script, and content type.</span></span>

<span data-ttu-id="6e093-154">[國際字型和文字顯示](international-fonts-and-text-display.md) 提供有關國際字型、複雜字集和圖像的資訊，以及在 Windows 平臺上轉譯印刷樣式的資訊。</span><span class="sxs-lookup"><span data-stu-id="6e093-154">[International Fonts and Text Display](international-fonts-and-text-display.md) provides information about international fonts, complex scripts and glyphs, and the fine rendering of typography on the Windows platform.</span></span>

<span data-ttu-id="6e093-155">[輸入方法管理員 (的輸出) ](input-method-manager.md) 是一種技術，可協助應用程式從輸入法編輯器中接收輸入 (輸入法) 軟體，進而允許使用標準鍵盤來輸入字元和符號，例如日文漢字的字元和符號。</span><span class="sxs-lookup"><span data-stu-id="6e093-155">[Input Method Manager (IMM)](input-method-manager.md) is a technology that helps the application receive input from Input Method Editor (IME) software, which in turn allows the entry of characters and symbols, such as Japanese kanji, for other languages by using a standard keyboard.</span></span>

## <a name="the-hello-mui-application"></a><span data-ttu-id="6e093-156">Hello MUI 應用程式</span><span class="sxs-lookup"><span data-stu-id="6e093-156">The Hello MUI Application</span></span>

<span data-ttu-id="6e093-157">國際開發中的一項常見工作，是從單一語言應用程式開始，您必須將該應用程式做好準備。</span><span class="sxs-lookup"><span data-stu-id="6e093-157">A common task in international development begins with a monolingual application that you must make world-ready.</span></span> <span data-ttu-id="6e093-158">您需要新增其他語言的支援，但不需要為每個新的語言或文化特性重寫程式碼。</span><span class="sxs-lookup"><span data-stu-id="6e093-158">You need to add support for additional languages, but in a way that does not require that you rewrite the code for each new language or culture.</span></span>

<span data-ttu-id="6e093-159">這項工作可讓您有機會提供教學課程，讓您逐步建立 Hello MUI 應用程式，並利用 [多語系消費者介面 (mui) ](multilingual-user-interface.md) 資源模型以及 Windows 中提供的相關支援。</span><span class="sxs-lookup"><span data-stu-id="6e093-159">This task provides the opportunity to present a tutorial that takes you step-by-step through the creation of a Hello MUI application, making use of the [Multilingual User Interface (MUI)](multilingual-user-interface.md) resource model and associated support provided in Windows.</span></span>

<span data-ttu-id="6e093-160">本教學課程採用熟悉的 Hello World 應用程式的概念，示範如何使用 MUI 來建立基本的多語系應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e093-160">The tutorial adopts the concept of the familiar Hello World application, demonstrating the use of MUI to build a basic multilingual application.</span></span>

<span data-ttu-id="6e093-161">您可以在 [將多語系消費者介面支援新增至應用程式](creating-a-multilingual-user-interface-application.md)時，開始 Hello MUI 教學課程。</span><span class="sxs-lookup"><span data-stu-id="6e093-161">You can begin the Hello MUI tutorial at [Adding Multilingual User Interface Support to an Application](creating-a-multilingual-user-interface-application.md).</span></span>

 

 
