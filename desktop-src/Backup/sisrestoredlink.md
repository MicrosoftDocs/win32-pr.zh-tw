---
title: 'SisRestoredLink 函式 (Sisbkup) '
description: 傳回指定的已還原 SIS 連結所指向的通用存放區檔案或檔案的名稱。
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- SisRestoredLink 函式備份
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934103"
---
# <a name="sisrestoredlink-function"></a>SisRestoredLink 函式

**SisRestoredLink** 函式會傳回指定之已還原 SIS 連結所指向的通用存放區檔案或檔案的名稱。

## <a name="syntax"></a>語法


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sisRestoreStructure* \[在\]
</dt> <dd>

從 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)傳回的 SIS 還原結構指標。

</dd> <dt>

*restoredFileName* \[在\]
</dt> <dd>

已還原之 SIS 連結檔的完整檔案名。

</dd> <dt>

*reparseData* \[在\]
</dt> <dd>

SIS 重新分析點內容的指標。 此重新分析點包含描述已還原之 SIS 連結的資料。 若要取出檔案的重新分析點資料，請使用 [**FSCTL \_ 取得重新 \_ 分析 \_ 點**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) 控制項程式碼。

</dd> <dt>

*reparseDataSize* \[在\]
</dt> <dd>

*ReparseData* 所指向之 SIS 重新分析點的內容大小（以位元組為單位）。

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[擴展\]
</dt> <dd>

*CommonStoreFilesToRestore* 參數中列出的檔案數目。

</dd> <dt>

*commonStoreFilesToRestore* \[擴展\]
</dt> <dd>

通用存放區檔案名陣列的指標。 這些檔案應該與 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)所要求的一般存放區檔案相同的時間還原。

如果 *countOfCommonStoreFilesToRestore* 參數的值不是0， *commonStoreFilesToRestore* 參數的值將會包含要在還原 SIS 連結後還原的通用存放區檔案的名稱。 如果值為0，則會傳回一般存放區檔案一次，或是磁片區上已有這些檔案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。 呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。

## <a name="remarks"></a>備註

您應該針對已還原的每個 SIS 連結呼叫此函式。

此函式會針對每個還原作業，最多傳回一次通用存放區檔案;任何嘗試還原其他會看到相同一般存放區檔案的 SIS 連結，都不會導致傳回該一般存放區的檔案名。

這項功能不會傳回一般存放區檔案，在備份作業期間不會傳回 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) 的呼叫，前提是儲存在媒體上的 SIS 重新分析資料尚未損毀。

還原 SIS 連結時，您的還原作業應該只建立適當的稀疏檔案、將任何配置的範圍初始化，然後寫入與在備份作業期間讀取的 SIS 重新分析資料完全相同的資料。 您的還原作業務必使用未配置的範圍建立稀疏檔案，而不是以零來初始化 (或非疏鬆檔案) 。

請注意，如果通用存放區檔案仍存在於磁片上，則此函式不一定會識別備份媒體上的一組 SIS 連結所對應的通用存放區檔案。 一般存放區檔案資料流程的內容永遠不會在建立後變更，因此如果該檔案已經存在於磁片上，就不需要將它還原。

一般存放區檔案名是全域唯一的，可確保還原作業的完整性，即使它不是在備份作業已存取的相同 SIS 啟用磁片區上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Sisbkup。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Sisbkup .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> </dl>

 

