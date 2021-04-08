---
title: coNtext_handle 屬性
description: '\ 內容 \_ 控制碼 \ 屬性會識別在遠端程序呼叫之間，維護伺服器上內容或狀態資訊的系結控制碼。'
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- coNtext_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681772"
---
# <a name="context_handle-attribute"></a>內容 \_ 控制碼屬性

**\[ 內容 \_ 控制碼 \]** 屬性會識別在遠端程序呼叫之間，維護伺服器上內容或狀態資訊的系結控制碼。

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定指標類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*宣告子和宣告子清單* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 內容控制碼的宣告子必須包含至少一個指標宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子清單包含一或多個宣告子， *並* 以逗號分隔。 函式宣告子中的參數名稱識別碼是選擇性的。

</dd> <dt>

*函數-attr-list* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[ 內容 \_ 控制碼 \]**。

</dd> <dt>

*ptr-decl* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 **\*** 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

指定適用于指定之參數類型的零或多個方向屬性、欄位屬性、使用方式屬性和指標屬性。 以逗號分隔多個屬性。

</dd> <dt>

*內容-控制碼類型* 
</dt> <dd>

指定識別碼，此識別碼會指定在採用 **\[ 內容 \_ 句 \] 柄** 屬性的 [**typedef**](typedef.md)宣告中所定義的內容控制碼類型。 取消常式是選擇性的。

**Windows ServerÂ2003與 WINDOWS XP：** 單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式存取 (序列化) 的內容控制碼，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。 這些存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。 損毀或修改內容控制碼狀態的方法必須序列化。 未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。 請注意，建立方法會以隱含方式序列化。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 內容 \_ 控制碼 \]** 屬性可以顯示為 IDL [**typedef**](typedef.md)型別屬性（attribute），做為函式傳回型別屬性（attribute），或做為參數屬性（attribute）。 當您將 **\[ 內容 \_ 控制碼 \]** 屬性套用至類型定義時，您也必須提供內容取消常式。 如需詳細資訊，請參閱 [伺服器內容執行常式](/windows/desktop/Rpc/server-context-run-down-routine) 。

當您在預設情況下使用 MIDL 編譯器 ([**/ms \_ Ext**](-ms-ext.md)) 模式時，只要符合此處所述的內容控制碼需求，內容控制碼就可以是使用者選取的任何指標類型。 與這類內容控制碼類型相關聯的資料，不會在網路上傳輸，因此應該只由伺服器應用程式操作。 DCE IDL 編譯器會將內容控制碼限制為 [**void**](void.md)類型的指標 **\*** 。 因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。

如同其他控制碼類型，內容控制碼對用戶端應用程式而言是不透明的，而且不會傳送任何與其相關聯的資料。 在伺服器上，內容控制碼可作為作用中內容上的控制碼，並可存取與內容控制碼類型相關聯的所有資料。

若要建立內容控制碼，用戶端會將 **\[** [](out-idl.md) **\]** 內容控制碼的 out、 **\[** [**ref**](ref.md) **\]** 指標傳遞給伺服器。  (內容控制碼本身可以有 **null** 或非 **null** 的值，只要其值與指標屬性一致。 例如，當內容控制碼類型套用 **\[** [**ref**](ref.md) **\]** 屬性時，它不能有 **Null** 值。 ) 必須提供另一個系結控制碼才能完成系結，直到建立內容控制碼為止。 如果未指定明確的控制碼，則會使用隱含系結。 當沒有 **\[** [**隱含 \_ 控制碼**](implicit-handle.md) **\]** 屬性存在時，就會使用自動控制碼。

伺服器上的遠端程式會建立活動內容控制碼。 用戶端必須在後續呼叫中使用該內容控制碼做為 **\[** [**in**](in.md) **\]** 或 **\[ in**、 **out \]** 參數。 僅供使用的內容控制碼可作為系結控制碼，因此它必須有非 **Null** 的值。 **\[ \]** 僅限 **\[ 內 \]** 的內容控制碼不會反映伺服器上的狀態變更。

在伺服器上，呼叫的程式可以視需要解讀內容控制碼。 例如，呼叫的程式可以配置堆積儲存體，並使用內容控制碼作為此儲存體的指標。

為了關閉內容控制碼，用戶端會以 **\[** [**in**](in.md) **\]** 、 **\[** [**out**](out-idl.md) **\]** 引數傳遞內容控制碼。 當伺服器不再代表呼叫端維護內容時，伺服器必須傳回 **Null** 內容控制碼。 例如，如果內容控制碼代表開啟的檔案，而呼叫關閉檔案，則伺服器必須將內容控制碼設為 **Null** ，然後將它傳回給用戶端。 **Null** 值在後續呼叫上是不正確系結控制碼。

內容控制碼只對一部伺服器有效。 當函數有兩個控制碼參數，且內容控制碼不是 **Null** 時，系結控制碼必須參考相同的位址空間。

當函式具有 **\[** [**in**](in.md) **\]** 或 **\[ in**、 **\] out** 內容控制碼時，其內容控制碼可以當做系結控制碼使用。 在此情況下，不會使用隱含系結，而且 **\[** 會忽略 [**隱含 \_ 控制碼**](implicit-handle.md) **\]** 或 **\[** [**自動 \_ 控制碼**](auto-handle.md) **\]** 屬性。

下列限制適用于內容控制碼：

-   內容控制碼不可以是陣列元素、結構成員或等位成員。 它們只能是參數。
-   內容控制碼不能將 **\[** [**傳輸 \_ as**](transmit-as.md) **\]** 或 **\[** [**表示 \_ 為**](represent-as.md) **\]** 屬性。
-   指向 **\[** [](out-idl.md) **\]** 內容控制碼指標的參數必須是 **\[** [**ref**](ref.md) **\]** 指標。
-   **\[**[**在**](in.md) **\]** 內容控制碼中，可以當做系結控制碼使用，且不能是 **Null**。
-   在輸入時， **\[ in**、 [**out**](out-idl.md)內容控制碼可以是 **Null** ，但只有在程式有另一個明確的控制碼參數時。 如果沒有其他明確的非 **Null** 內容控制碼參數， **\[ in**、 **out \]** 內容控制碼不可以是 **Null**。
-   內容控制碼無法與回呼一起使用。

## <a name="examples"></a>範例

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[**自動 \_ 處理**](auto-handle.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[用戶端內容重設](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[內容控制碼](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**處理**](handle.md)
</dt> <dt>

[系結和控制碼](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[多執行緒用戶端和內容控制碼](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**表示 \_ 為**](represent-as.md)
</dt> <dt>

[**RpcSsDestroyClientCoNtext**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[伺服器內容執行例行常式](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**傳輸 \_ 為**](transmit-as.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 