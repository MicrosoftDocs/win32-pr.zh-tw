---
description: Win32 \_ DesktopWMI 類別代表使用者桌面的一般特性。 使用者可以修改這個類別的屬性，以自訂桌面。
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Win32_Desktop 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c59adebd2fdf3c0727016473e6c347be3af139d539bb007c794eb2aafb4c1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002878"
---
# <a name="win32_desktop-class"></a>Win32 \_ Desktop 類別

**Win32 \_ Desktop**[WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表使用者桌面的一般特性。 使用者可以修改這個類別的屬性，以自訂桌面。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a>成員

**Win32 \_ Desktop** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ Desktop** 類別具有這些屬性。

<dl> <dt>

**BorderWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。DEFAULT \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| BorderWidth ") 
</dt> </dl>

所有具有可調整框線之視窗周圍的框線寬度。

範例：3

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**CoolSwitch**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| CoolSwitch" ) 
</dt> </dl>

開啟快速工作切換。 快速工作切換可讓使用者使用 **ALT + TAB 鍵** 的鍵盤組合在視窗之間切換。

</dd> <dt>

**CursorBlinkRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| CursorBlinkRate" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) 
</dt> </dl>

連續資料指標閃爍之間的時間長度。

範例：530

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

**DragFullWindows**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| DragFullWindows" ) 
</dt> </dl>

當使用者移動視窗時，會顯示視窗的內容。

</dd> <dt>

**GridGranularity**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| GridGranularity" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "8 圖元" ) 
</dt> </dl>

視窗在桌面上系結的格線間距。 這樣可讓您更輕鬆地整理 windows。 間距通常足以讓使用者不會注意到。

範例：1

</dd> <dt>

**IconSpacing**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing ") ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") 
</dt> </dl>

圖示之間的間距。

範例：75

</dd> <dt>

**IconTitleFaceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。DEFAULT \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| IconFont ") 
</dt> </dl>

圖示名稱所使用的字型。

範例： "MS San Serif"

</dd> <dt>

**IconTitleSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 字型 and Text 結構 \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "point" ) 
</dt> </dl>

圖示的字型大小。

範例：9

</dd> <dt>

**IconTitleWrap**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。DEFAULT \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap ") 
</dt> </dl>

圖示的標題文字會換行至下一行。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

識別目前桌面設定檔的名稱。

範例： "MainProf"

</dd> <dt>

**模式**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ 桌面 \| 模式」 ) 
</dt> </dl>

用來做為桌面背景的模式名稱。

</dd> <dt>

**ScreenSaverActive**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| ScreenSaveActive ") 
</dt> </dl>

螢幕保護裝置正在使用中。

</dd> <dt>

**ScreenSaverExecutable**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ 桌面 \|SCRNSAVE.EXE」 ) 
</dt> </dl>

目前螢幕保護裝置可執行檔的名稱。

範例：「登入。.SCR

</dd> <dt>

**ScreenSaverSecure**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| ScreenSaverIsSecure ") 
</dt> </dl>

啟用螢幕保護裝置的密碼。

</dd> <dt>

**ScreenSaverTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| ScreenSaveTimeOut ") ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" seconds ") 
</dt> </dl>

螢幕保護裝置啟動前經過的時間量。

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**桌布**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ 桌面 \| 壁紙」 ) 
</dt> </dl>

桌面背景上的壁紙設計檔案名。

範例： "WINNT.BMP"

</dd> <dt>

**WallpaperStretched**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| WallpaperStyle ") 
</dt> </dl>

背景圖樣會伸展以填滿整個畫面。 Microsoft Plus 必須先安裝，才能使用此選項。 如果 **為 FALSE**，則壁紙會在桌面背景保留其原始尺寸。

</dd> <dt>

**WallpaperTiled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| TileWallpaper ") 
</dt> </dl>

背景圖樣或置中對齊。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ Desktop** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

使用這個類別的呼叫進程必須在登錄所在的電腦上具有 **SE \_ RESTORE \_ NAME** 許可權。 例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。 如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。

## <a name="examples"></a>範例

下列程式碼範例說明如何取出桌面資訊。


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
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

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

