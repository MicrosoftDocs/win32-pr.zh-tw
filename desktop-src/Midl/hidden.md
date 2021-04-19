---
title: hidden 屬性
description: '\ Hidden \ 屬性工作表示專案存在，但不應該在使用者導向的瀏覽器中顯示。'
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- hidden 屬性 MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968898"
---
# <a name="hidden-attribute"></a>hidden 屬性

**\[ Hidden \]** 屬性工作表示專案存在，但不應該在使用者導向的瀏覽器中顯示。

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>參數

<dl> <dt>

*其他屬性* 
</dt> <dd>

零或多個選擇性 MIDL 屬性。

</dd> <dt>

*元素* 
</dt> <dd>

下列其中一個指示詞： [**coclass**](coclass.md)、 [**介面**](dispinterface.md)、 [**介面**](interface.md)或連結 [**庫**](library.md)。

</dd> <dt>

*元素名稱* 
</dt> <dd>

其他軟體元件可用來描繪目前元素的名稱。

</dd> <dt>

*定義* 
</dt> <dd>

指定組成元素定義的語句。

</dd> <dt>

*函數類型* 
</dt> <dd>

函數的傳回類型。

</dd> <dt>

*函數名稱* 
</dt> <dd>

用來叫用函數的名稱。

</dd> <dt>

*選擇性-參數-清單* 
</dt> <dd>

零或多個函數參數。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Hidden \]** 屬性可讓您從介面 (移除成員，方法是將其防護以進一步使用) ，同時維持與現有程式碼的相容性。 您可以對屬性、方法和 [**coclass**](coclass.md) [**、**](dispinterface.md)介面、[**介面**](interface.md)和連結 [**庫**](library.md)語句使用 **\[ hidden \]** 屬性。

針對程式庫指定時， **\[ 隱藏 \]** 的屬性會防止整個程式庫顯示。 此用法是與控制項搭配使用。 主機需要建立新的類型程式庫，以包裝控制項與擴充屬性。

### <a name="flags"></a>Flags

VARFLAG \_ FHIDDEN、FUNCFLAG \_ FHIDDEN、TYPEFLAG \_ FHIDDEN

## <a name="examples"></a>範例

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**圖書館**](library.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 