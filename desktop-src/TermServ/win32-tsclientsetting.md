---
title: Win32_TSClientSetting 類別
description: 定義與 \_ 連接原則相關的 Win32 終端機類別的設定。
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Win32_TSClientSetting 類別遠端桌面服務
- Win32_TSClientSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff3e4eb9d99288914fb6d4e9a6e2d22aa38689cdc6b60f227e7e5ba2e0c5323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349362"
---
# <a name="win32_tsclientsetting-class"></a>Win32 \_ TSClientSetting 類別

**Win32 \_ TSClientSetting** WMI 類別會定義與連接原則相關的 [**win32 \_ 終端**](win32-terminal.md)機類別的設定。

下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。 如需方法的參考資訊，請參閱本主題稍後的方法表格。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a>成員

**Win32 \_ TSClientSetting** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSClientSetting** 類別具有這些方法。



| 方法                                                                   | 描述                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | 設定這個類別的 **ConnectClientDrivesAtLogon**、 **ConnectPrinterAtLogon** 和 **DefaultToClientPrinter** 屬性。<br/>                      |
| [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md)                 | 不支援。<br/> **Windows 7 和 Windows Server 2008 R2：** 設定 **AllowDwm** 屬性。<br/>                                               |
| [**SetClientProperty**](win32-tsclientsetting-setclientproperty.md)     | 設定 **LPTPortMapping**、 **COMPortMapping**、 **AudioMapping**、 **ClipboardMapping**、 **DriveMapping** 或 **WindowsPrinterMapping** 屬性。<br/> |
| [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md)             | 設定 **ColorDepth** 屬性。<br/>                                                                                                                 |
| [**SetColorDepthPolicy**](win32-tsclientsetting-setcolordepthpolicy.md) | 設定 **ColorDepthPolicy** 屬性。<br/>                                                                                                           |
| [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md)           | 設定 **MaxMonitors** 屬性。<br/>                                                                                                                |
| [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md)     | 設定 **MaxXResolution** 屬性。<br/>                                                                                                             |
| [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md)     | 設定 **MaxYResolution** 屬性。<br/>                                                                                                             |



 

### <a name="properties"></a>屬性

**Win32 \_ TSClientSetting** 類別具有這些屬性。

<dl> <dt>

**AdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否啟用 RemoteApp 的 advanced RemoteFX 圖形。

**Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：** 在 Windows Server 2012 R2 和 Windows 8.1 之前，無法使用此屬性。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

已停用 Advanced graphics。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

已啟用先進的圖形。

</dd> </dl>

</dd> <dt>

**AllowDwm**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

無法使用這個屬性。

* * Windows 7 和 Windows Server 2008 R2： * *

指定是否要啟用或停用遠端桌面組合。 零會停用遠端桌面組合，而非零值會啟用它。

您可以使用 [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) 方法來修改此屬性。

</dd> <dt>

**AudioCaptureRedir**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否允許音訊捕獲重新導向。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0) 


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**AudioMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否停用或啟用音訊對應。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

音訊對應已啟用。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

音訊對應已停用。

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否偏好 AVC444 模式。

**Windows 8.1、Windows Server 2012 r2、Windows 8、Windows Server 2012、Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 10 或 Windows Server 2016 之前無法使用。

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0) 


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

簡短描述 (物件的單行字串) 。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ClipboardMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否停用或啟用剪貼簿對應。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

剪貼簿對應已啟用。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

剪貼簿對應已停用。

</dd> </dl>

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定色彩深度。 如需可能的值，請參閱 [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) 方法。

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8 位** (1) 


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 位** (2) 


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16 位** (3) 


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24 位** (4) 


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**32 位** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ColorDepthPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否要覆寫使用者的最大色彩設定。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

請勿覆寫使用者的原則。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

覆寫使用者的原則。

</dd> </dl>

</dd> <dt>

**COMPortMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 COM 埠對應是否已停用或啟用。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

已啟用 COM 埠對應。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

COM 埠對應已停用。

</dd> </dl>

</dd> <dt>

**ConnectClientDrivesAtLogon**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定在登入程式期間，是否會自動連接用戶端的磁片磁碟機。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

磁片磁碟機將不會自動連線。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

磁片磁碟機將會自動連接。

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器用來取得使用者連接設定的原則。

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) 


</dt> <dd>

使用者的連接設定有效。

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**伺服器-覆寫** (1) 


</dt> <dd>

伺服器會覆寫使用者的連接設定。

</dd> </dl>

</dd> <dt>

**ConnectPrinterAtLogon**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定在登入程式期間，用戶端的所有對應本機印表機是否會自動連接。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

本機印表機不會自動連線。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

本機印表機會自動連接。

</dd> </dl>

</dd> <dt>

**DefaultToClientPrinter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定列印工作是否會自動傳送至用戶端的本機印表機。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

列印工作不會自動傳送至用戶端的本機印表機。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

列印工作會自動傳送至用戶端的本機印表機。

</dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DriveMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否停用或啟用磁片磁碟機對應。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

磁片磁碟機對應已啟用。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

磁片磁碟機對應已停用。

</dd> </dl>

</dd> <dt>

**EncodeImageQuality**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 RDP 體驗的影像品質。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

無 **失真 (1**) 


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**高** (2) 


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**中型** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 RD 工作階段主機伺服器是否使用硬體圖形轉譯器作為預設介面卡。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0) 


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") 
</dt> </dl>

物件的安裝日期。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**LPTPortMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否停用或啟用 LPT 埠對應。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

啟用了 LPT 埠對應。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

已停用 LPT 埠對應。

</dd> </dl>

</dd> <dt>

**MaxMonitors**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

伺服器支援的監視器數目上限。 您可以使用 [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) 方法來修改此屬性。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

</dd> <dt>

**MaxXResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

伺服器支援的最大 X 解析度。 您可以使用 [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) 方法來修改此屬性。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

</dd> <dt>

**MaxYResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

伺服器支援的最大 Y 解析度。 您可以使用 [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) 方法來修改此屬性。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**PNPRedirection**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否允許隨插即用重新導向。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

允許隨插即用重新導向。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

不允許隨插即用重新導向。

</dd> </dl>

</dd> <dt>

**PolicyAdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否由伺服器或群組原則設定 **AdvancedRemoteAppGraphics** 屬性。

**Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：** 在 Windows Server 2012 R2 和 Windows 8.1 之前，無法使用此屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceAllowDwm**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

無法使用這個屬性。

* * Windows 7 和 Windows Server 2008 R2： * *

指出是否由伺服器或群組原則設定 **AllowDwm** 屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceAudioCaptureRedir**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否由伺服器或群組原則設定 **AudioCaptureRedir** 屬性。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceAudioMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **AudioMapping** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceAvc444ModePreferred**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出如何設定 **AVC444ModePreferredis** 屬性。

**Windows 8.1、Windows Server 2012 r2、Windows 8、Windows Server 2012、Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 10 或 Windows Server 2016 之前無法使用。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceClipboardMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **ClipboardMapping** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **ColorDepth** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepthPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **ColorDepthPolicy** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceCOMPortMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **COMPortMapping** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceDefaultToClientPrinter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **DefaultToClientPrinter** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceDriveMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **DriveMapping** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceEncodeImageQuality**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出如何設定 **EncodeImageQualityi** 。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceHardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出如何設定 **HardwareGraphicsAdapter** 。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceLPTPortMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **LPTPortMapping** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceMaxMonitors**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **MaxMonitors** 屬性是由伺服器、群組原則或預設值所設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

</dd> <dt>

**PolicySourceMaxResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **MaxXResolution** 和 **MaxYResolution** 屬性是否由伺服器、群組原則或預設值所設定。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourcePNPRedirection**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **PNPRedirection** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceRemoteSessionProfile**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出如何設定 **RemoteSessionProfile** 。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceSelectNetworkDetect**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出屬性 **SelectNetworkDetect** 的設定方式。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceSelectTransport**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出屬性 **SelectTransport** 的設定方式。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceVideoPlaybackRedir**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否由伺服器或群組原則設定 **VideoPlaybackRedir** 屬性。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceWindowsPrinterMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **WindowsPrinterMapping** 屬性是由伺服器、群組原則或預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**RemoteSessionProfile**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 RDP 體驗的設定檔。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

<span id="scale"></span><span id="SCALE"></span>

**調整** (1) 


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

**體驗** (2) 


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**頻寬** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SelectNetworkDetect**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否使用網路偵測。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

0
</dt> <dd>

在連線時間和穩定狀態中使用。

</dd> <dt>

1
</dt> <dd>

在連線時間停用

</dd> <dt>

2
</dt> <dd>

在穩定狀態中停用

</dd> <dt>

3
</dt> <dd>

在連線時間和穩定狀態中停用。

</dd> </dl>

</dd> <dt>

**SelectTransport**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定可使用哪些傳輸通訊協定來進行伺服器的 RDP 存取。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。

<dt>

0
</dt> <dd>

使用 UDP 和 TCP。

</dd> <dt>

1
</dt> <dd>

僅使用 TCP。

</dd> <dt>

2
</dt> <dd>

請使用 UDP 或 TCP。

</dd> </dl>

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

<dt>



  ( [確定] ) 


</dt> <dd></dd> <dt>



  ( 「錯誤」 ) 


</dt> <dd></dd> <dt>



  ( 「降級」 ) 


</dt> <dd></dd> <dt>



  ( 「未知」 ) 


</dt> <dd></dd> <dt>



  ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>



  ( 「開始」 ) 


</dt> <dd></dd> <dt>



  ( 「正在停止」 ) 


</dt> <dd></dd> <dt>



  ( "Service" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

終端機的名稱。

這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。

</dd> <dt>

**VideoPlaybackRedir**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否允許播放影片重新導向。

**Windows Server 2008 和 Windows Vista：** Windows Server 2008 R2 和 Windows 7 之前，無法使用此屬性。

<dt>

<span id="FALSE"></span><span id="false"></span>

**FALSE** (0) 


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**TRUE** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**WindowsPrinterMapping**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否停用或啟用用戶端視窗的印表機對應。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

印表機對應已啟用。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

印表機對應已停用。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

請注意，與主控台會話相關聯的視窗工作站無法存取此類別的方法和屬性。 如果嘗試將 "Console" 指定為 **TerminalName** 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。 如果視窗工作站嘗試呼叫此物件的方法來新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，也會傳回此錯誤碼。

若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。 針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。 針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為六。

下列 Visual Basic 腳本撰寫版 (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 終端機**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**CIM \_ 設定**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

