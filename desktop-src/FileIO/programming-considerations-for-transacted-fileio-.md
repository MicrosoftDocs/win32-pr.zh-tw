---
description: 描述交易式 NTFS 的各種程式設計考慮。
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: 交易式 NTFS 的程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3150746b1cb34495178cc8318805587f3d08f17e04cb8227e95a9c52ddce3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047938"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>交易式 NTFS 的程式設計考慮

如需交易式 NTFS 的各種程式設計考慮的說明，請參閱下列各節：

-   [哪些檔案變更為交易](#which-file-changes-are-transacted)
-   [壓縮](#compression)
-   [建立檔案或目錄](#creating-a-file-or-directory)
-   [刪除檔案](#deleting-a-file)
-   [刪除目錄](#deleting-a-directory)
-   [目錄鎖定問題](#directory-locking-issues)
-   [目錄列舉](#directory-enumeration)
-   [記憶體對應檔案](#memory-mapped-files)
-   [具名資料流](#named-streams)
-   [重新命名檔案或目錄](#renaming-a-file-or-directory)
-   [重新剖析點](#reparse-points)
-   [錯誤碼](#error-codes)
-   [加密檔案系統](#encrypted-file-system)
-   [檔案 i/o 函數和交易式 NTFS](#file-io-functions-and-transactional-ntfs)
    -   [交易函數](#transacted-functions)
    -   [由 TxF 變更的檔案 i/o 函數](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>哪些檔案變更為交易

大部分的檔案變更（例如檔案內容、資料流程、重新分析點、屬性和檔案系統命名空間的變更）都會進行交易。 當交易式檔案控制代碼上進行其中一項變更時，變更會與其他交易隔離，而且如果回復交易，變更就會復原。

不會影響檔案內容、中繼資料或檔案系統命名空間的變更，例如壓縮或磁碟重組的變更，並不會進行交易。 這些變更不會與其他交易隔離，而且如果回復交易，這些變更就不會復原。

## <a name="compression"></a>壓縮

無法變更在交易中開啟之檔案的壓縮狀態。

## <a name="creating-a-file-or-directory"></a>建立檔案或目錄

在交易中建立的檔案或目錄，在目前交易以外的任何地方都看不到。 在此交易之外，任何嘗試建立具有相同名稱的檔案都會失敗並出現錯誤 **\_ 交易 \_ 衝突**，並有效地保留交易認可或回復時的檔案名。

## <a name="deleting-a-file"></a>刪除檔案

藉由呼叫 [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) 函式所刪除的檔案或目錄，將會對所有外部讀取器保持可見。

> [!Note]  
> 在交易結束之前，必須先關閉檔案的所有交易控制碼。 如果控制碼未正確關閉，就不會進行刪除。 必須先關閉檔案的所有開啟的控制碼，才能執行刪除作業的認可，以將其視為交易的一部分。 這是因為系統不會實際刪除檔案，直到它的最後一個控制碼關閉為止，即使作業不是交易式，也是 Windows 檔案 i/o 子系統的一部分。

 

## <a name="deleting-a-directory"></a>刪除目錄

藉由呼叫 [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) 函式來刪除的目錄，將會對所有外部讀取器保持可見。

> [!Note]  
> 針對交易目錄作業的開啟控制碼，在檔案上的開啟控制碼也有相同的條件約束。 如需詳細資訊，請參閱 [刪除](#deleting-a-file)檔案。

 

## <a name="directory-locking-issues"></a>目錄鎖定問題

如果在交易中修改檔案，則在交易結束之前，會將檔案路徑的所有目錄元件稱為「已釘選」以進行 *重新命名* 。 也就是說，系統會在認可或回復交易之前，防止您將其重新命名。 嘗試重新命名在進行中的交易中已修改之檔案的上階目錄，將會因為錯誤而無法 **\_ \_ 中斷 \_ 交易 \_** 相依性的錯誤而失敗。

## <a name="directory-enumeration"></a>目錄列舉

由於使用列舉的 Api （例如 [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) 和 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) 函式），在列舉進行中時，可以變更目錄的內容。

對交易以外的目錄進行的變更不會與交易隔離，而且會立即顯示在交易內。 例如，如果非交易寫入器將檔案新增至目錄，則新檔案會立即顯示在交易內，因此呼叫 [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) 或 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) 函式會傳回新的檔案。

在交易內對目錄所做的變更會被隔離，直到交易認可為止。 例如，在目錄中建立做為交易一部分的檔案。 呼叫 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) 或 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) 函數的非交易讀取器在交易認可之前，將不會看到新建立的檔案。

## <a name="memory-mapped-files"></a>記憶體對應檔案

用戶端必須呼叫 [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) 函式，關閉檔案對應物件，並在記憶體對應檔案上認可相關聯的交易之前，關閉檔案控制代碼。

## <a name="named-streams"></a>具名資料流

命名資料流程是完整的交易式，但鎖定是在檔案層級執行，而非資料流程層級。 從交易外部的寫入器嘗試修改鎖定檔案內的任何資料流程時，會收到錯誤的錯誤 **\_ 共用 \_ 違規**。

您無法在交易中重新命名次要資料流程。

## <a name="renaming-a-file-or-directory"></a>重新命名檔案或目錄

若要將檔案重新命名為交易作業，請呼叫 [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) 以移動檔案。

## <a name="reparse-points"></a>重新剖析點

重新分析點的變更是交易式的，這表示如果新的重新分析點指派給交易中的檔案，其他交易就看不到它。 同樣地，在認可之前，不會顯示現有重新分析點的變更或移除。

## <a name="error-codes"></a>錯誤碼

核心交易管理員 (KTM) 使用範圍從6700到6799的系統錯誤碼。 交易式 NTFS (TxF) 使用範圍從6800到6899的 Windows 錯誤碼。 如需詳細資訊，請參閱 Winerror.h 和系統錯誤碼 (6000-8199) 。

## <a name="encrypted-file-system"></a>加密檔案系統

TxF 不支援 EFS 檔案的作業。 您無法為交易開啟 EFS 加密檔案。 在 EFS 檔案上呼叫 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) 函式將會失敗，並 **產生 \_ \_ \_ \_ \_ 交易中不允許** 的錯誤（efs）錯誤。 同樣地，在交易中呼叫檔案的 [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) 函式將會失敗，並 **出現 \_ \_ \_ \_ \_ 交易中不允許** 的錯誤「EFS」錯誤。

## <a name="file-io-functions-and-transactional-ntfs"></a>檔案 i/o 函數和交易式 NTFS

TxF 提供採用檔案名的新交易函數，並變更採用檔案控制代碼之現有檔案 i/o API 函式的行為。

### <a name="transacted-functions"></a>交易函數

如果您未呼叫下列其中一個交易函式來取代其非交易版本，則不會交易作業：

-   [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**CreateSymbolicLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**FindFirstFileNameTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**FindFirstStreamTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**GetFullPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**GetLongPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

例如， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數現在具有交易版本： [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)。

### <a name="file-io-functions-changed-by-txf"></a>由 TxF 變更的檔案 i/o 函數

下表列出其行為受交易式 NTFS 影響的函式。 例如， [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)函式的行為會根據 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式或 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)函數所建立的 *hFile* 參數而有所不同。



| 函式                                                                                                                                                                                                                                                                                                                                                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | 在認可交易之前，應用程式應該關閉所有系結至交易的控制碼。 在認可交易之前，應用程式必須關閉以檔案 **\_ 旗標 \_ 刪除 \_ \_** 開啟的交易控制碼，以便進行刪除作業。<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | 如果有與 *hFile* 相關聯的交易，則此函式所建立的檔案對應物件將會與相同的交易相關聯。 透過此檔案對應物件的視圖所進行的修改會進行交易。 應用程式必須呼叫 [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile)、取消所有視圖的對應，並在認可交易變更之前關閉檔案對應物件的所有控制碼。<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | 如果有交易系結至檔案列舉控制碼，則傳回的檔案會受到交易隔離規則的約束。<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**FSCTL \_ 設定 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | 您無法變更 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)開啟之檔案的壓縮狀態。<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)和 [ **GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | 如果有交易系結至檔案控制代碼，則函式會傳回隔離檔案視圖的資訊。<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)和 [ **GetFileSizeEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | 如果有交易系結至檔案控制代碼，則函式會傳回隔離檔案視圖的資訊。<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | 如果磁片區支援檔案系統交易，則函式會傳回檔案以支援 *lpFileSystemFlags* 中的 **\_ \_ 交易**。<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile)和 [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | 如果有一個交易與用來建立所對應之檔案對應物件的檔案控制代碼相關聯，則相關聯的視圖會是交易式的。 如果使用 view 來對檔案進行交易變更，則使用者必須呼叫 [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile)、關閉檔案對應物件，並在認可相關聯的交易之前關閉檔案控制代碼。<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | 如果有交易系結至目錄控制碼，則通知會反映目錄的隔離模式。 對目錄的交易視圖以外的檔案進行變更時，不會包含在通知中。<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)、 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)和 [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | 如果有交易系結至檔案控制代碼，則函式會從檔案的交易視圖傳回資料。 交易讀取控制碼保證會在控制碼期間顯示相同的檔案視圖。<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | 如果有交易系結至控制碼，則檔案結尾位置的變更就會經過交易。<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | 如果有交易系結至控制碼，則所做的變更將會針對資訊類別 **FileBasicInfo**、 **FileRenameInfo**、 **FileAllocationInfo**、 **FileEndOfFileInfo** 和 **FileDispositionInfo** 進行交易。<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**SetFileShortName**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | 如果有交易系結至控制碼，則檔案簡短名稱中的變更就會經過交易。<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | 如果有交易系結至控制碼，檔案時間的變更就會經過交易。<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)、 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)和 [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | 如果有交易系結至檔案控制代碼，就會將檔案寫入交易。<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

