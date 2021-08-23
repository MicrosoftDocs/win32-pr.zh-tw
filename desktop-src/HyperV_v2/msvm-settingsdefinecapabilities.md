---
description: 提供功能實例與資源的最小值、最大值、增量和預設設定之間的連結。
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7194632af7bc1154e6a9bbca1dd5ef0bcca0fb46ab13693d20160ea404068adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950459"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>Msvm \_ SettingsDefineCapabilities 類別

提供功能實例與資源的最小值、最大值、增量和預設設定之間的連結。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ SettingsDefineCapabilities** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SettingsDefineCapabilities** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ 功能**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

功能實例。 這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來定義相關聯功能實例的設定。 這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否將關聯設定資料實例的非 null、非索引鍵屬性單獨處理，或視為相互關聯的集合。 這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) ，且一律設定為 0 (獨立) 。

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別支援語句。

> [!Note]  
> 這個屬性是在 Windows 10 1703 版中加入的。

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**生產** (0) 


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**發行** 前版本 (1) 


</dt> <dd>

> [!Note]  
> 在 Windows 10 1703 版中 **非生產**。

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** 的 (。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

關於設定資料的所有非 null、非索引鍵屬性之解釋的任何進一步的語法。 這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

設定資料之非 null、非索引鍵屬性的解讀上的任何進一步語義。 這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**ValueRole** 和 **ValueRange** 屬性的值會用於下列配對：

-   Point/Default (0/0) 
-   最低/支援 (1/3) 
-   最大/支援 (2/3) 
-   遞增/支援 (3/3) 。

「點」表示 **PartComponent** 物件上的每個屬性都代表平臺預設值。

「最小值」和「最大值」表示 **PartComponent** 物件上的每個屬性都代表這些屬性的最小和最大可能值，這些屬性是根據您目前的電腦設定所支援的平臺。

「遞增」表示您可以增加或減少設定的資料細微性。

存取 **Msvm \_ SettingsDefineCapabilities** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ SettingsDefineCapabilities**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**Msvm \_ SettingsDefineCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[資源管理類別](resource-management-classes.md)
</dt> </dl>

 

