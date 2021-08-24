---
title: defaultvtable 屬性
description: '\ Defaultvtable \ 屬性會將介面定義為預設 Vtable 介面。'
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- defaultvtable 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffebc5907072f7fdfc539bbc2b06bf1e4ad9fb667826c6c3c5a96121b106326e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067338"
---
# <a name="defaultvtable-attribute"></a>defaultvtable 屬性

**\[ Defaultvtable \]** 屬性會將介面定義為預設 Vtable 介面。

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
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

適用于類別的其他屬性。 需要 **\[** [**來源**](source.md) **\]** 和 **\[** [**uuid**](uuid.md) **\]** 屬性。

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

預設 Vtable 介面不可以是介面介面，它必須是雙重或 Vtable 或介面。 如果介面是雙重介面，則接收會假設它們會透過 Vtable 接收事件。

類別可以是預設來源介面和預設 Vtable 來源介面（如範例所示）。 在此情況下，建議接收器應該使用 IID \_ IDISPATCH 來接收分派事件，並使用介面識別碼接收 Vtable 事件。

### <a name="typeflag-representation"></a>Typeflag 標記法

IMPLTYPEFLAG FDEFAULTVTABLE 的存在 \_ 。

## <a name="examples"></a>範例

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
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
</dt> <dt>

[**源**](source.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 