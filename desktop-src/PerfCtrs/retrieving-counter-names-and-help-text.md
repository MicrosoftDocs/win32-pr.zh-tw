---
description: 效能資料包含索引值，您可以用來尋找每個已註冊物件和計數器的名稱和解說文字。
ms.assetid: 9ddd1672-61cf-41c2-bec0-0d2b775bf970
title: 正在抓取計數器名稱和解說文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b49f852e6af22dc2ec31d341ee6176913f98e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989404"
---
# <a name="retrieving-counter-names-and-help-text"></a><span data-ttu-id="46c27-103">正在抓取計數器名稱和解說文字</span><span class="sxs-lookup"><span data-stu-id="46c27-103">Retrieving Counter Names and Help Text</span></span>

<span data-ttu-id="46c27-104">效能資料包含索引值，您可以用來尋找每個已註冊物件和計數器的名稱和解說文字。</span><span class="sxs-lookup"><span data-stu-id="46c27-104">The performance data contains index values that you use to locate the names and help text for each registered object and counter.</span></span> <span data-ttu-id="46c27-105">[**性能 \_ 物件 \_ 類型**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)結構的 **ObjectNameTitleIndex** 和 **ObjectHelpTitleIndex** 成員分別包含物件名稱和解說文字的索引值，而 [**性能 \_ 計數器 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)結構的 **CounterNameTitleIndex** 和 **CounterHelpTitleIndex** 成員分別包含計數器名稱和解說文字的索引值。</span><span class="sxs-lookup"><span data-stu-id="46c27-105">The **ObjectNameTitleIndex** and **ObjectHelpTitleIndex** members of the [**PERF\_OBJECT\_TYPE**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) structure contain the index values to the object name and help text, respectively, and the **CounterNameTitleIndex** and **CounterHelpTitleIndex** members of the [**PERF\_COUNTER\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) structure contain the index values to the counter name and help text, respectively.</span></span>

<span data-ttu-id="46c27-106">若要取出名稱或解說文字，請呼叫 [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="46c27-106">To retrieve the names or help text, call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function.</span></span> <span data-ttu-id="46c27-107">將 *hKey* 參數設定為下列其中一個預先定義的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="46c27-107">Set the *hKey* parameter to one of the following predefined keys.</span></span> <span data-ttu-id="46c27-108">一般而言，您會使用 **HKEY \_ 效能 \_ NLSTEXT** 金鑰，因此您不需要判斷使用者的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="46c27-108">Typically, you would use the **HKEY\_PERFORMANCE\_NLSTEXT** key, so you do not have to determine the user's language identifier.</span></span>



| <span data-ttu-id="46c27-109">Key</span><span class="sxs-lookup"><span data-stu-id="46c27-109">Key</span></span>                            | <span data-ttu-id="46c27-110">描述</span><span class="sxs-lookup"><span data-stu-id="46c27-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c27-111">**HKEY \_ 效能 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="46c27-111">**HKEY\_PERFORMANCE\_DATA**</span></span>    | <span data-ttu-id="46c27-112">根據您在 *lpValueName* 參數中指定的語言識別項值查詢字串。</span><span class="sxs-lookup"><span data-stu-id="46c27-112">Query strings based on the language identifier value that you specify in the *lpValueName* parameter.</span></span> <span data-ttu-id="46c27-113">將 *lpValueName* 參數設定為 "Counter &lt; langid &gt; " 或 "help &lt; langid &gt; " 可分別取出名稱或解說文字，其中 " &lt; langid &gt; " 是以 **零填補的3位數十六進位數位** 格式的系統語言識別項。</span><span class="sxs-lookup"><span data-stu-id="46c27-113">Set *lpValueName* parameter to either "Counter &lt;langid&gt;" or "Help &lt;langid&gt;" to retrieve the names or help text, respectively, where "&lt;langid&gt;" is the system language identifier formatted as **zero-padded 3-digit hex number**.</span></span> <span data-ttu-id="46c27-114">語言識別項是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="46c27-114">The language identifier is optional.</span></span> <span data-ttu-id="46c27-115">如果您未指定語言識別項，此函數會傳回英文字串。</span><span class="sxs-lookup"><span data-stu-id="46c27-115">If you do not specify a language identifier, the function returns English strings.</span></span> <span data-ttu-id="46c27-116">請檢查 `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` 登錄機碼，以取得您系統上可用的語言清單。</span><span class="sxs-lookup"><span data-stu-id="46c27-116">Check the `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` registry key for the list of languages available on your system.</span></span><br/><span data-ttu-id="46c27-117">若要取出大部分語言的文字，請只指定主要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="46c27-117">To retrieve text in most languages, specify the primary language identifier only.</span></span> <span data-ttu-id="46c27-118">例如，若要取出英文字串，請將語言識別項指定為009，而不是1033（英文）。</span><span class="sxs-lookup"><span data-stu-id="46c27-118">For example, to retrieve English strings, specify the language identifier as 009, not 1033 for English-US.</span></span><br/><span data-ttu-id="46c27-119">若要取出中文和葡萄牙文文字，請同時指定主要和語言識別項。</span><span class="sxs-lookup"><span data-stu-id="46c27-119">To retrieve Chinese and Portuguese text, specify both the primary and sublanguage identifiers.</span></span><br/><span data-ttu-id="46c27-120">**Windows Server 2003 和 WINDOWS XP：** 只指定葡萄牙文的主要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="46c27-120">**Windows Server 2003 and Windows XP:** Specify only the primary language identifier for Portuguese.</span></span><br/><span data-ttu-id="46c27-121">**Windows 10**： &lt; &gt; 使用自訂語言識別項的 "Help langid" 文字一律會以英文傳回字串，雖然仍可使用上述的索引鍵從登錄中取出當地語系化值。</span><span class="sxs-lookup"><span data-stu-id="46c27-121">**Windows 10**: "Help &lt;langid&gt;" text with custom language identifier always returns strings in English, although localized value can still be retrieved from the registry using the aforementioned key.</span></span><br/><br/> |
| <span data-ttu-id="46c27-122">**HKEY \_ 效能 \_ NLSTEXT**</span><span class="sxs-lookup"><span data-stu-id="46c27-122">**HKEY\_PERFORMANCE\_NLSTEXT**</span></span> | <span data-ttu-id="46c27-123">以目前使用者的預設 UI 語言為基礎的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="46c27-123">Query strings based on the default UI language of the current user.</span></span> <span data-ttu-id="46c27-124">將 *lpValueName* 參數設定為「計數器」或「說明」，分別取得名稱或解說文字。</span><span class="sxs-lookup"><span data-stu-id="46c27-124">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="46c27-125">**HKEY \_ 效能 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="46c27-125">**HKEY\_PERFORMANCE\_TEXT**</span></span>    | <span data-ttu-id="46c27-126">查詢英文字串。</span><span class="sxs-lookup"><span data-stu-id="46c27-126">Query English strings.</span></span> <span data-ttu-id="46c27-127">將 *lpValueName* 參數設定為「計數器」或「說明」，分別取得名稱或解說文字。</span><span class="sxs-lookup"><span data-stu-id="46c27-127">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |





<span data-ttu-id="46c27-128">函數會以字串清單的形式傳回資料。</span><span class="sxs-lookup"><span data-stu-id="46c27-128">The function returns the data as a list of strings.</span></span> <span data-ttu-id="46c27-129">每個字串都是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="46c27-129">Each string is null-terminated.</span></span> <span data-ttu-id="46c27-130">最後一個字串後面接著額外的 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="46c27-130">The last string is followed by an additional null terminator.</span></span> <span data-ttu-id="46c27-131">字串會成對列出。</span><span class="sxs-lookup"><span data-stu-id="46c27-131">The strings are listed in pairs.</span></span> <span data-ttu-id="46c27-132">每個配對的第一個字串是索引，而第二個字串是與索引相關聯的文字。</span><span class="sxs-lookup"><span data-stu-id="46c27-132">The first string of each pair is the index, and the second string is the text associated with the index.</span></span> <span data-ttu-id="46c27-133">計數器資料只會使用偶數編號的索引，而說明資料會使用奇數索引。</span><span class="sxs-lookup"><span data-stu-id="46c27-133">The counter data uses only even-numbered indexes, while the help data uses odd-numbered indexes.</span></span> <span data-ttu-id="46c27-134">配對會以遞增的索引順序傳回。</span><span class="sxs-lookup"><span data-stu-id="46c27-134">The pairs are returned in increasing index order.</span></span>

<span data-ttu-id="46c27-135">下列清單顯示 counter 和 help 資料的範例。</span><span class="sxs-lookup"><span data-stu-id="46c27-135">The following lists show examples of counter and help data.</span></span> <span data-ttu-id="46c27-136">將指定計數器的索引值遞增一，可提供計數器解說文字的索引。</span><span class="sxs-lookup"><span data-stu-id="46c27-136">Incrementing a given counter's index value by one gives you the index to the counter's help text.</span></span> <span data-ttu-id="46c27-137">例如，7是與計數器索引6相關聯的說明索引。</span><span class="sxs-lookup"><span data-stu-id="46c27-137">For example, 7 is the help index associated with counter index 6.</span></span>

<span data-ttu-id="46c27-138">計數器資料組。</span><span class="sxs-lookup"><span data-stu-id="46c27-138">Counter data pairs.</span></span>

<dl> <span data-ttu-id="46c27-139">2系統4記憶體6% 處理器時間</span><span class="sxs-lookup"><span data-stu-id="46c27-139">2 System 4 Memory 6 % Processor Time</span></span>
</dl>

<span data-ttu-id="46c27-140">協助資料組。</span><span class="sxs-lookup"><span data-stu-id="46c27-140">Help data pairs.</span></span>

<dl> <span data-ttu-id="46c27-141">3系統物件類型包含這些計數器 .。。5記憶體物件類型包含這些計數器 .。。7處理器時間以百分比表示。</span><span class="sxs-lookup"><span data-stu-id="46c27-141">3 The System object type includes those counters that ... 5 The Memory object type includes those counters that ... 7 Processor Time is expressed as a percentage of the ...</span></span>
</dl>

<span data-ttu-id="46c27-142">請注意，計數器資料中的第一對字串並不會識別計數器名稱，而且可以忽略。</span><span class="sxs-lookup"><span data-stu-id="46c27-142">Note that the first pair of strings in the counter data do not identify a counter name and can be ignored.</span></span> <span data-ttu-id="46c27-143">第一個配對的索引編號是1，而字串是代表系統計數器最大索引值的數值字串。</span><span class="sxs-lookup"><span data-stu-id="46c27-143">The index number of the first pair is 1 and the string is a numeric string that represents the maximum index value for system counters.</span></span>

<span data-ttu-id="46c27-144">如需提供者如何載入名稱和解說文字的詳細資訊，請參閱 [將計數器名稱和描述新增至](adding-counter-names-and-descriptions-to-the-registry.md)登錄。</span><span class="sxs-lookup"><span data-stu-id="46c27-144">For information on how a provider loads the name and help text, see [Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).</span></span>

<span data-ttu-id="46c27-145">文字中沒有任何資訊可指出文字是否識別計數器或效能物件。</span><span class="sxs-lookup"><span data-stu-id="46c27-145">There is no information in the text that indicates if the text identifies a counter or performance object.</span></span> <span data-ttu-id="46c27-146">判斷這個情況的唯一方法，或是計數器和物件之間的關聯性，就是查詢效能資料本身。</span><span class="sxs-lookup"><span data-stu-id="46c27-146">The only way to determine this, or the relationship between counters and objects, is to query the performance data itself.</span></span> <span data-ttu-id="46c27-147">例如，如果您想要在使用者介面中顯示物件及其計數器的清單，則必須取出效能資料，然後使用索引值來剖析字串的文字資料。</span><span class="sxs-lookup"><span data-stu-id="46c27-147">For example, if you want to display a list of objects and their counters in a user interface, you must retrieve the performance data, and then use the index values to parse the text data for the strings.</span></span> <span data-ttu-id="46c27-148">如需執行此程式的範例，請參閱 [顯示物件、實例和計數器名稱](displaying-object-instance-and-counter-names.md)。</span><span class="sxs-lookup"><span data-stu-id="46c27-148">For an example that does this, see [Displaying Object, Instance, and Counter Names](displaying-object-instance-and-counter-names.md).</span></span>

<span data-ttu-id="46c27-149">下列範例示範如何使用 **HKEY \_ 效能 \_ NLSTEXT** 來取出計數器和解說文字，以及建立資料表以供後續存取。</span><span class="sxs-lookup"><span data-stu-id="46c27-149">The following example shows how to use **HKEY\_PERFORMANCE\_NLSTEXT** to retrieve the counter and help text and build a table for subsequent access.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.


    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_NLSTEXT key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array


    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{    UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```



<span data-ttu-id="46c27-150">下列範例示範如何使用 **HKEY \_ 效能 \_ 資料** 來取出計數器文字。</span><span class="sxs-lookup"><span data-stu-id="46c27-150">The following example shows how to use **HKEY\_PERFORMANCE\_DATA** to retrieve the counter text.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);
LANGID GetLanguageId();

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.

    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_DATA key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;
    LANGID langid = 0;
    WCHAR wszSourceAndLangId[15];   // Identifies the source of the text; either
                                    // "Counter <langid>" or "Help <langid>"


    // Create the lpValueName string for the registry query.
    langid = GetLanguageId();
    if (0 == langid)
    {
        wprintf(L"GetLanguageId failed to get the default language identifier.\n");
        goto cleanup;
    }

    StringCchPrintf(wszSourceAndLangId, 15, L"%s %03x", pwszSource, langid);

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Retrieve the default language identifier of the current user. For most languages,
// you use the primary language identifier only to retrieve the text. In Windows XP and
// Windows Server 2003, you use the complete language identifier to retrieve Chinese
// text. In Windows Vista, you use the complete language identifier to retrieve Portuguese
// text.
LANGID GetLanguageId()
{
    LANGID langid = 0;  // Complete language identifier.
    WORD primary = 0;   // Primary language identifier.
    OSVERSIONINFO osvi;

    ZeroMemory(&osvi, sizeof(OSVERSIONINFO));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);

    if (GetVersionEx(&osvi))
    {
        langid = GetUserDefaultUILanguage();
        primary = PRIMARYLANGID(langid);

        if ( (LANG_PORTUGUESE == primary && osvi.dwBuildNumber > 5) || // Windows Vista and later
             (LANG_CHINESE == primary && (osvi.dwMajorVersion == 5 && osvi.dwMinorVersion >= 1)) ) // XP and Windows Server 2003
        {
            ; //Use the complete language identifier.
        }
        else
        {
            langid = primary;
        }
    }
    else
    {
        wprintf(L"GetVersionEx failed with 0x%x.\n", GetLastError());
    }

    return langid;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array

    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{   UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```
