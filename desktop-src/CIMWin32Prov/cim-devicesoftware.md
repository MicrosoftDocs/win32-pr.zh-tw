---
description: CIM DeviceSoftware 關聯性 \_ 會識別與裝置相關聯的軟體，例如驅動程式、設定或應用程式軟體或固件。
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: CIM_DeviceSoftware 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510633"
---
# <a name="cim_devicesoftware-class"></a>CIM \_ DeviceSoftware 類別

**CIM \_ DeviceSoftware** 關聯性會識別與裝置相關聯的軟體，例如驅動程式、設定或應用程式軟體或固件。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a>成員

**CIM \_ DeviceSoftware** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ DeviceSoftware** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SoftwareElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述 software 元素的 [**CIM \_ SoftwareElement**](cim-softwareelement.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述需要或使用軟體的邏輯裝置。

</dd> <dt>

**目的**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DeviceSoftware**.**PurposeDescription**") 
</dt> </dl>

軟體針對其相關聯裝置所採取的角色。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

不明。

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

其他。

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**驅動程式** (2) 


</dt> <dd>

司機。

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3) 


</dt> <dd>

設定軟體。

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**應用程式軟體** (4) 


</dt> <dd>

應用程式軟體。

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**檢測** (5) 


</dt> <dd>

檢測。

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**固件** (6) 


</dt> <dd>

固件。

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span id="BIOS"></span><span id="bios"></span>**BIOS** (7) 


</dt> <dd>

Bios。

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**開機 ROM** (8) 


</dt> <dd>

開機 ROM。

</dd> </dl>

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DeviceSoftware**.**目的**」 ) 
</dt> </dl>

提供 **目的** 屬性詳細資訊的自由格式字串，例如「應用程式軟體」。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。

**Cim \_ DeviceSoftware** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

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

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

