---
description: Win32 \_ VideoConfiguration 類別不在使用中。 因為沒有支援的提供者，所以它不會傳回任何實例。
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Win32_VideoConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510460"
---
# <a name="win32_videoconfiguration-class"></a>Win32 \_ VideoConfiguration 類別

**Win32 \_ VideoConfiguration** 類別不在使用中。 因為沒有支援的提供者，所以它不會傳回任何實例。

**Win32 \_ VideoConfiguration** 類別代表影片子系統的設定。 這個類別已被取代，以取代 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)和 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) 類別中包含的屬性

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>成員

**Win32 \_ VideoConfiguration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ VideoConfiguration** 類別具有這些屬性。

<dl> <dt>

**ActualColorResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API 裝置內容函式 \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每個圖元的位」 ) 
</dt> </dl>

表示影片顯示的目前色彩深度。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**AdapterChipType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| ChipType" ) 
</dt> </dl>

包含介面卡晶片的名稱。

範例： s3

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)、 [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

指定介面卡製造商的名稱。 此名稱可用來比較此裝置的相容性與電腦系統的需求。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| DACType" ) 
</dt> </dl>

指出介面卡中使用的數位到類比晶片 (DAC) 的名稱。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**AdapterDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

包含視訊卡的描述或描述性名稱。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Info \| VideoMemory" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

表示視訊卡的記憶體大小。

範例：16777216

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| 硬體 \\ \\ 描述 \\ \\ 系統 \\ \\ DisplayController \\ \\ 0 \\ \\ 識別碼」 ) 
</dt> </dl>

表示視訊卡的類型。

字元集：英數位元

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL" ) 
</dt> </dl>

指出代表顯示的每個圖元的實際位數。 這可能會調整為目前的影片設定 (由使用者的 ActualColorResolution 屬性) 表示。

範例：8

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**ColorPlanes**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API 裝置內容函式 \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| 平面」 ) 
</dt> </dl>

指出影片顯示中使用的目前色彩平面數目。 色彩平面是代表圖元色彩的另一種方式;色彩平面會將圖形分隔為每個主要色彩元件 (紅色綠色的) ，並將其儲存在自己的平面中，而不是將單一 RGB 值指派給每個圖元。 這允許在8和16位的影片系統上有更高的色彩深度。 呈現圖形系統的 bitwidth 夠大，足以儲存色彩深度資訊，因此只需要一個色彩平面。

範例：1

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS" ) 
</dt> </dl>

表示影片顯示色彩表中的色彩索引數目。 如果裝置的色彩深度小於每圖元8位，則會使用此屬性。 如果裝置具有較高的色彩深度，則會傳回-1。

範例：256

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS" ) 
</dt> </dl>

指出目前的裝置特定畫筆數目。 0xFFFFFFFF 的值表示裝置不支援畫筆。 畫筆用來繪製多邊形物件的線條和 theborders。

範例：3

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| DriverDate" ) 
</dt> </dl>

指出目前的視頻驅動程式安裝日期和時間。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES" ) 
</dt> </dl>

以水準方向指出目前的圖元數目 (X 軸的顯示) 。

範例：1024

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfPath" ) 
</dt> </dl>

指定視頻驅動程式 .inf 檔案的路徑。

範例： C： \\ Windows \\ System32 \\ 驅動程式

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection" ) 
</dt> </dl>

指出 Win32 影片資訊所在之 .inf 檔案的區段。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Defaule \| winspool.drv" ) 
</dt> </dl>

表示已安裝的視頻驅動程式名稱。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**MonitorManufacturer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

指出顯示裝置的製造商名稱。

範例： NEC

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**監視類型**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| 硬體 \\ \\ 描述 \\ \\ 系統 \\ \\ MonitorPeripheral \\ \\ 0 \| 識別碼」 ) 
</dt> </dl>

指出顯示裝置的型號名稱。

範例： NEC 5FGp

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)、 [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

包含 video configuration 類別的識別名稱。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**PixelsPerXLogicalInch**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX" ) 
</dt> </dl>

指出沿著 X 軸的每個邏輯英寸的圖元數 (水準方向) 顯示。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**PixelsPerYLogicalInch**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY" ) 
</dt> </dl>

指出沿著 Y 軸的每個邏輯英寸的圖元數， (垂直方向) 顯示。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH" ) 
</dt> </dl>

指出影片設定的更新頻率。 0或1值表示正在使用預設費率。

範例：72

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. 交錯" ) 
</dt> </dl>

指出顯示裝置是否為交錯式。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**非交錯** 式 ( 「非交錯」 ) 


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

**交錯** 式 ( 「交錯」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫米" ) 
</dt> </dl>

指定實體畫面的高度。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**ScreenWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫米" ) 
</dt> </dl>

指定實體畫面的寬度。

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE" ) 
</dt> </dl>

表示保留給系統使用的目前色彩索引項目數目。 此值僅適用于使用索引調色板的顯示設定。 索引的調色板不會用於每圖元8位以上的色彩深度。 如果色彩深度超過每圖元8位，此值會設為 **Null**。

範例：20

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES" ) 
</dt> </dl>

指出垂直方向中目前的圖元數目 (Y 軸的顯示) 。

範例：768

這個屬性已被取代，以改用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md) 和//或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)中所包含的對應屬性 (s) 。

</dd> </dl>

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

[**CIM \_ 設定**](cim-setting.md)
</dt> </dl>

 

 
