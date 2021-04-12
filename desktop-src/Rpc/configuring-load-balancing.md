---
title: 設定負載平衡
description: 設定負載平衡
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82dbfc23e491d53a6687b50aa77b23878ce52ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316240"
---
# <a name="configuring-load-balancing"></a>設定負載平衡

每個要作為負載平衡伺服器 (磅) 服務的 RPC Proxy 電腦都必須設定為具有伺服器陣列中伺服器知識的磅服務。 （選擇性）您可以設定預設的資源，並將 Proxy 的安全性設為磅和磅，以設定可設定的 RPC 呼叫。 這些設定是由一組必要的登錄機 **碼** 和 **選用** 的登錄機碼所設定，如下所述。

## <a name="required-registry-keys"></a>必要的登錄機碼

需要有數個登錄機碼和值，才能設定磅伺服器。 如果有任何索引鍵遺失或輸入錯誤，則會記錄 Windows 事件。 請參閱每個索引鍵和值的描述，以取得所記錄事件的相關資訊。

若要設定伺服器陣列，必須建立登錄機碼 **HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy** ，稱為 **LBSConfiguration**。 在 **LBSConfiguration** 機碼下，會為伺服器陣列中的每個資源建立金鑰。 索引鍵名稱是資源之 GUID 的字串標記法。 至少必須有一個資源金鑰存在，而且此資源與系結控制碼、RPC 系結控制碼上的用戶端所設定的 [**UUID**](./rpcdce/ns-rpcdce-uuid.md)相同，當它們建立 RPC/HTTP 系結時 (如需詳細資訊，請參閱 [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)) 。 [**\_ \_**](rpc-binding-handle.md) 在每個資源 UUID 索引鍵下，必須存在名為 **ConfigurationType** 的 DWORD 值，以描述所使用的設定。 也必須有以分號分隔之伺服器識別碼的 **REG \_ SZ** （稱為 **ServerFarm**）。 **ServerFarm** 機碼中識別的伺服器是負載平衡伺服器陣列成員的伺服器。

以下是所需登錄機碼和值的詳細細目：

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration**

登錄機碼。 **LBSConfiguration** 機碼是持有磅設定的登錄機碼。 這包括要平衡負載的資源 [**uuid**](./rpcdce/ns-rpcdce-uuid.md) 、每個資源的設定類型，以及伺服器陣列中參與負載平衡的伺服器。 如果此金鑰遺失或無效，則不會將磅視為已設定，而且不會執行磅服務。

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration 的 \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx**

登錄機碼。 **資源 uuid** 索引鍵會識別要進行負載平衡的資源 uuid。 此資源 UUID 與用戶端在系結控制碼、RPC 系結 [**\_ \_ 控制碼**](rpc-binding-handle.md)上設定的 [**uuid**](./rpcdce/ns-rpcdce-uuid.md)相同。 至少必須要有一個資源 UUID 可進行負載平衡，可能有多個資源 Uuid。 伺服器陣列中的所有伺服器都只能有一個伺服器陣列，而且所有端點都必須在伺服器陣列中的所有伺服器上。 如果無法將此金鑰剖析為有效的 UUID，事件 **RPCPROXY \_ EVENTLOG \_ LB \_ \_ (0xC0000006)** 將會記錄到 Windows 事件記錄檔中。

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx 的 \\ ConfigurationType**

DWORD。 **ConfigurationType** DWORD 會儲存在 **資源 UUID** 索引鍵下。 唯一允許的值為1。 如果這個值是1以外的任何值，事件 **RPCPROXY \_ EVENTLOG \_ LB \_ \_ \_ (0XC0000007)** 將會記錄到 Windows 事件記錄檔中。

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx 的 \\ ServerFarm**

REG \_ SZ。 **ServerFarm** 登錄值包含伺服器識別碼的分號 delimitated 清單。 伺服器識別碼的格式為：

"ServerID1，ServerPort1，LBSPort1， \[ LBSPort2，.。。LBSPortN \] ; "

**ServerFarm** 登錄機碼中應該會列出多個伺服器識別碼。 它們必須以分號分隔。 下表說明屬於伺服器識別碼的欄位。 如果無法正確剖析此欄位，事件 **RPCPROXY \_ EVENTLOG \_ LB LB \_ \_ \_ (0XC0000008)** 將會記錄到 Windows 事件記錄檔中。



| 識別碼欄位 | 需求 | 描述                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | 必要    | 伺服器的可解析網路名稱。 這可以是 DNS 名稱、netbios 名稱或 IP 位址。                                                                                                                                                                                |
| ServerPort       | 選擇性    | 如果指定的話，伺服器會在此埠上接聽 RPC/HTTP 連接。 如果未指定，則會使用伺服器電腦上的結束點對應程式來尋找伺服器埠。                                                                                                         |
| LBSPort          | 選擇性    | 如果指定的話，則為伺服器在其上接聽磅的埠。 若要使用此金鑰，您必須使用 netsh RPC firewall 命令將磅介面設定為靜態端點。 如需 netsh 命令的範例，請參閱 [負載平衡最佳做法](load-balancing-best-practices.md) 。 |



 

## <a name="optional-registry-keys"></a>選用的登錄機碼

有三個選擇性的登錄值可設定磅伺服器。 金鑰主要是控制對磅服務進行呼叫的安全性層級，也會控制要使用的預設資源 UUID。 以下是選用值：

以下是所需登錄機碼和值的詳細細目：

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD。 當 **NoSecurity** DWORD 不存在或設為0時，會拒絕對磅服務的傳入非安全呼叫。 如果存在且不是0，則不會拒絕對磅服務的連入非安全呼叫。 此金鑰會在啟動磅服務時讀取一次。

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD。 當 **AssumeResourceUUID** DWORD 不存在時，就不會發生任何變更。 當其存在時，必須使用有效的 [**UUID**](./rpcdce/ns-rpcdce-uuid.md)來設定。 此 **UUID** 將作為未指定資源 uuid 之所有連接的資源 uuid。 這通常用於用戶端建立 RPC/HTTP 系結時未指定資源 UUID 的情況，但系統管理員希望將 RPC/HTTP 流量負載平衡到伺服器陣列。 如果無法將此索引鍵剖析為 UUID，則會 lodged 內部 RPC 錯誤，如果已啟用，則會產生 [**rpc \_ 擴充的 \_ 錯誤 \_ 資訊**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) 。

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD。 當 **NoSecurity** DWORD 未呈現或設為0時，對磅服務發出的所有撥出電話都會有安全性。 如果存在且未設定為0，則對磅服務發出的所有撥出電話都不會有安全性。 請確定此設定符合 **HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ NoSecurity** 設定。

 

 