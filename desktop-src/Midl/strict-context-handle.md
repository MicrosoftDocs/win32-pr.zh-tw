---
title: strict_coNtext_handle 屬性
description: '\ Strict \_ 內容 \_ 控制碼 \ ACF 屬性會設定內容控制碼的限制。'
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_coNtext_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933113"
---
# <a name="strict_context_handle-attribute"></a>strict \_ 內容 \_ 控制碼屬性

**\[ Strict \_ 內容 \_ 控制碼 \]** ACF 屬性會設定內容控制碼的限制。

``` syntax
[ 
    strict_context_handle 
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

一般來說，當呼叫介面方法產生內容控制碼時，該控制碼會變成可供任何其他介面免費使用。 當您使用 **\[ strict \_ 內容 \_ 控制碼 \]** 屬性時，您保證該介面中的方法只會接受從相同介面中的方法所建立的內容控制碼。 不使用 **\[ strict \_ 內容 \_ 控制碼 \]** 編譯的介面無法接受在以 **\[ strict \_ 內容 \_ 控制碼 \]** 編譯之介面上建立的內容控制碼。

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

[輸入 \_ strict \_ 內容 \_ 控制碼](type-strict-context-handle.md)
</dt> </dl>

 

 