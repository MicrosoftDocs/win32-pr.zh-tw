---
title: 控制碼屬性
description: '\ Handle \ 屬性指定使用者定義或 \ 0034; 自訂 \ 0034;控制碼類型。'
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- 處理屬性 MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842288"
---
# <a name="handle-attribute"></a>控制碼屬性

\[ **Handle** \] 屬性指定使用者定義或「自訂」的控制碼類型。

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>參數

<dl> <dt>

*typename* 
</dt> <dd>

指定使用者定義的系結-控制碼類型的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

使用者定義控制碼允許開發人員設計對應用程式有意義的控制碼。 使用者定義控制碼只能在類型宣告中定義，而不能定義在函式宣告子中。

Handle 屬性所定義之類型的參數 \[  \] 會用來判斷呼叫的系結，並傳送至呼叫的程式。

使用者必須提供系結和解除系結常式，才能在基本與使用者定義的控制碼類型之間轉換。 假設使用者定義了類型 *名稱* 類型的控制碼，則使用者必須提供常式 *typename* 系結 \_ 和 *typename* \_ **解除** 系結。 例如，如果使用者定義控制碼類型的名稱是 MYHANDLE，則常式會命名為 MYHANDLE \_ **BIND** 和 MYHANDLE \_ **解除** 系結。

如果成功， *typename* 系結 \_ 常式應該會傳回有效的基本系結控制碼。 如果不成功，則常式應傳回 **Null**。 如果常式傳回 **Null**，則不會呼叫 *typename* \_ **解除** 系結常式。 如果系結常式傳回的系結控制碼與 **Null** 不同，則存根行為是未定義的。

當遠端程式以使用者定義控制碼做為參數或隱含控制碼時，用戶端 stub 會在呼叫遠端程式之前呼叫系結常式。 用戶端 stub 會在遠端呼叫之後呼叫解除系結常式。

在 DCE IDL 中，具有 \[ **handle** \] 屬性的參數必須顯示為遠端過程引數清單中的第一個參數。 後續的參數（包括其他 \[ **控制碼** \] 屬性）會被視為一般參數。 Microsoft 支援可延伸至 DCE IDL 的延伸模組，可讓使用者定義 \[ **控制碼** \] 參數出現在第一個參數以外的位置。

## <a name="examples"></a>範例

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[系結和控制碼](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 