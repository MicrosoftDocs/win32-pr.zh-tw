---
title: 等冪屬性
description: '\ 等冪 \ 屬性指定作業在每次執行時都不會修改狀態資訊並傳回相同的結果。 執行常式一次以上，其效果與執行一次相同。'
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- 等冪屬性 MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507536"
---
# <a name="idempotent-attribute"></a>等冪屬性

**\[ 等冪 \]** 屬性指定作業在每次執行時都不會修改狀態資訊，並傳回相同的結果。 執行常式一次以上，其效果與執行一次相同。

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
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

指定將套用 **\[ 等冪 \]** 屬性的函式名稱。

</dd> <dt>

*params* 
</dt> <dd>

函數參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

RPC 支援兩種類型的遠端呼叫語義：具有 **\[ 等 \] 冪** 屬性之作業的呼叫，以及呼叫作業 (*等* 冪運算) 不具 **\[ 等冪 \]** 屬性 (*非等* 冪的作業) 。 等冪運算可以執行一次以上，而且不會有任何不良影響。 相反地，無法執行一次非等冪運算，因為它會每次都會傳回不同的結果，或因為它會修改某些狀態。

若要確保在呼叫未完成時，會自動重新執行程式，請使用 **\[ 等冪 \]** 屬性。 如果 **\[ 等冪 \]**、 **\[** [**廣播**](broadcast.md) **\]** 或 **\[** [**可能**](maybe.md)的 **\]** 屬性不存在，則此程式預設會使用非等冪的語法。 在此情況下，作業只會執行一次。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**廣播**](broadcast.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**也許**](maybe.md)
</dt> </dl>

 

 




