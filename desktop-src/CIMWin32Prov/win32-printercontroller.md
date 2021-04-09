---
description: Win32 \_ PrinterController 關聯 WMI 類別會使印表機和印表機所連線的本機裝置產生關聯。 請注意，這個類別只會傳回本機印表機的實例。
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Win32_PrinterController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847321"
---
# <a name="win32_printercontroller-class"></a>Win32 \_ PrinterController 類別

**Win32 \_ PrinterController** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會使印表機和印表機所連線的本機裝置產生關聯。 請注意，這個類別只會傳回本機印表機的實例。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a>成員

**Win32 \_ PrinterController** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PrinterController** 類別具有這些屬性。

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器存取裝置的狀態。 當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Unknown

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

使用中

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

非使用中

</dd> </dl>

</dd> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 控制器**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

參考 [**CIM \_ 控制器**](cim-controller.md) 實例，代表與此印表機相關聯的本機裝置。

這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 印表機**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

[**Win32 \_ 印表機**](win32-printer.md)實例的參考，代表與本機裝置相關聯的印表機。

這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當有多個匯流排或連接資料寬度) 時，裝置之間的使用資料寬度 (。 資料寬度的指定單位為位。 如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。

這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當) 可能有數個匯流排或連線速度時，裝置 (的使用速度。 以每秒位數指定速度。 如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。

這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器發出的硬重設數目。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器發出的軟重設數目。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PrinterController** 類別衍生自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
