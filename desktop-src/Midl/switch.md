---
title: 切換屬性
description: Switch 關鍵字會選取封裝聯集的判別 \_ 。
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- 切換屬性 MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422b52a339a83cbaf59a9d65c0ed0e4e7e41533dcbf0be962147327145588a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013546"
---
# <a name="switch-attribute"></a>切換屬性

**Switch** 關鍵字會選取 [**封裝聯 \_ 集**](encapsulated-unions.md)的判別。

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>參數

<dl> <dt>

*切換類型* 
</dt> <dd>

指定 [**int**](int.md)、 [**char**](-char.md)、 [**列舉**](enum.md) 型別或解析成其中一種類型的識別碼。

</dd> <dt>

*參數名稱* 
</dt> <dd>

指定作為聯集判別之類型 *參數* 類型的變數名稱。

</dd> </dl>

## <a name="examples"></a>範例

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[Nonencapsulated 聯集](nonencapsulated-unions.md)
</dt> <dt>

[**切換 \_ 為**](switch-is.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> </dl>

 

 




