---
title: appobject 屬性
description: '\ Appobject \ 屬性會將 coclass 識別為應用程式物件，此物件與完整 EXE 應用程式相關聯。'
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject 屬性 MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54cbe8d5c1c7a573216ae9cb55075ba3b3766d0d8c7898233be9364488131e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808330"
---
# <a name="appobject-attribute"></a>appobject 屬性

**\[ Appobject \]** 屬性會將 [**coclass**](coclass.md)識別為應用程式物件，此物件與完整 EXE 應用程式相關聯。

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定 [**coclass**](coclass.md)的通用唯一識別碼。

</dd> <dt>

*coclass-屬性清單* 
</dt> <dd>

指定套用至 [**coclass**](coclass.md) 語句的零或多個屬性。 允許 **的 coclass** 屬性為 [**\[ helpstring \]**](helpstring.md)、 [**\[ helpcoNtext \]**](helpcontext.md)、 [**\[ 授權 \]**](licensed.md)、 [**\[ 版本 \]**](version.md)、 [**\[ 控制項 \]**](control.md)和 [**\[ 隱藏 \]**](hidden.md)。

</dd> <dt>

*classname* 
</dt> <dd>

指定在類型程式庫中已知元件物件的名稱。

</dd> <dt>

*coclass 定義* 
</dt> <dd>

指定組成 [**coclass**](coclass.md) 定義的語句。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Appobject \]** 屬性也表示 [**coclass**](coclass.md)的函式和屬性在目前的類型程式庫中為全域可用。

這個屬性的 typeflag 標記法為 TYPEFLAG \_ FAPPOBJECT

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**控制**](control.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**隱藏**](hidden.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 