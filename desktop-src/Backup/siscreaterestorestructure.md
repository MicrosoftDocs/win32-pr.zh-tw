---
title: 'SisCreateRestoreStructure 函式 (Sisbkup) '
description: 根據提供的資訊建立 SIS 還原結構。
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- SisCreateRestoreStructure 函式備份
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e2d8ae0033659392c43fc833c66a4ed9d9b7f75790bda2822f0bd6b5db7f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173989"
---
# <a name="siscreaterestorestructure-function"></a>SisCreateRestoreStructure 函式

**SisCreateRestoreStructure** 函式會根據所提供的資訊建立 SIS 還原結構。

## <a name="syntax"></a>語法


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*volumeRoot* \[在\]
</dt> <dd>

要備份之磁片區的磁片區根目錄（不含尾端反斜線）的檔案名。 例如，指定 "C：" 而非 "C： \\ "。 磁片區不能是系統或開機磁碟區。

</dd> <dt>

*sisRestoreStructure* \[擴展\]
</dt> <dd>

傳回 SIS 還原結構。 呼叫端應該將此結構視為不透明。

</dd> <dt>

*commonStoreRootPathname* \[擴展\]
</dt> <dd>

指定之磁片區通用存放區的完整路徑名稱。 例如 "c： \\ SIS Common Store"。

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[擴展\]
</dt> <dd>

*CommonStoreFilesToRestore* 參數中列出的檔案數目。

</dd> <dt>

*commonStoreFilesToRestore* \[擴展\]
</dt> <dd>

檔案名陣列的指標，指定 SIS 用來管理指定磁片區的內部檔案清單。 這些檔案應該與 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)所要求的一般存放區檔案相同的時間還原。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。 呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。

## <a name="remarks"></a>備註

此函數會以 [**SisCreateBackupStructure**](siscreatebackupstructure.md) 在指定磁片區上建立備份環境的方式，在指定的磁片區上建立還原環境。

請注意，如果通用存放區檔案或檔案仍存在於磁片上，則此函式不一定會識別備份媒體上的一組 SIS 連結所對應的通用存放區檔案。 一般存放區檔案資料流程的內容永遠不會在建立後變更，因此如果該檔案已經存在於磁片上，就不需要將它還原。

一般存放區檔案名是全域唯一的，可確保還原作業的完整性，即使它不是在備份作業已存取的相同 SIS 啟用磁片區上。

還原作業完成之後，請呼叫 [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)，將 *commonStoreFilesToRestore* 字串陣列所使用的記憶體解除配置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Sisbkup。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Sisbkup .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisFreeBackupStructure**](sisfreebackupstructure.md)
</dt> </dl>

 

