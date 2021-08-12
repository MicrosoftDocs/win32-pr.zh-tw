---
title: 'LB_DIR 訊息 (Winuser .h) '
description: 將名稱加入清單方塊所顯示的清單中。 訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。 LB \_ DIR 也可以在清單方塊中新增對應的磁碟機號。
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3add3c0ea14c637e0240ab296095bcc720aff9efb4c3e8e99a2f3de7019a711
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671664"
---
# <a name="lb_dir-message"></a>LB \_ DIR 訊息

將名稱加入清單方塊所顯示的清單中。 訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。 **LB \_DIR** 也可以在清單方塊中新增對應的磁碟機號。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要加入清單方塊之檔案或目錄的屬性。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                         | 意義                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**DDL \_ 封存**</dt> </dl>       | 包含封存的檔案。<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**DDL \_ 目錄**</dt> </dl> | 包含子目錄。 子目錄名稱會以方括弧括住 (\[ \]) 。<br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**DDL \_ 磁片磁碟機**</dt> </dl>          | 所有對應的磁片磁碟機都會新增至清單中。 磁片磁碟機會以 x 形式列出 \[ -  - \] ，其中 *x* 是磁碟機號。<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ 專屬**</dt> </dl> | 只包含具有指定屬性的檔案。 根據預設，即使未指定 DDL READWRITE，也會列出讀取/寫入檔案 \_ 。<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ 隱藏**</dt> </dl>          | 包含隱藏的檔案。<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ READONLY**</dt> </dl>    | 包含唯讀檔案。<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL \_ READWRITE**</dt> </dl> | 包含沒有其他屬性的讀取/寫入檔案。 這是預設值。<br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**DDL \_ 系統**</dt> </dl>          | 包含系統檔案。<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束的字串指標，指定絕對路徑、相對路徑或檔案名。 絕對路徑可以用磁碟機號開頭 (例如 d： \) 或 UNC 名稱 (例如， \\ \\ *machinename* \\ *共用*) 。

如果字串指定具有 *wParam* 參數所指定之屬性的檔案名或目錄，則會將檔案名或目錄加入至清單中。 如果檔案名或目錄名稱包含萬用字元 (？ 或 \*) ，所有符合萬用字元運算式的檔案或目錄，以及 *wParam* 參數指定的屬性都會新增至清單中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值是加入至清單中的最後一個名稱之以零為起始的索引。

如果發生錯誤，傳回值為 LB \_ ERR。 如果空間不足，無法儲存新的字串，則傳回值為 LB \_ ERRSPACE。

## <a name="remarks"></a>備註

[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。 它會保留指定的記憶體數量，讓後續的 **LB \_ DIR** 訊息可以花最短的時間。 您可以使用 *wParam* 和 *lParam* 參數的估計值。 如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。

如果 *wParam* 包含 DDL \_ 目錄旗標，而 *lParam* 指定第一層目錄的所有子目錄，例如 C： \\ TEMP \\ \* ，則清單方塊一律會包含根目錄的 ".." 專案。 即使根目錄有隱藏的或系統屬性，而且 \_ 未指定 ddl 隱藏和 ddl 系統旗標，也是如此 \_ 。 NTFS 磁片區的根目錄具有隱藏和系統屬性。

此清單會顯示長檔名（如果有的話）。

若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。 這可能會造成問題。 例如，日文 Windows 的非 Unicode 清單方塊中有重音的羅馬字元，將會出現混亂。 若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





