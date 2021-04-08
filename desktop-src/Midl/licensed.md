---
title: licensed 屬性
description: '\ 授權 \ 屬性工作表示其所套用的 coclass 已獲授權，必須使用 IClassFactory2 來具現化。'
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- 授權屬性 MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023345"
---
# <a name="licensed-attribute"></a>licensed 屬性

**\[ 授權 \]** 屬性工作表示其所套用的 [**coclass**](coclass.md)已獲得授權，而且必須使用 [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)具現化。

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*屬性清單* 
</dt> <dd>

指定套用至 [**coclass**](coclass.md) 語句的零或多個屬性。 允許的 **coclass** 屬性為 **\[** [**helpstring**](helpstring.md) **\]** 、 **\[** [**helpcoNtext**](helpcontext.md) **\]** 、 **\[ 授權 \]**、 **\[** [**版本**](version.md) **\]** 、 **\[** [**控制項**](control.md) **\]** 和 **\[** [**隱藏**](hidden.md) **\]** 。

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

授權是 COM 的功能，可控制物件的建立。 授權物件只能由獲得授權使用的用戶端建立。 授權是透過 [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) 介面在 COM 中執行，並支援可在執行時間傳遞的授權金鑰。

### <a name="flags"></a>Flags

TYPEFLAG \_ FLICENSED

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[型別程式庫的內容](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
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

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 