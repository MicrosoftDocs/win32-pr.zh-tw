---
Description: 檔案屬性是檔案系統儲存在磁片上的中繼資料值，系統會使用這些值，並可透過各種檔案 i/o Api 提供給開發人員使用。
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: '檔案屬性常數 (WinNT. h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: eae376462ae6c633be96e4434fbb782fa41c802f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976541"
---
# <a name="file-attribute-constants"></a>檔案屬性常數

檔案屬性是檔案系統儲存在磁片上的中繼資料值，系統會使用這些值，並可透過各種檔案 i/o Api 提供給開發人員使用。 如需相關 Api 和主題的清單，請參閱另請參閱一節。

## <a name="example"></a>範例
```cpp


FILE_BASIC_INFO basicInfo;
    BOOL result;

    result = GetFileInformationByHandleEx( hFile,
                                               FileBasicInfo,
                                               &basicInfo,
                                               sizeof(basicInfo));

\\...

printf("  File Attributes: ");
    PrintFileAttributes(basicInfo.FileAttributes);

\\...
VOID
PrintFileAttributes(
    ULONG FileAttributes
    )
{
    
    if (FileAttributes & FILE_ATTRIBUTE_ARCHIVE) {
        printf("Archive ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_DIRECTORY) {
        printf("Directory ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_READONLY) {
        printf("Read-Only ");
    }
}
```

範例取自 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) 。



| 常數/值                                                                                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**檔案 \_屬性 \_**</dt>封存 <dt>32 (0x20)</dt> </dl>                                                       | 作為封存檔案或目錄的檔案或目錄。 應用程式通常會使用此屬性來標示要備份或移除的檔案。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**檔案 \_屬性 \_ 壓縮**</dt> <dt>2048 (0x800)</dt> </dl>                                           | 壓縮檔案或目錄。 若為檔案，則會壓縮檔案中的所有資料。 針對目錄，新建立的檔案和子目錄預設為壓縮。<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**檔案 \_屬性 \_ 裝置**</dt> <dt>64 (0x40)</dt> </dl>                                                          | 此值已保留供系統使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**檔案 \_屬性 \_ 目錄**</dt> <dt>16 (0x10)</dt> </dl>                                                 | 識別目錄的控制碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**檔案 \_屬性 \_ 加密**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | 加密的檔案或目錄。 若為檔案，檔案中的所有資料流程都會加密。 針對目錄，加密是新建立的檔案和子目錄的預設值。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**檔案 \_屬性 \_ 隱藏**</dt> <dt>2 (0x2)</dt> </dl>                                                            | 檔案或目錄是隱藏的。 它不會包含在一般目錄清單中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**檔案 \_屬性 \_ 完整性 \_ 資料流程**</dt> <dt>32768 (0x8000)</dt> </dl>                      | 目錄或使用者資料流程已設定完整性 (只有在 ReFS 磁片區) 上支援。 它不會包含在一般目錄清單中。 如果檔案已重新命名，完整性設定就會與檔案一起保存。 如果檔案已複製，則如果來源檔案或目的地目錄具有完整性集，目的地檔案將會設定完整性。<br/> **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 在 Windows Server 2012 之前，不支援此旗標。<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**檔案 \_屬性 \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | 未設定其他屬性的檔案。 這個屬性只有在單獨使用時才有效。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**檔案 \_屬性 \_ 不是 \_ 內容 \_ 索引**</dt> <dt>8192 (0x2000)</dt> </dl>             | 檔案或目錄不是由內容索引服務編制索引。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**檔案 \_屬性 \_ 沒有 \_ 清除 \_ 資料**</dt> <dt>131072 (0x20000)</dt> </dl>                            | 背景資料完整性掃描器不會讀取的使用者資料流程 (也稱為清除程式) 。 在目錄上設定時，它只會提供繼承。 只有儲存空間和 ReFS 磁片區支援此旗標。 它不會包含在一般目錄清單中。<br/> **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 在 Windows 8 和 Windows Server 2012 之前，不支援此旗標。<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**檔案 \_屬性 \_ OFFLINE**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | 檔案的資料無法立即使用。 這個屬性工作表示檔案資料已實際移至離線儲存體。 這個屬性是由遠端存放所使用，也就是階層式存放裝置管理軟體。 應用程式不應該任意變更此屬性。<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**檔案 \_ATTRIBUTE \_ READONLY**</dt> <dt>1 (0x1)</dt> </dl>                                                      | 唯讀的檔案。 應用程式可以讀取檔案，但無法寫入或刪除檔案。 這個屬性不會在目錄中接受。 For more information, see [You cannot view or change the Read-only or the System attributes of folders in Windows Server 2003, in Windows XP, in Windows Vista or in Windows 7](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**檔案 \_\_ \_ \_ DATA \_ ACCESS**</dt> <dt>4194304 (0x400000)</dt>的屬性回收 </dl> | 當設定此屬性時，表示檔案或目錄不會在本機完全存在。 若為檔案，表示並非所有的資料都在本機儲存體上 (例如，可能會因為某些資料仍在遠端儲存體) 而很稀疏。 針對目錄，表示某些目錄內容會從另一個位置進行虛擬化。 讀取檔案/列舉目錄的成本會比平常更昂貴，例如，它會導致至少部分的檔案/目錄內容從遠端存放區中提取。 只有核心模式呼叫端可以設定此位。<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**檔案 \_\_ \_ \_ OPEN**</dt> <dt>262144 (0x40000)</dt>的屬性回收 </dl>                         | 這個屬性只會出現在目錄列舉類別中 (檔案 \_ 目錄 \_ 資訊、檔目錄 \_ \_ \_ 資訊等 ) 。 設定這個屬性時，表示檔案或目錄在本機系統上沒有實體標記法;此專案為 virtual。 開啟專案的成本會比平常更昂貴，例如，它會導致至少有部分從遠端存放區中提取。<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**檔案 \_屬性重新 \_ 分析 \_ 點**</dt> <dt>1024 (0x400)</dt> </dl>                                 | 具有相關重新分析點的檔案或目錄，或為符號連結的檔案。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**檔案 \_ATTRIBUTE \_ SPARSE \_ FILE**</dt> <dt>512 (0x200)</dt> </dl>                                        | 屬於稀疏檔案的檔案。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**檔案 \_屬性 \_ 系統**</dt> <dt>4 (0x4)</dt> </dl>                                                            | 作業系統使用的檔案或目錄，或專門使用的檔案或目錄。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**檔案 \_屬性 \_ 暫時**</dt> <dt>256 (0x100)</dt> </dl>                                               | 用於暫存儲存的檔案。 如果有足夠的可用快取記憶體，檔案系統會避免將資料寫回大量儲存空間，因為應用程式通常會在控制碼關閉之後刪除暫存檔。 在這種情況下，系統可以完全避免寫入資料。 否則，會在控制碼關閉後寫入資料。<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**檔案 \_屬性 \_ 虛擬**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | 此值已保留供系統使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>WinNT (包括 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[壓縮屬性](compression-attribute.md)
</dt> <dt>

[建立和開啟檔案](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




