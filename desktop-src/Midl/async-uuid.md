---
title: async_uuid 屬性
description: '\ Async \_ uuid \ 介面屬性會指示 MIDL 編譯器定義 COM 介面的同步和非同步版本。'
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- async_uuid 屬性 MIDL
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fd7b4d9d9bf7a595415e55de778a419d91051c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092678"
---
# <a name="async_uuid-attribute"></a>async \_ uuid 屬性

**\[ Async \_ uuid \]** 介面屬性會指示 MIDL 編譯器定義 COM 介面的同步和非同步版本。

``` syntax
[ 
    object, 
    uuid(string-uuid1), 
    async_uuid(string-uuid2)[ [, interface-attribute-list] 
]
interface interface-name : base-interface
{
    interface-definition
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*字串-uuid1* 
</dt> <dd>

Uuidgen.exe 公用程式所產生的 UUID 字串，可識別介面的同步版本。

</dd> <dt>

*字串-uuid2* 
</dt> <dd>

Uuidgen.exe 公用程式所產生的 UUID 字串，可識別介面的非同步版本。

</dd> <dt>

*介面屬性清單* 
</dt> <dd>

適用于整個介面的其他屬性。 您無法在 COM 介面中使用 [**\[ version \]**](version.md)屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

介面的名稱。

</dd> <dt>

*基底介面* 
</dt> <dd>

由此介面衍生的介面。 基底介面必須是 **iunknown** 或非同步介面（直接或間接衍生自 **iunknown**）。

</dd> <dt>

*介面定義* 
</dt> <dd>

指定組成介面定義的 IDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

使用這個屬性需要 Windows 2000 或更新版本的 Windows。

當您將 **\[ async \_ uuid \]** 屬性套用至 COM 介面 (也就是具有 [**\[ 物件 \]**](object.md)屬性) 的介面時，MIDL 編譯器除了傳統的同步版本之外，還會產生介面的非同步定義。 非同步介面會有與同步介面相同的名稱，但使用 "Async" 前置詞。 介面識別碼 (IID) 將會是指定為 **\[ 非同步 \_ UUID \]** 屬性參數的 UUID。

針對非同步介面，MIDL 會將每個方法分割成不同的 *begin* 和 *finish* 方法。 *Begin* 方法的同步方法名稱具有 "begin \_ " 前置詞，並包含來自同步方法的所有 [**\[ \] in**](in.md)參數。 *完成* 方法具有具有 "finish" 前置詞的同步方法名稱 \_ ，並且包含同步方法中的所有 [**\[ out \]**](out-idl.md)參數。 如果同步方法具有任何 **\[ in、out \] 參數，** 則這些參數會包含在 *begin* 和 *finish* 非同步方法中。

如果非同步介面方法具有 [**\[ 呼叫 \_ AS \]**](call-as.md)屬性，MIDL 將會產生 *begin* 和 *finish* 方法的宣告。 您必須執行這兩種方法。

每個非同步介面都是同步介面上的修飾詞，因此沒有個別的繼承圖形。 這表示您無法從非 **IUnknown**) 以外的非同步介面 (定義同步介面。 也不能同步介面繼承自非同步介面。 如果您嘗試其中一項，MIDL 編譯器將會發出錯誤訊息。

## <a name="examples"></a>範例

``` syntax
[
    object, 
    uuid(0c733a30-2a1c-11ce-ade5-00aa0044773d),
    async_uuid(1c733a30-2a1c-11ce-ade5-00aa0044773d),
    pointer_default(unique)
]
interface IMyInterface : IUnknown
{
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[定義 COM 介面](/windows/desktop/com/defining-com-interfaces)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**呼叫 \_ as**](call-as.md)
</dt> <dt>

[**iid \_ 為**](iid-is.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**物件**](object.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 