---
description: 表示顯示控制器。
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: CIM_DisplayController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983341"
---
# <a name="cim_displaycontroller-class"></a>CIM \_ DisplayController 類別

表示顯示控制器。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a>成員

**CIM \_ DisplayController** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ DisplayController** 類別具有這些屬性。

<dl> <dt>

**AcceleratorCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**。**CapabilityDescriptions**") 
</dt> </dl>

顯示控制器的圖形和3D 功能。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

**圖形加速器** (2) 


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

**3D 加速器** (3) 


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

**PCI Fast Write** (4) 


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

**MultiMonitor 支援** (5) 


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

**PCI 主控** (6) 


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

**第二種單色介面卡支援** (7) 


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

 (8) 的 **大型記憶體位址支援**


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**。**AcceleratorCapabilities**") 
</dt> </dl>

**AcceleratorCapabilities** 陣列的影片加速器功能詳細說明。 這個陣列中的專案會對應到 **AcceleratorCapabilities** 中的陣列專案。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.18 ") 
</dt> </dl>

物件的文字描述。

</dd> <dt>

**MaxMemorySupported**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

支援的最大記憶體數量（以位元組為單位）。

</dd> <dt>

**NumberOfVideoPages**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供目前的解析度和可用記憶體所支援的影片頁面數目。

</dd> <dt>

**OtherVideoArchitecture**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**.**VideoArchitecture**") 
</dt> </dl>

**VideoArchitecture** 屬性包含 "1" (其他) 的影片架構類型描述。

</dd> <dt>

**OtherVideoMemoryType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**.**VideoMemoryType**") 
</dt> </dl>

**VideoMemoryType** 屬性為 "1" (其他) 的視訊記憶體類型。

</dd> <dt>

**VideoArchitecture**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來產生視訊訊號的顯示器控制器影片架構。 通常，專用的視頻處理器會根據指定的架構產生影片信號。 架構會指出顯示控制器的最大解析功能。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

**CGA** (2) 


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

**EGA** (3) 


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

**VGA** (4) 


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

**SVGA** (5) 


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

**MDA** (6) 


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

**HGC** (7) 


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

**MCGA** (8) 


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

**8514A** (9) 


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

**XGA** (10) 


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

**線性框架緩衝區** (11) 


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (160) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (0x8000。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoMemoryType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.6 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**OtherVideoMemoryType**") 
</dt> </dl>

視訊記憶體的類型。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

**VRAM** (2) 


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

**DRAM** (3) 


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

**SRAM** (4) 


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

**WRAM** (5) 


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

**EDO RAM** (6) 


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

高載 **同步 DRAM** (7) 


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

**管線** 高載 SRAM (8) 


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

**CDRAM** (9) 


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

**3DRAM** (10) 


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

**SDRAM** (11) 


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

**SGRAM** (12) 


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoProcessor**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

影片處理器/控制器的文字描述。

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

 

