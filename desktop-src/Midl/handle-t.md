---
title: handle_t 屬性
description: 控制碼 \_ t 關鍵字會將物件宣告為基本型別控制碼 t 的基本控制碼類型 \_ 。 基本系結控制碼是可供應用程式用來代表系結的資料物件。
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t 屬性 MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314821"
---
# <a name="handle_t-attribute"></a>處理 \_ t 屬性

**控制碼 \_ t** 關鍵字會將物件宣告為基本型 **別控制碼 \_ t** 的基本控制碼類型。 基本系結控制碼是可供應用程式用來代表系結的資料物件。

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>參數

這個屬性沒有任何參數。

## <a name="remarks"></a>備註

**控制碼 \_ t** 類型是介面定義語言 (IDL) 其中一個預先定義的類型。 它可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

在 Microsoft RPC 中，類型 **控制碼 \_ t** 的參數只能 **\[** [**在參數中**](in.md)發生 **\]** 。 基本控制碼不能具有 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** 屬性。

不會在網路上傳輸) 的 **控制碼 \_ t** (基本控制碼參數類型的參數。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[系結和控制碼](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 