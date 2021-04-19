---
description: 描述序列控制器的功能和管理。
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: 'CIM_SerialController 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972070"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a>CIM_SerialController 類別 (Hyper-v 管理) 

描述序列控制器的功能和管理。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a>成員

**CIM \_ SerialController** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ SerialController** 類別具有這些屬性。

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 序列埠 \| 004.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**。**CapabilityDescriptions**") 
</dt> </dl>

序列控制器的晶片層級相容性。 此屬性描述可能在晶片硬體中固有之序列控制器的緩衝和其他功能。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

**XT/相容** (3) 


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

**16450 相容** (4) 


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

**16550 相容** (5) 


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

**16550A 相容** (6) 


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

**8251 相容** (160) 


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

**8251FIFO 相容** (161) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SerialController**。**功能**") 
</dt> </dl>

陣列，其中包含 **功能** 陣列中序列控制器功能的更詳細說明。 **CapabilityDescriptions** 陣列中的專案與 **功能** 陣列中的專案相互關聯。

</dd> <dt>

**MaxBaudRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 序列埠 \| 004.6 ") ， **PUnit** (" bit/second ") 
</dt> </dl>

序列控制器支援的最大傳輸速率（以每秒位數為單位）。

</dd> <dt>

**安全性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 序列埠 \| 004.9 ") 
</dt> </dl>

控制器的操作安全性。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (3) 


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

**外部介面被鎖定** (4) 


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

**已啟用外部介面** (5) 


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**開機略過** (6) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 控制器**](cim-controller.md)
</dt> </dl>

 

