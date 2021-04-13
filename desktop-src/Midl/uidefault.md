---
title: uidefault 屬性
description: '\ Uidefault \ 屬性工作表示類型資訊成員是要在使用者介面中顯示的預設成員。'
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- uidefault 屬性 MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375024"
---
# <a name="uidefault-attribute"></a>uidefault 屬性

**\[ Uidefault \]** 屬性指出型別資訊成員是在使用者介面中顯示的預設成員。

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>參數

<dl> <dt>

*方法-屬性清單* 
</dt> <dd>

適用于方法的其他屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

方法在完成執行時將會傳回的資料類型。

</dd> <dt>

*方法名稱* 
</dt> <dd>

方法的名稱。

</dd> <dt>

*方法-參數-清單* 
</dt> <dd>

方法的零或多個參數。

</dd> </dl>

## <a name="remarks"></a>備註

將 **\[ uidefault \]** 屬性套用至介面的成員或介面介面，會在設計階段告知 Visual Basic，以自動將此事件或屬性顯示給使用者。 這表示當使用者按兩下物件時，Visual Basic 會跳至具有 **\[ uidefault \]** 屬性之預設來源介面中的事件。 當使用者選取物件時，Visual Basic 的屬性瀏覽器會在具有這個屬性的預設來源介面中顯示內容。 如果沒有任何事件或屬性具有 **\[ uidefault \]** 屬性，Visual Basic 會顯示預設介面中列出的第一個事件或屬性。

### <a name="typeflag-representation"></a>Typeflag 標記法

FUNCFLAG \_ FUIDEFAULT 或 VARFLAG FUIDEFAULT 的存在 \_

## <a name="examples"></a>範例

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 