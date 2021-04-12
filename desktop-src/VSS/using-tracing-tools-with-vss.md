---
description: 若要收集 VSS 基礎結構的追蹤資訊，您可以使用 VssTrace 工具、Logman 工具或 Tracelog.exe 工具。
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: 使用追蹤工具搭配 VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191364"
---
# <a name="using-tracing-tools-with-vss"></a>使用追蹤工具搭配 VSS

若要收集 VSS 基礎結構的追蹤資訊，您可以使用 VssTrace 工具、Logman 工具或 Tracelog.exe 工具。 VssTrace 可在 Microsoft Windows 軟體開發套件 (SDK) 中取得，而且可用來在 Windows 7 和更新版本的 Windows 作業系統上追蹤 VSS 應用程式。 Logman 是追蹤事件和效能計數器的追蹤控制器;它也可以用來在 Windows 7 和更新版本的 Windows 作業系統上追蹤 VSS 應用程式。 Tracelog.exe 包含在 Windows 驅動程式套件 (WDK) 中。

若要使用追蹤工具搭配 [自動化系統復原 (asr) ](using-vss-automated-system-recovery-for-disaster-recovery.md)，請參閱搭配 [Asr 應用程式使用追蹤工具](using-tracing-tools-with-vss-asr-applications.md)。

> [!Note]  
> VssTrace、Logman 和 Tracelog.exe 都需要系統管理員許可權。

 

如需每個工具的相關資訊，請參閱下列各節：

-   [使用 VssTrace](#using-vsstrace)
    -   [VssTrace Command-Line 選項](#vsstrace-command-line-options)
-   [使用 Logman](#using-logman)
-   [使用 Tracelog.exe](#using-tracelog)

## <a name="using-vsstrace"></a>使用 VssTrace

若要從命令列執行 VssTrace 工具，請使用下列語法：

**vsstrace** *命令列選項*

若要顯示 VssTrace 工具的簡潔命令列說明，請使用下列語法：

**vsstrace-說明**

若要顯示 VssTrace 工具的詳細命令列說明，請使用下列語法：

**vsstrace-全部協助**

### <a name="vsstrace-command-line-options"></a>VssTrace Command-Line 選項

VssTrace 工具會使用下列命令列選項：

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *旗標*
</dt> <dd>

啟用旗 *標* 位元遮罩所指定之旗標的模組。 每個旗標都對應至一個 VSS 模組。 如果 *旗標* 為零，則不會啟用任何模組。 請注意，大部分的模組預設都會啟用。 這個選項可以與 **+** _模組_ 選項結合。 例如， **vsstrace-f 0 + WRITER + COORD** 會停用依預設啟用的所有模組的追蹤，並啟用 VSS 寫入器和 vss 服務的追蹤。 另外， **vsstrace + f 0XFFFF COORD** 也可以追蹤所有模組，但 VSS 服務除外。

> [!Note]  
> 如果您搭配使用 **-f** 選項與 **+** _模組_ 選項， **-f** 必須出現在 **+** _模組_ 選項之前。

 

下表列出每個可用模組的模組名稱和旗標。

| 模組 | 旗標       | 預設已啟用 | 追蹤的專案                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Yes                | C + + 例外狀況處理。                                                                                                                       |
| COORD  | 0x00000002 | Yes                | VSS 服務，也稱為 VSS 協調器。                                                                                    |
| SWPRV  | 0x00000004 | Yes                | VSS 系統陰影複製提供者服務。                                                                                                  |
| BUCOMP | 0x00000008 | Yes                | VSS 要求者和備份元資料處理。                                                                                             |
| WRITER | 0x00000010 | Yes                | VSS 寫入器作業和 VSS 託管的寫入器，例如 Windows 登錄寫入器。                                             |
| VSSAPI | 0x00000020 | Yes                | VSSAPI.DLL 匯出的 VSS API 的其他函式。                                                                                |
| HWDIAG | 0x00000040 | Yes                | VSS 硬體提供者基礎結構和操作。                                                                                          |
| ADMIN  | 0x00000080 | Yes                | VSS 命令列公用程式，例如 VSSADMIN.EXE 和 DISKSHADOW.EXE。                                                                           |
| VSSUI  | 0x00000100 | Yes                | 共用資料夾陰影複製設定使用者介面 (UI) 。 UI 僅適用于 Windows Server 作業系統。         |
| TEST   | 0x00000200 | Yes                | 不適用。  (此追蹤模組已保留。 )                                                                                             |
| IOCTL  | 0x00000400 | Yes                | VSS 服務藉由呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式所起始的 FSCTL 和 IOCTL 作業詳細資料。 |
| 根    | 0x00000800 | Yes                | 一般 VSS 公用程式函式，例如配置器、字串類別以及登錄和磁片區作業。                                        |
| WRXML  | 0x00001000 | No                 | 寫入器中繼資料的 XML 處理。 此課程模組的雜訊程度非常高。                                                               |
| VSSXML | 0x00002000 | No                 | XML 處理基類。 此課程模組的雜訊程度非常高。                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_模組_
</dt> <dd>

啟用 *模組* 指定的模組。 一次只能啟用一個以上的模組。 若要列出可用的模組，請在命令列提示字元中輸入 **vsstrace – help 模組** 。

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_模組_
</dt> <dd>

停用 *模組* 所指定的模組。 若要列出可用的模組，請在命令列提示字元中輸入 **vsstrace – help 模組** 。

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ pid** *ProcessId*
</dt> <dd>

啟用 *ProcessId* 所指定的進程。 若要啟用所有處理常式，請使用 " \* " 作為 *ProcessId* 的值。 一次可以指定一個以上的 **pid** 選項。 選項的順序會決定要啟用或停用的進程。 例如，若只要啟用其處理序識別碼為0xe8c 的進程，請使用 **vsstrace-pid \* + pid 0xe8c**。

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*
</dt> <dd>

停用 *ProcessId* 所指定的進程。 若要停用所有進程，請使用 " \* " 作為 *ProcessId* 的值。 一次可以指定一個以上的 **pid** 選項。 選項的順序會決定要啟用或停用的進程。 例如，若要停用進程識別碼為0xe8c 的進程以外的所有進程，請使用 **vsstrace-pid \* + pid 0xe8c**。

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ tid** *ThreadId*
</dt> <dd>

啟用 *ThreadId* 所指定的執行緒。 若要啟用所有線程，請使用 " \* " 作為 *ThreadId* 的值。 一次可以指定一個以上的 **tid** 選項。 選項的順序會決定哪些執行緒已啟用或停用。 例如，若只要啟用其處理序識別碼為0x31a 的執行緒，請使用 **vsstrace-tid \* + tid 0x31a**。

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*
</dt> <dd>

停用 *ThreadId* 指定的執行緒。 若要停用所有線程，請使用 " \* " 作為 *ThreadId* 的值。 一次可以指定一個以上的 **tid** 選項。 選項的順序會決定哪些執行緒已啟用或停用。 例如，若要停用進程識別碼為0x31a 之執行緒以外的所有線程，請使用 **vsstrace-tid \* + tid 0x31a**。

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *層級*
</dt> <dd>

使用 *層級* 所指定的追蹤層級。 層級愈高，追蹤輸出越詳細越好。 每個層級都包含所有較低的層級。 預設層級為170。 可用的層級如下。



| 層級 | 追蹤輸出中包含的資訊 |
|-------|------------------------------------------|
| 000   | 無                                     |
| 020   | 嚴重錯誤                             |
| 030   | 未處理的例外狀況                     |
| 040   | Errors                                   |
| 050   | 判斷提示                               |
| 060   | 警告                                 |
| 080   | 例外狀況處理                       |
| 100   | 事件記錄檔活動                       |
| 120   | 一般資訊                      |
| 140   | 程式碼流程                                |
| 160   | 函數 enter 和 exit                  |
| 170   | 函數傳回值                   |
| 180   | 函數參數 (簡易)               |
| 190   | 函數參數 (詳細資訊)             |
| 200   | 詳細資訊層級1              |
| 210   | 詳細資訊層級2              |
| 220   | 詳細資訊層級3              |
| 230   | 快速程式碼層級1                        |
| 240   | 快速程式碼層級2                        |
| 250   | 快速程式碼層級3                        |
| 255   | 全部                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+ 縮排**
</dt> <dd>

在每個函式和子界限上縮排格式化的追蹤輸出。

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**-縮排**
</dt> <dd>

請勿縮排格式化的追蹤輸出。

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*
</dt> <dd>

將 *EtlFile* 所指定的 Logman 輸出檔轉換為可讀取的文字格式。

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*
</dt> <dd>

將追蹤資訊儲存至 *OutputFile* 所指定的輸出檔案。 為了達到最佳效能，輸出檔案應該位於不屬於陰影複製的磁片區上。

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*
</dt> <dd>

顯示 *HelpOption* 所指定的命令列說明。 有效的 *HelpOption* 值為 **模組**、 **層級** 和 **全部**。 指定 **模組** 會導致列出模組。 指定 **層級** 會列出可用的層級。 指定 [ **全部** ] 會顯示詳細的說明。 如果未使用任何選項，則會顯示簡潔的說明。

</dd> </dl>

## <a name="using-logman"></a>使用 Logman

下列程式說明如何搭配使用 Logman 與 VSS 應用程式。

**搭配使用 Logman 與 VSS 應用程式**

1.  使用下列命令來開始追蹤：

    **logman 啟動 vss-o** *x： \\ * * * ets-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170**

    > [!Note]  
    > 以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。

     

2.  使用下列命令停止追蹤：

    **logman 停止 vss-ets**

追蹤記錄檔為 *x： \\*.vss。

如需 Logman 工具的詳細資訊，請參閱 [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11))。

## <a name="using-tracelog"></a>使用 Tracelog.exe

下列程式說明如何使用 Tracelog.exe。

**使用 Tracelog.exe**

1.  建立名為 .vss 的文字檔，其中只包含下列文字：

    **9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**

2.  使用下列命令來開始追蹤：

    **tracelog.exe-啟動 vss-f** *x： \\ * * * .vss-guid .vss-旗標 0xff-level 0xaa**

    > [!Note]  
    > 以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。

     

3.  使用下列命令停止追蹤：

    **tracelog.exe-停止 vss**

追蹤記錄檔為 *x： \\*.vss。

如需 Tracelog.exe 工具的詳細資訊，請參閱 [tracelog.exe](https://msdn.microsoft.com/library/ms797927.aspx)。

 

 
