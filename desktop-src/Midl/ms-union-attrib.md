---
title: ms_union 屬性
description: 關鍵字 \ ms \_ union \ 用來控制 nonencapsulated 等位的 NDR 對齊。
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union 屬性 MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022302"
---
# <a name="ms_union-attribute"></a>ms 聯 \_ 集屬性

關鍵字 \[ **ms 聯 \_ 集** \] 用來控制 nonencapsulated 等位的 NDR 對齊。

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*procedure 類型* 
</dt> <dd>

指定要套用屬性之程式的傳回型別。

</dd> <dt>

*程式-名稱* 
</dt> <dd>

指定程式的名稱。

</dd> <dt>

*param 清單* 
</dt> <dd>

指定程式的參數清單，此清單可能是空的。

</dd> </dl>

## <a name="remarks"></a>備註

請勿使用這個參數或具有新介面的屬性。 這是回溯相容性功能。這一版 Microsoft RPC 中的 MIDL 編譯器會鏡像 nonencapsulated 等位的憑證 DCE IDL 編譯器行為。 不過，因為舊版 MIDL 編譯器沒有這樣做，所以 [**/ms 聯 \_ 集**](-ms-union.md) 參數會提供與舊版 midl 編譯器的介面相容性。

**Ms 聯 \_ 集** 功能可以當做 idl 介面屬性、idl 型別屬性，或做為命令列參數來 ( [**/ms 聯 \_ 集**](-ms-union.md)) 。

## <a name="examples"></a>範例

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**/ms 聯 \_ 集**](-ms-union.md)
</dt> </dl>

 

 




