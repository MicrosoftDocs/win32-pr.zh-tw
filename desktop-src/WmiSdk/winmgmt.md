---
description: Winmgmt 是在 &0034 下執行的 SVCHOST 進程內的 WMI 服務 \# ;LocalSystem&\# 0034; 帳戶。
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: winmgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: d28d37faf454accd91281034d0aeb8df5e10dddb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879869"
---
# <a name="winmgmt"></a>winmgmt

Winmgmt 是在「LocalSystem」帳戶下執行的 SVCHOST 進程內的 WMI 服務。

在所有情況下，WMI 服務會在第一個管理應用程式或腳本要求與 WMI 命名空間的連接時自動啟動。 如需詳細資訊，請參閱[啟動和停止 WMI 服務](starting-and-stopping-the-wmi-service.md)。

> [!Note]  
> WMI 是 Windows 作業系統的核心元件，可讓開發人員和 IT 系統管理員撰寫腳本和應用程式，以將某些工作自動化。 Winmgmt.exe 是允許 WMI 在本機電腦上執行的服務。 如需使用 WMI 的詳細資訊，請參閱 [使用 wmi](using-wmi.md)。 如果您收到有關 winmgmt.exe 的錯誤訊息，請參閱 [WMI 疑難排解](wmi-troubleshooting.md)。 如需 Winmgmt.exe 的詳細資訊，請參閱 [使用 WMI 管理工具](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10))。

 

從命令提示字元執行時，WMI 服務會有下列參數。

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a>交換器

<dl> <dt>

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/backup** *&lt; 檔案名 &gt;* 
</dt> <dd>

導致 WMI 將存放庫備份至指定的檔案名。 *Filename* 引數應該包含檔案位置的完整路徑。 此程式需要儲存機制的寫入鎖定，如此一來，儲存機制的寫入作業才會暫止，直到備份程式完成為止。

如果您未指定檔案的路徑，它會放在% Windir% \\ System32 目錄中。

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/restore** *&lt; filename &gt;* *&lt; 旗 &gt;* 標 
</dt> <dd>

從指定的備份檔案手動還原 WMI 存放庫。 *Filename* 引數應該包含備份檔案位置的完整路徑。 若要執行還原作業，WMI 會儲存現有的存放庫，以在作業失敗時回寫。 然後，系統會從 *filename* 引數中指定的備份檔案還原存放庫。 如果無法取得存放庫的獨佔存取權，現有的用戶端就會從 WMI 中斷連線。

*旗* 標引數必須是 1 (強制中斷使用者連線，並還原) 或 0 (預設還原（如果沒有任何使用者連接) 並指定還原模式）。

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *&lt; winmgmt-服務-進程-識別碼 &gt;* 
</dt> <dd>

使用 WMI 註冊電腦的效能程式庫。 WMI PID 是 WMI 服務的處理序識別碼。

只有在效能監視類別未傳回可靠的結果時才需要。

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*&lt; 層 &gt; 級*\]
</dt> <dd>

將 Winmgmt 服務移至具有固定 DCOM 端點的獨立 Svchost 進程。 預設端點為「ncacn \_ ip \_ 0.24158」。 不過，您可以藉由執行 Dcomcnfg.exe 來變更端點。 如需設定 WMI 固定通訊埠的詳細資訊，請參閱 [設定 wmi 的固定通訊埠](setting-up-a-fixed-port-for-wmi.md)。

*層級* 引數是 Svchost 進程的驗證層級。 WMI 通常會作為共用服務主機的一部分來執行，而且您無法單獨增加 WMI 的驗證層級。 如果未指定 *層級* ，預設值為 4 (**RPC \_ C \_ 驗證 \_ level \_ PKT** 或 **WbemAuthenticationLevelPkt**) 。

您可以藉由將驗證等級提高為封包隱私權 (**RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權** 或 **WbemAuthenticationLevelPktPrivacy**) ，更安全地執行 WMI。 Visual Basic 和腳本的驗證層級會在 [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)中說明。 若為 c + +，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

將 Winmgmt 服務移至共用的 Svchost 進程。

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository** *&lt; 路徑 &gt;* 
</dt> <dd>

在 WMI 儲存機制上執行一致性檢查。 當您在沒有 *&lt; &gt; path* 引數的情況下新增 **/verifyrepository** 參數時，系統會驗證 WMI 目前使用的即時存放庫。 當您指定 *path* 引數時，您可以驗證儲存機制的任何儲存複本。 在此情況下，path 引數應該包含已儲存存放庫複本的完整路徑。 儲存的存放庫應該是整個存放庫資料夾的複本。 如需有關此命令所傳回錯誤的詳細資訊，請參閱「備註」一節。

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

在 WMI 存放庫上執行一致性檢查，如果偵測到不一致的情況，則重建存放庫。 不一致存放庫的內容會合並到重建的儲存機制中（如果可以讀取）。 搶救作業一律適用于 WMI 服務目前使用的存放庫。 如需有關此命令所傳回錯誤的詳細資訊，請參閱「備註」一節。

包含 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器語句的% MOF 檔案會還原至存放庫。

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

第一次安裝作業系統時，系統會將存放庫重設為初始狀態。 包含 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器語句的 MOF 檔案會還原至存放庫。

</dd> </dl>

## <a name="remarks"></a>備註

此工具位於% Windir% \\ System32 \\ wbem 目錄中。 如需可用參數的清單，請 `WinMgmt /?` 在命令提示字元中輸入。

WMI 存放庫（也稱為 CIM 存放庫）不只是單一檔案，而是存放庫資料夾中的檔案集合，可一起做為資料庫。 當您使用 **/backup** 參數來備份儲存機制時，產生的備份會是單一壓縮檔案。

如果驗證作業指出存放庫的狀態不一致，WMI 會傳回錯誤 **\_ 內部 \_ 資料庫 \_ 損毀** (net helpmsg 1358) 。 此錯誤可以從執行存放庫驗證的任何命令傳回，例如 **/verifyrepository** 或 **/salvagerepository**。

> [!Note]
>
> 如果 WMI 傳回錯誤訊息，請注意，它們可能不會指出 WMI 服務或 WMI 提供者中的問題。 失敗可能源自于作業系統的其他部分，並透過 WMI 出現錯誤。 在任何情況下，請勿將 WMI 儲存機制刪除為第一個動作，因為刪除存放庫可能會導致系統損毀或已安裝的應用程式。
>
> 如需問題來源的詳細資訊，請下載並執行[WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en)診斷命令列工具。 這項工具會產生一份報告，通常可以找出問題的來源，並提供如何修正問題的指示。 報表也會協助 Microsoft 支援服務協助您。 您可以下載[WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[從 Vista 開始從遠端連線至 WMI](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

