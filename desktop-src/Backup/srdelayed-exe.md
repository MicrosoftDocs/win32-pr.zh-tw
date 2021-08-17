---
title: Srdelayed.exe
description: 在作業系統啟動初期執行系統狀態還原作業的應用程式，可能無法使用檔案管理功能來移動、刪除或設定特定系統檔案的簡短名稱。
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Srdelayed.exe 備份
- 系統狀態修復備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdf95ff77fd17a578b85e6037c71146666eae9522d066bc1c4629fb9a2c24e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835536"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

在作業系統啟動初期執行系統狀態還原作業的應用程式，可能無法使用檔案管理功能來移動、刪除或設定特定系統檔案的簡短名稱。 Srdelayed.exe 是在 Windows Server 2008 中的 Windows Server Backup (WSB) 功能提供的可執行檔，可讓系統狀態修復應用程式移動、刪除和設定系統檔案的簡短名稱。

Srdelayed 工具適用于系統狀態恢復應用程式;它不會取代檔案管理功能。 只有當應用程式無法使用 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa)、 [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)和 [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) 函數來移動、刪除或設定系統檔案的簡短名稱時，才應該使用此工具。 在系統狀態還原和重新開機期間，系統還原和 wbadmin.exe 命令列工具會使用 Srdelayed.exe 來移動、刪除和設定特定系統檔案的簡短名稱。 因此，Srdelayed 可能會對需要能夠在自己的系統狀態復原應用程式中還原這些系統檔案的開發人員很有用。

Srdelayed 可以執行下列作業：

-   移動檔案作業類似于 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) 函式， **MOVEFILE 延遲到 \_ \_ \_ 重新開機** 旗標
-   類似于 [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) 函數的刪除檔案作業
-   類似于 [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) 函式的設定簡短名稱運算

若要使用 Srdelayed，您的應用程式需要 Srdelayed.exe 檔案位置的完整路徑，以及您所撰寫的 Unicode 文字檔的完整路徑，以包含工具執行所要求的所有檔案管理作業所需的資訊。 您的應用程式會負責確保這個文字檔不包含作業的重複要求，而且它會處理任何必要的檔案管理作業順序。 例如，由於資料夾必須是空的，因此，您的應用程式必須確保在要求刪除資料夾之前，文字檔會先移除資料夾內的所有檔案。

如果 **SetupExecute** 專案尚未存在於登錄中，則您的應用程式必須在下列登錄機碼底下，建立名 **為 SetupExecute** 的 **REG \_ 多重 \_ SZ** 類型專案： **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**。

您的應用程式應該使用下列格式，將 **SetupExecute** 的值設定為 Srdelayed.exe 檔案位置的完整路徑，以及文字檔位置的完整路徑。 將 " \\ \\ ？？ \\ " 前置詞設為文字檔的路徑，如下所示：

*Srdelayed.exe的完整路徑* \\ \\ ？ \\*文字檔的完整路徑*  


例如，下列 **SetupExecute** 值表示 Srdelayed.exe 位於 System32 資料夾中，而文字檔名為 DelayedOperations：

C： \\ Windows \\ System32 \\srdelayed.exe \\ \\ ？？ \\C： \\ temp \\ DelayedOperations  


路徑和名稱中的空格應該以十六進位編碼。 例如，在 *程式* 檔中，將路徑編碼為 " \\ \\ ？？ \\C:Program%20Files \\a.dll」。

在重新開機時還原登錄或系統時，您的應用程式必須確保 **SetupExecute** 會寫入正確的登錄 hive。 在 Srdelayed.exe 執行之前，會先執行登錄的復原。 應用程式需要將 **SetupExecute** 寫入至復原的登錄版本，因為這是所讀取的版本。

## <a name="format-for-the-srdelayed-input-file"></a>Srdelayed 輸入檔的格式

Srdelayed 執行檔案管理作業所需的所有資訊都指定為 Unicode 文字檔中的 Unicode 字元字串。 Unicode 字元的字串會分割成各自各自分割成四個欄位的記錄。 每一筆記錄會指定單一移動檔案、刪除檔案或設定簡短名稱作業。 每一筆記錄的四個欄位都包含作業的參數。 Srdelayed.exe 會依照其記錄出現在字串中的順序來執行每個作業。 您的應用程式應該檢查此檔案中是否有任何重複的記錄，並移除重複專案。

下列字串說明要求兩項作業並由兩筆記錄組成之檔案的格式。 每個參數欄位的結尾都是單一 L ' \\ 0 ' 字元。 記錄是由四個連續欄位所組成。 \\在所有記錄的結尾附加一個額外的單一 L ' 0 ' 字元。

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


第一個、第二、第三和第四個參數欄位的意義取決於記錄是否描述移動、刪除或設定的簡短名稱作業。

## <a name="format-for-a-move-file-record"></a>移動檔案記錄的格式

欄位1將此識別為移動檔案的要求。 此欄位中的值一律為 L "MoveFile"，而且會區分大小寫。

欄位2：指定檔案的來源位置。 Srdelayed 移動檔案操作不支援移動資料夾。 必須在此欄位中指定檔案。 這個欄位的值是附加至 "？？" 之檔案的完整路徑 \\ \\ \\ ，除非路徑包含 (GUID) 的全域唯一識別碼，這會使用 " \\ \\ ？ \\ " 作為前置詞。 請先移除 " \\ \\ ？ \\ " 再附加至 " \\ \\ ？？ \\ "。

欄位3：指定檔案的目的地。 移動檔案作業只會在磁片區內運作。 來源和目的地必須位於相同的磁片區上。 這個欄位的值是附加至 "？？" 之檔案的完整路徑 \\ \\ \\ ，除非路徑包含 (GUID) 的全域唯一識別碼，這會使用 " \\ \\ ？ \\ " 作為前置詞。 請先移除 " \\ \\ ？ \\ " 再附加至 " \\ \\ ？？ \\ "。

欄位4會接收來自 Srdelayed 的狀態資訊。 此欄位中的值應設定為 L "NotExecuted" 作為新記錄。

下列範例會依磁片磁碟機路徑來參考檔案。 如果來源的路徑和名稱為 C： \\ 階段 \\a.dll，此記錄會要求 Srdelayed 將它移至 C： \\ temp \\a.dll。

MoveFile \\ \\ ？？ \\C： \\ 階段 \\a.dll \\ \\ ？？ \\C： \\ temp \\a.dll NotExecuted  


下列範例會依磁片區 GUID 路徑來參考檔案。 如果來源的路徑和名稱是 \\ \\ ？ \\磁片區 {26a21bda-a627-11d7-9931-806e6f6e6963} \\ 階段 \\a.dll，此記錄會要求 Srdelayed 將它移至 \\ \\ ？ \\Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll

 MoveFile \\ \\ ？？ \\磁片區 {26a21bda-a627-11d7-9931-806e6f6e6963} \\ 階段 \\a.dll \\ \\ ？？ \\Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>刪除檔案記錄的格式

欄位1將此識別為刪除檔案的要求。 此欄位中的值一律為 L "DeleteFile"，而且會區分大小寫。

未使用欄位2。 此欄位中的值應設定為 L "未使用"。

欄位3：指定要移除的檔案。 資料夾必須是空的，才能移除。 移除資料夾之前，請使用 [刪除檔案作業] 移除資料夾中的所有檔案。 這個欄位的值是附加至 "？？" 之檔案的完整路徑 \\ \\ \\ ，除非路徑包含 (GUID) 的全域唯一識別碼，這會使用 " \\ \\ ？ \\ " 作為前置詞。 請先移除 " \\ \\ ？ \\ " 再附加至 " \\ \\ ？？ \\ "。

欄位4會接收來自 Srdelayed 的狀態資訊。 此欄位中的值應設定為 L "NotExecuted" 作為新記錄。

下列範例會依磁片磁碟機路徑來參考檔案。 如果路徑和名稱為 C： \\ temp \\b.dll，此記錄會要求 Srdelayed 刪除該檔案。

DeleteFile 未使用 \\ \\ ？？ \\C： \\ temp \\b.dll NotExecuted  


下列範例會依磁片區 GUID 來參考檔案。 如果路徑和名稱是 \\ \\ ？ \\磁片區 {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll，此記錄會要求 Srdelayed 移除該檔案。

DeleteFile 未使用 \\ \\ ？？ \\Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Set Short-Name Record 的格式

[欄位 1] 將此識別為要求設定檔案的簡短名稱。 此欄位中的值一律為 L "SetFileShortName"，而且會區分大小寫。

欄位2：指定簡短名稱。

[欄位 3] 欄位指定要接收簡短名稱的路徑和完整名稱。 此欄位的值是附加至 "？？" 之檔案的路徑和完整名稱 \\ \\ \\ ，除非路徑包含 (GUID) 的全域唯一識別碼，這會使用 " \\ \\ ？ \\ " 作為前置詞。 請先移除 " \\ \\ ？ \\ " 再附加至 " \\ \\ ？？ \\ "。

欄位4會接收來自 Srdelayed 的狀態資訊。 此欄位中的值應設定為 L "NotExecuted" 作為新記錄。

下列範例會依磁片磁碟機路徑來參考檔案。 如果檔案的路徑和名稱為 C： \\ temp \\ShortFileName.dll，此記錄會要求檔案收到簡短名稱 ShortN ~1.dll。

SetFileShortName ShortN ~1.dll \\ \\ ？？ \\C： \\ temp \\ShortFileName.dll NotExecuted  


下列範例會依磁片區 GUID 來參考檔案。 如果檔案的路徑和名稱是 \\ \\ ？ \\磁片區 {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ ，此記錄會要求檔案收到簡短名稱 ShortN ~1.dll。

SetFileShortName ShortN ~1.dll \\ \\ ？？ \\Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>Srdelayed 作業狀態

Srdelayed 會將 "SC =*>xxxxxxx*" 字串寫入到文字檔的每個記錄的第四個欄位中，其中 *>xxxxxxx* 是表示要求的作業狀態的十六進位。 值為零表示作業成功。

Srdelayed 會在 **HKEY \_ LOCAL \_ MACHINE** Software Microsoft Windows NT CurrentVersion 下建立名為 **SystemRestore** 的登錄機碼 \\  \\  \\  \\  ，以記錄整個還原作業的結果。 如果 Srdelayed 執行所有要求的作業成功，則名稱 RestoreStatusResult 會以零值寫入此索引鍵。 如果 Srdelayed 無法執行任何要求的作業，名稱 RestoreStatusResult 和 RestoreStatusDetails 會以非零值寫入此索引鍵下。 只有在 Srdelayed 無法執行任何要求的作業時，才會在此機碼下寫入名稱 RestoreStatusDetails。 如果設定檔案簡短名稱的作業不成功，Srdelayed 會繼續進行下一項作業。 Srdelayed 會將移動檔案和刪除檔案作業視為重要，且如果移動或刪除作業失敗，則不會繼續。

 

 