---
title: auto_handle 屬性
description: '\ Auto \_ handle \ ACF 屬性會指示存根自動為沒有明確系結控制碼參數的函式建立系結。請注意，此屬性已淘汰，不再支援。'
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462541"
---
# <a name="auto_handle-attribute"></a>自動 \_ 處理屬性

**\[ Auto \_ handle \]** ACF 屬性會指示存根自動建立沒有明確系結控制碼參數之函式的系結。

> [!Note]  
> 這個屬性已淘汰，不再支援。 建議使用 [**/robust**](-robust.md) 參數。

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的零或多個屬性，例如程式 [**代碼**](code.md) 或 [**了 nocode**](nocode.md)。 以逗號分隔介面屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*介面定義* 
</dt> <dd>

指定組成介面定義的 IDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Auto \_ 控制碼 \]** 屬性會出現在 ACF 的介面標頭中。 當您指定 MIDL 編譯器參數 [**/app \_**](-app-config.md)設定時，它也會出現在 IDL 檔案的介面標頭中。

當用戶端呼叫使用自動系結的函式，但不存在任何伺服器系結時，存根會自動建立系結。 系結會在使用自動系結之介面中的其他函式的後續呼叫中重複使用。 用戶端應用程式不需要宣告或執行任何與系結控制碼相關的處理。

當 ACF 不存在或未包含 [**\[ 隱含 \_ 控制碼 \]**](implicit-handle.md)屬性時，MIDL 編譯器會使用 **\[ 自動 \_ 處理 \]** ，併發出參考用訊息。 如果有需要，MIDL 編譯器也會使用 **\[ auto \_ 控制碼 \]** 來建立 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)的初始系結。

只有在未發生 [**\[ 隱含 \_ 控制碼 \]**](implicit-handle.md)或 [**\[ 明確 \_ 控制碼 \]**](explicit-handle.md)屬性時，才會發生 **\[ auto \_ 控制碼 \]** 屬性。 **\[ 自動 \_ 控制碼 \]** 屬性可以出現在 ACF 或 IDL 介面標頭中最多一次。

> [!Note]  
> 您無法使用自動系結 (搭配 **\[ auto \_ handle \]** 屬性，或根據預設) （如果您是透過管道處理資料）。

 

## <a name="examples"></a>範例

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**/app \_ 設定**](-app-config.md)
</dt> <dt>

[**代碼**](code.md)
</dt> <dt>

[**明確 \_ 控制碼**](explicit-handle.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> <dt>

[**了 nocode**](nocode.md)
</dt> </dl>

 

 




