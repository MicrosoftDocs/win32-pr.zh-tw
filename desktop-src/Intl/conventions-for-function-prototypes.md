---
description: Windows SDK 在泛型、Windows 字碼頁和 Unicode 版本中提供函數原型。
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: 函數原型的慣例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd37171ed4cd1f0f00267b935ec57f17ef2957514b63d770efdc851b9c08bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746138"
---
# <a name="conventions-for-function-prototypes"></a>函數原型的慣例

Windows SDK 在泛型、 [Windows 字碼頁](code-pages.md)和[Unicode](unicode.md)版本中提供函數原型。 您可以編譯原型來產生 Windows 字碼頁原型或 Unicode 原型。 本主題將討論這三個原型，並使用 [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) 函式的程式碼範例來說明。

以下是泛用原型的範例。


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



標頭檔提供了實作成巨集的泛用函數名稱。


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



預處理器會將宏展開 Windows 字碼頁或 Unicode 函數名稱。 您可以視需要在泛型函式名稱的結尾加上字母 "A" (ANSI) 或 "W" (Unicode) 。 標頭檔接著會提供兩個特定的原型，一個用於 Windows 字碼頁，另一個用於 Unicode，如下列範例所示。


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



如[Windows 字串的資料類型](windows-data-types-for-strings.md)中所述，泛型函式原型會使用 text 參數的資料類型 LPCTSTR。 不過，Windows 字碼頁原型是使用 LPCSTR 類型，而 Unicode 原型則使用 LPCWSTR。

凡是具有文字引數的任何函數，應用程式通常都應使用泛用函數原型。 如果應用程式在標頭檔的 **\# include** 語句之前或編譯期間定義 "UNICODE"，語句將會編譯成 UNICODE 函式。

> [!Note]  
> 新的 Windows 應用程式應該使用 Unicode，以避免不同的程式字碼頁不一致，並方便當地語系化。 它們應該以泛型函式撰寫，且應該定義 UNICODE 以將函式編譯成 Unicode 函數。 在應用程式必須使用8位字元資料的幾個地方，它可以明確地使用 Windows 字碼頁的函式。

 

您的應用程式應該一律使用泛用函數原型搭配泛用字串和字元類型。 名稱以大寫 "W" 結尾的所有函數都是採用 Unicode (即寬字元) 參數。 某些函式只存在於 Unicode 版本中，而且只能搭配適當的資料類型使用。 例如， [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) 和 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 只有 Unicode 版本。

每個 Unicode 和字元集函式的參考檔中的需求一節提供支援的作業系統所執行之函式版本的相關資訊。 如果包含以 "Unicode" 開頭的行，此函式會有個別的 Unicode 和 Windows 字碼頁版本。

> [!Note]  
> 當函數具有字元字串的長度參數時，長度應該記錄為字串中的 TCHAR 值計數。 這種資料型別是指函式 Windows 字碼頁版本的位元組，或 Unicode 版本的16位單字。 不過，需要或傳回非類型記憶體區塊（例如 [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) 函式）之指標的函式通常會以位元組為單位，而不論使用的原型為何。 如果不具類型的記憶體配置是針對字串，則應用程式必須將字元數乘以 sizeof (TCHAR) 。 如需詳細資訊，請參閱 [使用泛型資料類型](using-generic-data-types.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows API 中的 Unicode](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
