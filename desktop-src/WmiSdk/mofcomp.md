---
description: 受控物件格式 (MOF) 編譯器會剖析包含 MOF 語句的檔案，並將檔案中定義的類別和類別實例新增至 WMI 存放庫。
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848394"
---
# <a name="mofcomp"></a>mofcomp.exe

[*受控物件格式 (mof)*](gloss-m.md)編譯器會剖析包含 MOF 語句的檔案，並將檔案中定義的類別和類別實例新增至 WMI 存放庫。 MOF 檔案通常會在安裝時自動編譯，但您也可以使用此工具來編譯 MOF 檔案。

如需尋找和使用 mofcomp.exe 的詳細資訊，請參閱 [使用 WMI 管理工具](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10))。 如需從 WMI 儲存機制移除類別和實例的詳細資訊，請參閱 [**pragma deleteclass**](pragma-deleteclass.md) 預處理器命令。

下列程式碼範例顯示如何在檔案上執行 MOF 編譯器。

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a>交換器

<dl> <dt>

<span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-自動回復**
</dt> <dd>

將命名的 MOF 檔案新增至儲存機制復原期間所編譯的檔案清單。 自動回復 MOF 檔案的清單儲存在登錄機碼中：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**

此登錄專案中列出的 MOF 檔案必須位於本機電腦上，因為使用 [ **自動** 復原] 命令的 mof 檔案無法復原位於遠端電腦上的 mof 檔案。

> [!Note]  
> 若要確保在 WMI 失敗並重新啟動時，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請使用 [*受控物件格式*](gloss-m.md) (MOF) 檔中的 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。

 

</dd> <dt>

<span id="-check"></span><span id="-CHECK"></span>**-檢查**
</dt> <dd>

要求編譯器只執行語法檢查並列印適當的錯誤訊息。 此參數不能使用其他參數。 使用此參數時，不會建立 Windows Management Instrumentation (WMI) 的連線，也不會對 WMI 存放庫進行任何修改。

</dd> <dt>

<span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N： <** _namespacepath_*_>_*
</dt> <dd>要求編譯器將 MOF 檔案載入至指定為 *namespacepath* 的命名空間。 除非使用此參數，否則已編譯的 MOF 會載入預設的 Mofcomp.exe 命名空間（根 \\ 預設值）。 您也可以將預處理器命令 **\# pragma 命名空間 (**「_命名空間路徑_」*_)_* 在 MOF 檔案中，以達到相同的效果。 如果同時使用 **-N：** switch 和 \# <a href="pragma-namespace.md">pragma namespace</a>命令，則會優先使用 \# **pragma namespace** **自動** 回復。 在此情況下，將 MOF 編譯成另一個命名空間的唯一方法，是編輯 MOF 檔案並變更 \# **pragma namespace** 命令。 您可以使用 \\ \\ machinename \\ 根 \\ 預設值來指定遠端電腦。</dd> <dt>

<span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class：以**
</dt> <dd>

要求編譯器不會對現有的類別進行任何變更。 使用這個參數時，如果 MOF 檔案中指定的類別已存在，編譯作業就會終止。

</dd> <dt>

<span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class： forceupdate**
</dt> <dd>

存在衝突的子類別時，強制更新類別。 例如，假設類別限定詞是在子類別中定義，而且基類嘗試加入相同的辨識符號。 在 **類別中： forceupdate** 模式，MOF 編譯器會藉由刪除子類別中的衝突辨識符號來解決這項衝突。 如果子類別具有實例，強制更新會失敗。

</dd> <dt>

<span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class： safeupdate**
</dt> <dd>

即使有子類別，也允許更新類別，只要變更不會造成與子類別的衝突。 例如，這個旗標可讓您將新的屬性加入至先前未在子類別中提及的基類。 如果子類別具有實例，則更新會失敗。

</dd> <dt>

<span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class： updateonly**
</dt> <dd>

要求編譯器不會建立任何新的類別。 使用這個參數時，如果 MOF 檔案中指定的類別不存在，編譯作業就會終止。

</dd> <dt>

<span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance： updateonly**
</dt> <dd>

要求編譯器不會建立任何新的實例。 使用這個參數時，如果 MOF 檔案中指定的實例不存在，編譯作業就會終止。

</dd> <dt>

<span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance：以**
</dt> <dd>

要求編譯器不會對現有的實例進行任何變更。 使用這個參數時，如果 MOF 檔案中指定的實例已經存在，編譯作業就會終止。

</dd> <dt>

<span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B： <** _filename_*_>_*
</dt> <dd>

要求編譯器建立具有名稱 *檔案名* 的二進位版本 MOF 檔案，而不需要對 WMI 儲存機制進行任何修改。

如果您使用 **-B： <** _filename_ *_>_* 選項來建立二進位 MOF 檔案，則只有預設的限定詞類別會儲存在 WMI 存放庫中。

二元 MOF 格式是將 WDM 驅動程式與 MOF 結合為資源的中繼格式。 二元 MOF 代表類別和實例，就像是文字 MOF 檔案一樣，並且會在儲存于磁片之前壓縮。

</dd> <dt>

<span id="-WMI"></span><span id="-wmi"></span>**-WMI**
</dt> <dd>

要求編譯器執行 WMI 語法檢查。 必須搭配此參數使用 **-B：** switch。 **-WMI** 參數僅用來建立可供 WDM 設備磁碟機使用的二進位 MOF 檔案。 此參數會叫用個別的二進位 MOF 檔案檢查程式，並在建立二元 MOF 檔案之後執行。

</dd> <dt>

<span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P： <**_密碼_*_>_*
</dt> <dd>

指定 *密碼* 做為登入時電腦使用者輸入的密碼。

</dd> <dt>

<span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U： <** 使用者 _名稱_*_>_*
</dt> <dd>

指定 *使用者* 名稱做為登入使用者的名稱。

</dd> <dt>

<span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A： <**_授權_ 單位 *_>_*
</dt> <dd>

將 *授權* 單位指定為登入 WMI 時所要使用 (功能變數名稱) 的授權單位。

</dd> <dt>

<span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF： <**_路徑_*_>_*
</dt> <dd>

非語言相關輸出的名稱。 搭配 **-修訂** 參數使用，以指定將產生的語言中性 MOF 檔案的名稱。

</dd> <dt>

<span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL： <**_路徑_*_>_*
</dt> <dd>

特定語言輸出的名稱。 與 **-修訂** 參數搭配使用，以指定將產生的語言特定 MOF 檔案的名稱。

</dd> <dt>

<span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-修訂： <**_地區_ 設定 *_>_*
</dt> <dd>

將 MOF 檔案分割成非語言相關和特定版本。 MOF 編譯器會建立 MOF 檔案的語言中性形式，其中已移除所有修改過的限定詞。 您也可以使用 MFL 副檔名來建立 MOF 檔案的當地語系化版本。 *Locale* 參數會指定子命名空間的名稱，其中包含當地語系化的類別定義。 *地區* 設定參數的格式為 MS \_ xxx，其中 XXX 是 Windows LCID 的十六進位值。 例如，美式英文的地區設定為 MS \_ 409。

</dd> <dt>

<span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <的** _coNtext.resourcename_*_>_*
</dt> <dd>

從命名資源中解壓縮二進位 MOF。 此參數會從 WMI 存放庫中的類別取得二進位 MOF，而-B 參數會從 MOF 檔案建立二進位 MOF 格式。

</dd> <dt>

<span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L： <** _ResourceLocale_*_>_*
</dt> <dd>

選擇性。 搭配-ER 參數使用時，從二進位 MOF 中解壓縮當地語系化的 MOF 描述。

</dd> <dt>

<span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*
</dt> <dd>

要剖析的檔案名。

</dd> </dl>

## <a name="return-values"></a>傳回值

MOF 編譯器做為第一次作業時，會對 MOF 檔案執行語法檢查。 如果編譯器發現任何錯誤，則會列印錯誤訊息，且進程會終止。

MOF 編譯器可能會傳回下列值：

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

MOF 編譯操作成功。

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

MOF 編譯器無法與 WMI 伺服器連接。 這可能是因為有語意錯誤，例如與現有 WMI 存放庫不相容，或實際的錯誤，例如 WMI 伺服器無法啟動。

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

一或多個命令列參數無效。

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

發生 MOF 語法錯誤。

</dd> </dl>

如果 MOF 檔案已正確剖析，但嘗試執行命令列參數所禁止的作業，則編譯器會傳回 WMI 產生的錯誤碼，而不是上述清單中所列的任何傳回碼。 例如，當指定 **-instance： updateonly** 參數，且 MOF 檔案嘗試建立實例時，會傳回 WMI 錯誤碼。

如果 [**\# pragma 自動**](pragma-autorecover.md)回復預處理器語句不在檔案中，則會傳回下列警告：

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a>備註

MOF 編譯器可在% Windir% \\ System32 \\ wbem 目錄中取得。 您必須將 MOF 檔案指定為 MOF 編譯器的參數。 如果您想要自動重新編譯 MOF 檔案（如果必須自動復原 CIM 存放庫），您也可以指定自動重設開關。 如需詳細資訊，請輸入 **mofcomp.exe/？** 。

使用 Unicode 字元集的 MOF 檔案，會將簽章包含為檔案的前兩個位元組。 此簽章可以是 U + FFFE 或 U + FEFF，視檔案的位元組順序而定。

當剖析程式中未發生任何錯誤時，MOF 編譯器會連接到本機電腦上執行的 WMI 伺服器，除非已指定 **-check** 參數。 MOF 檔案中定義的類別和實例會新增至 WMI 存放庫。

當更新 WMI 儲存機制發生錯誤時，編譯器不會在編譯器開始處理之前，嘗試將存放庫傳回其狀態。

**Windows 8：** 在安裝提供者時，mofcomp.exe \[ 會將金鑰 \] 和 \[ 靜態限定詞視為 \] true （如果存在的話），而不論其實際值為何。 如果有其他限定詞存在但未明確設定為 true，則會將它們視為 false。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**pragma 命名空間**](pragma-namespace.md)
</dt> <dt>

[編譯 MOF 檔案](compiling-mof-files.md)
</dt> <dt>

[編譯當地語系化的 MOF 檔案](compiling-localized-mof-files.md)
</dt> <dt>

[註冊提供者](registering-a-provider.md)
</dt> <dt>

[**IMOFCompiler::CompileFile**](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

