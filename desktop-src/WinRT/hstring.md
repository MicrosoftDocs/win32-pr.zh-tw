---
description: Windows 執行階段字串的控制碼。
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: 'HSTRING (Hstring) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970996"
---
# <a name="hstring"></a>HSTRING

Windows 執行階段字串的控制碼。


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>備註

使用 **HSTRING** 代表 Windows 執行階段中的不可變字串。

JavaScript 和其他語言（例如 C 和 \# Microsoft Visual Basic）都可以使用使用 **HSTRING** 表示的字串。 下表顯示 **HSTRING** 如何以其他語言表示。



| 程式設計語言                                                                    | 字串表示                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [winrt：： hstring](/uwp/cpp-ref-for-winrt/hstring) 類別     |
| Visual C++ 元件延伸模組 ([c + +/cx](/cpp/cppcx/visual-c-language-reference-c-cx))  | [Platform：： String](/cpp/cppcx/platform-string-class) 類別 |
| JavaScript                                                                              | 字串物件                                              |
| .NET Framework                                                                          | System.String 類別                                        |



 

**HSTRING** 控制碼是標準的控制碼類型。 就語義而言，包含 **Null** 值的 **HSTRING** 代表空字串，其中包含零個內容字元和一個結束的 **Null** 字元。 以零個字元透過 [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) 建立字串，會產生控制碼值 **Null**。 使用值 **Null** 來呼叫 [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer)時，將會傳回空字串的指標，該字串後面只有 **NUL** 終止字元。 沒有相異值可代表未初始化的 **HSTRING** 。

呼叫 [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) 函式來建立新的 **HSTRING**，然後呼叫 [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) 函式來釋放支援字串記憶體的參考。 呼叫 [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) 函式來建立字串參考，也稱為 *快速傳遞字串*。

藉由呼叫 [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)函數來複製 **HSTRING** 。

藉由呼叫 [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) 函數來串連兩個字串。

藉由呼叫 [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) 函數來存取支援字串記憶體。

**HSTRING** 可以儲存和使用內嵌的 **NUL** 字元。 使用 [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) 函式在使用可能產生非預期結果的任何函式之前，先檢查內嵌的 **NUL** 字元。 例如，大部分的 Windows 函式會使用 **LPCWSTR** 做為輸入參數，而且只會計算字串的長度，直到遇到第一個 **NUL** 為止。

支援字串必須維持不變且以 null 終止。 當呼叫程式碼使用 [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) 函式來建立字串參考時，包含支援字串表示的記憶體是由呼叫端所擁有。 Windows 執行階段依賴原始字串的內容保持不變。 將字串參考傳遞至 Windows 執行階段時，呼叫端必須負責確保字串的內容不會改變，而且會在呼叫期間以 **NUL** 終止。 當呼叫傳回時，Windows 執行階段會釋放字串參考的所有參考。

當您以 out 參數的形式接收 **HSTRING** 時，最好在完成時將控制碼設為 **Null** 。

呼叫 [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) 函式來配置可變動的字串緩衝區，您可用來建立不可變的 **HSTRING**。 當您完成填入緩衝區時，就會呼叫 [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) 函數來建立 **HSTRING**。 這兩個階段的結構模式會啟用類似于「字串產生器」的功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Hstring。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
