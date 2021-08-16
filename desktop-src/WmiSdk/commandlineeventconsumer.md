---
description: 當事件傳遞給它時，CommandLineEventConsumer 類別會在本機系統中啟動任意進程。
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: CommandLineEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dce5100ba83a04ef2f6252421ec49068e84730141830e7b01f177c81bbac21b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319587"
---
# <a name="commandlineeventconsumer-class"></a>CommandLineEventConsumer 類別

當事件傳遞給它時， **CommandLineEventConsumer** 類別會在本機系統中啟動任意進程。 此類別是 WMI 提供的其中一個標準事件取用者。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

> [!Note]  
> 使用 **CommandLineEventConsumer** 類別時，請保護您想要啟動的可執行檔。 如果可執行檔不在安全的位置，或使用強式存取控制清單來保護 (ACL) ，未經授權的使用者就可以使用惡意可執行檔來取代您的可執行檔。 如需 acl 的詳細資訊，請造訪 Microsoft Windows 軟體開發套件 (SDK) 的安全性一節，並參閱[建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。

 

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a>成員

**CommandLineEventConsumer** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CommandLineEventConsumer** 類別具有這些屬性。

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定要啟動之進程的標準字串範本。 這個屬性可以是 **Null**，而且會使用 **ExecutablePath** 屬性做為命令列。

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

未使用。 如果將值指派給這個屬性，就會產生追蹤訊息。 如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則新的進程是新進程群組的根進程。 進程群組包含此根進程下階的所有進程。 新進程群組的處理序識別碼與此進程識別碼相同。 [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent)方法會使用進程群組來啟用將 Ctrl + C 或 CTRL + BREAK 信號傳送給一組主控台進程。

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，新的進程會在 (VDM) 的私人虛擬 DOS 機器上執行。 只有在啟動在16位 Windows 作業系統上執行的應用程式時，這才有效。 如果設定為 **False**，在16位 Windows 作業系統上執行的所有應用程式都會在單一共用的 VDM 中以執行緒的形式執行。 如需詳細資訊，請參閱本主題的「備註」一節。

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**， [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 方法會在共用虛擬 DOS 機器 (VDM) 中執行新的進程。 如果設定為 **True**，此屬性可以覆寫 Win.ini Windows 區段中的 DefaultSeparateVDM 參數。 如需詳細資訊，請參閱本主題的「備註」一節。

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安全識別碼 (SID) ，可唯一識別建立篩選的使用者。 根據作業系統而定，WMI 會儲存建立 [**\_ \_ EventConsumer**](--eventconsumer.md)實例或系統管理員 SID 之使用者的 SID。 如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**DesktopName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

未使用。 如果將值指派給這個屬性，就會產生追蹤訊息。 如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要執行的模組。 此字串可以指定要執行之模組的完整路徑和檔案名，或者可以指定部分名稱。 如果指定了部分名稱，則會假設為目前的磁片磁碟機和目前的目錄。

**ExecutablePath** 屬性可以是 **Null**。 在此情況下，模組名稱必須是 **CommandLineTemplate** 屬性值中的第一個空白字元分隔標記。 如果使用包含空格的長檔名，請使用加上引號的字串來指出檔案名的結尾，而引數則會開始闡明檔案名。

> [!Note]  
> 因為 **CommandLineTemplate** 屬性可以是要執行的模組所提供的範本，所以 **Null** **ExecutablePath** 屬性會允許在參數中指定的模組執行，然後不在您的控制項中。 一律在 **CommandLineEventConsumer** 註冊中將 **ExecutablePath** 屬性設定為包含必要的可執行檔，以避免事件參數的覆寫。 如果您必須使用範本和變數來指定要執行的模組，請小心將命名空間中的完整寫入權限授與誰。

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定在主控台應用程式中建立新的主控台視窗時的初始文字和背景色彩

</dd> <dt>

**FillAttributes**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

初始文字和背景色彩，如果在主控台應用程式中建立新的主控台視窗。 GUI 應用程式會忽略這個屬性。 值可以是下列值的任何組合。

<dt>

1 (0x1) 
</dt> <dd>

藍色前景

</dd> <dt>

2 (0x2) 
</dt> <dd>

綠色前景

</dd> <dt>

4 (0x4) 
</dt> <dd>

紅色前景

</dd> <dt>

8 (0x8) 
</dt> <dd>

前景濃度

</dd> <dt>

16 (0x10) 
</dt> <dd>

藍色背景

</dd> <dt>

32 (0x20) 
</dt> <dd>

綠色背景

</dd> <dt>

64 (0x40) 
</dt> <dd>

紅色背景

</dd> <dt>

128 (0x80) 
</dt> <dd>

背景濃度

</dd> </dl>

例如，下列組合會在白色背景產生紅色文字：


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  或  


```mof
0x74
```



</dd> <dt>

**ForceOffFeedback**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則會在進程啟動時強制關閉意見反應資料指標。 一般游標隨即顯示。

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則在呼叫 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 之後，資料指標處於意見反應模式兩秒。 在這兩秒鐘內，如果程式進行第一個 GUI 呼叫，系統會在進程中提供五秒鐘的時間。 在這五秒內，如果進程顯示視窗，系統會為程式提供另五秒的時間，以完成視窗繪製。

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

WMI 服務在結束進程 0 (零之前等候的數目（以秒為單位）) 表示不終止進程。 終止進程可防止進程無限期執行。

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。

這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

特定取用者的佇列上限，以位元組為單位。

這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](key-qualifier.md)
</dt> </dl>

取用者的唯一名稱。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

排程進程執行緒的優先權層級。 下列清單列出可用的優先權層級。

<dt>

32 (0x20) 
</dt> <dd>

表示不需要排程的一般處理常式。

</dd> <dt>

64 (0x40) 
</dt> <dd>

指出只有在系統閒置時才會執行執行緒的進程，並由在較高優先順序類別中執行之進程的執行緒佔用。 螢幕保護裝置是一個例子。 閒置優先權類別是由子進程繼承。

</dd> <dt>

128 (0x80) 
</dt> <dd>

表示執行高優先順序、時間關鍵工作的進程。 高優先順序類別進程的執行緒會 shutdown 一般優先順序或閒置優先順序類別進程的執行緒。 其中一個範例就是工作清單，當使用者呼叫時，無論系統的負載為何，都必須快速回應。 使用高優先順序類別時請特別小心，因為具有高優先順序類別的 CPU 系結應用程式可使用幾乎所有可用的迴圈。

</dd> <dt>

256 (0x100)
</dt> <dd>

表示具有最高可能優先順序的進程。 即時優先權類別進程的執行緒會優先處理所有其他進程的執行緒，包括執行重要工作的作業系統進程。 例如，執行超過短暫間隔的即時程式可能會導致磁碟快取無法排清，或導致滑鼠沒有回應。

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則會在互動式 WinStation 中啟動進程。 如果 **為 False**，則會在預設服務 WinStation 中啟動進程。 這個屬性會覆寫 **DesktopName** 屬性。 這個屬性只會在本機使用，而且只有在互動式使用者是設定取用者的相同使用者時才會使用。

從 Windows Vista 開始，執行 **CommandLineEventConsumer** 實例的進程會在 **LocalSystem** 帳戶下啟動，而且會在會話0中啟動。 在會話0中執行的服務無法與使用者會話互動。

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

視窗顯示狀態。 它可以是任何可在 [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數中指定的值。

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則會使用預設的錯誤模式。

</dd> <dt>

**System.windows.controls.page.windowtitle**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

出現在進程標題列上的標題。 GUI 應用程式會忽略這個屬性。

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此進程的工作目錄。

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從畫面的左邊緣到視窗左邊緣的 X 位移（以圖元為單位），如果已建立新視窗。

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果已建立新的主控台視窗，則為字元資料行中的螢幕緩衝區寬度。 GUI 進程會忽略這個屬性。

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

新視窗的寬度（以圖元為單位），如果已建立新視窗。

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以圖元為單位的 Y 位移（以圖元為單位），表示已建立新視窗。

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

螢幕緩衝區高度，在字元資料列中，如果已建立新的主控台視窗。 GUI 進程會忽略這個屬性。

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

新視窗的高度（以圖元為單位），如果已建立新視窗。

</dd> </dl>

## <a name="remarks"></a>備註

**CommandLineEventConsumer** 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。

**CreateSeparateWowVdm** 屬性指出新的進程是否會在 (VDM) 的私人虛擬 DOS 電腦中執行。 另外執行的優點是損毀只會終止單一的 VDM。 在相異 VDMs 中執行的程式會繼續正常運作，而在不同 VDMs 中執行的16位 Windows 應用程式會有不同的輸入佇列。 這表示，如果某個應用程式停止回應，則個別 VDMs 中的應用程式會繼續接收輸入。 另外執行的缺點是，它需要更多的記憶體才能執行這項作業。 只有當使用者要求以16位 Windows 為基礎的應用程式在自己的 VDM 中執行時，才應該將此屬性設定為 **True** 。

> [!Note]  
> **CommandLineEventConsumer** 會在內部使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)方法，並將 **ExecutablePath** 和 **CommandLineTemplate** 屬性作為 *lpApplicationName* 和 *lpCommandLine* 參數傳遞。 下列受控物件格式 (MOF) 程式碼範例不會正確地使用 **CommandLineEventConsumer** 。

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



[**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)方法會將 *lpCommandLine* 傳遞為 `argv[0]` 、 `argv[1]` 等等。 因為 `argv[0]` 針對用來保留可執行檔名稱的16位應用程式，所以先前的 MOF 程式碼會導致建立程式，如同在命令提示字元中輸入下列命令： **c： \\ windows \\ system32 \\cscript.exe param1 param2**。

先前的命令不會成功，因為 Cscript.exe 不會查看 `argv[0]` ，所以無法辨識它不包含自己的名稱，而是其他 ( "c： \\ \\ scripts \\ \\MyScript.js" ) 。 下列範例會識別 **CommandLineEventConsumer** 的建議用法。


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



先前使用的 **CommandLineEventConsumer** 結果是在命令提示字元中輸入下列命令時所建立的進程： **c： \\ windows \\ system32 \\cscript.exe c： \\ scripts \\MyScript.js param1 param2**

因為「c： \\ \\ 腳本 \\ \\MyScript.js」現在已 `argv[1]` Cscript.exe，所以命令會成功。

如需詳細資訊，請參閱 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數。

## <a name="examples"></a>範例

如需使用 **CommandLineEventConsumer** 來建立取用者的範例，請參閱 [根據事件從命令列執行程式](running-a-program-from-the-command-line-based-on-an-event.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ 訂用帳戶<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[標準取用者類別](standard-consumer-classes.md)
</dt> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[建立邏輯取用者](creating-a-logical-consumer.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

