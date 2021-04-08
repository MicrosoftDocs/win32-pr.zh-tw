---
title: defaultcollelem 屬性
description: '\ Defaultcollelem \ 屬性會將屬性標示為預設集合之元素的存取子函數。'
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- defaultcollelem 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023422"
---
# <a name="defaultcollelem-attribute"></a>defaultcollelem 屬性

**\[ Defaultcollelem \]** 屬性會將屬性標示為預設集合之元素的存取子函數。

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>參數

<dl> <dt>

*屬性屬性-清單* 
</dt> <dd>

適用于屬性的其他屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*屬性名稱* 
</dt> <dd>

屬性的名稱。

</dd> <dt>

*元件-param 清單* 
</dt> <dd>

與屬性相關聯的零或多個參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Defaultcollelem \]** 屬性用於 Visual BasicÂ®程式碼優化。 如果介面或分配介面的成員標示為存取子函式，則呼叫會直接移至該成員。

**\[ Defaultcollelem \]** 的使用必須與屬性一致。 例如，如果您在 *Get* 屬性上使用屬性，則它也必須出現在 *Let* 屬性上。

### <a name="typeflags-representation"></a>Typeflags 標記法

FUNCFLAG \_ FDEFAULTCOLLELEM 或 VARFLAG FDEFAULTCOLLELEM 的存在 \_ 。

## <a name="examples"></a>範例

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 