---
description: Hyper-v 複寫 API 會定義下列程式設計項目。
ms.assetid: 0A6FDE16-6A0A-4E6F-9241-79BCF77627E2
title: Hyper-v 複寫 API 參考
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65518cf0476229e5325390ad04b78b657ea15f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974586"
---
# <a name="hyper-v-replication-api-reference"></a>Hyper-v 複寫 API 參考

Hyper-v 複寫 API 會定義下列程式設計項目。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)<br/>     | 代表客體作業系統內網路介面卡的設定，這些設定將在容錯移轉時套用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Msvm \_ ReplicationProvider**](msvm-replicationprovider.md)<br/>                                 | 表示可用的複寫提供者。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)<br/>                         | 表示複寫關聯性的複寫狀態。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**Msvm \_ ReplicaSystemDependency**](msvm-replicasystemdependency.md)<br/>                         | 代表 Cim 系統類型實例之間的關聯 [**， \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 該類別代表虛擬機器複本，以及表示測試虛擬機器複本的 **cim \_ 系統類型** 實例。<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)<br/> | 代表復原伺服器的授權專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Msvm \_ ReplicationService**](msvm-replicationservice.md)<br/>                                   | 管理虛擬機器的複寫。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**Msvm \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md)<br/>             | 代表復原主機上複寫服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 [**Msvm \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) 方法來修改任何這些屬性。<br/>                                                                                                                                                                                                                                                                                        |
| [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md)<br/>                           | 代表虛擬機器的複寫特定設定。 用戶端會將這個類別的實例傳遞至 [**Msvm \_ ReplicationService >createreplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md) ，以建立複寫關聯性。 用戶端無法直接變更這個類別之任何屬性的值;它必須呼叫 [**Msvm \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) 方法來變更值。 每個複寫關聯性都有單一的設定實例。<br/> |
| [**Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md)<br/>                             | 提供虛擬機器的複寫統計資料。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Msvm \_ SystemReplicationRelationship**](msvm-systemreplicationrelationship.md)<br/>             | 代表 Msvm 的實例（代表虛擬 [**機 \_**](msvm-computersystem.md) 的實例）與代表虛擬機器之複寫關聯性的 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 實例之間的關聯。 <br/>                                                                                                                                                                                                                                                                                                |



 

 

