---
title: union 屬性
description: Union 關鍵字會出現在與區分等位相關聯的函式中。
ms.assetid: 135a6581-e03e-4b90-9fd8-15690820dbd0
keywords:
- union 屬性 MIDL
topic_type:
- apiref
api_name:
- union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc683472d67775c4a2900695246d5f9ca920ca32
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507589"
---
# <a name="union-attribute"></a>union 屬性

**Union** 關鍵字會出現在與區分等位相關聯的函式中。

``` syntax
/* Encapsulated union*/
typedef [[ [type-attribute-list] ]] union [[ struct-name ]] switch (switch-type switch-name) [[ union-name ]] 
{
  C-style-case-list 
  [[ [ field-attribute-list <> ] ]] type-specifier <> declarator-list <>;

        ...
}

/* Non-encapsulated union*/
typedef [switch_type(switch-type) [[ , type-attr-list ]] ] union [[ tag ]] 
{ 
    [ case ( limited-expr-list) ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  [[ [ default ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  ]]
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至聯集類型的零或多個屬性。 有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md)、 **\]** 指標屬性 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md)， **\]** 以及 **\[** [**忽略**](ignore.md) **\]** 。 封裝聯集也可以有 **\[** [**ref**](ref.md) **\]** 指標類型屬性。 以逗號分隔多個屬性。

</dd> <dt>

*結構名稱* 
</dt> <dd>

指定選擇性標記，此標記會為 MIDL 編譯器所產生的結構命名。

</dd> <dt>

*切換類型* 
</dt> <dd>

指定 [**int**](int.md)、 [**char**](char-idl.md)、 [**列舉**](enum.md) 型別或解析成其中一種類型的識別碼。

</dd> <dt>

*參數名稱* 
</dt> <dd>

指定作為聯集判別之類型 *參數* 類型的變數名稱。

</dd> <dt>

*聯集-名稱* 
</dt> <dd>

指定選擇性的識別碼，此識別碼會命名結構中的聯集（由 MIDL 編譯器所產生），其中包含聯集和判別。

</dd> <dt>

*C 樣式-大小寫清單* 
</dt> <dd>

"**Case** *const-expr* ：" 的清單

</dd> <dt>

*有限運算式清單* 
</dt> <dd>

指定一或多個 C 語言運算式。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。 清單中的個別運算式應以逗號分隔。

</dd> <dt>

*欄位屬性清單* 
</dt> <dd>

指定套用至聯集成員的零或多個欄位屬性。 有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**\_ length**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size \_**](size-is.md)、usage、 **\]** usage **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** 、coNtext、coNtext、 **\[** [**coNtext \_**](context-handle.md)、 **\]** **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md)、 **\]** and （適用于 nonencapsulated 聯集的成員）、union 屬性 **\[** [**參數 \_ 類型**](switch-type.md) **\]** 。 Nonencapsulated 等位也可以使用 **\[** [**ref**](ref.md) **\]** 指標欄位屬性。 以逗號分隔多個欄位屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、**等位、**[**列舉**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

一或多個標準 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 在遠端程序呼叫中傳輸的等位中，不允許 (函式宣告子和位欄位宣告。 除非您使用 MIDL 編譯器參數 [**/osf**](-osf.md)，否則不會傳送的等位中可以有這些宣告子。 ) 以逗號分隔多個宣告子。

</dd> <dt>

*標籤* 
</dt> <dd>

指定選擇性標記。

</dd> </dl>

## <a name="remarks"></a>備註

MIDL 支援兩種差異聯集類型： [封裝](encapsulated-unions.md) 的等位和 [nonencapsulated](nonencapsulated-unions.md)聯集。 封裝聯集與先前的 RPC (NCA 版本 1) 相容。 Nonencapsulated 聯集會排除封裝聯集的某些限制，並提供比封裝聯集更可見的判別。

封裝聯集是由 [**switch**](switch.md) 關鍵字來識別，而不是其他等位相關的關鍵字。

Nonencapsulated 聯集（也稱為「聯集」）是由 switch 的存在所識別， **\[** [**\_**](switch-is.md) **\]** 而 **\[** [**switch \_ 型**](switch-type.md)別關鍵字則是用 **\]** 來識別判別及其型別。

當您使用 **\[** [**in**](in.md)、 [**out**](out-idl.md) **\]** 等位時，請注意在呼叫期間變更 union 參數的值，可能會讓遠端呼叫的行為與本機呼叫的行為不同。 傳回時，存根會將 in、 **\] out** 參數複製到已存在於用戶端上的記憶體 **\[ 中**。 當遠端程式修改 union 參數的值，因而變更資料物件的大小時，存根可以用 **\[ out \]** 值覆寫有效的記憶體。 當 union switch 將資料物件從基底類型變更為指標類型時，當存根將指標指向的記憶體位置複製到基底類型的 **\[ in \]** 值所指示的記憶體位置時，就可以覆寫有效的記憶體。

等位的形狀在各平臺之間必須相同，以確保互連能力。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[封裝聯集](encapsulated-unions.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[Nonencapsulated 聯集](nonencapsulated-unions.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**切換 \_ 為**](switch-is.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> </dl>

 

 




