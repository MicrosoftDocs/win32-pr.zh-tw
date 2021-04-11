---
title: aggregatable 屬性
description: '\ 聚合 \ 屬性工作表示類別支援匯總。'
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- 聚合屬性 MIDL
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314842"
---
# <a name="aggregatable-attribute"></a>aggregatable 屬性

匯總屬性指出類別支援匯總。 **\[ \]**

``` syntax
[
   coclass-attribute-list,
   aggregatable
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

在 [**coclass**](coclass.md)語句上使用可匯總屬性，讓使用者知道類別支援匯總。 **\[ \]** 也就是說，類別可讓容器類別公開其介面，如同這些介面是容器本身的介面。

這個屬性的 typeflag 標記法為 TYPEFLAG \_ FAGGREGATABLE。

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 