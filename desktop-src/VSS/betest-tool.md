---
description: BETest 是可測試 advanced backup 和 restore 作業的 VSS 要求者。
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: BETest 工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f37e8bfc224061a8205bf0759cbba4798b0d53227e4f12d89b1e9ddf629d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471148"
---
# <a name="betest-tool"></a>BETest 工具

BETest 是可測試 advanced backup 和 restore 作業的 VSS 要求者。 此工具可用來測試應用程式使用複雜 VSS 功能的方式，如下所示：

-   增量和差異備份
-   複雜還原選項，例如權威還原
-   向前復原選項

> [!Note]  
> BETest 隨附于適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 。 VSS 7.2 SDK 包含只能在 Windows Server 2003 上執行的 BETest 版本。 本主題說明 Windows SDK 版本的 BETest，而不是 VSS 7.2 SDK 隨附的 Windows Server 2003 版本。 如需下載 Windows SDK 和 VSS 7.2 SDK 的詳細資訊，請參閱[磁碟區陰影複製服務](volume-shadow-copy-service-portal.md)。

 

在 Windows SDK 安裝中，您可以 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (在64位 Windows) 和 (32 位 Windows) 中找到 BETest 工具 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 。

## <a name="running-the-betest-tool"></a>執行 BETest 工具

若要從命令列執行 BETest 工具，請使用下列語法：

**BETest** *命令列選項*

下列使用範例示範如何搭配使用 BETest 工具與 [Vss 測試編寫器工具](vss-test-writer-tool.md)，這是 vss 寫入器工具。

**BETest 工具使用範例**

1.  建立名為 C： BETest 的測試目錄 \\ 。 將下列檔案複製到此目錄中：
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  建立名為 C： TestPath 的目錄 \\ 。 將部分測試資料檔案放在此目錄中。
3.  建立名為 C： BackupDestination 的目錄 \\ 。 將此目錄保留空白。
4.  開啟兩個提高許可權的命令視窗，並將每個的工作目錄設定為 C： \\ BETest。
5.  在第一個命令視窗中，啟動 [VSS 測試寫入器工具](vss-test-writer-tool.md) ，如下所示：

    **vswriter.exe VswriterSample.xml**

    vswriterSample.xml 的檔案會設定 VSS 測試寫入器工具 (vswriter) 來報告 c： TestPath 目錄的內容，以 \\ 準備備份作業。 請注意，在偵測到來自要求者（例如 BETest）的活動之前，VSS 測試寫入器工具將不會產生輸出。 若要停止 VSS 測試編寫器工具，請按 CTRL + C。

6.  在第二個命令視窗中，使用 BETest 工具來執行備份作業，如下所示：

    **betest.exe/B/S backup.xml/D C： \\ BackupDestination/x BetestSample.xml**

    BETest 會將檔從 C： \\ TestPath 目錄備份到 c： \\ BackupDestination 目錄。 它會將備份元件檔儲存至 C： \\ BETest \\backup.xml。

7.  如果備份作業成功，請刪除 C： \\ TestPath 目錄的內容，並使用 BETest 工具來執行還原作業，如下所示：

    **betest.exe/R/S backup.xml/D C： \\ BackupDestination/x BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>BETest 工具 Command-Line 選項

BETest 工具會使用下列命令列選項來識別要執行的工作。

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

針對 Active Directory 或 Active Directory 應用程式模式執行授權還原作業。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**後退**
</dt> <dd>

執行備份操作，但不執行還原。

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

只執行備份完成作業。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *檔案名*
</dt> <dd>

> [!Note]  
> 此命令列選項僅提供回溯相容性。 您應該改為使用 **/x** 命令列選項。

 

根據 *檔案名* 所指定的設定檔內容，選取要備份或還原的元件。 這個檔案必須只包含0到127範圍內的 ANSI 字元，而且必須大於 1 MB。 檔案中的每一行都必須使用下列格式：

*WriterId* ： *ComponentName*;

其中 *WriterId* 是寫入器識別碼，而 *ComponentName* 是其中一個寫入器元件的名稱。 寫入器識別碼和元件名稱必須以引號括住，而且在冒號 (： ) 之前和之後必須有空格。 如果指定了兩個以上的元件，則必須以逗號分隔。 例如：

"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *路徑*
</dt> <dd>

儲存備份的檔案，或從 *Path* 指定的備份目錄還原這些檔案。

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

省略備份完成作業。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/O**
</dt> <dd>

指定備份包含可開機的系統狀態。

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/P**
</dt> <dd>

建立持續性陰影複製。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *檔案名*
</dt> <dd>

如果在 **/t** 命令列選項中指定的備份類型是 [增量] 或 [差異]，請將備份檔案設定為 [ *檔案名* ] 所指定的檔案，以用於先前的完整或增量備份。

**Windows Server 2003 和 Windows XP：** 不支援此命令列選項。

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/R**
</dt> <dd>

執行還原，但不執行備份。 必須與 **/s** 命令列選項一起使用。

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

建立可用於應用程式復原的陰影複製。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *檔案名*
</dt> <dd>

如果是備份，請將備份檔案儲存至 *檔案名* 所指定的檔案。 如果只還原，則會從這個檔案載入備份檔案。

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

建立磁片區陰影複製，但不執行備份或還原。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

發生第一個寫入器錯誤時停止 BETest。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*
</dt> <dd>

指定備份類型。 *BackupType* 可以是 FULL、LOG、COPY、增量或差異。 如需備份類型的詳細資訊，請參閱 [**VSS \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)。

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/V**
</dt> <dd>

產生可用於疑難排解的詳細資訊輸出。

**Windows Server 2003：** 不支援此命令列選項。

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *檔案名*
</dt> <dd>

根據 *Filename* 指定的 XML 設定檔內容，選取要備份或還原的元件。 這個檔案必須只包含0到127範圍內的 ANSI 字元。 XML 檔案的格式是由 BETest.xml 檔案中的架構所定義。 如需範例設定檔，請參閱 BetestSample.xml。 這兩個檔案都在 vsstools 目錄中。

> [!Note]  
> 您可以在 Internet Explorer 中查看 BETest.xml 的檔案。 開啟這個檔案之前，請確定 xdr-schema 與 BETest.xml 在相同的目錄中。 Xdr-schema xsl 檔案包含轉譯指令，可讓 BETest.xml 檔案更容易讀取。

 

**Windows Server 2003：** 不支援此命令列選項。

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>範例 XML 設定檔： BetestSample.xml

下列範例設定檔 BetestSample.xml 可在 Vsstools 目錄中找到。

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

此簡單設定檔的範例會選取要備份或還原的一個元件。

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>範例 XML 設定檔： VswriterSample.xml

下列範例設定檔 VswriterSample.xml 可在 Vsstools 目錄中找到。

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

此設定檔中的根項目命名為 TestWriter。 所有其他專案會排列在 TestWriter 元素之下。

與 TestWriter 相關聯的第一個屬性是 usage 屬性。 這個屬性會指定透過 [**IVssExamineWriterMetadata：： GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) 方法回報的使用類型。 此屬性的其中一個可能值為使用者 \_ 資料。

第二個屬性是 deleteFiles 屬性。 這個屬性會在設定 [寫入器屬性](vss-test-writer-tool.md)中說明。

根項目的第一個子項目是 RestoreMethod 元素。 這個元素會指定下列專案：

-   在此情況下，restore 方法 (， \_ 如果 \_ 可以 \_ 取代則還原 \_) 
-   寫入器是否需要還原事件 (在此情況下，一律) 
-   還原寫入器之後是否需要重新開機 (在此案例中為否) 

這個元素可以選擇性地指定替代位置對應。  (在此案例中，未指定替代位置 ) 。如需詳細資訊，請參閱 [指定替代位置](vss-test-writer-tool.md)對應。

第二個子項目是元件元素。 此元素會導致寫入器將元件新增至其中繼資料。 元件專案包含屬性，用來描述元件和子項目，以描述元件的內容，如下所示：

-   componentType，指出這是否為檔案群組或資料庫 (在此案例中為檔案群組) 
-   logicalPath 元件邏輯路徑的在此案例中，未指定任何 () 
-   componentName：在此案例中為元件名稱 ("TestFiles" ) 
-   可選取以指出可選取的備份狀態

Component 元素也有一個名為 ComponentFile 的子專案，可將檔案規格新增至此元件。  (元件元素可以有任意數目的 ComponentFile 元素，可為每個元件指定。 ) 此 ComponentFile 元素具有下列屬性：

-   path = "c： \\ TestPath"
-   filespec = " \* "
-   遞迴 = "no"

 

 



