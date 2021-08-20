---
title: noncreatable 屬性
description: '\ Noncreatable \ 屬性定義無法本身具現化的物件。'
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- noncreatable 屬性 MIDL
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e59c53d8e4c05d15d55a6ccd9d7fb2b5cd8783463d1f59d439c74240fdd93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066938"
---
# <a name="noncreatable-attribute"></a>noncreatable 屬性

**\[ Noncreatable \]** 屬性會定義無法本身具現化的物件。

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*coclass-屬性清單* 
</dt> <dd>

適用于類別的其他屬性。

</dd> <dt>

*coclass-名稱* 
</dt> <dd>

類別的名稱。

</dd> <dt>

*coclass-介面清單* 
</dt> <dd>

類別的介面清單。

</dd> </dl>

## <a name="remarks"></a>備註

使用 [**coclass**](coclass.md)語句上的 **\[ noncreatable \]** 屬性，向使用者指出他們無法在最上層建立這個類別的新物件，也就是呼叫 **CreateInstance** 或 **CoCreateInstance**。 此類別的物件具現化需要對另一個物件進行方法呼叫。 例如，在 Microsoft Excel 中，"Cell" 物件是 noncreatable 的，而且必須從 Microsoft Excel 工作表物件取得。

傳回 noncreatable 類別之實例的方法應該傳回物件的確切型別，而不是 **VARIANT** 或 **IDispatch** \* 類型。

### <a name="typeflag-representation"></a>Typeflag 標記法：

缺少 TYPEFLAG \_ FCANCREATE。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 