---
title: C-MIDL 的預處理器需求
description: 此頁面僅適用于具有特定原因的開發人員，以將 Microsoft C/c + + 預處理器取代為 MIDL 所使用的預處理器，或必須指定自訂預處理器參數的開發人員。
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL 編譯器 MIDL、C-預處理器、需求
- C-預處理器 MIDL，需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932441"
---
# <a name="c-preprocessor-requirements-for-midl"></a>C-MIDL 的預處理器需求

此頁面僅適用于具有特定原因的開發人員，以將 Microsoft C/c + + 預處理器取代為 MIDL 所使用的預處理器，或必須指定自訂預處理器參數的開發人員。 MIDL 參數 [**/cpp \_ cmd**](-cpp-cmd.md)、 [**/cpp \_ opt**](-cpp-opt.md)和 [**/no \_ cpp**](-no-cpp-nocpp.md) 可用來覆寫編譯器的預設行為。 通常不需要取代 Microsoft C/c + + 預處理器，也不需要指定自訂的預處理器參數。

MIDL 編譯器會在 IDL 檔案的初始處理期間使用 C 預處理器。 編譯 IDL 檔案時所使用的組建環境與預設的 C/c + + 預處理器相關聯。 如果要使用不同的預處理器，MIDL 編譯器參數 [**/cpp \_ cmd**](-cpp-cmd.md) 會啟用預設 C/c + + 預處理器名稱的覆寫：

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*預處理器 \_ 名稱*
</dt> <dd>

指定 MIDL 要使用的預處理器名稱。 可以使用二進位檔的路徑來指定。 .Exe 副檔名是選擇性的。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

指定 IDL 檔案的名稱。

</dd> </dl>

-   MIDL 編譯器預期任何預處理器都必須遵守下列慣例：
-   輸入檔會指定為命令列上的最後一個引數。
-   預處理器必須將輸出重新導向至標準輸出裝置（stdout）。
-   在預處理器的輸出資料流程中，會出現 **\# 行** 指示詞，以啟用更佳的診斷訊息。
-   Line 指示詞是輸出資料流程中唯一的預處理器指示詞。

MIDL 假設衍生的預處理器已從編譯器的輸入資料流程中移除所有預處理器指示詞，但在編譯器訊息中指出來源位置所需的行指示詞除外。 當指出不同于 Microsoft C/c + + 預處理器的預處理器，或使用 [**/cpp \_ opt**](-cpp-opt.md) 參數指定預處理器選項時，必須指定適當的預處理器選項，以在編譯器的輸入資料流程中放置行指示詞。 例如，針對 Microsoft C/c + + 預處理器，必須使用 **/e** 選項：

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

MIDL 會接受下列其中一種形式的 **\# 行** 指示詞：

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

如需直線指示詞和其他預處理器指示詞的完整說明，請參閱所使用之 C 編譯器的檔。

MIDL 只接受行預處理器指示詞。 因此，如果使用 [**/no \_ cpp**](-no-cpp-nocpp.md) 參數，則輸入檔案不能有其他的預處理器指示詞，或者輸入檔必須在叫用 MIDL 之前經過處理。

如需詳細資訊，請參閱 [處理 \# IDL 檔案中的定義](dealing-with-defines-in-idl-files-2.md)。

 

 




