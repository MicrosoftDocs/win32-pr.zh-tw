---
description: Win32 \_ ProcessStartup abstract WMI 類別代表以 Windows 為基礎之進程的啟動設定。
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Win32_ProcessStartup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10b0732b89d5240b457152f4bd19f951f69b8ee693baec54daea3bd6bbba9439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759348"
---
# <a name="win32_processstartup-class"></a>Win32 \_ ProcessStartup 類別

**Win32 \_ ProcessStartup** abstract [WMI 類別](../wmisdk/retrieving-a-class.md)代表以 Windows 為基礎之進程的啟動設定。 類別定義為方法類型定義，這表示它只會用來將資訊傳遞給 [**Win32 \_ 進程**](win32-process.md)類別的 [**Create**](create-method-in-class-win32-process.md)方法。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a>成員

**Win32 \_ ProcessStartup** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ProcessStartup** 類別具有這些屬性。

<dl> <dt>

**CreateFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒函數 \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags" ) 
</dt> </dl>

控制優先權類別和建立進程的其他值。 您可以依照任何組合來指定下列建立值（如所述）。

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug \_進程** (1) 


</dt> <dd>

如果設定此旗標，則會將呼叫進程視為偵錯工具，並正在調試新的進程。 系統會向偵錯工具通知在正在進行的進程中發生的所有偵錯工具事件。

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug \_只有 \_ 這個 \_ 進程** (2) 


</dt> <dd>

如果未設定此旗標，而且正在調試呼叫進程，新進程會成為另一個正在進行調試的進程。 如果呼叫進程不是正在進行調試的進程，就不會發生任何與偵錯工具相關的動作。

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**建立 \_已暫** 止 (4) 


</dt> <dd>

新進程的主要執行緒是以暫停狀態建立的，而且在呼叫 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 方法之前，不會執行。

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>卸 **離 \_進程** (8) 


</dt> <dd>

針對主控台進程，新進程無法存取父進程的主控台。 如果已設定 [ **建立 \_ 新的 \_ 主控台** ] 旗標，則無法使用此旗標。

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**建立 \_ (\_** 16) 的新主控台


</dt> <dd>

這個新的進程有新的主控台，而不是繼承父主控台。 此旗標不可與卸 **離的 \_ 進程** 旗標一起使用。

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**建立 \_新的 \_ 進程 \_ 群組** (512) 


</dt> <dd>

這個新的程式是新進程群組的根進程。 進程群組包含此根進程下階的所有進程。 新進程群組的處理序識別碼與 [**Win32 \_ 進程**](win32-process.md)類別的 **ProcessID** 屬性中所傳回的進程識別碼相同。 [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent)方法會使用進程群組來啟用將 Ctrl + C 信號或 CTRL + BREAK 信號傳送給一組主控台進程的作業。

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**建立 \_Unicode \_ 環境** (1024) 


</dt> <dd>

**EnvironmentVariables** 屬性中所列的環境設定會使用 Unicode 字元。 如果未設定此旗標，則環境區塊會使用 ANSI 字元。

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**建立 \_預設 \_ 錯誤 \_ 模式** (67108864) 


</dt> <dd>

新建立的進程會獲得呼叫進程的系統預設錯誤模式，而不是繼承父進程的錯誤模式。 此旗標適用于在停用硬性錯誤的情況下執行的多執行緒 shell 應用程式。

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**建立 \_\_從 \_ 作業** (16777216) BREAKAWAY


</dt> <dd>

用來建立的進程不會受到工作物件的限制。

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HKEY \_ 目前的 \_ 使用者 \\ \\ 環境" ) 
</dt> </dl>

電腦設定的設定清單。 環境變數會指定檔案的搜尋路徑、暫存檔的目錄、應用程式特定的選項，以及其他類似的資訊。 系統會維護每個使用者的環境設定區塊，以及一部電腦的環境設定。 系統內容區塊代表特定電腦之所有使用者的環境變數。 使用者的環境區塊代表系統為特定使用者維護的環境變數，並包含系統內容變數集。 根據預設，每個進程都會收到其父進程的環境區塊複本。 一般來說，這是登入之使用者的環境區塊。 進程可以針對其子進程指定不同的環境區塊。

</dd> <dt>

**ErrorMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Error 函數 \| SetErrorMode" ) 
</dt> </dl>

在某些非 x86 處理器上，未對齊的記憶體參考會導致對齊錯誤例外狀況。 沒有旗標的 **\_ 對齊 \_ 錯誤 \_** （旗標）可讓您控制作業系統是否自動修正這類對齊錯誤，或讓應用程式看得到它們。 在每秒數百萬個指令 (MIPS) 平臺上，應用程式必須明確地呼叫 [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) ，但 **不含 \_ 對齊 \_ 錯誤 \_** ，因為旗標會讓作業系統自動修正對齊錯誤。

作業系統處理數種嚴重錯誤類型的方式。 您可以指定作業系統進程錯誤，或應用程式可以接收和處理錯誤。

預設設定是讓作業系統能夠看見應用程式的對齊錯誤。 因為 x86 平臺不會讓應用程式看見對齊錯誤，所以旗標 **除了旗標 \_ \_ \_ 以外** ，不會造成作業系統引發對齊錯誤的錯誤，即使未設定旗標。 [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)的預設狀態是將所有旗標設定為 0 (零) 。

<dt>



 (1)


</dt> <dd>

預設

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**失敗 \_嚴重 \_ 錯誤** (2) 


</dt> <dd>

如果設定此旗標，當發生這類錯誤時，作業系統不會顯示 [重大錯誤處理常式] 訊息方塊。 相反地，作業系統會將錯誤傳送到呼叫的進程。

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**否 \_ (4) \_ \_ 以外的對齊錯誤**


</dt> <dd>

如果設定此旗標，作業系統會自動修正記憶體對齊錯誤，並讓應用程式看不到這些錯誤。 它會針對呼叫和子系進程執行此工作。 此旗標適用于精簡的指令集運算 (RISC) ，而且對 x86 處理器沒有任何影響。

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**否 \_GP \_ 錯誤 \_ \_** 方塊 (8) 


</dt> <dd>

如果設定此旗標，作業系統不會在發生 GP 錯誤時， (GP) 錯誤訊息框中顯示一般保護。 此旗標只能透過可處理 GP 錯誤的應用程式來設定。

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**否 \_開啟 \_ 檔案 \_ 錯誤 \_** 方塊 (16) 


</dt> <dd>

如果設定此旗標，作業系統不會在找不到檔案時顯示訊息方塊。 相反地，錯誤會傳回給呼叫的進程。 目前忽略此旗標。

</dd> </dl>

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute" ) 
</dt> </dl>

如果在主控台應用程式中建立新的主控台視窗，則為文字和背景色彩。 這些值會在圖形化使用者介面中忽略， (GUI) 應用程式。 若要同時指定前景和背景色彩，請將值相加。 例如，若要在藍色背景上 (4) 的紅色類型 (16) ，請將 FillAttribute 設定為20。

<dt>

1
</dt> <dd>

前景 \_ 藍色

</dd> <dt>

2
</dt> <dd>

前景 \_ 綠色

</dd> <dt>

4
</dt> <dd>

前景 \_ 紅色

</dd> <dt>

8
</dt> <dd>

前景 \_ 濃度

</dd> <dt>

16
</dt> <dd>

背景 \_ 藍色

</dd> <dt>

32
</dt> <dd>

背景 \_ 綠色

</dd> <dt>

64
</dt> <dd>

背景 \_ 紅色

</dd> <dt>

128
</dt> <dd>

背景 \_ 濃度

</dd> </dl>

</dd> <dt>

**PriorityClass**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| [**JOBOBJECT \_ 基本 \_ 限制 \_ 資訊**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass」 ) 
</dt> </dl>

新進程的 Priority 類別。 您可以使用這個屬性來判斷進程中線程的排程優先權。 如果屬性是空的，除非建立進程的 priority 類別處於閒置或低於正常狀態，否則優先權類別會預設為 [正常] \_ 。 在這些情況下，子進程會接收呼叫進程的預設優先權類別。

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (32) 


</dt> <dd>

表示不需要特殊排程的一般進程。

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**閒置** (64) 


</dt> <dd>

表示只有當系統閒置時才會執行的進程，並由在較高優先順序類別中執行之進程的執行緒佔用。 螢幕保護裝置是一個例子。 閒置優先權類別是由子進程繼承。

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (128) 


</dt> <dd>

表示執行必須立即執行才能正確執行之時間關鍵工作的進程。 高優先順序類別進程的執行緒會優先處理一般優先順序或閒置優先順序類別進程的執行緒。 其中一個範例是 Windows 工作清單，當使用者呼叫時，無論作業系統上的負載為何，都必須快速回應。 使用高優先順序類別時請特別小心，因為高優先順序類別的 CPU 系結應用程式幾乎可以使用所有可用的迴圈。 只有設定為此層級的即時優先權 shutdown 執行緒。

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**即時** (256) 


</dt> <dd>

表示具有最高可能優先順序的進程。 即時優先權類別進程的執行緒會優先處理所有其他進程的執行緒，包括執行重要工作的高優先順序執行緒和作業系統進程。 例如，執行超過一小段時間間隔的即時程式可能會導致磁碟快取無法排清，或造成滑鼠沒有回應。

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**以下 \_一般** (16384) 


</dt> <dd>

表示優先順序高於閒置但低於正常的進程。

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**以上 \_一般** (32768) 


</dt> <dd>

表示優先順序高於正常但低於高的進程。

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow" ) 
</dt> </dl>

視窗顯示給使用者的方式。 它可以是任何可在 [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數中指定的值。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle" ) 
</dt> </dl>

建立新的主控台視窗時，標題列中顯示的文字;用於主控台進程。 如果是 **Null**，就會使用可執行檔的名稱做為視窗標題。 如果 GUI 或主控台進程未建立新的主控台視窗，此屬性必須是 **Null** 。

</dd> <dt>

**WinstationDesktop**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop" ) 
</dt> </dl>

電腦的名稱或桌上型電腦和視窗的名稱。 字串中的反斜線表示字串同時包含桌面和視窗工作站名稱。 如果 **WinstationDesktop** 為 **Null**，則新的進程會繼承其父進程的桌面和視窗工作站。 如果 **WinstationDesktop** 是空字串，進程就不會繼承其父進程的桌面和視窗。 系統會決定是否必須建立新的桌面和視窗工作站。 視窗工作站是安全的物件，其中包含剪貼簿、一組全域原子，以及一組桌面物件。 指派給互動式使用者登入會話的互動式視窗工作站也包含鍵盤、滑鼠和顯示裝置。 桌面是包含在視窗工作站內的安全物件。 桌面具有邏輯顯示介面，並且包含視窗、功能表和勾點。 視窗工作站可以有多個桌面。 只有互動式視窗工作站的桌面可以看見，並接收使用者輸入。

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX" ) 
</dt> </dl>

視窗左上角的 X 位移（如果建立新視窗）（以圖元為單位）。 位移是從畫面的左上角。 若是 GUI 進程，當 **CreateWindow** 的 *X* 參數是 **CW \_ USEDEFAULT** 時，新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)來建立重迭的視窗時，就會使用指定的位置。

> \[!附注 X\]  
> 和 **Y** 不能獨立指定。

 

</dd> <dt>

**XCountChars**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars" ) 
</dt> </dl>

字元資料行中的螢幕緩衝區寬度。 這個屬性會用於建立主控台視窗的進程，而且在 GUI 進程中會被忽略。

> [!Note]  
> **XCountChars** 和 **YCountChars** 不能獨立指定。

 

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize" ) 
</dt> </dl>

視窗的圖元寬度（如果已建立新視窗）。 若是 GUI 進程，只有在新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 來建立重迭的視窗時，才會使用此程式，如果 **CreateWindow** 的 nWidth 參數是 **CW \_ USEDEFAULT**。

> [!Note]  
> **XSize** 和 **YSize** 不能獨立指定。

 

</dd> <dt>

**Y**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY" ) 
</dt> </dl>

當建立新視窗時，視窗左上角的圖元位移。 位移是從畫面的左上角。 若是 GUI 進程，當 **CreateWindow** 的 *y* 參數是 **CW \_ USEDEFAULT** 時，新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)來建立重迭的視窗時，就會使用指定的位置。

> \[!附注 X\]  
> 和 **Y** 不能獨立指定。

 

</dd> <dt>

**YCountChars**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars" ) 
</dt> </dl>

字元資料列中的螢幕緩衝區高度。 這個屬性會用於建立主控台視窗的進程，但是 GUI 進程會忽略此屬性。

> [!Note]  
> **XCountChars** 和 **YCountChars** 不能獨立指定。

 

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize" ) 
</dt> </dl>

如果建立新視窗，則為視窗的圖元高度。 若是 GUI 進程，只有在新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)來建立重 **迭的視窗** 時，才會使用此程式，如果 *nWidth* 參數是 **CW \_ USEDEFAULT**。

> [!Note]  
> **XSize** 和 **YSize** 不能獨立指定。

 

</dd> </dl>

## <a name="remarks"></a>備註

這個類別衍生自 [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md)。

概觀

[**Win32 \_ Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md)方法可讓您針對在電腦上執行的任何新進程設定啟動選項。 例如，您可以設定一個進程，讓它從「隱藏」視窗開始，以防止使用者看到，也可能會中斷。 如果進程是在命令視窗中執行，您可以設定視窗的大小、標題和前景和背景色彩。

啟動選項是使用 **Win32 \_ ProcessStartup** 類別來設定。 **Win32 \_ProcessStartup** 是方法類型類別;方法類型類別僅存在於將資訊傳遞給方法。 在此情況下， **win32 \_ ProcessStartup** 實例的所有屬性都會傳遞給 [**win32 \_ 進程**](win32-process.md)的實例。

**使用 Win32 \_ ProcessStartup**

1.  建立 **Win32 \_ ProcessStartup** 的實例。
2.  設定新實例的屬性。
3.  將此實例包含為 [**Win32 \_ 進程**](win32-process.md) Create 方法的一部分。

例如，如果您已建立名為 objConfig 的 **Win32 \_ ProcessStartup** 實例，則會在 Create 方法中傳遞物件名稱，如下所示：

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>範例

您可以使用 **Win32 \_ ProcessStartup** 類別來設定進程的各種啟動選項。 這些選項包括（但不限於）在隱藏視窗中建立進程，以及建立更高優先順序的程式等事項。 下列 VBScript 會在隱藏視窗中建立處理常式。


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



下列 VBScript 會建立較高優先順序的進程。


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



下列 VBScript 程式碼範例會在本機電腦上建立記事本進程。 **Win32 \_ProcessStartup** 用來設定處理常式設定。


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
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

[**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> <dt>

[**Win32 \_ 進程**](win32-process.md)
</dt> <dt>

[**\_\_ProviderHostQuotaConfiguration**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[WMI 工作：進程](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
