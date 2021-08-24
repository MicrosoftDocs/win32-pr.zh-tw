---
title: '篩選子層識別碼 (Fwpmu .h) '
description: WFP API 管理篩選子層識別碼常數。
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d597fa1b75f6c965da9cf8d71bcc3e729d0b0b2f4f4220c984a1be8c94c09d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068878"
---
# <a name="filtering-sublayer-identifiers"></a>篩選子層識別碼

Windows 篩選平台 (WFP) 子層識別碼都是由 GUID 表示。

這些識別碼的定義如下。

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM \_ 子層 \_ EDGE \_ 遍歷/FWPM \_ 子層 \_ TEREDO**
</dt> <dd> <dl> <dt>



Edge 遍歷篩選會新增至此子層。

> [!Note]  
> 針對 Windows 7 和更新版本，請使用 **FWPM \_ 子層 \_ EDGE \_ 遍歷**。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM \_ 子層 \_ 檢查**
</dt> <dd> <dl> <dt>



這是最低的加權子層。 它僅用於檢查篩選。


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM \_ 子層 \_ IPSEC \_ DOSP**
</dt> <dd> <dl> <dt>



IPsec DoS 保護篩選器會新增至此子層。

> [!Note]  
> 僅適用于 Windows Vista （含 SP1）、Windows Server 2008 及更新版本。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM \_ 子層 \_ IPSEC \_ 轉送 \_ 輸出 \_ 通道**
</dt> <dd> <dl> <dt>



IPsec 轉送輸出通道篩選器會新增至此子層。

> [!Note]  
> 只能在 Windows 7、Windows Server 2008 R2 和更新版本上使用。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM \_ 子層 \_ IPSEC \_ 通道**
</dt> <dd> <dl> <dt>



IPsec 通道篩選器會新增至此子層。


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM \_ 子層 \_ LIP**
</dt> <dd> <dl> <dt>



舊版 IPsec 篩選器會新增至此子層。


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM \_ 子層 \_ RPC \_ AUDIT**
</dt> <dd> <dl> <dt>



RPC audit 篩選器會新增至此子層。 這些篩選準則會以 C2 和通用準則合規性的一部分來審核 RPC 撥入電話。


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM \_ 子層 \_ 安全 \_ 通訊端**
</dt> <dd> <dl> <dt>



安全通訊端篩選器會新增至此子層。


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM \_ 子層 \_ TCP \_ 煙囪 \_ 卸載**
</dt> <dd> <dl> <dt>



TCP 煙囪卸載篩選器會新增至此子層。


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM \_ 子層 \_ TCP \_ 範本** 
</dt> <dd> <dl> <dt>



TCP 範本篩選器會新增至此子層。

> [!Note]  
> 只能在 Windows 8、Windows Server 2012 和更新版本上使用。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM \_ 子層 \_ 通用**
</dt> <dd> <dl> <dt>



此子層裝載所有未指派給任何其他子層的篩選器。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Fwpmu。h</dt> </dl> |



 

 





