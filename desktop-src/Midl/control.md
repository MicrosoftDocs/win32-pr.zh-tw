---
title: control 屬性
description: '\ Control \ 屬性會將 coclass 或程式庫識別為 COM 控制項，以供容器網站衍生其他型別程式庫或元件物件類別。'
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- control 屬性 MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681771"
---
# <a name="control-attribute"></a>control 屬性

**\[ 控制項 \]** 屬性會將 [**coclass**](coclass.md)或連結 [**庫**](library.md)識別為 COM 控制項，容器網站會從中衍生其他型別程式庫或元件物件類別。

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*屬性清單* 
</dt> <dd>

指定適用于連結 [**庫**](library.md) 或 [**coclass**](coclass.md) 語句的零或多個屬性。 以逗號分隔多個屬性。

</dd> <dt>

*lib 或-coclassname* 
</dt> <dd>

指定連結 [**庫**](library.md) 或 [**coclass**](coclass.md)的名稱。

</dd> <dt>

*定義* 
</dt> <dd>

MIDL 語句，可指定連結 [**庫**](library.md) 或 [**coclass**](coclass.md)的成員。

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性可讓您標記描述控制項的類型程式庫，使其不會顯示在適用于非視覺化物件的型別瀏覽器中。

### <a name="flags"></a>Flags

TYPEFLAG \_ FCONTROL、LIBFLAG \_ FCONTROL

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**圖書館**](library.md)
</dt> </dl>

 

 