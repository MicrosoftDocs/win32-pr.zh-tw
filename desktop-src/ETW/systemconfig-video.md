---
description: SystemConfig_Video 類別-此類別是影片設定事件的事件種類類別。
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: SystemConfig_Video 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 09d68fcd2710e4f16b315182624ce32eaa3729f370a4a6a071c55f705dcbe6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811698"
---
# <a name="systemconfig_video-class"></a>SystemConfig \_ 影片類別

此類別是影片設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>成員

**SystemConfig \_ Video** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ Video** 類別具有這些屬性。

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (8) ， **最大** (256) ， **格式 ( "s" )**
</dt> </dl>

介面卡的名稱或描述。

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (9) ， **最大** (256) ， **格式 ( "s" )**
</dt> </dl>

介面卡的 BIOS 名稱。

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 
</dt> </dl>

用來顯示每個圖元的位數。

</dd> <dt>

**ChipType**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) ， **最大** (256) ， **格式 ( "s" )**
</dt> </dl>

介面卡的晶片名稱。

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) ， **最大** (256) ， **格式 ( "s" )**
</dt> </dl>

數位轉類比轉換器 (DAC 的介面卡) 晶片名稱。

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (10) ， **最大** (256) ， **格式 ( "s" )**
</dt> </dl>

用來唯一命名邏輯裝置的位址或其他識別資訊。

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) 
</dt> </dl>

支援的最大記憶體數量（以位元組為單位）。

</dd> <dt>

**StateFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (11) ， **格式 ( "x" )**
</dt> </dl>

裝置狀態旗標。 它可以是下列任何合理的組合。



| 值                                                                                                                                                                                                                                                                                        | 意義                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**顯示 \_\_連接 \_ 到 \_ 桌面**</dt> <dt>1 (0x1)</dt>的裝置 </dl> | 裝置是桌面的一部分。<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**顯示 \_裝置 \_ 鏡像 \_ 驅動程式**</dt> <dt>8 (0x8)</dt> </dl>           | 代表用來鏡像應用程式繪圖以連接到遠端電腦或其他用途的虛擬裝置。 不可見的虛擬監視器與此裝置相關聯。 例如，NetMeeting 會使用它。<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**顯示 \_裝置 \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | 裝置的顯示模式比輸出裝置支援的還多。<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**顯示 \_裝置 \_ 主要 \_ 裝置**</dt> <dt>4 (0x4)</dt> </dl>                 | 主要桌面在裝置上。 針對具有單一顯示配接器的系統，一律會設定此設定。 針對具有多個顯示配接器的系統，只有一部裝置可以有此組。<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**顯示 \_裝置 \_ 可移動**</dt> <dt>32 (0x20)</dt> </dl>                               | 裝置為可移動;它不能是主顯示器。<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**顯示 \_裝置 \_ VGA \_ 相容**</dt> <dt>16 (0x10)</dt> </dl>               | 裝置與 VGA 相容。<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 
</dt> </dl>

目前的重新整理速率（以赫茲為單位）。

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 
</dt> </dl>

目前的水準圖元數目。

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 
</dt> </dl>

目前的垂直圖元數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




