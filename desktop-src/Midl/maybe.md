---
title: 也許是屬性
description: 關鍵字 \ 可能會指出遠端程序呼叫不需要在每次呼叫時執行，而且用戶端不會預期回應。 請注意，\ 可能的 \ 通訊協定可確保不會傳遞，也不會完成呼叫。
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- 可能是 MIDL 屬性
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 178faf3d308f7dd282e31a8f0eabf8708bb8b3fe1a0d52a981e65adddb258ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067148"
---
# <a name="maybe-attribute"></a>也許是屬性

關鍵字 **\[ 可能 \]** 指出遠端程序呼叫不需要在每次呼叫時執行，而且用戶端不會預期回應。 請注意， **\[ 可能 \]** 的通訊協定可確保未傳遞，也不會完成呼叫。

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的零或多個 IDL 屬性清單。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定要套用至函數的其他屬性。 以逗號分隔多個屬性。

</dd> <dt>

*returntype* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 **\[ 可能 \]** 套用屬性之目標函數的名稱。

</dd> <dt>

*params* 
</dt> <dd>

函數參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

使用 **\[ 可能 \]** 屬性的呼叫不能包含輸出參數，而是隱含的 **\[** [**等冪**](idempotent.md) **\]** 呼叫。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**廣播**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> </dl>

 

 




