---
title: Win32_TSGatewayServer 類別的 Import 方法
description: 將指定的設定匯入遠端桌面閘道 (RD 閘道) server。
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- 匯入方法遠端桌面服務
- 匯入方法遠端桌面服務，Win32_TSGatewayServer 類別
- Win32_TSGatewayServer 類別遠端桌面服務，匯入方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2629e8e44acd0f617e86a846cc127ab77250673c8612f2d2f53ab8c0238d9f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574568"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Win32 TSGatewayServer 類別的 Import 方法 \_

將指定的設定匯入遠端桌面閘道 (RD 閘道) server。

## <a name="syntax"></a>語法


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ImportType* \[在\]
</dt> <dd>

要匯入的內容。 在 *ImportType* 參數中設定對應的位，以設定匯入類型。 您可以設定多個匯入類型。 例如，如果設定0位，將會匯入遠端桌面服務的連線授權原則 (RD Cap) 。 如果設定0和第2位，則會匯入 RD Cap 和遠端桌面服務資源授權原則 (RD Rap) 。

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>匯 **入所有 CAPs** (1) 


</dt> <dd>

匯入所有 RD Cap。

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>匯 **入所有 Radius 伺服器** (2) 


</dt> <dd>

) 伺服器 (的 NPS 匯入所有網路原則伺服器的清單。

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>匯 **入所有 rap** (4) 


</dt> <dd>

匯入所有 RD Rap。

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>匯 **入所有 RGs** (8) 


</dt> <dd>

匯入所有資源群組。

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>匯 **入所有負載平衡伺服器** (16) 


</dt> <dd>

匯入所有負載平衡伺服器的清單。

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>匯 **入所有伺服器設定** (32) 


</dt> <dd>

匯入所有 RD 閘道相關的伺服器設定。

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>匯 **入所有健康原則** (64) 


</dt> <dd>

匯入所有健康狀態原則。

* * Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 和 Windows Server 2008： * *

Windows Server 2016 之前，不支援這個值。

</dd> </dl> </dd> <dt>

*XmlString* \[在\]
</dt> <dd>

以 XML 字串形式設定的設定。

</dd> <dt>

*MergeOrReplace* \[在\]
</dt> <dd>

指出當發生衝突時，是否要合併或取代資料。

> [!Note]  
> 尚未實行合併。 因此，會忽略此參數值。

 

</dd> <dt>

*LogString* \[擴展\]
</dt> <dd>

匯入作業期間所產生的記錄資訊。

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

 

