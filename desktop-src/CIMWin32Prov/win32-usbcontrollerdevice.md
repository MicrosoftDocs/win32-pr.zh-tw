---
description: Win32 \_ USBControllerDevice 關聯 WMI 類別會建立通用序列匯流排 (USB) 控制器和與其連接的 CIM \_ LogicalDevice 實例的關聯。
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Win32_USBControllerDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999830"
---
# <a name="win32_usbcontrollerdevice-class"></a>Win32 \_ USBControllerDevice 類別

**Win32 \_ USBControllerDevice** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立通用序列匯流排 (USB) 控制器和與其連接的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)實例的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ USBControllerDevice** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ USBControllerDevice** 類別具有這些屬性。

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出控制器是否正在主動命令或存取裝置。 當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Active** (1) 


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**非** 使用中 (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ USBController**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ USBController" ) 
</dt> </dl>

[**CIM \_ USBController**](cim-usbcontroller.md) ，表示與此裝置相關聯的通用序列匯流排 (USB) 控制器。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「cim \| CIM \_ LogicalDevice」 ) 
</dt> </dl>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述連線到通用序列匯流排 (USB) 控制器的邏輯裝置。

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bits" ) 
</dt> </dl>

當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。 資料寬度的指定單位為位。 如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。

這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒位數」 ) 
</dt> </dl>

當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。 以每秒位數指定速度。 如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器發出的硬重設數目。 硬重設會將裝置傳回到其初始化或啟動狀態。 所有內部裝置狀態資訊和資料都會遺失。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器發出的軟重設數目。 軟重設並不會完全清除目前的裝置狀態和資料。 確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ USBControllerDevice** 類別衍生自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

如需使用的相關討論，請參閱 [使用 WMI blog 的顯示 USB 裝置](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) 一文。 如需使用關聯類別的討論，請參閱 [PowerShell 文章中的「取得 USB-使用 WMI 關聯類別](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) 」。

## <a name="examples"></a>範例

下列 PowerShell 範例會抓取相依的邏輯裝置，並顯示相關的資訊。


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
