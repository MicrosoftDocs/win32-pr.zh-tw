---
title: midl_pragma 警告屬性
description: 使用 midl \_ pragma warning 選項，在編譯時期暫時覆寫 midl 的警告訊息行為。
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma 警告屬性 MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841108"
---
# <a name="midl_pragma-warning-attribute"></a>midl \_ pragma warning 屬性

使用 **midl \_ pragma warning** 選項，在編譯時期暫時覆寫 midl 的警告訊息行為。

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>參數

<dl> <dt>

*warning \_ 選項* 
</dt> <dd>

警告選項可以是下列其中一項： [停用]、[啟用]、[預設]。

</dd> <dt>

*郵寄清單 \_* 
</dt> <dd>

以空格分隔的訊息編號清單。

</dd> </dl>

## <a name="remarks"></a>備註

Pragma 可以像 C 編譯器 pragma 一樣使用。 也就是說，它會停用、啟用或返回指定 MIDL 警告的預設行為。

## <a name="examples"></a>範例

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




