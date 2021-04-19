---
description: 代表 CRT 桌面監視器。
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: 'CIM_DesktopMonitor 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972683"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a>CIM_DesktopMonitor 類別 (Hyper-v 管理) 

代表 CRT 桌面監視器。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a>成員

**CIM \_ DesktopMonitor** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ DesktopMonitor** 類別具有這些屬性。

<dl> <dt>

**頻寬**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "mhz" ) ， **PUnit** ( "赫茲 \* 10 ^ 6" ) 
</dt> </dl>

MHertz 中顯示的頻寬。 "0" 表示不明。

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

CRT 監視器的顯示類型類型。 例如，multiscan color 或單色。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

**Multiscan 色彩** (2) 


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

**Multiscan 單色** (3) 


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

**固定頻率色彩** (4) 


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

**固定頻率單色** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

顯示器的邏輯高度，以螢幕座標為單位。

</dd> <dt>

**ScreenWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

顯示器的邏輯寬度，以螢幕座標為單位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 顯示**](cim-display.md)
</dt> </dl>

 

