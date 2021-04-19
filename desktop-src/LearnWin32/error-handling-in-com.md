---
title: 使用 Win32 和 c + +) 開始 COM (中的錯誤處理
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965049"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>使用 Win32 和 c + +) 開始 COM (中的錯誤處理

COM 會使用 **HRESULT** 值來指出方法或函式呼叫的成功或失敗。 各種 SDK 標頭會定義各種 **HRESULT** 常數。 Winerror.h 中會定義一組通用的全系統程式碼。 下表顯示其中一些全系統的傳回碼。



| 常數            | 數值 | Description                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ ACCESSDENIED** | 0x80070005    | 拒絕存取。                                       |
| **E \_ 失敗**         | 0x80004005    | 未指定的錯誤。                                   |
| **E \_ INVALIDARG**   | 0x80070057    | 參數值無效。                             |
| **E \_ OUTOFMEMORY**  | 0x8007000E    | 記憶體不足。                                       |
| **E \_ 指標**      | 且顯示0x80004003    | 指標值未正確傳遞 **Null** 。 |
| **E 未 \_ 預期**   | 0x8000FFFF    | 未預期的情況。                                |
| **S \_ 確定**           | 0x0           | 成功。                                             |
| **S \_ FALSE**        | 0x1           | 成功。                                             |



 

前置詞為 "E" 的所有常數 \_ 都是錯誤碼。 常數 **S \_ OK** 和 **S \_ FALSE** 都是成功的代碼。 可能是99% 的 COM 方法 **會 \_ 在成功時傳回** ，但不讓這項事實誤導您。 方法可能會傳回其他成功的程式碼，因此請一律使用 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) 或 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 的宏來測試錯誤。 下列範例程式碼顯示錯誤的方式，以及測試函數呼叫是否成功的正確方式。


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



成功碼 **\_ 為 FALSE** ，則值得提及。 某些方法會 **使用 \_ FALSE** 來平均表示非失敗的負條件。 它也可以表示「無作業」—方法成功，但不會有任何作用。 例如，如果您從相同的執行緒呼叫第二次， [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函式會傳回 **S \_ FALSE** 。 如果您需要區分程式碼中的 **\_ [確定] 和 [** **\_ FALSE** ]，您應該直接測試值，但仍使用 [ [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) ] 或 [ [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) ] 來處理其餘的案例，如下列範例程式碼所示。


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



某些 **HRESULT** 值專屬於特定的 Windows 功能或子系統。 例如，Direct2D 圖形 API 會定義錯誤碼 **D2DERR \_ 不支援的 \_ 圖元 \_ 格式**，這表示程式使用的像素格式不受支援。 MSDN 檔通常會提供方法可能會傳回的特定錯誤碼清單。 不過，您不應該將這些清單視為具有決定性。 方法一律會傳回檔中未列出的 **HRESULT** 值。 同樣地，請使用 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) 和 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 的宏。 如果您測試特定的錯誤碼，也請包含預設案例。


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a>錯誤處理模式

本節探討以結構化方式處理 COM 錯誤的一些模式。 每個模式都有優缺點。 在某些程度上，選擇是一種感受。 如果您使用現有的專案，它可能已經有 proscribe 特定樣式的編碼方針。 無論您採用哪種模式，健全的程式碼都將遵守下列規則。

-   針對傳回 **HRESULT** 的每個方法或函式，請先檢查傳回值再繼續。
-   使用之後釋放資源。
-   請勿嘗試存取無效或未初始化的資源，例如 **Null** 指標。
-   在您釋放資源之後，請勿嘗試使用它。

考慮這些規則，以下是處理錯誤的四種模式。

-   [嵌套的 ifs](#nested-ifs)
-   [串聯式 ifs](#cascading-ifs)
-   [失敗時跳](#jump-on-fail)
-   [失敗時擲回](#throw-on-fail)

### <a name="nested-ifs"></a>嵌套的 ifs

在傳回 **HRESULT** 的每次呼叫之後，請使用 **if** 語句來測試是否成功。 然後，將下一個方法呼叫放在 **if** 語句的範圍內。 如 **有需要** ，可以將更多語句嵌套至語句。 此課程模組中先前的程式碼範例已使用此模式，但在此會再次出現：


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



優點

-   變數可以用基本的範圍宣告。 例如，在使用 *pItem* 之前，不會宣告。
-   在每個 **if** 語句中，特定的非變異值為 True：所有先前的呼叫都已成功，且所有取得的資源仍有效。 在上述範例中，當程式到達最內層的 **if** 語句時， *pItem* 和 *pFileOpen* 都已知有效。
-   您可以明確地釋放介面指標和其他資源。 您會在 **if** 語句的結尾釋放資源，緊接在取得資源的呼叫之後。

缺點

-   有些人發現深層的嵌套難以閱讀。
-   錯誤處理與其他分支和迴圈語句混合在一起。 這可能會使整體程式邏輯更難追蹤。

### <a name="cascading-ifs"></a>串聯式 ifs

在每個方法呼叫之後，請使用 **if** 語句來測試是否成功。 如果方法成功，請將下一個方法呼叫放在 **if** 區塊內。 但是，請將每個後續 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded)的測試放在先前的 **if** 區塊之後，而不是進一步嵌套 **if** 語句。 如果有任何方法失敗，則所有其餘 **成功** 的測試都只會失敗，直到到達函式的底部為止。


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



在此模式中，您會在函式的最一端釋放資源。 如果發生錯誤，當函式結束時，某些指標可能會無效。 在不正確指標上呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 將會使程式 (或更糟的) 而損毀，因此您必須將所有指標初始化為 **null** ，並檢查它們是否為 **null** ，然後再釋放它們。 此範例使用函式 `SafeRelease` ; 智慧型指標也是不錯的選擇。

如果您使用此模式，您必須小心使用迴圈結構。 在迴圈中，如果有任何呼叫失敗，請中斷迴圈。

優點

-   這個模式所建立的嵌套小於「nested ifs」模式。
-   您可以更輕鬆地查看整體控制流程。
-   資源會在程式碼中的某個時間點釋放。

缺點

-   所有變數都必須在函式頂端宣告和初始化。
-   如果呼叫失敗，函式會進行多個不必要的錯誤檢查，而不是立即結束函式。
-   因為控制流程會在失敗之後繼續執行函式，所以您必須在函式主體中小心，不要存取不正確資源。
-   迴圈內的錯誤需要特殊大小寫。

### <a name="jump-on-fail"></a>失敗時跳

在每個方法呼叫之後，測試失敗 (不是成功的) 。 失敗時，跳至接近函式底部的標籤。 在標籤之後，但在結束函式之前，釋放資源。


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



優點

-   您可以輕鬆看到整個控制流程。
-   檢查 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 之後，在程式碼中的每個點，如果您沒有跳到標籤，就保證所有先前的呼叫都已成功。
-   資源會在程式碼中的一個位置釋放。

缺點

-   所有變數都必須在函式頂端宣告和初始化。
-   某些程式設計人員不想在其程式碼中使用 **goto** 。  (不過，請注意， **這種用法是高度** 結構化的：程式碼永遠不會跳到目前的函式呼叫之外。 ) 
-   **goto** 語句會略過初始化運算式。

### <a name="throw-on-fail"></a>失敗時擲回

您可以在方法失敗時擲回例外狀況，而不是跳至標籤。 如果您用來撰寫例外狀況安全的程式碼，這可能會產生更慣用的 c + + 樣式。


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



請注意，此範例會使用 **CComPtr** 類別來管理介面指標。 一般而言，如果您的程式碼擲回例外狀況，您應該遵循 RAII (資源取得是) 模式的初始化。 也就是說，每個資源都應該由其可保證正確釋放資源的物件來管理。 如果擲回例外狀況，就一定會叫用此函式。 否則，您的程式可能會洩漏資源。

優點

-   與使用例外狀況處理的現有程式碼相容。
-   與擲回例外狀況的 c + + 程式庫相容，例如標準範本程式庫 (STL) 。

缺點

-   需要 c + + 物件來管理資源，例如記憶體或檔案控制代碼。
-   需要充分瞭解如何撰寫例外狀況安全程式碼。

## <a name="next"></a>下一個

[模組3。Windows 圖形](module-3---windows-graphics.md)

 

 
