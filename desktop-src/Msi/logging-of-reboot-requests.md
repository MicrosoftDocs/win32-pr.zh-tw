---
description: 如果 [InstallValidate] 動作偵測到檔案的安裝已在使用中，則會顯示 [FilesInUse] 對話方塊，並記錄下列資訊。
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: 重新開機要求的記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514149"
---
# <a name="logging-of-reboot-requests"></a>重新開機要求的記錄

如果 [ [InstallValidate] 動作](installvalidate-action.md) 偵測到檔案的安裝已在使用中，則會顯示 [ [FilesInUse] 對話方塊](filesinuse-dialog.md) ，並記錄下列資訊。

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

如果安裝程式偵測到它即將覆寫正在使用中的檔案，則會記錄下列資訊。

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

\[Filename \] 標記實際上可能包含副檔名為 rbf 的檔案路徑。 在此情況下，rbf 檔案實際上是由1603訊息記錄的原始檔案，而該檔案已重新命名為 rbf 檔案。 使用中的檔案會先以 rbf 副檔名重新命名，然後再刪除。

若要取得安裝程式嘗試覆寫這個特定檔案的詳細資訊，您可以使用 [詳細資訊記錄] 選項。 \_在 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)的呼叫中使用 INSTALLLOGMODE VERBOSE 值，或使用 [命令列選項](command-line-options.md)的詳細輸出選項。 這會記錄下列資訊。

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

記錄檔將會包含訊息，例如「現有的檔案是較低的版本」或「現有的檔案已損毀 (不正確總和檢查碼) 」

 

 



