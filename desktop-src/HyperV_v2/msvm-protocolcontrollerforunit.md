---
description: 此關聯表示邏輯裝置的子類別 (例如，存放磁片區) 透過特定的通訊協定控制器連線。
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 73b8478e561d53212e0439219622595751ad954e13d0d086fabdbf57a483039d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086628"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>Msvm \_ ProtocolControllerForUnit 類別

此關聯表示邏輯裝置的子類別 (例如，存放磁片區) 透過特定的通訊協定控制器連線。 在許多情況下 (例如儲存體 LUN 遮罩) ，可能會有許多這些關聯與不同的物件相關聯。 因此，已定義子類別來優化關聯的列舉。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>成員

**Msvm \_ ProtocolControllerForUnit** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ProtocolControllerForUnit** 類別具有這些屬性。

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

透過此控制器存取裝置所提供的優先權。 最高優先順序的路徑會有此參數的最小值。 此類別繼承自 **CIM \_ ProtocolControllerForDevice**。

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出控制器是否正在主動命令或存取裝置 (2) 或不 (3) 。 此外，也可以定義值 0 (未知的) ）。 當邏輯裝置可透過多個通訊協定控制器來發出或存取時，這項資訊是必要的。 此類別繼承自 **CIM \_ ProtocolControllerForDevice**。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2) 
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**非** 使用中 (3 ) 
</dt> </dl>

</dd> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

通訊協定控制器。 此類別繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

受控制的裝置。 此類別繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

透過此控制器授與裝置的存取權限。 此類別繼承自 **CIM \_ ProtocolControllerForUnit**。



| 值                                                                               | 意義                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>        | 讀取/寫入<br/>      |
| <dl> <dt>3</dt> </dl>        | 唯讀<br/>       |
| <dl> <dt>4</dt> </dl>        | 沒有存取權。<br/>      |
| <dl> <dt>5. 15999</dt> </dl> | 已保留 DMTF<br/>   |
| <dl> <dt>16000 .。。</dt> </dl>  | 保留的廠商<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

前一個控制器內容中相關聯裝置的位址。 此類別繼承自 **CIM \_ ProtocolControllerForDevice**。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ ProtocolControllerForUnit** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ ProtocolControllerForUnit**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**CIM \_ ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[儲存體類](storage-classes.md)
</dt> </dl>

 

