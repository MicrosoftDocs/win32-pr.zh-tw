---
title: coNtext_handle_serialize 屬性
description: '\ 內容 \_ 控制碼 \_ 序列化 \ ACF 屬性可保證無論應用程式的預設行為為何，都會永遠序列化內容控制碼。'
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- coNtext_handle_serialize 屬性 MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965012"
---
# <a name="context_handle_serialize-attribute"></a>內容 \_ 控制碼 \_ 序列化屬性

無論應用程式的預設行為為何， **\[ 內容 \_ 控制碼都會 \_ 序列化 \]** ACF 屬性，以保證會一律序列化內容控制碼。

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>參數

<dl> <dt>

*類型-acf-attribute-list* 
</dt> <dd>

適用于型別的任何其他 ACF 屬性。

</dd> <dt>

*內容-控制碼類型* 
</dt> <dd>

指定內容控制碼類型的識別碼，如 [**typedef**](typedef.md) 宣告中所定義。 這是在 IDL 檔案中接收 **\[ 內容 \_ 句 \_ 柄 \] 序列化** 屬性的型別。

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

**\[ 內容 \_ 控制碼 \_ 序列化 \]** 屬性可識別系結控制碼，此控制碼會在遠端程序呼叫之間，維護伺服器上的內容或狀態資訊。 屬性可以顯示為 IDL [**typedef**](typedef.md) 型別屬性（attribute）、函數傳回型別屬性（attribute），或做為參數屬性（attribute）。

依預設，會序列化對內容控制碼的呼叫，但應用程式可以呼叫 [**RpcSsDontSerializeCoNtext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) 來覆寫此預設行為。 在 ACF 檔中使用 **\[ 內容 \_ 控制碼 \_ 序列化 \]** 屬性可保證將會序列化這個特定內容控制碼上的呼叫，即使呼叫的應用程式已覆寫預設序列化。 內容取消常式是選擇性的。

這個屬性可在 MIDL 5.0 版中使用。

**Windows ServerÂ2003與 WINDOWS XP 或更新版本：** 單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式存取 (序列化) 的內容控制碼，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。 這些存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。 損毀或修改內容控制碼狀態的方法必須序列化。 未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。 請注意，建立方法會以隱含方式序列化。

## <a name="examples"></a>範例

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[ACF 屬性](acf-attributes.md)
</dt> <dt>

[**內容 \_ 控制碼 \_ noserialize**](context-handle-noserialize.md)
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

 

 