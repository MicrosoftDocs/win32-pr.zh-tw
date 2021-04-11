---
title: Win32_TSGatewayServer 類別的 Export 方法
description: 以 XML 字串形式傳回遠端桌面閘道 (RD 閘道) 伺服器設定。
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Export 方法遠端桌面服務
- Export 方法遠端桌面服務，Win32_TSGatewayServer 類別
- Win32_TSGatewayServer 類別遠端桌面服務，Export 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935138"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a>Win32 TSGatewayServer 類別的 Export 方法 \_

以 XML 字串形式傳回遠端桌面閘道 (RD 閘道) 伺服器設定。

## <a name="syntax"></a>語法


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ExportType* \[在\]
</dt> <dd>

要匯出的內容。 設定匯出類型，方法是在 *ExportType* 參數中設定對應的位。 您可以設定多個匯出類型。 例如，如果設定0位，則會匯出 (RD Cap) 的遠端桌面服務連線授權原則。 如果設定0和第2位，則會匯出 RD Cap 和遠端桌面服務資源授權原則 (RD Rap) 。

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**匯出所有 CAPs** (1) 


</dt> <dd>

匯出所有 RD Cap。

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>將 **所有 Radius 伺服器匯出** (2) 


</dt> <dd>

將所有網路原則伺服器的清單匯出 (NPS) 伺服器。

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>將 **所有 Rap 匯出** (4) 


</dt> <dd>

匯出所有 RD Rap。

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>將 **所有 RGs 匯出** (8) 


</dt> <dd>

匯出所有資源群組。

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>將 **所有負載平衡伺服器匯出** (16) 


</dt> <dd>

匯出所有負載平衡伺服器的清單。

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>將 **所有伺服器設定匯出** (32) 


</dt> <dd>

匯出所有 RD 閘道相關的伺服器設定。

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>將 **所有健康原則匯出** (64) 


</dt> <dd>

匯出所有健康情況原則。

* * Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 和 Windows Server 2008： * *

Windows Server 2016 之前不支援這個值。

</dd> </dl> </dd> <dt>

*XmlString* \[擴展\]
</dt> <dd>

XML 字串。

</dd> </dl>

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

