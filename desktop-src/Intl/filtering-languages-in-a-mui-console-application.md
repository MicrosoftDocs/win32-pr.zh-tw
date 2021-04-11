---
description: MUI 主控台應用程式可支援其使用者介面語言的系統設定或應用程式特定的設定。 本主題討論此類型應用程式的語言篩選。
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: 在 MUI 主控台應用程式中篩選語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849483"
---
# <a name="filtering-languages-in-a-mui-console-application"></a><span data-ttu-id="335f1-104">在 MUI 主控台應用程式中篩選語言</span><span class="sxs-lookup"><span data-stu-id="335f1-104">Filtering Languages in a MUI Console Application</span></span>

<span data-ttu-id="335f1-105">MUI 主控台應用程式可支援其使用者介面語言的系統設定或應用程式特定的設定。</span><span class="sxs-lookup"><span data-stu-id="335f1-105">A MUI console application can support either system settings or application-specific settings for its user interface languages.</span></span> <span data-ttu-id="335f1-106">本主題討論此類型應用程式的語言篩選。</span><span class="sxs-lookup"><span data-stu-id="335f1-106">This topic discusses the filtering of languages for this type of application.</span></span>

## <a name="limit-the-languages-to-display"></a><span data-ttu-id="335f1-107">限制顯示的語言</span><span class="sxs-lookup"><span data-stu-id="335f1-107">Limit the Languages to Display</span></span>

<span data-ttu-id="335f1-108">與圖形化視窗不同的是，Windows 主控台無法顯示 [複雜的腳本](uniscribe-glossary.md)，例如阿拉伯文、希伯來文、波斯文、印度文、烏爾化、泰文和其他許多專案。</span><span class="sxs-lookup"><span data-stu-id="335f1-108">Unlike a graphical window, the Windows console cannot display [complex scripts](uniscribe-glossary.md), such as Arabic, Hebrew, Persian, Hindi, Urdu, Thai, and many others.</span></span> <span data-ttu-id="335f1-109">因此，在任何情況下，主控台都無法顯示許多使用者介面語言。</span><span class="sxs-lookup"><span data-stu-id="335f1-109">Therefore, many user interface languages cannot be displayed by the console under any circumstances.</span></span>

<span data-ttu-id="335f1-110">主控台只能顯示與非 Unicode 應用程式目前語言相關聯的單一 [OEM 字碼頁](code-pages.md) 中的字元。</span><span class="sxs-lookup"><span data-stu-id="335f1-110">The console can display only characters from the single [OEM code page](code-pages.md) associated with the current language for non-Unicode applications.</span></span> <span data-ttu-id="335f1-111">針對每個 OEM 字碼頁，主控台會使用特定字型，而這可能不會提供該字碼頁的完整涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="335f1-111">For each OEM code page, the console uses a particular font, and this might not provide full coverage for that code page.</span></span>

<span data-ttu-id="335f1-112">這些主控台相關的限制會減少主控台可在特定電腦上顯示的使用者介面語言數目。</span><span class="sxs-lookup"><span data-stu-id="335f1-112">These console-related limitations reduce the number of user interface languages that the console can display on a particular computer.</span></span> <span data-ttu-id="335f1-113">比方說，如果非 Unicode 應用程式目前的語言是日文，而使用者嘗試在主控台中顯示德文文字，則有變音符號的字元就不會正確顯示。</span><span class="sxs-lookup"><span data-stu-id="335f1-113">For example, if the current language for non-Unicode applications is Japanese and the user tries to display German text in the console, characters with umlauts do not display correctly.</span></span> <span data-ttu-id="335f1-114">如果非 Unicode 應用程式目前的語言為德文，且使用者想要在主控台中顯示日文文字，結果會更糟，因此轉譯文字幾乎費解。</span><span class="sxs-lookup"><span data-stu-id="335f1-114">If the current language for non-Unicode applications is German and the user wants to display Japanese text in the console, the results are much worse, rendering the text almost incomprehensible.</span></span>

> [!Note]  
> <span data-ttu-id="335f1-115">為您的 MUI 應用程式提供主控台支援時，請記住，主控台僅提供對 [輸入法編輯器](input-method-manager.md)的有限支援。</span><span class="sxs-lookup"><span data-stu-id="335f1-115">When providing console support for your MUI applications, remember that the console provides only limited support for [input method editors](input-method-manager.md).</span></span>

 

## <a name="set-the-language-for-console-output"></a><span data-ttu-id="335f1-116">設定主控台輸出的語言</span><span class="sxs-lookup"><span data-stu-id="335f1-116">Set the Language for Console Output</span></span>

<span data-ttu-id="335f1-117">在 Windows Vista 和更新版本上，主控台應用程式會藉由呼叫 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)來設定支援主控台顯示的語言。</span><span class="sxs-lookup"><span data-stu-id="335f1-117">On Windows Vista and later, a console application sets the language to support the console display by calling [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="335f1-118">在此呼叫中，應用程式會 \_ \_ 在 *dwFlags* 參數中傳遞 MUI 主控台篩選器，並在 *pwszLanguagesBuffer* 中傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="335f1-118">In this call, the application passes MUI\_CONSOLE\_FILTER in the *dwFlags* parameter and **NULL** for *pwszLanguagesBuffer*.</span></span> <span data-ttu-id="335f1-119">替代方法是呼叫語言識別項為0的 [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) 。</span><span class="sxs-lookup"><span data-stu-id="335f1-119">An alternative is to call [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span> <span data-ttu-id="335f1-120">這種設定會讓函數選取最能支援主控台顯示的語言。</span><span class="sxs-lookup"><span data-stu-id="335f1-120">This setting causes the function to select the language that best supports the console display.</span></span>

<span data-ttu-id="335f1-121">在 Windows XP 中，應用程式只能透過呼叫語言識別項為0的 [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) ，來設定主控台輸出的語言。</span><span class="sxs-lookup"><span data-stu-id="335f1-121">On Windows XP, the application can only set the language for console output by calling [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="335f1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="335f1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="335f1-123">設定應用程式語言喜好設定</span><span class="sxs-lookup"><span data-stu-id="335f1-123">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> </dl>

 

 
