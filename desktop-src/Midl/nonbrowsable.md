---
title: nonbrowsable 屬性
description: 使用 \ nonbrowsable \ 屬性來標記不應該在屬性瀏覽器中顯示的介面或分配介面成員。
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- nonbrowsable 屬性 MIDL
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6349683c3a3c591752036d9a5e2995d368460a049a79d2e1cf4123beb2b0ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066948"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable 屬性

使用 **\[ nonbrowsable \]** 屬性來標記不應該在屬性瀏覽器中顯示的介面或分配介面成員。

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>參數

<dl> <dt>

*屬性屬性-清單* 
</dt> <dd>

適用于屬性的其他屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

方法所傳回的資料類型。

</dd> <dt>

*屬性名稱* 
</dt> <dd>

屬性或方法的名稱。

</dd> <dt>

*元件-param 清單* 
</dt> <dd>

要傳遞給方法的零或多個參數。

</dd> </dl>

## <a name="remarks"></a>備註

某些屬性不應顯示在屬性瀏覽器中。 這可能是因為取出值會花費很長的時間。 此範例會防止使用者嘗試抓取 *Count* 屬性，此屬性會傳回動態集內的資料列數目。此數目可能代表非常大型查詢的結果。

其他屬性可能會在瀏覽器上產生未預期的效果。 例如，請考慮具有屬性 "IsSelected" 的控制項，以分辨是否已選取控制項。 如果 "IsSelected" 設為 false，以選取專案為基礎的屬性瀏覽器會流覽不同的物件。

請注意，標記為 **\[ nonbrowsable \]** 的屬性仍會顯示在物件瀏覽器中，而不會顯示內容值。

### <a name="typeflag-representation"></a>Typeflag 標記法

FUNCFLAG \_ FNONBROWSABLE 或 VARFLAG FNONBROWSABLE 的存在 \_ 。

## <a name="examples"></a>範例

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 