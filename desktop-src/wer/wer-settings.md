---
title: WER 設定
description: 設定來自訂問題報告體驗。 所有這些設定都可以使用群組原則來設定。 您也可以在 [行動中心] 中變更 Windows 7 和 Windows 8 的部分變更。 針對 Windows 10，請使用設定中的搜尋功能來尋找 View advanced 系統設定。
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows 錯誤報告 Windows 錯誤報告，設定
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 4586c4f282cbc5c4e2f683c0764eac048f6c05d22a1972cb0ceb84f9699c7925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442227"
---
# <a name="wer-settings"></a>WER 設定

Windows 錯誤報告 (WER) 提供許多設定來自訂問題報告體驗。 所有這些設定都可以使用群組原則來設定。 您也可以在 [**行動中心**] 中變更 Windows 7 和 Windows 8 的部分變更。 針對 Windows 10，請使用設定中的搜尋功能來尋找 **View advanced 系統設定**。 WER 設定位於下列其中一個登錄子機碼中：

-   **HKEY \_\_** \\  \\ **Microsoft** \\ **Windows** \\ **Windows 錯誤報告** 的目前使用者軟體
-   **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **Windows 錯誤報告**

## <a name="windows-error-reporting-subkey"></a>Windows 錯誤報告子機碼

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>

0-停用資料略過節流。 如果許可已停用或未設定為原則設定，則 WER 預設會節流資料。 如果報表包含相同事件種類的相關資料，則 WER 不會上傳多個 CAB 檔。

</dd> <dd>

1-啟用資料略過節流。 WER 不會對資料進行節流。 WER 會上傳額外的封包檔，其可能包含與先前上傳報表相同之事件種類的相關資料。

</dd> </dl>

是否要啟用 WER 用戶端資料節流的略過

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>1-參數 (預設值 Windows 7) </dd> <dd>2-Windows Vista) 上的所有資料 (預設值</dd> </dl>

是否只封存參數或所有資料

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**同意 \\ DefaultConsent**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>1-一律詢問 (預設) </dd> <dd>2-僅限參數</dd> <dd>3-參數和安全資料</dd> <dd>4-所有資料</dd> </dl>

預設同意選項

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**同意 \\ DefaultOverrideBehavior**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0-垂直同意會覆寫預設的同意 (預設值) </dd> <dd>1-預設同意將覆寫應用程式特定同意</dd> </dl>

預設同意是否覆寫垂直同意

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**同意 \\ \[ VerticalName\]**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>1-一律詢問 (預設) </dd> <dd>2-僅限參數</dd> <dd>3-參數和安全資料</dd> <dd>4-所有資料</dd> </dl>

WER 外掛程式的同意選擇

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**
</dt> <dd>

**REG \_ SZ**

目錄路徑

伺服器上的目標目錄

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**
</dt> <dd>

**REG \_ DWORD**

埠號碼

要與公司伺服器搭配使用的埠號碼

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**
</dt> <dd>

**REG \_ SZ**

伺服器的名稱

公司伺服器名稱

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0-沒有 (預設值) </dd> <dd>1 - 是</dd> </dl>

是否要使用 Windows 整合式驗證

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0-沒有 (預設值) </dd> <dd>1 - 是</dd> </dl>

是否要使用 SSL

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ ExeName \] (\[ 以 .exe 檔案的實際名稱取代 "ExeName \] "，例如 "notepad.exe" )**
</dt> <dd>

**REG \_ DWORD**

可能的值：

<dl> <dd>0-具有可執行映射名稱 **\[ ExeName \]** 的處理常式不需要使用者選擇 [ **Debug** ] 或 [**繼續**] (預設) </dd> <dd>1-具有可執行映射名稱 **\[ ExeName \]** 的處理常式需要使用者選擇 [ **Debug** ] 或 [ **Continue** ]</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* ( " \* " 是常值名稱)**
</dt> <dd>

**REG \_ DWORD**

可能的值：

<dl> <dd>0-在 [設定 **DebugApplications \\ \[ \] ExeName** ] 中明確指定的所有進程都不需要使用者選擇 [ **Debug** ] 或 [**繼續**] (預設值) </dd> <dd>1-在 [設定 **DebugApplications \\ \[ \] ExeName** ] 中明確指定的所有進程都需要使用者選擇 [ **Debug** ] 或 [ **Continue** ]</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0 - 已啟用</dd> <dd>1 - 已停用</dd> </dl>

啟用或停用封存

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>啟用 0 (預設) </dd> <dd>1 - 已停用</dd> </dl>

啟用或停用 WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0 - 已啟用</dd> <dd>1 - 已停用</dd> </dl>

啟用或停用報表佇列

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0-UI (預設) </dd> <dd>1-沒有 UI</dd> </dl>

啟用或停用 WER UI

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0-傳送 (預設值) </dd> <dd>1-不要傳送</dd> </dl>

是否防止傳送第二層資料

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications \\ \[ 應用程式名稱\]**
</dt> <dd>

**REG \_ SZ**

使用 [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

排除的應用程式清單

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0-沒有 (預設值) </dd> <dd>1 - 是</dd> </dl>

是否要將所有報表傳送至使用者的佇列

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\DumpFolder** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ DumpFolder**
</dt> <dd>

**REG \_ EXPAND \_ SZ**

目錄路徑。 預設值為% LOCALAPPDATA% \\ CrashDumps。 如果未使用預設值，則應用程式必須確定資料夾有足夠的 ACL。

**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。 請注意，此行為隨 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 變更。

要儲存傾印檔案的路徑。

請注意，每個進程的設定會覆寫任何存在的全域設定。如需詳細資訊，請參閱 [收集 User-Mode](collecting-user-mode-dumps.md)傾印。

**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\DumpCount** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ DumpCount**
</dt> <dd>

**REG \_ DWORD**

最大數目。 預設值為 10。 當超過最大值時，資料夾中最舊的傾印檔案將會取代為新的傾印檔案。

**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。 請注意，此行為隨著 Windows Server 2008 和 Windows Vista SP1 而變更。

資料夾中傾印檔案的最大數目。

**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\DumpType** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ DumpType**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0-自訂傾印</dd> <dd>1-小型傾印 (預設) </dd> <dd>2-完整傾印</dd> </dl>

**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。 請注意，此行為隨著 Windows Server 2008 和 Windows Vista SP1 而變更。

傾印類型。

**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\CustomDumpFlags** 或 **LocalDumps \\ \[ 應用程式名稱 \] \\ CustomDumpFlags**
</dt> <dd>

**REG \_ DWORD**

小型傾印 [**\_ 類型**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) 列舉中的一或多個值。 預設值為 {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}。

**Windows Vista：** 不支援 **LocalDumps** 機碼下的登錄值。 請注意，此行為隨著 Windows Server 2008 和 Windows Vista SP1 而變更。

要使用的自訂傾印選項。 只有當 **DumpType** 設為0時，才會使用這個值。

**HKEY \_ 目前的 \_ 使用者** 登錄區中不支援此設定。

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**REG \_ DWORD**

可能的值：<dl> <dd>0–已啟用 (預設) </dd> <dd>1–已停用</dd> </dl>

啟用或停用記錄

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**REG \_ DWORD**

可能值的範圍：1–5000。 預設值是 1000。

檔案中封存的大小上限

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**REG \_ DWORD**

可能值的範圍： 1-500。 預設值為 50。

佇列的大小上限

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**REG \_ DWORD**

天數

要檢查解決方案的使用者提醒間隔（以天為單位）

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules！ \[ pwszOutOfProcessCallbackDll 名稱，包括路徑\]**
</dt> <dd>

**REG \_ DWORD**

系統會忽略值的內容。

值的名稱是用來提取 pwszOutOfProcessCallbackDll 值。

**Windows server 2008、Windows Vista Windows server 2003 和 Windows XP：** 不支援這個登錄值。

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>WER 即時核心報表設定

接下來會說明 WER 的即時核心報告設定，兩者都位於下列登錄子機碼底下：

-   **HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **CrashControl**

## <a name="fulllivekernelreports-subkey"></a>FullLiveKernelReports 子機碼

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

每個元件可以建立完整即時傾印的頻率，以小時為單位的閾值 () 。 此值必須大於或等於 **SystemThrottleThreshold**。 將兩者設定為零 (0) 將會停用所有以時間為基礎的節流。 預設值為 168 (7 天) 。

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**REG \_ DWORD**

在任何指定時間可在磁片上的完整即時傾印數目上限。 預設值是 1。 將此值設定為零 (0) 將會停用即時傾印功能。

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**REG \_ QWORD**

[SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ，表示系統或特定 >reporttype 的上次完整即時報告時間。 這是用來計算是否已滿足原則閾值。

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

系統上的任何元件可以建立完整的即時傾印，以小時為單位的閾值 () 。 預設值為 120 (5 天) 。

</dd> </dl>

## <a name="livekernelreports-subkey"></a>LiveKernelReports 子機碼

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**REG \_ SZ**


即時核心報告的重新導向儲存位置。 預設位置為%systemroot%\LiveKernelReports。 此值必須是有效的路徑。 路徑必須是 NT 路徑格式。 例如， \? ？ \c： \LiveDumpsFolder。  如需路徑格式的詳細資訊，請參閱[Windows 系統上的檔案路徑格式](/dotnet/standard/io/file-path-formats)。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WER 參考](wer-reference.md)
</dt> </dl>

 

 
