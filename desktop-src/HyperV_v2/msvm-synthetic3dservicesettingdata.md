---
description: 代表存在於單一主機系統上的綜合3-d 服務的設定。
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Msvm_Synthetic3DServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114957"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a>Msvm \_ Synthetic3DServiceSettingData 類別

代表存在於單一主機系統上的綜合3-d 服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 [**Msvm \_ Synthetic3DService. ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) 方法來修改任何這些屬性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a>成員

**Msvm \_ Synthetic3DServiceSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ Synthetic3DServiceSettingData** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**GPUOvercommitEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制虛擬機器指派是否會將 GPU 記憶體限制納入考慮。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

