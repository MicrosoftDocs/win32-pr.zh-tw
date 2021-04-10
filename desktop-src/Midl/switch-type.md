---
title: switch_type 屬性
description: '\ Switch \_ 類型 \ 屬性會識別用來當做聯集判別的變數類型。 參數類型可以是整數、字元、布林值或列舉類型。'
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type 屬性 MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841339"
---
# <a name="switch_type-attribute"></a>切換 \_ 類型屬性

**\[ Switch \_ type \]** 屬性會識別當做聯集判別使用的變數類型。 參數類型可以是整數、字元、布林值或列舉類型。

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>參數

<dl> <dt>

*參數類型規範* 
</dt> <dd>

指定 [**int**](int.md)、 [**char**](char-idl.md)、 [**Boolean**](boolean.md)或 [**enum**](enum.md) 型別，或這類類型的識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Switch \_ type \]** 屬性會識別變數型別，而參數 **\[** [**\_ 是**](switch-is.md)屬性（attribute）， **\]** 它會指定做為聯集判別的參數名稱。 **\[ Switch \_ type \]** 屬性會套用至結構或等位的參數或成員。

Union 及其判別必須在相同的邏輯層級上指定。 當 union 是參數時，聯集判別必須是另一個參數。 當聯集是結構的欄位時，判別必須是結構與聯集欄位相同層級的另一個欄位。

## <a name="examples"></a>範例

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**字元**](char-idl.md)
</dt> <dt>

[封裝聯集](encapsulated-unions.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[Nonencapsulated 聯集](nonencapsulated-unions.md)
</dt> <dt>

[**切換 \_ 為**](switch-is.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> </dl>

 

 




