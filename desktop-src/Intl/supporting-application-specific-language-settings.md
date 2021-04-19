---
description: 您的應用程式可以支援目標作業系統所支援的一組不同的使用者介面語言。 本主題將討論此類型的支援，並使用完整範例中的程式碼片段。
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: 支援 Application-Specific 語言設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bddfe94586751d3b0f4757c670c006317e49b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975227"
---
# <a name="supporting-application-specific-language-settings"></a><span data-ttu-id="b4089-104">支援 Application-Specific 語言設定</span><span class="sxs-lookup"><span data-stu-id="b4089-104">Supporting Application-Specific Language Settings</span></span>

<span data-ttu-id="b4089-105">您的應用程式可以支援目標作業系統所支援的一組不同的使用者介面語言。</span><span class="sxs-lookup"><span data-stu-id="b4089-105">Your application can support a different set of user interface languages from those supported by the target operating system.</span></span> <span data-ttu-id="b4089-106">本主題將討論此類型的支援，並使用完整範例中的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="b4089-106">This topic discusses this type of support, using snippets from complete samples.</span></span>

## <a name="interpret-users-language-preference"></a><span data-ttu-id="b4089-107">解讀使用者的語言喜好設定</span><span class="sxs-lookup"><span data-stu-id="b4089-107">Interpret User's Language Preference</span></span>

<span data-ttu-id="b4089-108">您的應用程式必須先根據使用者喜好設定來決定要顯示的使用者介面語言。</span><span class="sxs-lookup"><span data-stu-id="b4089-108">Your application must first determine which user interface language to display, based on user preference.</span></span> <span data-ttu-id="b4089-109">程式碼可以從設定檔或登錄設定中讀取設定。</span><span class="sxs-lookup"><span data-stu-id="b4089-109">The code can read the settings from a configuration file or from registry settings.</span></span>

<span data-ttu-id="b4089-110">下列範例會定義兩個函式，用來解讀使用者的語言喜好設定。</span><span class="sxs-lookup"><span data-stu-id="b4089-110">The following example defines two functions used to interpret the user's language preference.</span></span> <span data-ttu-id="b4089-111">第一個函式說明如何從檔案中讀取語言的分隔清單，在程式碼中以 "langs.txt" 表示。</span><span class="sxs-lookup"><span data-stu-id="b4089-111">The first function illustrates the reading of a delimited list of languages from a file, represented in the code as "langs.txt".</span></span> <span data-ttu-id="b4089-112">範例中支援的分隔符號為 "，"、";"; "." 和 ""。</span><span class="sxs-lookup"><span data-stu-id="b4089-112">The delimiters supported in the sample are ",",";";"." and " ".</span></span> <span data-ttu-id="b4089-113">第二個函式會將從檔案讀取的字串轉換成多字串值。</span><span class="sxs-lookup"><span data-stu-id="b4089-113">The second function converts the string read from the file to a multi-string value.</span></span> <span data-ttu-id="b4089-114">這是必要作業，因為用來設定語言的 MUI 函數只接受多字串值。</span><span class="sxs-lookup"><span data-stu-id="b4089-114">This operation is necessary because the MUI functions used to set languages only accept multi-string values.</span></span>


```C++
BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // Very simple implementation - assumes that first 'langStrSize' characters of the
    // L".\\langs.txt" file comprises a string of one or more languages.
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0,
                                    NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // Clear the input variables.
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle, langStr, langStrSize*sizeof(WCHAR), &bytesActuallyRead, NULL)
           && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize)
                              ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
            langStr[nullIndex] = L'\0';
        }
        CloseHandle(langConfigFileHandle);
    }
    return rtnVal;
}
BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
{
    BOOL rtnVal = FALSE;
    size_t strLen = 0;
    rtnVal = SUCCEEDED(StringCchLengthW(langStr, USER_CONFIGURATION_STRING_BUFFER*2, &strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // Make sure you validate the user input.
            if(SUCCEEDED(StringCchLengthW(last, LOCALE_NAME_MAX_LENGTH, &strLen))
               && IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,
                                    (langMultiStrSize - (langMultiStrPtr - langMultiStr)), next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL, L",; :", &context);
            if(next)
                last = next;
        }
        // Make sure there is a double null term for the multi-string.
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr)))
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // Fail and guard anyone whom might use the multi-string.
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



## <a name="set-the-application-language"></a><span data-ttu-id="b4089-115">設定應用程式語言</span><span class="sxs-lookup"><span data-stu-id="b4089-115">Set the Application Language</span></span>

<span data-ttu-id="b4089-116">在閱讀語言喜好設定資訊之後，應用程式程式碼必須使用抓取的設定來設定應用程式語言。</span><span class="sxs-lookup"><span data-stu-id="b4089-116">After reading the language preference information, the application code must use the retrieved setting to set the application language.</span></span> <span data-ttu-id="b4089-117">在 Windows 7 和更新版本中，應用程式可以藉由呼叫 [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) 函式，在進程層級設定語言。</span><span class="sxs-lookup"><span data-stu-id="b4089-117">On Windows 7 and later, the application can set the language at the process level by calling the [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) function.</span></span>


```C++
DWORD langCount = 0;
// Using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications).
if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
```



<span data-ttu-id="b4089-118">在 Windows Vista 和更新版本上，會藉由呼叫 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) 函數，線上程層級設定應用程式語言。</span><span class="sxs-lookup"><span data-stu-id="b4089-118">On Windows Vista and later, the application language is set at the thread level by calling the [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) function.</span></span>


```C++
DWORD langCount = 0;
// The following line of code is supported on Windows Vista and later.
if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
return 1;
```



## <a name="related-topics"></a><span data-ttu-id="b4089-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4089-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4089-120">設定應用程式語言喜好設定</span><span class="sxs-lookup"><span data-stu-id="b4089-120">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> <dt>

[<span data-ttu-id="b4089-121">MUI： (Windows Vista) 的 Application-Specific 設定範例 </span><span class="sxs-lookup"><span data-stu-id="b4089-121">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="b4089-122">MUI： (Windows Vista 之前的 Application-Specific 設定範例) </span><span class="sxs-lookup"><span data-stu-id="b4089-122">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



