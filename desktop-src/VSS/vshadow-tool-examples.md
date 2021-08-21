---
description: 深入瞭解： VShadow 工具範例
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: VShadow 工具範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec0a753f2865be98cfed76cd192a73cfc785b3fcdc487f7685c9f4ae7d52e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056346"
---
# <a name="vshadow-tool-examples"></a>VShadow 工具範例

下列範例示範如何使用 VShadow 工具來執行最常見的工作：

-   [從 CMD 腳本存取陰影複製屬性](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [存取非持續性陰影複製](#accessing-nonpersistent-shadow-copies)
-   [從陰影複製複製檔案](#copying-a-file-from-a-shadow-copy)
-   [列舉陰影複製裝置上的所有檔案](#enumerating-all-files-on-a-shadow-copy-device)
-   [匯入可轉移的陰影複製](#importing-a-transportable-shadow-copy)
-   [包含寫入器或元件](#including-writers-or-components)
-   [排除寫入器或元件](#excluding-writers-or-components)
-   [使用 BreakSnapshotSetEx 方法的中斷陰影複製集](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

如需命令列選項及其用法的完整清單，請參閱 [VShadow 工具和範例](vshadow-tool-and-sample.md)。

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>從 CMD 腳本存取陰影複製屬性

如果您在建立陰影複製時使用 **-script** 選擇性旗標，VShadow 會建立 CMD 腳本檔案，其中包含與新建立的陰影複製相關的環境變數，如下所示：

-   陰影複製集識別碼，儲存在% VSHADOW \_ set \_ id% 環境變數中
-   陰影複製識別碼，儲存在格式為% VSHADOW \_ ID NNN% 的變數中 \_ **，其中 *NNN* 代表 VSHADOW 命令列中來源磁片區的索引
-   陰影複製裝置名稱，儲存在表單% VSHADOW \_ 裝置 NNN% 的變數中 \_ **，其中 *NNN* 是 VSHADOW 命令列中來源磁片區的索引

您可以使用產生的 CMD 檔案，對陰影複製執行有限的管理作業。

> [!Note]  
> [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)寫入器事件會在執行 **-exec** 腳本之後傳送。 VSS 會呼叫 **>ivssbackupcomponents：： BackupComplete** 方法，以向寫入器告知備份已完成，而寫入器可能會在此時截斷記錄。 因此，請務必確認陰影/備份確實已完成。 如果備份失敗，您可以在執行的腳本/命令中傳回非零的結束代碼，以取消建立進程。  (請參閱 [Windows 命令列參考](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11))中的結束命令檔。 ) 如果自訂命令傳回非零結束代碼，則會取消陰影複製建立，且不會呼叫 **>ivssbackupcomponents：： BackupComplete** 。

 

下列範例顯示如何從命令列建立持續性陰影複製，並使用 CMD 腳本來公開它。

1.  **vshadow-p-nw-script = SETVAR1 .cmd c：**
2.  **呼叫 SETVAR1 .cmd**
3.  **C： \\>vshadow-el =% vshadow \_ ID \_ 1%，c： \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>存取非持續性陰影複製

在此情況下，非持續性陰影複製會在建立它們的程式 (時自動刪除，VShadow) 結束。 若要存取這些陰影複製的內容，VShadow 可以讓您在建立陰影複製之後，但在 VShadow 程式結束之前執行腳本。

下列範例顯示如何使用-exec 命令列選項來執行名為 "enum" 的腳本：

**vshadow-nw-exec = enum c：**

在執行的腳本中，您也可以在這個自訂命令中執行產生的 SETVAR 腳本。 這可讓腳本直接存取陰影複製的內容。 請記住，您可以從 VSHADOW \_ 裝置 NNN 環境變數中取出陰影裝置 \_ 。

以下是範例列舉 .cmd 腳本：

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

以下是用來執行列舉 .cmd 腳本的命令列：

**vshadow-nw-exec = c： \\ enum。 cmd-script = setvar1 .cmd c：**

## <a name="copying-a-file-from-a-shadow-copy"></a>從陰影複製複製檔案

下列範例顯示如何從陰影複製複製檔案。

1.  **dir > c： \\somefile.txt**
2.  **vshadow-p-nw-script = SETVAR1 .cmd c：**
3.  **呼叫 SETVAR1 .cmd**
4.  **複製% VSHADOW \_ DEVICE \_ 1% \\somefile.txt c： \\ somefile.txt 之 \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>列舉陰影複製裝置上的所有檔案

下列範例顯示如何從批次檔列舉陰影複製裝置上的所有檔案。

1.  **dir > c： \\somefile.txt**
2.  **vshadow-p-nw-script = SETVAR1 .cmd c：**
3.  **呼叫 SETVAR1 .cmd**
4.  **若為/R% VSHADOW \_ 裝置 \_ 1%%% \\ i in (\*) 進行 @echo %% i**

## <a name="importing-a-transportable-shadow-copy"></a>匯入可轉移的陰影複製

若要在一部電腦上建立可轉移的陰影複製，並將其匯入到另一部電腦上，您必須有兩部透過 SAN 設定連接 (的電腦) 至支援 VSS 硬體陰影複製的存放裝置陣列。 每部電腦上都必須安裝 VSS 硬體提供者。

下列範例顯示如何建立和匯入陰影複製。

1.  在命令提示字元下輸入下列命令，在電腦 A 上建立陰影複製集 (生產伺服器) ：

    **vshadow-p-t =bc1.xml**

    這不會公開電腦 A 上的任何陰影複製裝置。

2.  將備份元件檔 (bc1.xml) 從電腦 A 複製到電腦 B。
3.  輸入下列命令，以匯入電腦 B 上的陰影集合：

    **vshadow-i =bc1.xml**

（選擇性）您可以將這些陰影複製公開為磁碟機號或裝載的資料夾。 此外，您可能會中斷陰影組，使新的陰影複製磁片區可讀寫。

若要將陰影集管理程式自動化，您可以使用 **-script** 命令列選項來產生包含陰影複製識別碼的 CMD 腳本。 然後，您可以將產生的腳本連同備份元件複製到另一部電腦上。

下列範例示範如何使用 CMD 腳本建立、公開及中斷可轉移的陰影複製。

1.  從命令列 (生產伺服器) 建立電腦 A 上的陰影複製集，如下所示：

    **vshadow-p-t =bc1.xml-script = sc1 .cmd**

    指定 **-script** 選項以產生包含適當環境變數定義的腳本。 請注意，這不會公開電腦 A 上的任何陰影複製裝置。

2.  將備份元件檔 (bc1.xml) 和產生的腳本 (sc1 從電腦 A) 到電腦 B。
3.  輸入下列命令，以匯入電腦 B 上的陰影集合：

    **vshadow-i =bc1.xml**

    這會顯示電腦 B 上所建立的裝置。

4.  執行產生的腳本，藉由在命令提示字元中輸入檔案名來設定陰影複製集的環境變數，如下列範例所示：

    **sc1 .cmd**

    這會設定相關的環境變數，如從 CMD 腳本存取陰影複製屬性中所述。

5.  輸入下列命令，以公開電腦 B 上的陰影複製：
    1.  **rmdir/s c： \\ 裝入 \_ 點**
    2.  **mkdir c： \\ 裝入 \_ 點**
    3.  **vshadow – el =% VSHADOW \_ ID \_ 1%，c： \\ 裝入 \_ 點**

    這會呈現電腦 B 上所建立的陰影複製裝置。
6.  輸入下列命令，以中斷陰影複製集，使磁片區可供寫入：**C： \\>vshadow – bw =% vshadow \_ set \_ ID%**

請注意，您也可以匯入非持續性的可轉移陰影複製，但在 **vshadow** **-i** 進程結束時，會自動將其刪除。 若要在刪除陰影複製之前將其匯入，您必須使用「存取永久性陰影複製」中所述的 **-exec** 命令列選項。

## <a name="including-writers-or-components"></a>包含寫入器或元件

依預設，所有寫入器都會參與陰影複製的建立。 若要判斷哪些寫入器和元件將包含在陰影複製集中，請使用 **-wm** 或 **-wm2-downloadbtn** 命令列選項，如 [清單寫入器狀態和中繼資料](vshadow-tool-and-sample.md)所述。

若要確認是否包含所有寫入器的元件，請使用下列任何格式的 **-wi-fi** 選擇性旗標：

-   **vshadow** **-wi-fi** *WriterName*
-   **vshadow** **-wi-fi** ****「_寫入器名稱字串_*__* 」
-   **vshadow** **-wi-fi** **{**_WriterID_*_}_*
-   **vshadow** **-wi-fi** **{**_InstanceID_*_}_*

若要確認是否包含特定的元件，請使用下列任何格式的 **-wi-fi** 選擇性旗標：

-   **vshadow** **-wi-fi** *WriterName ***： \\** _LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wi-fi** **"**_Writer Name String_*_"： \\_* _LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi-fi** **{**_WriterID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi-fi** **{**_InstanceID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_

下列範例示範如何使用 **-wi-fi** 選擇性旗標。

-   指定 *WriterName*： \\ *LogicalPath* \\ *ComponentName*：

    **vshadow-wi-fi = "Registry Writer： \\ registry"**

-   指定 {*WriterID*}：

    **vshadow-wi-fi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   指定一個以上的寫入器或元件：

    **vshadow-wi-fi = "Registry Writer： \\ registry"-wi-fi = "COM + REGDB Writer"**

## <a name="excluding-writers-or-components"></a>排除寫入器或元件

若要排除所有寫入器，請在建立陰影複製時使用 **-nw** 選擇性旗標。

若要排除所有寫入器的元件，請使用下列任何格式的 **-wx** 選擇性旗標：

-   **vshadow** **-wx** *WriterName*
-   **vshadow** **-wx** **"**_Writer Name String_*_"_*
-   **vshadow** **-wx** **{**_WriterID_*_}_*
-   **vshadow** **-wx** **{**_InstanceID_*_}_*

若要排除特定的元件，請使用下列任何一種格式的 **-wx** 選擇性旗標：

-   **vshadow** **-wx** *WriterName ***： \\** _LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wx** **"**_Writer Name String_*_"： \\_* _LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_WriterID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_InstanceID_*_}： \\_* _LogicalPath_ *_\\_* _ComponentName_

下列範例示範如何使用 **-wx** 選擇性旗標。

-   指定 *WriterName*： \\ *LogicalPath* \\ *ComponentName*：

    **vshadow-wx = "Registry Writer： \\ registry"**

-   指定 {*WriterID*}：

    **vshadow-wx = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   指定一個以上的寫入器或元件：

    **vshadow-wx = "Registry Writer： \\ registry"-wx = "COM + REGDB Writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>使用 BreakSnapshotSetEx 方法的中斷陰影複製集

下列範例示範如何使用 **-bex** 命令列選項。

-   指定陰影複製 LUN 將會從主機遮罩：

    **vshadow** **-bex** **-mask**

-   指定將陰影複製 LUN 公開給主機作為讀取/寫入磁片區：

    **vshadow** **-bex** **-rw**

-   指定陰影複製 LUN 會以讀取/寫入磁片區的形式公開給主機，而且陰影複製 Lun 上的磁片簽章都不會還原為原始 Lun 的磁片簽章：

    **vshadow** **-bex** **-norevert**

 

 
