---
title: notify_flag 屬性
description: '\ 通知 \_ 旗標 \ 屬性會提供通知，指出是否呼叫伺服器常式。'
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag 屬性 MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9fb7479667fb9757924dcba765c34138cf01c1ad6645ce7bfdc525be393e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066869"
---
# <a name="notify_flag-attribute"></a>通知 \_ 旗標屬性

**\[ 通知 \_ 旗 \]** 標屬性會提供通知，指出是否呼叫伺服器常式。

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>參數

<dl> <dt>

*程式-名稱* 
</dt> <dd>

與通知 \_ 旗標程式相關聯的遠端程式名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 通知 \_ 旗 \]** 標屬性類似于 [ **\[ 通知 \]** ] 屬性的使用方式。

[ **\[ 通知 \_ 旗 \]** 標程式名稱] 是以 [ **\_ 通知] \_ 旗** 標做為尾碼的遠端程式名稱。 **\_ 通知 \_ 旗** 標程式不需要任何參數，也不會傳回結果。 這項程式的原型也會在標頭檔中產生。 例如，如果 IDL 檔案包含下列內容：

``` syntax
MyProcedure([in] short S);
```

在 ACF for MIDL 中指定下列各項，以產生 **\_ 通知 \_ 旗** 標呼叫：

``` syntax
[notify_flag] MyProcedure();
```

MIDL 編譯器將會產生包含下列 **\_ 通知 \_ 旗** 標程式呼叫的伺服器 stub 程式碼：

``` syntax
MyProcedure_notify_flag();
```

標頭檔將包含原型：

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

如果呼叫伺服器常式， **\_ MIDL \_ NotifyFlag** 為 **TRUE** 。

## <a name="examples"></a>範例

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**通知**](notify.md)
</dt> </dl>

 

 




