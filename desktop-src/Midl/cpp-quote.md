---
title: cpp_quote 屬性
description: Cpp \_ 引號關鍵字會指示 MIDL 將指定的字串（不含引號字元）發出至產生的標頭檔。
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote 屬性 MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022596"
---
# <a name="cpp_quote-attribute"></a>cpp \_ quote 屬性

**Cpp \_ 引號** 關鍵字會指示 MIDL 將指定的字串（不含引號字元）發出至產生的標頭檔。

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>參數

<dl> <dt>

*string* 
</dt> <dd>

指定在產生的標頭檔中發出的加上引號的字串。 字串必須以引號括住，以防止 C 預處理器進行擴充。

</dd> </dl>

## <a name="remarks"></a>備註

出現在 IDL 檔案中的 c 語言前置處理指示詞是由 C 編譯器的預處理器所處理。 IDL 編譯期間會提供 IDL 檔案中的 **\# 定義** 指示詞，但 C 編譯器無法使用這些指示詞。

例如，當預處理器遇到「定義 WINDOWS 4」指示詞時 \# ，預處理器會將 IDL 檔案中所有出現的 "WINDOWS" 取代為 "4"。 C 語言編譯期間無法使用符號 "WINDOWS"。

若要允許 C 預處理器巨集定義傳遞 MIDL 編譯器至 C 編譯器，請使用 **\# pragma MIDL \_ echo** 或 **cpp \_ 引號** 指示詞。 這些指示詞會指示 MIDL 編譯器產生包含參數字串的標頭檔，並移除引號。 **\# Pragma midl \_ echo** 和 **cpp \_ 引號** 指示詞是相等的。

MIDL 編譯器會將 **cpp \_ 引號** 和 [**pragma**](pragma.md) 指示詞中所指定的字串，以 idl 檔案中指定的順序，以及 idl 檔案中其他介面元件的相對順序，放在標頭檔中。 在所有匯 [**入**](import.md) 作業之後，字串通常應該會出現在 IDL 檔案介面主體區段中。

## <a name="examples"></a>範例

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**進口**](import.md)
</dt> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




