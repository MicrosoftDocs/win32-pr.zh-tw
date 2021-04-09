---
title: 'CB_DIR 訊息 (Winuser .h) '
description: 將名稱新增至下拉式方塊所顯示的清單。 訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。 CB \_ DIR 也可以將對應的磁碟機號新增至清單。
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR message Windows 控制項
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843576"
---
# <a name="cb_dir-message"></a>CB \_ DIR 訊息

將名稱新增至下拉式方塊所顯示的清單。 訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。 **CB \_DIR** 也可以將對應的磁碟機號新增至清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要加入至下拉式方塊之檔案或目錄的屬性。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                         | 意義                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**DDL \_ 封存**</dt> </dl>       | 包含封存的檔案。<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**DDL \_ 目錄**</dt> </dl> | 包含子目錄，以方括弧括住 (\[ \]) 。<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**DDL \_ 磁片磁碟機**</dt> </dl>          | 所有對應的磁片磁碟機都會新增至清單中。 磁片磁碟機會以 x 形式列出 \[ -  - \] ，其中 *x* 是磁碟機號。<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ 專屬**</dt> </dl> | 只包含具有指定屬性的檔案。 根據預設，即使未指定 DDL READWRITE，也會列出讀取/寫入檔案 \_ 。<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ 隱藏**</dt> </dl>          | 包含隱藏的檔案。<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ READONLY**</dt> </dl>    | 包含唯讀檔案。<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL \_ READWRITE**</dt> </dl> | 包含沒有其他屬性的讀取/寫入檔案。 此為預設值。<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**DDL \_ 系統**</dt> </dl>          | 包含系統檔案。<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

**LPCTSTR** 指標，指向以 null 終止的字串，這個字串會指定絕對路徑、相對路徑或檔案名。 絕對路徑可以用磁碟機號開頭 (例如 d： \) 或 UNC 名稱 (例如， \\ \\ *machinename* \\ *共用*) 。 如果字串指定具有 *wParam* 參數所指定之屬性的檔案名或目錄，則會將檔案名或目錄加入至清單中。 如果檔案名或目錄名稱中包含萬用字元 (？ 或 \*) ，所有符合萬用字元運算式的檔案或目錄，以及 *wParam* 參數指定的屬性，都會新增至下拉式方塊中顯示的清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值是加入至清單中的最後一個名稱之以零為起始的索引。

如果發生錯誤，傳回值會是 CB \_ ERR。 如果空間不足，無法儲存新的字串，則傳回值為 CB \_ ERRSPACE。

## <a name="remarks"></a>備註

如果 *wParam* 包含 DDL \_ 目錄旗標，而 *lParam* 指定第一層目錄的所有子目錄，例如 C： \\ TEMP \\ \* ，則清單方塊一律會包含根目錄的 ".." 專案。 即使根目錄有隱藏的或系統屬性，而且 \_ 未指定 ddl 隱藏和 ddl 系統旗標，也是如此 \_ 。 NTFS 磁片區的根目錄具有隱藏和系統屬性。

此清單會顯示長檔名（如果有的話）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





