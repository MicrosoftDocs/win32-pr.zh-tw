---
title: 陣列屬性
description: 陣列是索引或元素編號所存取的同質資料集合。
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- 陣列屬性 MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57682252c36284a89a3fb659c69446902c3d0181cbf82d494b200b5769e087e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808276"
---
# <a name="arrays-attribute"></a>陣列屬性

陣列是索引或元素編號所存取的同質資料集合。

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*類型-attr-list* 
</dt> <dd>

指定套用至類型的零或多個屬性。 有效的型別屬性包括 [**\[ 句 \] 柄**](handle.md)、 [**\[ 切換 \_ 類型 \]**](switch-type.md)、 [**\[ 傳輸 \_ 為 \]**](transmit-as.md); 指標屬性 [**\[ ref \]**](ref.md)、 [**\[ unique \]**](unique.md)或 [**\[ ptr \]**](ptr.md); 以及使用方式屬性 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)、 [**\[ 字串 \]**](string.md)和 [**\[ 略 \]**](ignore.md)過。 以逗號分隔多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定類型識別碼、基底類型、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型。 類型規格可以包含選擇性的儲存規格。

</dd> <dt>

*指標-decl* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中所使用的指標宣告子相同，它是以 **\* *_ 指示項、修飾詞（例如 _* 遠**）和限定詞 [**const**](const.md)等修飾詞所構成。

</dd> <dt>

*陣列-宣告子* 
</dt> <dd>

指定陣列的名稱，後面接著陣列的每個維度的下列其中一種結構： "**\[ \]**"、" **\[\*\]** "、" **\[** _const1_ *_\]_* " 或 " **\[** _lower .。。upper_ *_\]_* ：*較低* 和 *上限* 是代表下限和上限的常數值。 常數 *下限* 必須評估為零。

</dd> <dt>

*標籤* 
</dt> <dd>

指定結構或等位的選擇性標記。

</dd> <dt>

*欄位屬性清單* 
</dt> <dd>

指定套用至結構、聯集成員或函數參數的零或多個欄位屬性。 有效的欄位屬性 [**\[ 包括 \_ first \]**](first-is.md)、 [**\[ last \_ \]**](last-is.md) [**\[ 、length、 \_ length \]**](length-is.md)、 [**\[ \_ max \]**](max-is.md)、 [**\[ size、usage 屬性 \_ 字串和 ignore; 指標屬性 ref、unique 和 ptr; 以及 union 屬性參數類型。 \]**](size-is.md) [**\[ \]**](ref.md) [**\[ \_ \]**](switch-type.md) [**\[ \]**](string.md) [**\[ \]**](ignore.md) [**\[ \]**](unique.md) [**\[ \]**](ptr.md) 以逗號分隔多個欄位屬性。 請注意，上面列出的屬性（ **\[ first \_ ） \] 是**、 **\[ last \_ \]** 和 [**\[ ignore \]**](ignore.md)對等位無效。

</dd> <dt>

*有限運算式* 
</dt> <dd>

指定 C 語言運算式。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 [**\[ \] 回呼**](callback.md)、 [**\[ local \]**](local.md)、指標屬性 [**\[ ref \]**](ref.md)、 [**\[ unique \]**](unique.md)或 [**\[ ptr \]**](ptr.md); 以及使用方式屬性 [**\[ 字串 \]**](string.md)和 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*param-attr-list* 
</dt> <dd>

指定方向屬性以及套用至陣列參數的一或多個選擇性欄位屬性。 有效 [**\[ \_ 的 \]**](max-is.md)欄位屬性包括 max、 [**\[ size \_ \]**](size-is.md)、 [**\[ \_ length \]**](length-is.md)、 [**\[ first \_ 是 \]**](first-is.md)和 [**\[ last \_ 。 \]**](last-is.md)

</dd> </dl>

## <a name="remarks"></a>備註

MIDL 中的陣列使用類似于但與 C 和 c + + 不完全相同的樣式。 如需詳細資訊，請參閱 [MIDL 陣列](midl-arrays.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

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

[**處理**](handle.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
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

[**傳輸 \_ 為**](transmit-as.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 




