---
title: coNtext_handle_noserialize 屬性
description: '\ 內容 \_ 控制碼 \_ NOSERIALIZE \ ACF 屬性可保證不論應用程式的預設行為為何，都不會序列化內容控制碼。'
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- coNtext_handle_noserialize 屬性 MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40556db0d63441e42d46a0ed7f9bd45edb8b2ce65f8d4b9b84e3a848325ddbb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013996"
---
# <a name="context_handle_noserialize-attribute"></a>內容 \_ 控制碼 \_ noserialize 屬性

無論應用程式的預設行為為何， **\[ 內容 \_ 控制碼 \_ noserialize \]** ACF 屬性都保證永遠不會序列化內容控制碼。

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>參數

<dl> <dt>

*類型-acf-attribute-list* 
</dt> <dd>

適用于型別的任何其他 ACF 屬性。

</dd> <dt>

*內容-控制碼類型* 
</dt> <dd>

指定內容控制碼類型的識別碼，如 [**typedef**](typedef.md) 宣告中所定義。 這是在 IDL 檔案中接收 [**\[ 內容 \_ 句 \] 柄**](context-handle.md)屬性的型別。

</dd> <dt>

*函數-acf-attribute-list* 
</dt> <dd>

適用于函數的任何其他 ACF 屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

IDL 檔案中所定義的函式名稱。

</dd> <dt>

*參數-acf-attribute-list* 
</dt> <dd>

適用于參數的任何其他 ACF 屬性。

</dd> <dt>

*參數名稱* 
</dt> <dd>

在 IDL 檔案中定義之參數的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

[**\[ 內容 \_ 控制碼 \]**](context-handle.md)屬性會識別在遠端程序呼叫之間，維護伺服器上內容或狀態資訊的系結控制碼。 屬性可以顯示為 IDL [**typedef**](typedef.md) 型別屬性（attribute）、函數傳回型別屬性（attribute），或做為參數屬性（attribute）。

依預設，會序列化對內容控制碼的呼叫。 應用程式可以呼叫 [**RpcSsDontSerializeCoNtext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) 來覆寫此預設行為。 使用 ACF 檔中的 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)屬性可保證不會序列化這個特定內容控制碼上的呼叫，不論呼叫應用程式的行為為何。 提供內容取消常式是選擇性的。

這個屬性可在 MIDL 5.0 版中使用。

**Windows ServerÂ2003和 windows XP 或更新版本：** 單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式存取 (序列化) 的內容控制碼，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。 這些存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。 損毀或修改內容控制碼狀態的方法必須序列化。 未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。 請注意，建立方法會以隱含方式序列化。

## <a name="examples"></a>範例

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ACF 屬性](acf-attributes.md)
</dt> <dt>

[**內容 \_ 控制碼 \_ 序列化**](context-handle-serialize.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[內容控制碼](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeCoNtext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[伺服器內容執行例行常式](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[多執行緒用戶端和內容控制碼](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 