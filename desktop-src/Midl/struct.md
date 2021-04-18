---
title: struct 屬性
description: Struct 關鍵字用於結構類型規範中。
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- struct 屬性 MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106976336"
---
# <a name="struct-attribute"></a>struct 屬性

**Struct** 關鍵字用於結構類型規範中。

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*結構標記* 
</dt> <dd>

指定結構的選擇性標記。

</dd> <dt>

*欄位屬性清單* 
</dt> <dd>

指定套用至結構成員的零或多個欄位屬性。 有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length、 \_ length**](length-is.md) **\]** 、 **\[** [**max \_ 為**](max-is.md) **\]** 和 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 和 **\[** [**ignore**](ignore.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 union 屬性 **\[** [**參數 \_ 類型**](switch-type.md) **\]** 。 以逗號分隔多個欄位屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、 **結構**、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。 在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。 未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。

</dd> </dl>

## <a name="remarks"></a>備註

IDL 結構類型規範（ **struct**）與標準 C 類型規範的差異如下：

-   每個結構成員都可以與選擇性欄位屬性相關聯，這些屬性會描述該結構成員的特性，以供遠端程序呼叫之用。
-   在遠端程序呼叫中使用的結構中不允許使用位欄位和函數宣告子。 只有當結構不是在網路上傳輸時，才能使用這些標準 C 宣告子結構。

結構的形狀在各平臺之間必須相同，以確保互連能力。

## <a name="examples"></a>範例

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**/c \_ ext**](-c-ext.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 