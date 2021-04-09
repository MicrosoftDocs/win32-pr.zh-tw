---
title: implicit_handle 屬性
description: '\ 隱含 \_ 控制碼 \ ACF 屬性會指定用於不包含明確控制碼做為程式參數之函數的控制碼。'
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841112"
---
# <a name="implicit_handle-attribute"></a>隱含 \_ 控制碼屬性

**\[ 隱含 \_ 控制碼 \]** ACF 屬性會指定用於不包含明確控制碼做為程式參數之函數的控制碼。

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>參數

<dl> <dt>

*控制碼類型* 
</dt> <dd>

指定控制碼資料類型，例如基底類型 [**控制碼 \_ t**](handle-t.md) 或使用者定義的控制碼類型。

</dd> <dt>

*控制碼名稱* 
</dt> <dd>

指定控制碼的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

視程式的本質而定， **\[ 隱含 \_ 控制碼 \]** 屬性指定的控制碼會以不同的方式使用。 如果程式是遠端的，則會使用控制碼做為遠端呼叫的系結控制碼。 隱含控制碼也可以用來建立使用內容控制碼之函式的初始系結。 如果程式是序列化程式，則會使用控制碼做為控制作業的序列化控制碼。 在序列化類型的情況下，會使用控制碼作為所有序列化類型的序列化控制碼。

**\[ 隱含 \_ 控制碼 \]** 屬性指定的全域變數包含任何需要隱含控制碼的函式所使用的控制碼。

隱含系結控制碼類型必須是 [**處理 \_ t**](handle-t.md) (或以 **控制碼 \_ t**) 為基礎的型別，或是以 [**handle**](handle.md) 屬性指定的使用者定義控制碼類型。 隱含序列化控制碼必須是以 **控制碼 \_ t** 為基礎的型別。

如果 IDL 檔中未定義隱含控制碼類型，或是在 MIDL 電腦的 IDL 檔案包含和匯入的任何檔案中定義，則當您編譯存根時，必須提供包含控制碼類型定義的檔案。 您可以使用 ACF [**include**](include.md) 語句來包含包含控制碼類型定義的檔案。

**\[ 隱含 \_ 控制碼 \]** 屬性最多隻能出現一次。 只有當 [**\[ 自動 \_ 控制碼 \]**](auto-handle.md)和 [**\[ 明確的 \_ 控制碼 \]**](explicit-handle.md)屬性不發生時，才會發生 **\[ 隱含 \_ 句 \]** 柄屬性。

## <a name="examples"></a>範例

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**自動 \_ 處理**](auto-handle.md)
</dt> <dt>

[**明確 \_ 控制碼**](explicit-handle.md)
</dt> <dt>

[**處理 \_ t**](handle-t.md)
</dt> <dt>

[**包括**](include.md)
</dt> </dl>

 

 




