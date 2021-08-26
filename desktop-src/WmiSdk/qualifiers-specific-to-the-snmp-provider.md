---
description: 限定詞包含執行特定的內容資訊和傳輸屬性，可定義 SNMP 提供者存取 SNMP 代理程式的方式。 以下列出 SNMP 提供者唯一的限定詞。
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: SNMP 提供者專用的限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3b05e2d6994bd0bee1a1f0e30287169c23b69ef574ba47fab1f3d8b5db5abedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996088"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a>SNMP 提供者專用的限定詞

限定詞包含執行特定的內容資訊和傳輸屬性，可定義 SNMP 提供者存取 SNMP 代理程式的方式。 以下列出 SNMP 提供者唯一的限定詞。

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

資料類型： **CIM \_ 字串**

與 SNMP 代理程式相關聯的傳輸位址，例如 IP 位址或 DNS 名稱。 您應該將 **AgentAddress** 設定為有效的單點傳送主機位址，或是可透過作業系統的網域名稱解析程式來解析的網域主機名稱。 **AgentAddress** 沒有預設值。

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize** 
</dt> <dd>

資料類型： **CIM \_ SINT32**

尚未收到回應時，可傳送到此代理程式的同時未完成 SNMP 要求數目上限。 SNMP 要求會被視為未處理，直到接收到 PDU 回應或已超時。大型的視窗大小通常會改善效能，但某些代理程式在繁重的負載下可能無法正常運作。 **AgentFlowControlWindowSize** 可以設定為0，表示無限視窗大小或介於1和 2 ^ 32-1 之間的整數。 預設值是 10。 此辨識符號是選擇性的。

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName** 
</dt> <dd>

資料類型： **CIM \_ 字串**

SNMP 代理程式在讀取作業期間用來驗證 SNMP 通訊協定資料單位的可變長度八位字串 (PDU)  (SNMP 取得/取得下一個要求) 。 群體名稱必須對應至 Unicode 字串，且僅限英數位元。 預設值為 public。 此辨識符號是選擇性的。

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount** 
</dt> <dd>

資料類型： **CIM \_ SINT32**

在要求被視為失敗之前，單一 SNMP 要求可以重試的次數（如果沒有來自 SNMP 代理程式的回應）。 **AgentRetryCount** 必須設定為介於0到 2 ^ 32-1 之間的整數。 預設值為 1。 此辨識符號是選擇性的。

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout** 
</dt> <dd>

資料類型： **CIM \_ SINT32**

將 SNMP 通訊協定資料單位 (PDU) 之前的時間（以毫秒為單位）視為已卸載。 這是等候傳送至 SNMP 代理程式的 SNMP 要求回應所需的毫秒數。 **AgentRetryTimeout** 必須設定為介於0到 2 ^ 32-1 之間的整數。 預設值為 500。 此辨識符號是選擇性的。

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion** 
</dt> <dd>

資料類型： **CIM \_ 字串**

與 SNMP 代理程式通訊時所要使用的 SNMP 通訊協定版本。 目前，唯一有效的值為 1 (適用于 SNMPv2C) 的 SNMPv1) 和 2C (。 預設值為 1。 此辨識符號是選擇性的。

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport** 
</dt> <dd>

資料類型： **CIM \_ 字串**

用來與 SNMP 代理程式通訊的傳輸通訊協定。 目前唯一有效的值是網際網路通訊協定 (IP) 和網際網路封包 Exchange (IPX) 。 預設值為 [IP]。 此辨識符號是選擇性的。

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu** 
</dt> <dd>

資料類型： **CIM \_ SINT32**

單一 SNMP PDU 內包含的最大變數系結數目。 每個傳送至 SNMP 代理程式的 SNMP 要求都包含一或多個 SNMP 變數。 此參數會指定單一要求中可包含的最大變數數目。 **AgentVarBindsPerPdu** 可以設定為 0 (零) ，使實作為判斷最佳變數系結或介於1到 2 ^ 32-1 之間的整數。 請注意，增加此值可以改善效能，某些代理程式和網路無法處理產生的要求。 預設值是 10。 此辨識符號是選擇性的。

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName** 
</dt> <dd>

資料類型： **CIM \_ 字串**

SNMP 代理程式在寫入作業期間，用來驗證 SNMP 通訊協定資料單位的可變長度八進位字串 (PDU)  (SNMP 組要求) 。 群體名稱必須對應至 Unicode 字串，且僅限英數位元。 預設值為 public。 此辨識符號是選擇性的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



 

 




