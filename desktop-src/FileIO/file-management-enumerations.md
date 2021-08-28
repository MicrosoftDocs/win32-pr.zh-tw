---
description: 檔案管理中使用的列舉。
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: 檔案管理列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e9e75120046a63057ee70e6c92314ba5e90c0e53ae872dad7efd44fba96830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927807"
---
# <a name="file-management-enumerations"></a>檔案管理列舉

檔案管理中會使用下列列舉。

## <a name="in-this-section"></a>本節內容



| 列舉型別                                                                   | 描述                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COPYFILE2 \_ 複製 \_ 階段**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | 指出發生錯誤時複製的階段。<br/>                                                                                                                                                                           |
| [**COPYFILE2 \_ 訊息 \_ 動作**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | 由 [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) 回呼函式傳回，以指出應針對暫止的複製作業採取的動作。<br/>                                                             |
| [**COPYFILE2 \_ 訊息 \_ 類型**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | 指出傳遞至 [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine)回呼函式之 [**COPYFILE2 \_ 訊息**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message)結構中的訊息類型。<br/>                                       |
| [**CSV \_ 控制 \_ OP**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | 指定要與 [**FSCTL \_ csv \_ control**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control) 控制項程式碼搭配使用的 csv 控制作業類型。<br/>                                                                                                       |
| [**檔案 \_ 識別碼 \_ 類型**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | 檔案 [**\_ 識別碼 \_ 描述**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) 元結構中聯集的鑒別子。<br/>                                                                                                                                 |
| [**\_ \_ 依 \_ 控制碼類別的檔案資訊 \_**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | 識別應設定 [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) 應該取得或 [**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) 的檔案資訊類型。<br/>                |
| [**FINDEX \_ 資訊 \_ 層級**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | 定義與 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) 函數搭配使用的值，以指定傳回資料的資訊層級。<br/>                                                                                 |
| [**FINDEX \_ 搜尋 \_ OPS**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | 定義與 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) 函數搭配使用的值，以指定要執行之篩選的類型。<br/>                                                                                           |
| [**取得 \_ FILEEX \_ 資訊 \_ 層級**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | 定義搭配 [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) 和 [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) 函數使用的值，以指定傳回資料的資訊層級。<br/> |
| [**PRIORITY \_ 提示**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | 定義與 [**file \_ IO \_ PRIORITY \_ 提示 \_ 資訊**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info) 結構搭配使用的值，以指定檔案 i/o 作業的優先權提示。<br/>                                                      |
| [**資料流程 \_ 資訊 \_ 層級**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | 定義與 [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) 函數搭配使用的值，以指定傳回資料的資訊層級。<br/>                                                                               |



 

 

