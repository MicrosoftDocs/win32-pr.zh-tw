---
title: v1_enum 屬性
description: '\ V1 \_ enum \ 屬性會指示指定的列舉型別以32位實體（而非16位預設值）傳輸。'
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum 屬性 MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7afb814cde879f0ada5124b1a19d8ac8b8c851deafcda7e75295a6e5338f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382782"
---
# <a name="v1_enum-attribute"></a>v1 \_ 列舉屬性

**\[ V1 \_ 列舉 \]** 屬性會指示指定的列舉型別以32位實體的形式傳送，而不是16位的預設值。

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>參數

這個屬性沒有任何參數。

## <a name="remarks"></a>備註

使用 **\[ v1 \_ enum \]** 屬性將列舉型別傳輸為32位實體，可提高在結構或等位中內嵌這類列舉時，封送處理和封送處理資料的效率。

為了改善效能，建議您將 **\[ v1 \_ 列舉 \]** 屬性套用至32位應用程式中的枚舉器。 不過請記住，在16位平臺上，C 編譯器會將列舉型別視為16位 [**整數**](int.md)。因此，16位用戶端應用程式需要將 [**列舉**](enum.md) 類型轉換為 [**long**](long.md) 以進行遠端傳輸，以避免覆寫資料或傳送不正確的值。

## <a name="examples"></a>範例

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> </dl>

 

 




