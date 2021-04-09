---
title: async 屬性
description: '\ Async \ ACF 屬性會將遠端程序呼叫定義為非同步作業。'
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- async 屬性 MIDL
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933157"
---
# <a name="async-attribute"></a>async 屬性

\[ **Async** \] ACF 屬性會將遠端程序呼叫定義為非同步作業。

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>參數

<dl> <dt>

*opt-acf-屬性* 
</dt> <dd>

指定選擇性的應用程式設定屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

在 IDL 檔案中指定函數的名稱。

</dd> <dt>

*param 清單* 
</dt> <dd>

指定選擇性參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

此屬性不適用於 COM 介面。

若要將 RPC 函式宣告為非同步，請先將函數宣告為 IDL 檔案中介面定義的一部分。 然後藉由套用 async 屬性，在應用程式佈建檔 (ACF) 內修改該函式宣告 \[  \] 。 請注意，函式宣告不會提及非同步控制碼，且系結控制碼為第一個參數。 \[  \] 在 ACF 檔案中套用 async 屬性會產生適當的程式碼，以便在呼叫此函式時，非同步伺服器預期會在其他參數之前接收非同步控制碼。

> [!Note]  
> Async 屬性無法搭配 [**/osf**](-osf.md) 命令列參數使用。

 

## <a name="examples"></a>範例

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[非同步 RPC](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 