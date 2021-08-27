---
description: 使用 CreateFile 函數建立或開啟檔案的考慮。
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: 建立和開啟檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e80449942fbceb39c37604bf6d8b5410d171d195
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469925"
---
# <a name="creating-and-opening-files"></a>建立和開啟檔案

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式可以建立新的檔案，或開啟現有的檔案。 您必須指定檔案名、建立指示和其他屬性。 當應用程式建立新檔案時，作業系統會將它新增至指定的目錄。

作業系統會針對使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)開啟或建立的每個檔案，指派一個稱為 *控制碼* 的唯一識別碼。 應用程式可以使用此控制碼來處理讀取、寫入和描述檔案的函式。 它會一直有效，直到該控制碼的所有參考都已關閉為止。 當應用程式啟動時，如果將控制碼建立為可繼承，它就會從啟動它的進程繼承所有開啟的控制碼。

應用程式應該先檢查 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 傳回的控制碼值，再嘗試使用控制碼來存取檔案。 如果發生錯誤，控制碼值將會是 **不正確 \_ 控制碼 \_ 值** ，而且應用程式可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數來取得延伸的錯誤資訊。

當應用程式使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)時，它必須使用 *dwDesiredAccess* 參數來指定是否要從檔案讀取、寫入檔案、讀取和寫入，或兩者皆非。 這就是所謂的要求 *存取模式*。 應用程式也必須使用 *dwCreationDisposition* 參數來指定檔案已存在時要採取的動作，稱為「 *建立* 配置」。 例如，應用程式可以呼叫 **CreateFile** ，並將 *dwCreationDisposition* 設定 **為 \_ 一律建立新** 檔案，即使已經存在相同名稱的檔案 (因此會覆寫現有的檔案) 。 這是否成功或不取決於前一個檔案的屬性和安全性設定等因素 (如需) 詳細資訊，請參閱下列各節。

應用程式也會使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 來指定是否要共用檔案以進行讀取、寫入、或兩者皆非。 這就是所謂的 *共用模式*。 未共用的開啟檔案 (*dwShareMode* 設為零) 無法再由開啟它的應用程式或其他應用程式重新開啟，直到其控制碼關閉為止。 這也稱為獨佔存取權。

當進程使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 嘗試開啟已在共用模式中開啟的檔案 (*dwShareMode* 設定為有效的非零) 值時，系統會將所要求的存取和共用模式，與開啟檔案時所指定的模式進行比較。 如果您指定的存取或共用模式與先前呼叫中指定的模式衝突， **CreateFile** 就會失敗。

下表說明使用各種存取模式來 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 兩個呼叫的有效組合，以及 (*dwDesiredAccess*、 *dwShareMode* 分別) 的共用模式。 進行 **CreateFile** 呼叫的順序並不重要。 不過，每個檔案控制代碼上的任何後續檔案 i/o 作業仍會受限於與該特定檔案控制代碼相關聯的目前存取和共用模式。




| 第一次呼叫<a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a> | CreateFile 的有效第二次呼叫<a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong></strong></a> | 
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>， <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 




 

除了標準檔案屬性之外，您也可以將 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構的指標包含為 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)的第四個參數，以指定安全性屬性。 不過，基礎檔案系統必須支援安全性，才能產生任何影響 (例如，NTFS 檔案系統支援它，但不) 各種 FAT 檔案系統。 如需安全性屬性的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。

建立新檔案的應用程式可以提供範本檔案的選擇性控制碼， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 會從中取得檔案屬性和擴充屬性，以建立新檔案。

## <a name="createfile-scenarios"></a>CreateFile 案例

有幾個基本案例可以使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式來初始存取檔案。 這些摘要如下所示：

-   當同名的檔案不存在時，建立新的檔案。
-   即使已經存在相同名稱的檔案，也會建立新檔案，清除其資料並開始空白。
-   只有在現有檔案存在時才會開啟，而且只有完整檔案。
-   開啟現有的檔案（如果有的話），並將它截斷為空白。
-   開啟檔案一律為：依原樣存在，如果存在，則建立新的檔案（如果不存在的話）。

這些案例是由適當使用 *dwCreationDisposition* 參數所控制。 以下是這些案例如何對應至這個參數的值，以及使用時所發生的情況的明細。

當您在使用該名稱的檔案不存在時建立或開啟新檔案 (*dwCreationDisposition* 設定為 [ **建立 \_ 新** 的]、[ **建立 \_ 永遠**] 或 [ **開啟 \_ always**) ] 時， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數會執行下列動作：

-   將 *dwFlagsAndAttributes* 指定的檔案屬性和旗標與 **檔 \_ 屬性 \_** 封存合併。
-   將檔案長度設定為零。
-   如果指定了 *hTemplateFile* 參數，則會將範本檔案提供的擴充屬性複製到新檔案 (這會覆寫先前) 指定的所有 **檔 \_ 屬性 \_ \*** 旗標。
-   設定 **bInheritHandle** 成員所指定的繼承旗標，以及 *LpSecurityAttributes* 參數的 **lpSecurityDescriptor** 成員所指定的安全描述項， ([**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構) （如果有提供的話）。

當您建立新檔案時，即使已經有相同名稱的檔案 (*dwCreationDisposition* 設定為 [ **建立 \_ 永遠**) ]， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數會執行下列動作：

-   檢查目前的檔案屬性和安全性設定是否有寫入權限，如果拒絕，則失敗。
-   結合 *dwFlagsAndAttributes* 指定的檔案屬性和旗標與 **檔 \_ 屬性 \_** 封存和現有的檔案屬性。
-   將檔案長度設定為零 (也就是說，檔案中的任何資料都無法再使用，且檔案是空的) 。
-   如果指定了 *hTemplateFile* 參數，則會將範本檔案提供的擴充屬性複製到新檔案 (這會覆寫先前) 指定的所有 **檔 \_ 屬性 \_ \*** 旗標。
-   設定 *lpSecurityAttributes* 參數的 **bInheritHandle** 成員所指定的繼承旗標 ([**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構) （如果有提供的話），但忽略 **安全性 \_ 屬性** 結構的 **lpSecurityDescriptor** 成員。
-   否則，如果 (成功，則 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)會傳回有效的控制碼) ，呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)將會產生程式碼錯誤，即使在這個特定的使用案例中，如果您想要建立 "new" (空白的) 檔案來取代現有的) 檔案，也不會造成 (錯誤。 **\_ \_**

開啟現有的檔案時 (*dwCreationDisposition* 設定為 [ **開啟 \_ 現有** 的]、[ **\_ 永遠開啟**] 或 [ **截斷 \_ 現有** 的) ] 時， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式會執行下列動作：

-   檢查目前的檔案屬性和安全性設定是否有要求的存取權，失敗（若已拒絕）。
-   將 _dwFlagsAndAttributes * 指定的檔案旗標 (檔案 **\_ 旗 \_ \** 標 _) 與現有的檔案屬性結合，並忽略) * 指定的任何檔案屬性 ( * * 檔 \_ 屬性 \_ \** _ _dwFlagsAndAttributes。
-   只有當 *dwCreationDisposition* 設定為 **截斷 \_ 現有** 的時，才會將檔案長度設定為零，否則會維護目前的檔案長度，並依原樣開啟檔案。
-   忽略 *hTemplateFile* 參數。
-   設定 *lpSecurityAttributes* 參數的 **bInheritHandle** 成員所指定的繼承旗標 ([**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構) （如果有提供的話），但忽略 **安全性 \_ 屬性** 結構的 **lpSecurityDescriptor** 成員。

## <a name="file-attributes-and-directories"></a>檔案屬性和目錄

檔案屬性是與檔案或目錄相關聯之中繼資料的一部分，而且每個屬性都有自己的用途，以及如何設定和變更的規則。 其中有些屬性只適用于檔案，有些只適用于目錄。 例如， **file \_ attribute \_ DIRECTORY** 屬性只適用于目錄：檔案系統會使用它來判斷磁片上的物件是否為目錄，但無法針對現有的檔案系統物件加以變更。

某些檔案屬性可以設定為目錄，但只有在該目錄中建立的檔案才有意義，作為預設屬性。 例如，您可以在目錄物件上設定 **檔 \_ 屬性 \_ 壓縮** 的，但因為目錄物件本身不包含任何實際的資料，所以不會真正壓縮; 不過，以這個屬性標記的目錄會告訴檔案系統將任何新增的檔案壓縮到該目錄中。 可以在目錄上設定的任何檔案屬性，也會針對新增至該目錄的新檔案進行設定，稱為 *繼承的屬性*。

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式會在建立檔案時，提供用來設定特定檔案屬性的參數。 一般而言，這些屬性是應用程式在檔案建立時最常見的使用方式，但並非所有可能的檔案屬性都可供 **CreateFile**。 某些檔案屬性需要在檔案已存在之後使用其他函式，例如 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)、 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)或 [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) 。 在 **檔 \_ 屬性 \_ 目錄** 的案例中， [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) 函數是在建立時需要的，因為 **CreateFile** 無法建立目錄。 其他需要特殊處理的檔案屬性是 **檔 \_ 屬性重新 \_ 分析 \_ 點** 和 **檔 \_ 屬性 \_ 的 \_ 稀疏** 檔案（需要 **DeviceIoControl**）。 如需詳細資訊，請參閱 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)。

如先前所述，當檔案建立時，會從檔案所在的目錄屬性讀取檔案屬性，以繼承檔案屬性。 下表摘要說明這些繼承的屬性，以及它們與 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 功能的關聯性。



| 目錄屬性狀態                                      | [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 新檔案的繼承覆寫功能      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **檔案 \_屬性 \_ 壓縮** 集。<br/>                | 沒有控制項。 使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 清除。<br/>    |
| **檔案 \_未設定屬性 \_ 壓縮** 。<br/>            | 沒有控制項。 使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 設定。<br/>      |
| **檔案 \_屬性 \_ 加密** 集。<br/>                 | 沒有控制項。 使用 [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea)。<br/>                      |
| **檔案 \_未設定屬性 \_ 加密** 。<br/>             | 可以使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)來設定。<br/>                       |
| **檔案 \_屬性 \_ 不是 \_ 內容 \_ 索引** 集。<br/>     | 沒有控制項。 使用 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) 清除。<br/> |
| **檔案 \_未 \_ 設定 \_ 內容 \_ 編制索引的屬性** 。<br/> | 沒有控制項。 使用 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) 設定。<br/>   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[存取控制](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**檔案屬性常數**](file-attribute-constants.md)
</dt> <dt>

[檔案壓縮和解壓縮](file-compression-and-decompression.md)
</dt> <dt>

[檔案加密](file-encryption.md)
</dt> <dt>

[檔案管理功能](file-management-functions.md)
</dt> <dt>

[控制碼和物件](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[處理繼承](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[開啟檔案進行讀取或寫入](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

