---
description: Win32 \_ PRINTERCONFIGURATION WMI 類別代表印表機裝置的設定。 這包括解析度、色彩、字型和方向等功能。
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Win32_PrinterConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936417"
---
# <a name="win32_printerconfiguration-class"></a>Win32 \_ PrinterConfiguration 類別

**Win32 \_ PrinterConfiguration** [WMI 類別](../wmisdk/retrieving-a-class.md)代表印表機裝置的設定。 這包括解析度、色彩、字型和方向等功能。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a>成員

**Win32 \_ PrinterConfiguration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PrinterConfiguration** 類別具有這些屬性。

<dl> <dt>

**BitsPerPel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

用來表示此設定中之色彩的位數， (每圖元) 的位數。 這個屬性已經過時。 相反地，請使用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) 類別中的屬性來判斷如何表示色彩。

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

**自動分頁**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則應該將列印的頁面分頁。 若要進行 collate，請在列印下一個複本之前列印出整份檔，而不是列印出檔的每個頁面所需的次數。

除非印表機驅動程式表示支援定序，否則會忽略這個屬性。

</dd> <dt>

**色彩**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

檔的色彩。 有些彩色印表機可以使用 true 黑色來列印，而不是使用青色、洋紅和黃色 (CMY) 的組合。 這通常會為檔建立深色且更清晰的文字。 此選項僅適用于支援真黑色列印的彩色印表機。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

單色 (true 黑色) 

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

Color

</dd> </dl>

</dd> <dt>

**份數**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要列印的份數。 印表機驅動程式必須支援列印多頁複製。

範例：2

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

**DeviceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

印表機的易記名稱。 此名稱對印表機的類型而言是唯一的，而且可能因為其衍生來源之字串的限制而遭到截斷。

範例： "PCL/HP LaserJet"

</dd> <dt>

**DisplayFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出顯示裝置為彩色或單色，以及掃描的類型是 noninterlaced 或交錯式。 這個屬性已經過時。 相反地，請使用顯示內容，例如 **Win32 \_ DesktopMonitor** 類別的 **DisplayType** 屬性。

</dd> <dt>

**DisplayFrequency**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

顯示垂直的重新整理頻率。 監視器的重新整理頻率是每秒重繪螢幕 (頻率) 的次數。 這個屬性已經過時。 請改為使用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) 類別中的屬性。

</dd> <dt>

**DitherType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

印表機的遞色類型。 這個屬性可以假設預先定義的值為1到5，或從6到256的驅動程式定義值。 線條藝術遞色是一種特殊的遞色方法，可在黑色、白色和灰色 scalings 之間產生定義完善的框線。 它不適用於包含濃度和色調（如掃描的相片）中連續 graduations 的影像。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

無遞色

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

粗略筆刷

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

精細筆刷

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**億**


</dt> <dd>

線狀圖

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**.5**


</dt> <dd>

灰階

</dd> </dl>

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以 Windows 為基礎的印表機驅動程式的版本號碼。 版本號碼是由驅動程式製造商建立和維護。

</dd> <dt>

**雙工**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會在兩端進行列印。 若 **為 FALSE**，則只會在媒體的一端進行列印。

</dd> <dt>

**FormName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

不支援。

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：每英寸 [**單位**](../wmisdk/standard-qualifiers.md) (每英寸的點數) 
</dt> </dl>

列印工作的 X 軸 (寬度) 的列印解析度以點為單位， (類似于過時的 **XResolution** 屬性) 。 只有當這個類別的 **PrintQuality** 屬性是正數時，才會設定這個值。

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

有三種可能的色彩比對方法的特定值 (稱為意圖) ，預設應該使用。 ICM 應用程式使用 ICM 函數來建立意圖。 這個屬性可以假設預先定義的值為1到3，或從4到256的驅動程式定義值。 非 ICM 應用程式可以使用此值來判斷印表機處理彩色列印工作的方式。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

飽和度

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

這個

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

確切色彩

</dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

處理 ICM 的方式。 若為非 ICM 應用程式，這個屬性會決定 ICM 是啟用或停用。 針對 ICM 應用程式，系統會檢查這個屬性，以判斷電腦系統中哪一部分處理 ICM 支援。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Disabled

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

Windows

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

設備磁碟機

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**億**


</dt> <dd>

裝置

</dd> </dl>

</dd> <dt>

**LogPixels**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

每個邏輯英寸的圖元數。 此過時的屬性僅適用于使用圖元的裝置，這會排除印表機之類的裝置。 沒有適用于印表機的取代值。

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

印表機列印的媒體類型。 屬性可以設定為預先定義的值，或是大於或等於256的驅動程式定義值。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

標準

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

透明度

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

光澤

</dd> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/standard-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

與此設定相關聯的印表機名稱。 這個值符合相關聯的 [**Win32 \_ 印表機**](win32-printer.md)實例的 **Name** 屬性。

</dd> <dt>

**Orientation**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列印紙張的方向。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

直向

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

橫向

</dd> </dl>

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (十分之一毫米) 
</dt> </dl>

紙張的長度。 若要以英寸為單位判斷紙張大小，請將此值除以254。

範例：2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

紙張大小。 可能的大小可在相關聯的 [**Win32 \_ 印表機**](win32-printer.md)類別的 **PaperSizesSupported** 屬性中找到。

範例：「A4 或字母」。

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (十分之一毫米) 
</dt> </dl>

紙張的寬度。 若要以英寸為單位判斷紙張大小，請將此值除以254。

範例：2159

</dd> <dt>

**PelsHeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

不支援這個屬性。

</dd> <dt>

**PelsWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

不支援這個屬性。

</dd> <dt>

**PrintQuality**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列印工作的四個品質等級之一。 如果指定了正值，則會以每英寸的點來測量品質。

<dt>

<span id="-1"></span>

<span id="-1"></span>**-1**


</dt> <dd>

草稿

</dd> <dt>

<span id="-2"></span>

<span id="-2"></span>**-2.png**


</dt> <dd>

低

</dd> <dt>

<span id="-3"></span>

<span id="-3"></span>**-3**


</dt> <dd>

中

</dd> <dt>

<span id="-4"></span>

<span id="-4"></span>**-4**


</dt> <dd>

高

</dd> </dl>

</dd> <dt>

**縮放**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (百分比) 
</dt> </dl>

要調整列印輸出的依據因數。 例如，縮放比例75可將列印輸出縮減為3/4 的原始高度和寬度。

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

**SpecificationVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與以 Windows 為基礎的印表機相關聯之裝置的初始化資料版本號碼。

</dd> <dt>

**TTOption**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出如何列印 TrueType 字型。

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**點陣圖** (1) 


</dt> <dd>

將 TrueType 字型列印為圖形。 這是點陣印表機的預設動作。

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**下載** (2) 


</dt> <dd>

以軟字型下載 TrueType 字型。 這是使用印表機控制語言 (PCL) 印表機的預設動作。

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**替代** (3) 


</dt> <dd>

替代 TrueType 字型的裝置字型。 這是 PostScript 印表機的預設動作。

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：每英寸 [**單位**](../wmisdk/standard-qualifiers.md) (每英寸的點數) 
</dt> </dl>

沿著 y 軸列印解析度 (列印工作的高度)  (類似于過時的 **YResolution** 屬性) 。 只有當這個類別的 **PrintQuality** 屬性是正數時，才會設定這個值。

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

這個屬性已經過時。 請改用 **HorizontalResolution** 屬性。

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

這個屬性已經過時。 請改用 **VerticalResolution** 屬性。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PrinterConfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

**概觀**

您必須先深入瞭解這些資源，才能判斷如何以最佳方式散發和使用您的列印資源。 例如，部門 A 可能只有三個印表機，相較于部門 B 中的五部印表機。但是，如果部門 A 的印表機可以列印每分鐘20頁，而部門 B 中的印表機每分鐘只能列印5個頁面，則部門 A 中的使用者實際上會有更多列印容量。 若未知道這些印表機的詳細功能，您可能會誤結論該部門 A 的列印容量很短，因此購買的其他印表機最後將無法使用。

WMI 包含兩個類別： [**Win32 \_ 印表機**](win32-printer.md) 和 **win32 \_ PrinterConfiguration**，可用來傳回電腦上所安裝之所有印表機的詳細資訊。

## <a name="examples"></a>範例

下列程式碼範例會抓取印表機資訊。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



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

[**CIM \_ 設定**](./cim-setting.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
