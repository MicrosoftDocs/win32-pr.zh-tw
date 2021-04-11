---
title: propputref 屬性
description: '\ Propputref \ 屬性會指定使用參考而非值的屬性設定函數。'
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref 屬性 MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933115"
---
# <a name="propputref-attribute"></a>propputref 屬性

**\[ Propputref \]** 屬性會指定使用參考而非值的屬性設定函數。

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>參數

<dl> <dt>

*選用屬性-屬性* 
</dt> <dd>

零或多個屬性屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

遠端程式所傳回的資料類型。

</dd> <dt>

*函數名稱* 
</dt> <dd>

遠端程式的名稱。

</dd> <dt>

*parameters* 
</dt> <dd>

遠端程式的零或多個參數。

</dd> </dl>

## <a name="remarks"></a>備註

具有 **\[ propputref \]** 屬性的函式也必須具有（其最後一個參數）具有 **\[** [**in**](in.md)屬性（attribute）的指標 **\]** 。

屬性的名稱必須與函數相同。 最多可以為函式 **\[** [](propget.md) **\]** 指定 propget、 **\[** [**propput**](propput.md) **\]** 和 **\[ \] propputref** 屬性的其中一個。

### <a name="flags"></a>Flags

叫用 \_ PROPERTYPUTREF

## <a name="examples"></a>範例

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 