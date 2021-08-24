---
title: 端點屬性
description: '\ Endpoint \ 屬性（attribute）會指定已知的埠或埠 (通訊端點，) 在哪些伺服器上接聽呼叫。'
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- endpoint 屬性 MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea4951a407f09c1407c6e897938460d780e0429e888210e7e1ade392b5e94af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383178"
---
# <a name="endpoint-attribute"></a>端點屬性

**\[ 端點 \]** 屬性會指定已知的埠或埠 (通訊端點，) 在其上，介面的伺服器會接聽呼叫。

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>參數

<dl> <dt>

*通訊協定順序* 
</dt> <dd>

指定代表 RPC 通訊協定 (的有效組合的字元字串，例如 "ncacn" ) 、傳輸通訊協定 (例如 "tcp" ) 和網路通訊協定 (例如 "ip" ) 。 如需有效通訊協定順序的清單，請參閱 [通訊協定順序常數](/windows/desktop/Rpc/protocol-sequence-constants)。

</dd> <dt>

*端點-埠* 
</dt> <dd>

指定表示指定之通訊協定系列之端點指定的字串。 埠字串的語法為每個通訊協定順序所特有。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 端點 \]** 屬性會指定傳輸家族，例如 tcp/ip 連接導向的通訊協定、NetBIOS 連接導向的通訊協定，或具名管道連接導向的通訊協定。 **\[ 端點 \]** 屬性的使用與其他新增端點的方法一致，而且不提供端點的其他或特殊服務，只會提供呼叫 API 的快捷方式。

> [!Note]  
> 在中指定端點。IDL 介面定義不會將介面的存取限制為指定的端點。 將端點加入至。IDL 介面定義允許透過該進程中的任何端點來呼叫介面，並允許在該進程中使用端點來呼叫其他介面。

 

*通訊協定序列* 值會決定 *端點埠* 的有效值。 MIDL 編譯器只會檢查 *端點埠* 專案的一般語法。 執行時間程式庫會報告埠規格錯誤。 如需每個通訊協定順序之允許值的相關資訊，請參閱 [通訊協定順序常數](/windows/desktop/Rpc/protocol-sequence-constants)。

Microsoft RPC： **ncacn \_ osi \_ dna** 和 **ncadg \_ dds** 提供的 MIDL 編譯器不支援 DCE 指定的下列通訊協定順序。

請確定您已正確地在端點中括住反斜線字元。 當端點是具名管道時，通常會發生這個錯誤。

IDL 檔案中指定的端點資訊是由 RPC 執行時間函式 [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) 和 [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)所使用。

## <a name="examples"></a>範例

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 