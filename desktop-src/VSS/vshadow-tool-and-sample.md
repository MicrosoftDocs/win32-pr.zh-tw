---
description: VShadow 是一種命令列工具，可讓您用來建立和管理磁片區陰影複製。
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: VShadow 工具和範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469100"
---
# <a name="vshadow-tool-and-sample"></a>VShadow 工具和範例

VShadow 是一種命令列工具，可讓您用來建立和管理磁片區陰影複製。

> [!Note]  
> VShadow 隨附于適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 。 VSS 7.2 SDK 包含的 VShadow 版本只會在 Windows Server 2003 上執行。 如需下載 Windows SDK 和 VSS 7.2 SDK 的詳細資訊，請參閱 [磁碟區陰影複製服務](volume-shadow-copy-service-portal.md)。

 

VShadow 工具會使用命令列選項和選擇性旗標來識別要執行的工作。 使用時若沒有任何命令列選項，VShadow 命令會建立新的陰影複製集。

VShadow 命令會執行下列作業：

-   [建立陰影複製集](#creating-a-shadow-copy-set)
-   [匯入陰影複製集](#importing-a-shadow-copy-set)
-   [查詢陰影複製屬性](#querying-shadow-copy-properties)
-   [刪除陰影複製](#deleting-shadow-copies)
-   [中斷陰影複製集](#breaking-a-shadow-copy-set)
-   [使用 BreakSnapshotSetEx 方法中斷陰影複製集](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [在本機公開陰影複製](#exposing-a-shadow-copy-locally)
-   [遠端公開陰影複製](#exposing-a-shadow-copy-remotely)
-   [列出寫入器狀態和中繼資料](#listing-writer-status-and-metadata)
-   [執行還原作業](#performing-restore-operations)
-   [還原為先前的陰影複製](#reverting-to-a-previous-shadow-copy)
-   [重新同步處理 Lun](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>建立陰影複製集

**vshadow** \[OptionalFlags \] *VolumeList*

此命令會建立新的陰影複製集。

*VolumeList* 是磁片區名稱的清單。 VShadow 會為清單中的每個磁片區建立一個陰影複製。 您可以選擇性地以反斜線 () 來終止磁片區名稱 \\ 。 例如，C：和 C： \\ 都是有效的磁片區名稱。 您也可以指定裝載的資料夾 (例如，C： \\ DirectoryName) 或磁片區 GUID 名稱 (例如 \\ \\ ？ \\磁片區 {edbed95e-7e8d-11d8-9d01-505054503030} ) 。

*OptionalFlags* 是下表中選擇性旗標值的位元遮罩。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>選擇性旗標值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br/></td>
<td>此選擇性旗標指定差異硬體陰影複製。 此旗標和 <strong>-ap</strong> 旗標互斥。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong><br/></td>
<td>此選擇性旗標指定了 plex 硬體陰影複製。 此旗標和 <strong>-ad</strong> 旗標彼此互斥。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-bc =</strong><em>File</em><strong>.xml</strong><br/></td>
<td>這個選擇性旗標會指定不可傳送的陰影複製，並將備份元件檔儲存到指定的檔案中。 此檔案可用於後續的還原作業。 此旗標和 <strong>-t</strong> 旗標互斥。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>命令</em><br/></td>
<td>這個選擇性旗標會在建立陰影複製之後，但在 VShadow 工具結束之前，執行命令或腳本。 <em>命令</em> 可以指定可執行檔 shell 命令或 CMD 檔。 如果指定了 shell 命令，就不能指定任何命令參數。<br/>
<blockquote>
[!Note]<br />
為了安全起見，並讓執行保持簡單， <strong>-exec</strong> 選擇性旗標不會接受將參數傳遞給命令或腳本。 傳遞至 <strong>-exec</strong> 選擇性旗標的整個字串會被視為單一的 CMD 或 EXE 檔案。 如需這項限制的詳細資訊，請參閱 VShadow 原始程式碼。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>這個選擇性旗標會指定只有在可以還原所有磁片簽章時，才會完成陰影複製作業。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/> <strong>Windows Server 2003：</strong> 不支援。<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong><br/></td>
<td>此選擇性旗標指定當陰影複製集中斷時，應該從電腦遮罩陰影複製 Lun。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/> <strong>Windows Server 2003：</strong> 不支援。<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong><br/></td>
<td>這個選擇性旗標會指定不含自動復原的陰影複製。 如需此選項的詳細資訊，請參閱 <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> 列舉之 VSS_VOLSNAP_ATTR_NO_AUTORECOVERY 旗標的檔。<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br/></td>
<td>這個選擇性旗標指定不應復原磁碟簽章。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/> <strong>Windows Server 2003：</strong> 不支援。<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong><br/></td>
<td>這個選擇性旗標會指定陰影複製，而不涉及寫入器。 如需不含寫入器參與之陰影複製的詳細資訊，請參閱 <a href="shadow-copy-creation-details.md">陰影複製建立詳細資料</a>。 此旗標和 <strong>-wi-fi</strong> 和 <strong>-wx</strong> 旗標互斥。<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>這個選擇性旗標會指定 <a href="vssgloss-p.md"><em>持續性陰影複製</em></a>。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong><br/></td>
<td>此選擇性旗標指定當陰影複製集中斷時，應該將陰影複製 Lun 設為讀取/寫入。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/> <strong>Windows Server 2003：</strong> 不支援。<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>這個選擇性旗標會指定 <a href="vssgloss-c.md"><em>用戶端可存取的陰影複製</em></a>。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em></em><strong>.cmd</strong><br/></td>
<td>這個選擇性旗標會產生 CMD 檔案，其中包含與建立的陰影複製相關的環境變數，例如陰影複製識別碼和陰影複製集識別碼。<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>.xml</strong><br/></td>
<td>這個選擇性旗標會指定可轉移的陰影複製，並將備份元件檔儲存到 <em>File.xml</em> 參數所指定的檔案中。 此檔案可用於後續的匯入和/或還原作業。 此旗標和 <strong>-bc</strong> 旗標彼此互斥。<br/> <strong>Windows server 2003、Standard edition 和 Windows server 2003、Web edition：</strong> 不支援可轉移的陰影複製。 所有版本的 Windows Server 2003 Service Pack 1 (SP1) 支援可轉移的陰影複製。<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong><br/></td>
<td>這個選擇性旗標會指定在建立陰影複製時應該強制執行 TxF 復原。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援此旗標。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-追蹤</strong><br/></td>
<td>這個選擇性旗標會產生可用於疑難排解的詳細資訊輸出。<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong><br/></td>
<td>此選擇性旗標會在結束之前，讓 VShadow 工具等候使用者確認。<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi-fi =</strong><em>寫入器</em><br/></td>
<td>這個選擇性旗標會驗證指定的寫入器或元件是否包含在陰影複製中。 <em>寫入器</em> 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。 此旗標和 <strong>-nw</strong> 旗標互斥。<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx =</strong><em>Writer</em><br/></td>
<td>這個選擇性旗標會驗證指定的寫入器或元件是否已從陰影複製中排除。 <em>寫入器</em> 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。 此旗標和 <strong>-nw</strong> 旗標互斥。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>匯入陰影複製集

**vshadow** \[OptionalFlags \] **-i =**_File_*_.xml_*

**-I** 命令列選項會匯入可轉移的陰影複製集。

> [!Note]  
> 只有在 Windows server 作業系統上才支援此命令列選項。

 

*File.xml* 檔必須是以 **-t** 或 **-bc** 選擇性旗標建立之可轉移陰影複製集的備份元件檔檔。

如果是以 **-p** 選擇性旗標建立的陰影複製集，則為 [*持續陰影複製*](vssgloss-p.md)。 如果可轉移的陰影複製集為非持續性，則會在執行陰影複製建立命令時短暫出現，並在命令傳回時自動刪除。 您只能在建立陰影複製時匯入非持續性陰影複製，方法是使用 **-exec** 選擇性旗標建立陰影複製集，以執行 **呼叫 VShadow 的** CMD 檔。

**-I** 命令列選項不能與其他命令列選項結合。

*OptionalFlags* 是下表中選擇性旗標值的位元遮罩。



| 選擇性旗標值                                                                                                            | Description                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_命令_<br/> | 這個選擇性旗標會在匯入陰影複製之後，但在 VShadow 工具結束之前，執行命令或腳本。 *命令* 可以指定可執行檔 shell 命令或 CMD 檔。 如果指定了 shell 命令，就不能指定任何命令參數。<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-追蹤**<br/>                                                  | 這個選擇性旗標會產生可用於疑難排解的詳細資訊輸出。<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-wait**<br/>                                                           | 此選擇性旗標會在結束之前，讓 VShadow 工具等候使用者確認。<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>查詢陰影複製屬性

**vshadow** **-q**

**vshadow** **-qx =**_ShadowCopySetId_

**vshadow** **-s =**_ShadowCopyId_

**-Q** 命令列選項會列出電腦上所有陰影複製的屬性。

**-Qx** 命令列選項會列出陰影複製集中所有陰影複製的屬性，其識別碼是由 *ShadowCopySetId* 所指定。

**-S** 命令列選項會列出 *SHADOWCOPYID* 指定其識別碼的陰影複製屬性。

這些命令列選項使用 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) 和 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) 的組合來取得指定陰影複製集的屬性。

**-Q**、 **-qx** 和 **-s** 命令列選項都是互斥的，且無法與其他命令列選項結合。

## <a name="deleting-shadow-copies"></a>刪除陰影複製

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-dx =**_ShadowCopySetId_

**vshadow** **-ds =**_ShadowCopyId_

**-Da** 命令會刪除電腦上的所有陰影複製。

> [!Note]  
> **-Da** 命令列選項需要使用者確認。

 

**-Do** 命令列選項會刪除電腦上最舊的陰影複製。

**-Dx** 命令列選項會刪除陰影複製集中的所有陰影複製，其識別碼是由 *ShadowCopySetId* 所指定。

**-Ds** 命令列選項會刪除 *SHADOWCOPYID* 指定其識別碼的陰影複製。

這些命令列選項僅適用于持續性 [*陰影複製*](vssgloss-p.md) 。 非持續性陰影複製不需要明確刪除，因為它們會在 VShadow 建立命令結束時自動刪除。

**-Da**、 **-do**、 **-dx** 和 **-ds** 命令列選項都是互斥的，且無法與其他命令列選項結合。

## <a name="breaking-a-shadow-copy-set"></a>中斷陰影複製集

**vshadow** **-b =**_ShadowCopySetId_

**vshadow** **-bw =**_ShadowCopySetId_

**-B =**_ShadowCopySetId_ 命令列選項會將陰影複製集中的每個陰影複製轉換成獨立唯讀磁片區。

**-Bw =**_ShadowCopySetId_ 命令列選項會將陰影複製集中的每個陰影複製轉換成獨立的可寫入磁片區。

> [!Note]  
> 只有在 Windows server 作業系統上才支援 **-b** 和 **-bw** 命令列選項。

 

如需有關中斷陰影複製集的詳細資訊，請參閱 [中斷陰影](breaking-shadow-copies.md)複製。

陰影複製組中斷之後，陰影複製組和個別的陰影複製就不存在，而且無法使用 VSS 命令來管理。

如果是使用 **-p** 選擇性旗標建立陰影複製集，則其為持續性。 如果可轉移的陰影複製集為非持續性，則會在執行陰影複製建立命令時短暫出現，並在命令傳回時自動刪除。 您只能在建立陰影複製時中斷非持續性陰影複製集，方法是使用 **-exec** 選擇性旗標建立陰影複製集，以執行呼叫 **vshadow** **-b** 或 **vshadow** **bw** 的 CMD 檔。

**-B** 和 **-bw** 命令列選項互斥，而且無法與其他命令列選項結合。

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>使用 BreakSnapshotSetEx 方法中斷陰影複製集

**vshadow** **-bex**

**-Bex** 命令列選項會根據選擇性 **遮罩**、 **-rw**、 **-forcerevert** 和 **-norevert** 旗標所指定的選項來中斷陰影複製集。 此命令列選項類似于 **-b** 和 **-bw** 命令列選項。 **-Bex** 命令列選項會使用 [**IVssBackupComponentsEx2：： BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)方法，而 **-b** 和 **-bw** 命令列選項則使用 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)方法。

如需有關中斷陰影複製集的詳細資訊，請參閱 [中斷陰影](breaking-shadow-copies.md)複製。

> [!Note]  
> 只有在 Windows server 作業系統上才支援 **-bex** 命令列選項。

 

**vshadow** **-bex** **-mask**

**遮罩** 旗標指定將從主機遮罩陰影複製 LUN。 如果指定 **-mask** 旗標，則無法指定 **-rw**、 **-forcerevert** 和 **-norevert** 旗標。

**vshadow** **-bex** **-rw**

**-Rw** 旗標指定將陰影複製 LUN 公開給主機，作為讀取/寫入磁片區。

**vshadow** **-bex** **-forcerevert**

**-Forcerevert** 旗標會指定所有陰影複製 lun 的磁片識別碼都會還原為原始 lun 的磁片識別碼。 但是，如果有任何原始 Lun 存在於系統上，此作業將會失敗，而且不會還原任何識別碼。 此旗標和 **-norevert** 旗標互斥。

**vshadow** **-bex** **-norevert**

**-Norevert** 旗標指定不會還原任何陰影複製 LUN 磁片識別碼。 此旗標和 **-forcerevert** 旗標互斥。

## <a name="exposing-a-shadow-copy-locally"></a>在本機公開陰影複製

**vshadow** **-el =**_ShadowCopyId_*_、_*_LocalEmptyDirectory_

 **vshadow** **-el =**_ShadowCopyId_*_、_*_UnusedDriveLetter_

**-El** 命令列選項會將掛接的資料夾或磁碟機號指派給持續性陰影複製。 請注意，除非您後續呼叫 **vshadow** **-bw** 來中斷陰影複製集，否則磁片區內容將維持唯讀狀態。

> [!Note]  
> 無法在本機公開非持續性陰影複製和 [*用戶端可存取的陰影複製*](vssgloss-c.md) 。

 

例如，如果 {edbed95e-7e8d-11d8-9d01-505054503030} 是現有持續性陰影複製的 GUID，而 X：是未使用的磁碟機號，則下列命令會在 X 下公開陰影複製：

**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}，x：**

下列範例示範如何在裝載的資料夾 C： ShadowCopies June23 下公開相同的陰影 \\ 複製 \\ ：

**mkdir c： \\ ShadowCopies \\ June23**

**vshadow** **-el = {edbed95e-7e8d-11d8-9d01-505054503030}，c： \\ ShadowCopies \\ June23**

**-El** 命令列選項不能與其他命令列選項結合。

## <a name="exposing-a-shadow-copy-remotely"></a>遠端公開陰影複製

**vshadow** **-er =**_ShadowCopyId_*_，_*_UnusedShareName_

 **vshadow** **-er =**_ShadowCopyId_*_、_*_UnusedShareName_*_、_*_PathFromRootOnShadow_

**-Er** 命令列選項會將唯讀共用名稱指派給根目錄 (或從陰影複製) 子目錄。 請注意，除非您後續呼叫 **vshadow** **-bw** 來中斷陰影複製集，否則共用內容將維持唯讀狀態。

> [!Note]  
> [*用戶端可存取的陰影複製*](vssgloss-c.md) 無法從遠端公開。

 

例如，如果 {edbed95e-7e8d-11d8-9d01-505054503030} 是現有持續性陰影複製的 GUID，而共用 \_ 123 是未使用的共用名稱，則下列命令會公開共用123底下的陰影複製 \_ ：

**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}，共用 \_ 123**

下列範例示範如何只在相同的共用下，公開名稱為 "Folder1 \\ Folder2" ) 的子樹 (的相同陰影複製：

**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}，Share \_ 123，Folder1 \\ Folder2**

**-Er** 命令列選項不能與其他命令列選項結合。

## <a name="listing-writer-status-and-metadata"></a>列出寫入器狀態和中繼資料

**vshadow** **-ws**

**vshadow** **-wm**

**vshadow** **-wm2-downloadbtn**

**vshadow** **-wm3**

**-Ws** 命令列選項會列舉目前正在電腦上執行的 VSS 寫入器，並說明其狀態。 此命令相當於 [Vssadmin list 寫入](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) 器命令。 有六個可能的狀態值：穩定、失敗、未知、等待凍結、凍結，以及等待完成。

**-Wm** 命令列選項會列出寫入器中繼資料的摘要，包括受影響的磁片區。

**-Wm2-downloadbtn** 命令列選項會列出所有寫入器中繼資料。

**-Wm3** 命令列選項會以原始 XML 格式列出所有寫入器中繼資料。

**Windows Vista 和 Windows Server 2003：** 不支援 **-wm3** 命令列選項。

您可以使用這項資訊來判斷要包含在磁片區陰影複製集中的磁片區。

> [!Note]  
> 如果寫入器狀態為穩定或等候完成，寫入器可視為處於穩定狀態，可供下一次備份之用。

 

**-Ws**、 **-wm**、 **-wm2-downloadbtn** 和 **-wm3** 命令列選項都是互斥的，且無法與其他命令列選項結合。

## <a name="performing-restore-operations"></a>執行還原作業

**vshadow** \[OptionalFlags \] **-r =**_File_*_.xml_*

**vshadow** \[OptionalFlags \] **-rs =**_File_*_.xml_*

**-R** 命令列選項會執行還原作業。

**-Rs** 命令列選項會執行模擬的還原作業。

*File.xml* 檔案必須是使用 **-t** 或 **-bc** 選擇性旗標所建立的陰影複製集的備份元件檔檔。

**-R** 和 **-rs** 命令列選項互斥，而且無法與其他命令列選項結合。

*OptionalFlags* 是下表中選擇性旗標值的位元遮罩。



| 選擇性旗標值                                                                                                            | Description                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi-fi =**_寫入器_<br/>             | 這個選擇性旗標會驗證指定的寫入器或元件是否包含在還原中。 *寫入器* 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx =**_Writer_<br/>             | 這個選擇性旗標會驗證指定的寫入器或元件是否排除在還原之外。 *寫入器* 可以指定元件路徑、寫入器名稱、寫入器識別碼或寫入器實例識別碼。<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_命令_<br/> | 這個選擇性旗標會在傳送至寫入器的還原前和還原後事件之間執行命令或腳本。 *命令* 可以指定可執行檔 shell 命令或 CMD 檔。 如果指定了 shell 命令，就不能指定任何命令參數。<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-追蹤**<br/>                                                  | 這個選擇性旗標會產生可用於疑難排解的詳細資訊輸出。<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>還原為先前的陰影複製

**vshadow** **-revert =**_ShadowCopyId_

> [!Note]  
> 只有在 Windows server 作業系統上才支援此命令列選項。

 

**Windows server 2008 和 Windows server 2003：** 不支援。

**-Revert** 命令列選項會將磁片區還原為先前的陰影複製，其識別碼是由 *ShadowCopyId* 所指定。

**-Revert** 命令列選項不能與其他命令列選項結合。

## <a name="resynchronizing-luns"></a>重新同步處理 Lun

**vshadow** **-addresync =**_ShadowCopyId_ **-resync =**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync =**_ShadowCopyId_*_，_* *TargetVolumeDriveLetter* **-resync =**_BCDFileName_ \[ OptionalResyncFlags\]

**-Addresync** 命令列選項會指定要包含在 LUN 重新同步作業中的磁片區。 *ShadowCopyId* 參數會指定陰影複製的識別碼。 選擇性的 *TargetVolumeDriveLetter* 參數會指定要複製陰影複製磁片區內容的目的地磁片區。

**-Resync** 命令列選項會起始 LUN 重新同步作業。 作業完成之後，每個目標 LUN 的簽章應與目標磁片區 LUN 的簽章相同。 *BCDFileName* 參數會指定包含備份元件檔的 XML 檔案名。

> [!Note]  
> 只有在 Windows server 作業系統上才支援 **-addresync** 和 **-resync** 命令列選項。

 

**Windows server 2008 和 Windows server 2003：** 不支援。

*OptionalResyncFlags* 是下表中選擇性旗標值的位元遮罩。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>選擇性旗標值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong><br/></td>
<td>此選擇性旗標指定在作業完成之後，每個目標 LUN 的簽章應與用來建立陰影複製的原始 LUN 相同，而不是目標磁片區 LUN。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援 <strong>-revertsig</strong> 旗標。
</blockquote>
<br/> <strong>Windows server 2008 和 Windows server 2003：</strong> 不支援。<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>此選擇性旗標指定 VSS 服務不應該檢查 LUN 重新同步作業將覆寫的未選取磁片區。<br/>
<blockquote>
[!Note]<br />
只有在 Windows server 作業系統上才支援 <strong>-novolcheck</strong> 旗標。
</blockquote>
<br/> <strong>Windows server 2008 和 Windows server 2003：</strong> 不支援。<br/></td>
</tr>
</tbody>
</table>



 

 

 
