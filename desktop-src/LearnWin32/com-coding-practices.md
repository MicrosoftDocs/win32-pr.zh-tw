---
title: COM 編碼作法
description: 本主題說明讓您的 COM 程式碼更有效率且更穩固的方式。
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104093436"
---
# <a name="com-coding-practices"></a>COM 編碼作法

本主題說明讓您的 COM 程式碼更有效率且更穩固的方式。

-   [\_ \_ Uuidof 運算子](/windows)
-   [IID \_ PPV \_ ARGS 宏](/windows)
-   [SafeRelease 模式](#the-saferelease-pattern)
-   [COM 智慧型指標](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>\_ \_ Uuidof 運算子

當您建立程式時，可能會收到類似下列的連結器錯誤：

`unresolved external symbol "struct _GUID const IID_IDrawable"`

此錯誤表示 GUID 常數是使用外部連結 (**extern**) 宣告，而連結器找不到常數的定義。 GUID 常數的值通常會從靜態程式庫檔案匯出。 如果您使用 Microsoft Visual C++，則可以避免使用 **\_ \_ uuidof** 運算子連結靜態程式庫的需求。 此運算子是 Microsoft 語言擴充功能。 它會從運算式傳回 GUID 值。 運算式可以是介面型別名稱、類別名稱或介面指標。 使用 **\_ \_ uuidof**，您可以建立一般專案對話方塊物件，如下所示：


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



編譯器會從標頭中解壓縮 GUID 值，因此不需要任何程式庫匯出。

> [!Note]  
> GUID 值是藉由 `__declspec(uuid( ... ))` 在標頭中宣告來與型別名稱相關聯。 如需詳細資訊，請參閱 Visual C++ 檔中的 **\_ \_ declspec** 檔。

 

## <a name="the-iid_ppv_args-macro"></a>IID \_ PPV \_ ARGS 宏

我們看到 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)和 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))都需要將最後一個參數強迫回 **void \* \*** 型別。 這會造成類型不符的可能性。 請考慮下列程式碼片段：


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



此程式碼會要求 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 介面，但會傳入 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 指標。 **重新解譯 \_ cast** 運算式會規避 c + + 類型系統，因此編譯器不會攔截這個錯誤。 在最佳情況下，如果物件不會執行要求的介面，呼叫就會失敗。 在最糟的情況下，函式會成功，而且您會有不相符的指標。 換句話說，指標類型與記憶體中的實際 vtable 不相符。 如您所見，此時不會有任何好處。

> [!Note]  
> *Vtable* (虛擬方法資料表) 是函數指標的資料表。 Vtable 是 COM 如何在執行時間將方法呼叫系結至其實作為。 剛好，vtable 是大部分 c + + 編譯器如何執行虛擬方法的方式。

 

[**IID \_ PPV \_ ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args)宏可協助避免此錯誤類別。 若要使用這個宏，請取代下列程式碼：


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



取代為這個：


```C++
IID_PPV_ARGS(&pFileOpen)
```



宏會自動插入 `__uuidof(IFileOpenDialog)` 介面識別碼，因此保證會符合指標類型。 以下是修改過的 (和正確的) 程式碼：


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



您可以搭配使用相同的宏與 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))：


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>SafeRelease 模式

參考計數是在程式設計中的其中一項作業，基本上是很簡單，但也很繁瑣，讓您很容易出錯。 一般錯誤包含：

-   當您完成使用介面指標時，無法釋放介面指標。 這個 bug 類別會導致您的程式流失記憶體和其他資源，因為物件並未損毀。
-   呼叫具有無效指標的 [**版本**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。 例如，如果從未建立物件，就會發生這個錯誤。 這類 bug 可能會導致您的程式損毀。
-   呼叫 [**發行**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 之後的介面指標。 這個 bug 可能會導致您的程式損毀。 更糟的是，它可能會導致您的程式在一段時間後損毀，因此難以追蹤原始錯誤。

避免這些錯誤的其中一種方式，是透過安全釋放指標的函式來呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。 下列程式碼顯示執行此動作的函式：


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



此函式會採用 COM 介面指標做為參數，並執行下列動作：

1.  檢查指標是否為 **Null**。
2.  如果指標不是 **Null**，則呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。
3.  將指標設定為 **Null**。

以下是如何使用的範例 `SafeRelease` ：


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



如果 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 成功，則為 `SafeRelease` 釋放指標的呼叫。 如果 **CoCreateInstance** 失敗， *PFileOpen* 會維持 **Null**。 此函式會 `SafeRelease` 檢查這一點，並略過 [**發行**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)的呼叫。

也可以安全地 `SafeRelease` 在相同的指標上呼叫一次以上，如下所示：


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>COM 智慧型指標

函式 `SafeRelease` 很有用，但您需要記住兩件事：

-   將每個介面指標初始化為 **Null**。
-   `SafeRelease`在每個指標超出範圍之前呼叫。

如果您是 c + + 程式設計人員，您可能會認為您不需要記住這其中一項。 畢竟，c + + 具有函式和析構函數。 要有一個包裝基礎介面指標的類別，並自動初始化和釋放指標，是很好的作法。 換句話說，我們需要像這樣的內容：


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



此處所示的類別定義不完整，而且無法使用，如下所示。 您至少需要定義複製的函式、指派運算子，以及存取基礎 COM 指標的方式。 幸運的是，您不需要執行這項工作，因為 Microsoft Visual Studio 已經提供智慧型指標類別做為 Active Template Library (ATL) 的一部分。

ATL 智慧型指標類別的名稱是 **CComPtr**。  (也有一個 **CComQIPtr** 類別，這並不在此討論 ) 。此處的 [開啟對話方塊](example--the-open-dialog-box.md) 範例已重寫為使用 **CComPtr**。


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



這段程式碼與原始範例之間的主要差異在於，這個版本不會明確地呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)。 當 **CComPtr** 實例超出範圍時，此函式會在基礎指標上呼叫 **Release** 。

**CComPtr** 是類別範本。 範本引數是 COM 介面型別。 就內部而言， **CComPtr** 會保存該型別的指標。 **CComPtr** 會覆寫 **運算子-> ()** 和 **運算子& ()** 讓類別的行為就像基礎指標。 例如，下列程式碼相當於直接呼叫 **IFileOpenDialog：： Show** 方法：


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** 也會定義 **CComPtr：： CoCreateInstance** 方法，它會使用一些預設參數值來呼叫 COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。 唯一必要的參數是類別識別碼，如下一個範例所示：


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



**CComPtr：： CoCreateInstance** 方法純粹是為了方便起見而提供;如果您想要的話，還是可以呼叫 COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函數。

## <a name="next"></a>下一個

[COM 中的錯誤處理](error-handling-in-com.md)

 

 