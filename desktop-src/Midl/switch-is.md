---
title: switch_is 屬性
description: '\ 參數 \_ 是 \ 屬性，它會指定運算式或識別碼，做為選取聯集成員的聯集判別。'
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is 屬性 MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1975dcf38a04fc127de199e7cc663c8af41b63e6ce8f92d38be2115316ed0727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382839"
---
# <a name="switch_is-attribute"></a>切換 \_ 為屬性

**\[ 參數 \_ 為 \]** attribute 指定運算式或識別碼，做為選取聯集成員的聯集判別。

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*結構標記* 
</dt> <dd>

指定結構的選擇性標記。

</dd> <dt>

*有限-expr* 
</dt> <dd>

指定 MIDL 所支援的 C 語言運算式。 幾乎所有的 C 語言運算式都受到支援。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許前置和後置遞增以及前置和後置遞減運算子。

</dd> <dt>

*欄位-attr-list* 
</dt> <dd>

指定適用于聯集成員的零或多個欄位屬性。 有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 和 **\[** [**coNtext \_ 控制碼**](context-handle.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md); **\]** 以及本身聯集的成員（union attribute **\[** [**switch \_ 型**](switch-type.md)別） **\]** 。 以逗號分隔多個欄位屬性。

</dd> <dt>

*union 類型規範* 
</dt> <dd>

指定聯 [**集**](union.md) 類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*宣告子和宣告子清單* 
</dt> <dd>

指定標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。 在遠端程序呼叫中傳輸的等位中，不允許 (函式宣告子和位欄位宣告。 未傳輸的等位中允許這些宣告子。 ) 以逗號分隔多個宣告子。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local、**](local.md) **\]** 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*指標宣告子* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*param-attr-list* 
</dt> <dd>

指定適用于指定之參數類型的零或多個屬性。 參數屬性可以取得和 **\[ \] 輸出** 方向 **\[ \] 性屬性，** **\[ 第一個 \_ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** 欄位屬性 **\[ \_ 是、最後一個、長度為、最大值、大小為，以及切換類型、指標屬性 ref、unique 或 ptr; 以及 usage 屬性內容控制碼和字串。 \]** **\[ \_ \]** Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。 以逗號分隔多個屬性。

</dd> <dt>

*聯集類型* 
</dt> <dd>

識別聯 [**集**](union.md) 類型規範。

</dd> </dl>

## <a name="remarks"></a>備註

與 **\[ \_ 參數 \]** 相關聯的判別必須在與聯集相同的邏輯層級上定義：

-   當 union 是參數時，聯集判別必須是另一個參數。
-   當聯集是結構的欄位時，判別必須是相同結構的另一個欄位。

結構或函數參數清單中的順序並不重要。 聯集可以在判別之前或之後。

參數的屬性可以顯示為欄位屬性，或做為參數屬性。 **\[ \_ \]**

## <a name="examples"></a>範例

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[封裝聯集](encapsulated-unions.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[Nonencapsulated 聯集](nonencapsulated-unions.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 




