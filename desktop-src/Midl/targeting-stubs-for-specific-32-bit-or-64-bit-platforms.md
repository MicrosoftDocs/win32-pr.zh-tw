---
title: 以特定32位或64位平臺為目標的存根
description: Microsoft RPC 和 MIDL 3.0 和更新版本編譯器的部分功能是平臺特定的功能。
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- 32位平臺 MIDL
- 64位平臺 MIDL
- stub MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e0f78e47ed078bf7cd1fd78fa8730b597554a6c8ba1ed4fc5a67bc562e7d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641168"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>以特定32位或64位平臺為目標的存根

Microsoft RPC 和 MIDL 3.0 和更新版本編譯器的部分功能是平臺特定的功能。

為了預防起見，MIDL 3.0 和更新版本的編譯器會產生防止在 C 編譯階段進行相容性檢查的防護。 MIDL 會產生兩種類型的防護：與平臺相關的防護 (32 位和64位) ，以及相依于 (功能集相依性) 的相依性防護。 例如，MIDL 會產生下列防護，以防止 C-編譯其他平臺的32位存根：

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

發行相依的防護是由在處理的 IDL 檔案 (s) 和 [**/target**](-target.md) 參數中找到的一組功能所觸發。 例如，如果介面使用僅在 Windows 2000 或更新版本上支援的功能，MIDL 會產生具有目標 \_ \_ NT50 \_ 或 \_ 更新版本宏的防護。

Rpcndr 中定義的 guard 宏取決於 WINVER 和 WIN32 WINNT 的設定， \_ \_ 並由 C/c + + 編譯器進行評估。

如果您在 C 編譯時間收到錯誤訊息，指出您需要特定平臺來執行存根，請先檢查以確定您未使用此平臺上無法使用的功能。 觸發特定防護的功能會列在此防護主體中。 在上述範例中，-Oicf 編譯器參數觸發了此防護。 這種類型的值得注意的功能包括 [**/robust**](-robust.md)參數和 \[ [](async.md) \] windows 2000 和更新版本上可用的 async 屬性、[**管道**](pipe.md)類型的函式、/Oif 編譯器選項，以及 \[ [**使用者 \_ 封送**](user-marshal.md)處理 \] 和 \[ [**網路 \_ 封送**](wire-marshal.md)處理 \] 屬性。 使用這些功能的存根將無法在舊版系統上執行。

如果您知道您的目標平臺對您所使用的功能而言是正確的，但仍收到錯誤，您可能需要適當地設定環境變數。

**若要建立 Windows 2000 或更新版本**

-   將這一行新增至您的 makefile：

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**/target**](-target.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**async**](async.md)
</dt> <dt>

[**非同步 \_ uuid**](async-uuid.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**管道**](pipe.md)
</dt> <dt>

[**網路 \_ 封送處理**](wire-marshal.md)
</dt> <dt>

[**使用者 \_ 封送處理**](user-marshal.md)
</dt> <dt>

[封送處理 OLE 資料類型](marshaling-ole-data-types.md)
</dt> </dl>

 

 




