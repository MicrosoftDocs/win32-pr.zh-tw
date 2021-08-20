---
description: 代表復原主機上複寫服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 Msvm \_ ReplicationService. ModifyServiceSettings 方法來修改任何這些屬性。
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Msvm_ReplicationServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6300e7a090d3e62451e64b829930a28ba576cd0626d0965a026e7641450bc1aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810914"
---
# <a name="msvm_replicationservicesettingdata-class"></a>Msvm \_ ReplicationServiceSettingData 類別

代表復原主機上複寫服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 [**Msvm \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) 方法來修改任何這些屬性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a>成員

**Msvm \_ ReplicationServiceSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ReplicationServiceSettingData** 類別具有這些屬性。

<dl> <dt>

**AllowedAuthenticationType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

定義連接到復原主機伺服器時允許的驗證模式。

<dt>

0
</dt> <dd>

未定義。

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos 驗證** (1) 


</dt> <dd>

Kerberos 驗證。

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>以 **憑證為基礎的驗證** (2) 


</dt> <dd>

以憑證為基礎的驗證。

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>以 **憑證為基礎的驗證和 kerberos 驗證** (3) 


</dt> <dd>

以憑證為基礎的驗證與整合式驗證。

</dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為 "Replication Service 設定"。

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128) 
</dt> </dl>

當 **AuthenticationType** 是以憑證為基礎的驗證時，所要使用的憑證指紋。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬機器複寫設定資料」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為 "Replication Service 設定"。

</dd> <dt>

**HttpPort**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在接受複寫的非安全連線時，所要使用的復原伺服器埠號碼。 預設值是 80。

</dd> <dt>

**HttpsPort**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在接受用於複寫的安全連線時，要使用的復原伺服器埠號碼。 預設值為443。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**MonitoringInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

應該重設複寫統計資料的間隔（以秒為單位）。 預設間隔為12小時 (43200 秒) 。 最小有效值為60分鐘 (3600 秒) ，最大值為7天 (604800 秒) 。

</dd> <dt>

**MonitoringStartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

複寫監視的開始時間（UTC）。 預設值為 9:00 A.M.、當地時間，以 UTC 表示。 **Datetime** 物件的日期元素必須為零。

</dd> <dt>

**RecoveryServerEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否將 Hyper-v 主機啟用為復原伺服器。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

