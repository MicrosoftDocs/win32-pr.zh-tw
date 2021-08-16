---
title: 解碼屬性
description: '\ 解碼 \ ACF 屬性指定程式或類型需要還原序列化支援。'
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- 解碼屬性 MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30c70c821906bcfa4dedb8dbe87aab882866a4f21b7d561b16d3613f9041e0f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384721"
---
# <a name="decode-attribute"></a>解碼屬性

解碼 ACF 屬性指定程式或類型需要還原序列化支援。 **\[ \]**

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定適用于整個介面的其他屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*介面定義* 
</dt> <dd>

指定組成介面定義的 IDL 語句。

</dd> <dt>

*op-屬性清單* 
</dt> <dd>

指定適用于程式的其他操作屬性，例如 **\[** [**編碼**](encode.md) **\]** 。

</dd> <dt>

*進程名稱* 
</dt> <dd>

指定程式的名稱。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定其他屬性，例如 **\[** [**編碼**](encode.md) **\]** 和 **\[** [**配置**](allocate.md) **\]** 。

</dd> <dt>

*類型名稱* 
</dt> <dd>

指定 IDL 檔案中定義的類型。

</dd> </dl>

## <a name="remarks"></a>備註

解碼屬性會導致 MIDL 編譯器產生程式碼，應用程式可以使用該程式碼從緩衝區取出序列化的資料。 **\[ \]** **\[**[**編碼**](encode.md) **\]** 屬性提供序列化支援，產生將資料序列化為緩衝區的程式碼。

使用 **\[** [](encode.md) **\]** ACF 中的 **\[ \]** 編碼和解碼屬性，為介面的 IDL 檔中定義的程式或類型產生序列化程式碼。 當做介面屬性使用 **時， \[ \] 解碼** 會套用至 IDL 檔案中定義的所有類型和程式。 當做型別屬性使用時， **\[ \] 解碼只適用于指定** 的型別。 作為操作屬性使用時， **\[ \] 只會套用至** 該程式。

如需使用此序列化支援的詳細資訊，請參閱 [序列化服務](/windows/desktop/Rpc/serialization-services)和 **\[** [**編碼**](encode.md) **\]** 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**分配**](allocate.md)
</dt> <dt>

[**編碼**](encode.md)
</dt> </dl>

 

 