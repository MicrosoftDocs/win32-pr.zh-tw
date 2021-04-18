---
title: out 屬性
description: '\\ 屬性會識別從被呼叫程式傳回至呼叫程式的指標參數， (從伺服器到用戶端) 。'
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- out 屬性 MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965234"
---
# <a name="out-attribute"></a>out 屬性

\[ **Out** \] 屬性會識別從呼叫程式傳回至呼叫程式的指標參數， (從伺服器到用戶端) 。

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 \[ [**回呼**](callback.md) \] 、 \[ [**local**](local.md)、 \] 指標屬性 \[ [**ref**](ref.md) \] 、 \[ [**unique**](unique.md) \] 或 \[ [**ptr**](ptr.md) \] ; 以及使用方式屬性 \[ [**字串**](string.md) \] 、 \[ [**忽略**](ignore.md) \] 和 \[ [**內容 \_ 控制碼**](context-handle.md) \] 。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底 \_ 類型](midl-base-types.md)、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*指標宣告子* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

指定適用于指定之參數類型的零或多個屬性。 具有 out 屬性的參數屬性 \[  \] 也可以取得方向屬性 \[  \] \[ ，[**第一個欄位屬性 \_ 是**](first-is.md) \] 、 \[ [**last \_**](last-is.md) \] 、 \[ [**length、 \_**](length-is.md) \] max、size、 \[ [**\_**](max-is.md) \] \[ [**\_ size**](size-is.md) \] 、and \[ [**switch \_ type**](switch-type.md)、 \] 指標屬性 \[ [**ref**](ref.md) \] 、 \[ [**unique**](unique.md) \] 或 \[ [**ptr**](ptr.md) \] ; 以及 usage 屬性 \[ [**內容 \_ 控制碼**](context-handle.md) \] 和 \[ [**字串**](string.md) \] 。 Usage 屬性 \[ [**ignore**](ignore.md) \] 不能用來做為參數屬性。 以逗號分隔多個屬性。

</dd> <dt>

*符中* 
</dt> <dd>

指定標準宣告子，例如識別碼、指標宣告子和陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。

</dd> </dl>

## <a name="remarks"></a>備註

\[ **Out** \] 屬性工作表示在記憶體中作為指標的參數和其相關聯的資料，會從被呼叫的程式傳回給呼叫程式。

\[ **Out** \] 屬性必須是指標。 在參數宣告中，DCE IDL 編譯器需要有明確的 \* ，做為指標宣告子。 Microsoft IDL 提供的延伸模組會捨棄這項需求，並允許陣列或先前定義的指標類型。

中的相關屬性（attribute） \[ [](in.md) \] 表示參數是從呼叫程式傳遞至被呼叫的進程。 \[ **In** \] 和 \[ **out** \] 屬性指定傳遞參數的方向。 參數可以定義為 \[  \] 僅限 in、 \[ **out** \] 或 \[ **in**、 **out** \] 。

\[  \] 當呼叫遠端程式時，系統會假設不定義 out 參數，而伺服器會設定物件的記憶體。 因為最上層指標/參數必須一律指向有效的儲存體，因此不能是 **Null**，所以 \[  \] 無法套用至最上層的 \[ [**unique**](unique.md) \] 或 \[ [**ptr**](ptr.md) \] 指標。 \[**唯一** \] 或 \[ **ptr** \] 指標的參數必須是 \[ [**in**](in.md) \] 或 \[ **in**、 **out** \] 參數。

## <a name="examples"></a>範例

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 