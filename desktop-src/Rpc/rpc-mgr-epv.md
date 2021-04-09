---
title: 'RPC_MGR_EPV (Rpcdce) '
description: 資料類型 RPC \_ MGR \_ EPV 定義了管理員進入點向量。
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685586"
---
# <a name="rpc_mgr_epv"></a>RPC \_ MGR \_ EPV

資料類型 **RPC \_ MGR \_ EPV** 定義了管理員進入點向量。

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>成員

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**if-name**
</dt> <dd>

指定介面的名稱。

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**傳回類型**
</dt> <dd>

指定 IDL 檔案中指出的函式 **Functionname** 所傳回的類型。

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**
</dt> <dd>

指定 IDL 檔案中指出的函數名稱。

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**param 清單**
</dt> <dd>

針對 IDL 檔案中的函式 **Functionname** 指定指定的參數。

</dd> </dl>

## <a name="remarks"></a>備註

 (EPV) 的 manager 進入點向量是函式指標的陣列。 陣列包含 IDL 檔案中指定之函式的實作為指標。 陣列中的元素數目會設定為 IDL 檔案中指定的函數數目。 應用程式也可以有多個 EPVs，表示介面中指定之函式的多個實作為。

MIDL 編譯器會產生名為 * if-name ***\_ SERVER \_ EPV** 的預設 **EPV** 資料類型，其中 *if-name* 會在 IDL 檔案中指定介面識別碼。 MIDL 編譯器會初始化此預設 **EPV** ，以包含 IDL 檔案中所指定之每個程式的函式指標。

當伺服器提供相同介面的多個型別時，伺服器應用程式必須針對每個介面的執行，宣告和初始化一個類型的變數（ *如果-name * * * \_ server \_ EPV**）。 每個 **EPV** 都必須針對 IDL 檔案中定義的每個程式，各包含一個進入點 (函式指標) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce (包含 Rpc) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





