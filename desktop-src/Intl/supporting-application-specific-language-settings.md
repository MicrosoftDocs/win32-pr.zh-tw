---
description: 您的應用程式可以支援目標作業系統所支援的一組不同的使用者介面語言。 本主題將討論此類型的支援，並使用完整範例中的程式碼片段。
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: 支援 Application-Specific 語言設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c934ea2f01c37eb2f9e846382447a50ccbedcd9b69fe20069216fa46521b02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130058"
---
# <a name="supporting-application-specific-language-settings"></a>支援 Application-Specific 語言設定

您的應用程式可以支援目標作業系統所支援的一組不同的使用者介面語言。 本主題將討論此類型的支援，並使用完整範例中的程式碼片段。

## <a name="interpret-users-language-preference"></a>解讀使用者的語言喜好設定

您的應用程式必須先根據使用者喜好設定來決定要顯示的使用者介面語言。 程式碼可以從設定檔或登錄設定中讀取設定。

下列範例會定義兩個函式，用來解讀使用者的語言喜好設定。 第一個函式說明如何從檔案中讀取語言的分隔清單，在程式碼中以 "langs.txt" 表示。 範例中支援的分隔符號為 "，"、";"; "." 和 ""。 第二個函式會將從檔案讀取的字串轉換成多字串值。 這是必要作業，因為用來設定語言的 MUI 函數只接受多字串值。


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



## <a name="set-the-application-language"></a>設定應用程式語言

在閱讀語言喜好設定資訊之後，應用程式程式碼必須使用抓取的設定來設定應用程式語言。 在 Windows 7 和更新版本上，應用程式可以藉由呼叫 [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)函數，在進程層級設定語言。


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



在 Windows Vista 和更新版本上，會藉由呼叫 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)函數，線上程層級設定應用程式語言。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定應用程式語言喜好設定](setting-application-language-preferences.md)
</dt> <dt>

[MUI： Application-Specific 設定範例 (Windows Vista) ](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI： Application-Specific 設定範例 (早 Windows Vista) ](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



