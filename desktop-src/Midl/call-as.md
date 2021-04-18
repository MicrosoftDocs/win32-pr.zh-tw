---
title: call_as 屬性
description: '\ 呼叫 \_ as \ 屬性可讓您將無法遠端呼叫的函式對應至遠端函式。'
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as 屬性 MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968679"
---
# <a name="call_as-attribute"></a>呼叫 \_ 為屬性

**\[ Call \_ as \]** 屬性可讓您將無法遠端呼叫的函式對應至遠端函式。

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>參數

<dl> <dt>

*本機進程* 
</dt> <dd>

指定作業定義的常式。

</dd> <dt>

*操作-屬性清單* 
</dt> <dd>

指定套用至作業的一或多個屬性。 以逗號分隔多個屬性。

</dd> <dt>

*操作-名稱* 
</dt> <dd>

指定要呈現給應用程式的已命名操作。

</dd> </dl>

## <a name="remarks"></a>備註

將無法從遠端呼叫的函式對應至遠端函式的能力，在具有許多參數類型且無法透過網路傳輸的介面上特別有用。 **\[** [**\_**](represent-as.md) **\]** **\[** [**\_**](transmit-as.md) **\]** 您可以使用 **\[ 呼叫 \_ 做 \]** 為常式來合併所有轉換，而不是使用許多表示 as 和傳輸類型。 您可以 (用戶端和伺服器端) 提供兩個 **\[ 呼叫 \_ \]** ，以系結應用程式呼叫與遠端呼叫之間的常式。

**\[ 呼叫 \_ as \]** 屬性可用於物件介面。 在此情況下，介面定義可用於本機呼叫和遠端呼叫，因為 **\[ 呼叫 \_ as \]** 允許無法從遠端存取介面，以明確地對應到遠端介面。 **\[ 呼叫 \_ as \]** 屬性不能與 [**/osf**](-osf.md)模式搭配使用。

例如，假設物件介面 **IFace** 中的常式 **f1** 需要在使用者呼叫和實際傳輸的之間進行許多轉換。 下列範例說明介面 **IFace** 的 IDL 和 ACF 檔案：

在介面 **IFace** 的 IDL 檔案中：

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

在介面 **IFace** 的 ACF 中：

``` syntax
[call_as( f1 )] Remf1();
```

這會導致產生的標頭檔使用 **f1** 的定義來定義介面，但它也提供 **Remf1** 的存根。

MIDL 編譯器會在介面 **IFace** 的標頭檔中產生下列 Vtable：

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

然後，用戶端 proxy 會有一般 MIDL 產生的 proxy 以進行 **Remf1**，而 **Remf1** 的伺服器端 STUB 會與一般 MIDL 產生的存根相同：

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

然後，兩個 (用戶端和伺服器端) 的 **\[ 呼叫 \_ \]** ，都必須手動編碼：

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

針對物件介面，這些是適用于證券紙的原型。

針對用戶端：

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

針對伺服器端：

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

針對非物件介面，這些是適用于此類證券紙的原型。

針對用戶端：

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

針對伺服器端：

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**表示 \_ 為**](represent-as.md)
</dt> <dt>

[**傳輸 \_ 為**](transmit-as.md)
</dt> </dl>

 

 




