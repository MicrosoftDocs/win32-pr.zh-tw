---
title: 編碼屬性
description: '\ 編碼 \ ACF 屬性指定程式或資料類型需要序列化支援。'
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- 編碼屬性 MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933119"
---
# <a name="encode-attribute"></a>編碼屬性

**\[ 編碼 \]** ACF 屬性指定程式或資料類型需要序列化支援。

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
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

指定適用于程式的其他操作屬性，例如解碼 **\[** [](decode.md) **\]** 。

</dd> <dt>

*進程名稱* 
</dt> <dd>

指定程式的名稱。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定適用于類型的其他屬性，例如解碼 **\[** [](decode.md) **\]** 和 **\[** [**配置**](allocate.md) **\]** 。

</dd> <dt>

*類型名稱* 
</dt> <dd>

指定 IDL 檔案中定義的類型。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 編碼 \]** 屬性會導致 MIDL 編譯器產生程式碼，應用程式可以使用該程式碼將資料序列化為緩衝區。 解碼 **\[** [](decode.md) **\]** 屬性會產生用來從緩衝區封送資料的程式碼。

使用 ACF 中的 **\[ \] 編碼** 和解碼 **\[** [](decode.md) **\]** 屬性，為介面的 IDL 檔中定義的程式或類型產生序列化程式碼。 當做介面屬性使用時，會將 **\[ 編碼 \]** 套用至 IDL 檔案中定義的所有類型和程式。 當做操作屬性使用時，只會將 **\[ 編碼 \]** 套用至指定的程式。 當做型別屬性使用時，只會將 **\[ 編碼 \]** 套用至指定的型別。

當 **\[ 編碼 \]** 或解碼 **\[** [](decode.md) **\]** 屬性套用至程式時，MIDL 編譯器會以類似的方式產生序列化存根，以產生遠端常式的遠端存根。 程式可以是遠端或序列化程式，但不能同時為這兩種方法。 產生之常式的原型會傳送至存根。H 檔案，而存根本身會進入存根的 \_ c. 檔案。

MIDL 編譯器會針對 **\[ 編碼 \]** 屬性所套用的每個類型產生兩個函式，並針對解碼 **\[** 屬性套用的每個類型產生一個 [**額外的函**](decode.md)式 **\]** 。 例如，針對名為 MyType 的使用者定義型別，編譯器會針對 MyType \_ 編碼、MyType 解碼 \_ 和 MyType AlignSize 函數產生程式碼 \_ 。 針對這些函式，編譯器會將原型寫入存根。H 和來源程式碼至 STUB \_ C.C。

如需有關序列化控制碼和編碼或解碼資料的詳細資訊，請參閱 [序列化服務](/windows/desktop/Rpc/serialization-services)。

## <a name="examples"></a>範例

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**分配**](allocate.md)
</dt> <dt>

[**解碼**](decode.md)
</dt> </dl>

 

 