---
title: type_strict_coNtext_handle 屬性
description: 在 ACF 檔案中，使用 \ 類型 \_ strict \_ 內容 \_ 控制碼 \ 來設定內容控制碼的限制。
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_coNtext_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462981"
---
# <a name="type_strict_context_handle-attribute"></a>輸入 \_ strict \_ 內容 \_ 控制碼屬性

在 ACF 檔案中使用 **\[ 類型 \_ strict \_ 內容 \_ 控制碼 \]** ，以設定內容控制碼的限制。

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

適用于整個介面的其他 ACF 屬性。 有效的屬性 [**包括 \_ 自動控制碼**](auto-handle.md)、 [**隱含 \_ 控制碼**](implicit-handle.md)、 [**明確 \_ 控制碼**](explicit-handle.md)和 [**優化**](optimize.md)、程式 [**代碼**](code.md)或 [**了 nocode**](nocode.md)。 以逗號分隔多個屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

介面的名稱。

</dd> <dt>

*介面定義語句* 
</dt> <dd>

定義 [**介面**](interface.md)元素的一或多個 MIDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

若要使用這個屬性，在執行 midl.exe 時，必須將-target 旗標設為 NT60 (或更高的) 。

\[型別 \_ strict \_ 內容 \_ 控制碼 \] 是 \[ strict \_ 內容 \_ 控制碼的功能超集合 \] 。 在 \[ strict \_ 內容 \_ 控制碼中 \] ，控制碼的型別識別碼一律為0，而在 \[ 型別 \_ STRICT \_ 內容 \_ 控制碼中 \] ，MIDL 編譯器會指派唯一的型別識別碼。

建議使用 \[ 類型 \_ strict \_ 內容 \_ 控制碼， \] 而不是 \[ strict \_ 內容 \_ 控制碼 \] 。 內容控制碼預設不會與特定類型相關聯。 在相同的進程中使用多種類型的內容控制碼時，惡意用戶端可能會傳遞內容控制碼來取代另一個，以產生不想要的結果。 使用 \[ 類型 \_ strict \_ 內容 \_ 控制碼 \] 可讓應用程式強制執行內容控制碼類型一致性，並防止任何不相符的內容控制碼類型使用方式。

具有型別 strict 內容控制碼之屬性的內容控制碼， \[ \_ \_ \_ \] 也不能以 \[ strict 內容控制碼進行屬性化 \_ \_ \] 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**代碼**](code.md)
</dt> <dt>

[內容控制碼](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**內容 \_ 控制碼 \_ 序列化**](context-handle-serialize.md)
</dt> <dt>

[**內容 \_ 控制碼 \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**明確 \_ 控制碼**](explicit-handle.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> <dt>

[**了 nocode**](nocode.md)
</dt> <dt>

[**優化**](optimize.md)
</dt> <dt>

[strict \_ 內容 \_ 控制碼](strict-context-handle.md)
</dt> </dl>

 

 