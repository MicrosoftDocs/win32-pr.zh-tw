---
title: error_status_t 屬性
description: 錯誤 \_ 狀態 \_ t 關鍵字會指定物件的類型，該物件包含通訊狀態或錯誤狀態資訊。
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t 屬性 MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312218"
---
# <a name="error_status_t-attribute"></a>錯誤 \_ 狀態 \_ t 屬性

**錯誤 \_ 狀態 \_ t** 關鍵字會指定物件的類型，該物件包含通訊狀態或錯誤狀態資訊。

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*ACF 函式-屬性* 
</dt> <dd>

指定零個或多個 ACF 函數屬性，例如， **\[** [**comm \_ status**](comm-status.md) **\]** 、 **\[** [**fault \_ status**](fault-status.md) **\]** 或 **\[** [**了 nocode**](nocode.md) **\]** 。 函數屬性以方括弧括住。 有零或多個屬性可以套用至函數。 以逗號分隔多個函式屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 IDL 檔案中所定義的函式名稱。

</dd> <dt>

*ACF-參數-屬性* 
</dt> <dd>

指定適用于參數的屬性。 請注意，您可以將零個、一個或多個屬性套用至參數。 以逗號分隔多個參數屬性。 參數屬性以方括弧括住。 ACF 中不允許 IDL 參數屬性（例如方向屬性）。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定 IDL 檔案中定義之函數的參數。 函數的每個參數都必須以相同的順序指定，且使用與 IDL 檔案中所定義的相同名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**錯誤 \_ 狀態 \_ t** 類型會當做 IDL 中例外狀況處理架構的一部分來使用。 此類型對應到不 [**帶正負**](unsigned.md)號的 [**long**](long.md)。 捕捉錯誤情況的應用程式具有 **\[** [](out-idl.md) **\]** 指定為 **錯誤 \_ 狀態 \_ t** 之程式的 OUT 參數或傳回類型，並使用 ACF 中的 [通訊狀態] 或 [錯誤狀態] 屬性來限定 **錯誤 \_ 狀態 \_ t** **\[** [**\_**](comm-status.md) **\]** **\[** [**\_**](fault-status.md) **\]** 。 如果參數或傳回型別未以 **\[ comm \_ 狀態 \]** 或 **\[ 錯誤 \_ 狀態 \]** 屬性限定，則參數的運作方式就如同不帶正負號的 long。

從2.0 版開始，MIDL 編譯器會產生包含適當錯誤處理架構的存根。 不過，舊版 MIDL 編譯器會處理參數或傳回 **錯誤 \_ 狀態 \_ t** 的型別，如同已套用的 **\[** [**通訊 \_ 狀態**](comm-status.md) **\]** 和 **\[** [**錯誤 \_ 狀態**](fault-status.md) **\]** 屬性一樣，即使它們不是也是一樣。 使用 MIDL 2.0 或更新版本時，您必須明確地將 **\[ 通訊 \_ 狀態 \]** 和 **\[ 錯誤 \_ 狀態 \]** 屬性套用至 ACF 中的參數或程式。

**錯誤 \_ 狀態 \_ t** 類型是其中一種預先定義的介面定義語言類型。 預先定義的型別可以在 [**typedef**](typedef.md) 宣告中顯示為類型指定名稱，在一般宣告中，也可以在函式宣告子中做為函式的傳回型別或) 的參數類型指定名稱， (。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**通訊 \_ 狀態**](comm-status.md)
</dt> <dt>

[**錯誤 \_ 狀態**](fault-status.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> </dl>

 

 




