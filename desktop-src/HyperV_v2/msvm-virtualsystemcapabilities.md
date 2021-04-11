---
description: 描述相關聯 Msvm 的非程式的功能 \_ 。
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Msvm_VirtualSystemCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191160"
---
# <a name="msvm_virtualsystemcapabilities-class"></a>Msvm \_ VirtualSystemCapabilities 類別

描述相關聯 Msvm 的非 [**程式 \_**](msvm-computersystem.md)的功能。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemCapabilities** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemCapabilities** 類別具有這些屬性。

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

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以修改 **ElementName** 屬性。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 **ElementName** 的限制，以正則運算式表示。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。

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

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

資料類型： **unit16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **int32.maxvalue** (256) 
</dt> </dl>

指定 **ElementName** 屬性支援的最大長度。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

資料類型： **unit16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出在啟用的邏輯元素上使用 **RequestStateChange** 方法時，可以要求的可能狀態。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。



| 值                                                                         | 意義              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | 已啟用<br/>   |
| <dl> <dt>3</dt> </dl>  | 禁用<br/>  |
| <dl> <dt>4</dt> </dl>  | 關閉<br/> |
| <dl> <dt>6</dt> </dl>  | 離線<br/>   |
| <dl> <dt>7</dt> </dl>  | 測試<br/>      |
| <dl> <dt>8</dt> </dl>  | 推遲<br/>     |
| <dl> <dt>9</dt> </dl>  | 靜止<br/>   |
| <dl> <dt>10</dt> </dl> | 重新啟動<br/>    |
| <dl> <dt>11</dt> </dl> | 重設<br/>     |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

