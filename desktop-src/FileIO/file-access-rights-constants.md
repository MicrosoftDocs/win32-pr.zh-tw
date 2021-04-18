---
description: 列出檔案和目錄的特定存取權限。
ms.assetid: c534e853-b61f-414d-befe-8d3c4bf08d22
title: '檔案存取權限常數 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf3e0a34cedbf106e2a2793b2a126a224c2f18c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971593"
---
# <a name="file-access-rights-constants"></a>檔案存取權限常數

檔案和目錄的有效存取權限包括 **刪除**、**讀取 \_ 控制**、**寫入 \_ DAC**、**寫入 \_ 擁有** 者，以及 **同步處理**[標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。 下表列出檔案和目錄的特定存取權限。



| 常數/值                                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ADD_FILE"></span><span id="file_add_file"></span><dl> <dt>**檔案 \_新增 \_**</dt>檔案 <dt>2</dt> </dl>                                      | 若為目錄，則為在目錄中建立檔案的許可權。<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span><dl> <dt>**檔案 \_新增 \_ 子目錄**</dt> <dt>4</dt> </dl>              | 若為目錄，則為建立子目錄的許可權。<br/>                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ALL_ACCESS"></span><span id="file_all_access"></span><dl> <dt>**檔案 \_所有 \_ 存取**</dt><dt></dt> </dl>                                 | 檔案的所有可能存取權限。<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span><dl> <dt>**檔案 \_附加 \_ 資料**</dt> <dt>4</dt> </dl>                             | 檔案物件的許可權，將資料附加至檔案。 針對本機檔案 (，如果指定了此旗標，但未指定檔案 **\_ 寫入 \_ 資料**，寫入作業將不會覆寫現有的資料。 ) 目錄物件的許可權，就是建立子目錄 (檔案 **\_ 新增 \_ 子目錄**) 。<br/>                                                                                        |
| <span id="FILE_CREATE_PIPE_INSTANCE"></span><span id="file_create_pipe_instance"></span><dl> <dt>**檔案 \_建立 \_ 管道 \_ 實例**</dt> <dt>4</dt> </dl> | 具名管道的建立管道的許可權。<br/>                                                                                                                                                                                                                                                                                                                           |
| <span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span><dl> <dt>**檔案 \_刪除 \_ 子**</dt> <dt>64 (0x40)</dt> </dl>                  | 若為目錄，則為刪除目錄的許可權，以及其包含的所有檔案，包括唯讀檔案。<br/>                                                                                                                                                                                                                                                              |
| <span id="FILE_EXECUTE"></span><span id="file_execute"></span><dl> <dt>**檔案 \_執行**</dt> <dt>32 (0x20)</dt> </dl>                                  | 原生程式碼檔案的執行許可權。 此存取權限提供給腳本，視腳本解譯器而定，可能會導致腳本成為可執行檔。<br/>                                                                                                                                                                                                   |
| <span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span><dl> <dt>**檔案 \_列出 \_ 目錄**</dt> <dt>1</dt> </dl>                    | 目錄的許可權，以列出目錄的內容。<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span><dl> <dt>**檔案 \_讀取 \_ 屬性**</dt> <dt>128 (0x80)</dt> </dl>        | 讀取檔案屬性的許可權。<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="FILE_READ_DATA"></span><span id="file_read_data"></span><dl> <dt>**檔案 \_讀取 \_ 資料**</dt> <dt>1</dt> </dl>                                   | 檔案物件的讀取對應檔案資料的許可權。 若為目錄物件，則為讀取對應目錄資料的許可權。<br/>                                                                                                                                                                                                                           |
| <span id="FILE_READ_EA"></span><span id="file_read_ea"></span><dl> <dt>**檔案 \_讀取 \_ EA**</dt> <dt>8</dt> </dl>                                         | 讀取擴充檔案屬性的許可權。<br/>                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_TRAVERSE"></span><span id="file_traverse"></span><dl> <dt>**檔案 \_跨越**</dt> <dt>32 (0x20)</dt> </dl>                               | 如果是目錄，則為流覽目錄的許可權。 根據預設，系統會將 **略過的「略過 \_ 遍歷 \_ 檢查**」 [許可權](/windows/desktop/SecAuthZ/privileges)指派給使用者，這會忽略 **檔案的 \_** [訪問](/windows/desktop/SecAuthZ/access-rights-and-access-masks)許可權。 如需詳細資訊，請參閱 [檔安全性和存取權限](file-security-and-access-rights.md) 中的備註。<br/> |
| <span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span><dl> <dt>**檔案 \_寫入 \_ 屬性**</dt> <dt>256 (0x100)</dt> </dl>    | 寫入檔案屬性的許可權。<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span><dl> <dt>**檔案 \_寫入 \_ 資料**</dt> <dt>2</dt> </dl>                                | 檔案物件的許可權，這是將資料寫入檔案的許可權。 若為目錄物件，則為在目錄中建立檔案的許可權， (檔案 **\_ 新增 \_** 檔案) 。<br/>                                                                                                                                                                                                                      |
| <span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span><dl> <dt>**檔案 \_寫入 \_ EA**</dt> <dt>16 (0x10)</dt> </dl>                              | 寫入擴充檔案屬性的許可權。<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="STANDARD_RIGHTS_READ"></span><span id="standard_rights_read"></span><dl> <dt>**標準 \_許可權 \_ 讀取**</dt><dt></dt> </dl>                  | 包含 **讀取 \_ 控制項**，這是在檔案或目錄物件的安全描述項中讀取資訊的許可權。 這不包含 SACL 中的資訊。<br/>                                                                                                                                                                                        |
| <span id="STANDARD_RIGHTS_WRITE"></span><span id="standard_rights_write"></span><dl> <dt>**標準 \_許可權 \_ 寫入**</dt><dt></dt> </dl>               | 與 **標準 \_ 許可權 \_ 讀取** 相同。<br/>                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>WinNT (包括 Windows .h) </dt> </dl> |



 

