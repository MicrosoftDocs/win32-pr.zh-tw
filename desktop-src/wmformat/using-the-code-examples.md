---
title: 使用 Windows Media Format SDK 程式碼範例
description: 使用 Windows Media Format SDK 程式碼範例
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK，程式碼範例
- Windows Media Format SDK，範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383785"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>使用 Windows Media Format SDK 程式碼範例

此 SDK 的許多說明章節都包含程式碼範例。 這些範例會盡可能清楚且簡潔地撰寫。 閱讀範例時，您應該注意下列慣例。

-   所有範例都假設為包含 windows .h 和 wmsdk .h。 解說文字中提及任何其他必要的標頭檔。
-   如果發生錯誤，則錯誤檢查已限制為無法中斷函數。 在應用程式中，您應該檢查特定的錯誤碼，並提供某種類型的錯誤報表。

    檢查傳回 **HRESULT** 值的方法或函式傳回值時，您應該使用 **FAILED** 宏來探索傳回值是否指出失敗。

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    本檔中的許多範例都使用名為 GOTO EXIT 的宏 \_ \_ \_ （如果失敗），這是在下列程式碼中定義的。

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    這些範例函式每個都有一個名為 "Exit：" 的標記，之後會釋出函式中配置的所有介面和記憶體，並傳回錯誤碼（如果有的話）。

-   在程式碼範例中，會使用名為 SAFE \_ RELEASE 和 safe \_ ARRAY DELETE 的宏來釋放介面和記憶體 \_ 。 這些宏會在下列程式碼中定義：
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   通常，您必須在另一個範例中包含一個範例的邏輯，讓範例有意義。 在這些情況下，會包含 TODO 批註以及適當程式碼範例的參考。
-   為了讓程式碼更容易閱讀，本檔中的範例函式都不會驗證其輸入參數。 如果您將任何這些函式複製到您的程式碼中，您應該驗證任何輸入參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](getting-started.md)
</dt> </dl>

 

 




