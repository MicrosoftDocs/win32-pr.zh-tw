---
title: 'SisCreateBackupStructure 函式 (Sisbkup) '
description: 根據提供的資訊建立 SIS 備份結構。
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- SisCreateBackupStructure 函式備份
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655dfe09285e72b0b961f81c26d6afcc4aae53101a3b12b1bf0a9f1823a45d2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021366"
---
# <a name="siscreatebackupstructure-function"></a>SisCreateBackupStructure 函式

**SisCreateBackupStructure** 函式會根據所提供的資訊建立 SIS 備份結構。

## <a name="syntax"></a>語法


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*volumeRoot* \[在\]
</dt> <dd>

要備份之磁片區的磁片區根目錄（不含尾端反斜線）的檔案名。 例如，指定 "C：" 而非 "C： \\ "。

</dd> <dt>

*sisBackupStructure* \[擴展\]
</dt> <dd>

傳回 SIS 備份結構。

</dd> <dt>

*commonStoreRootPathname* \[擴展\]
</dt> <dd>

指定之磁片區通用存放區的完整路徑名稱。 例如 "c： \\ SIS Common Store"。

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[擴展\]
</dt> <dd>

*CommonStoreFilesToBackUp* 參數中列出的檔案數目。

</dd> <dt>

*commonStoreFilesToBackUp* \[擴展\]
</dt> <dd>

檔案名陣列的指標，指定 SIS 用來管理指定磁片區的內部檔案清單。 這些檔案應該同時以 SisCSFilesToBackupForLink 所要求的一般存放區檔案相同的方式進行備份。 [ ](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。 呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。

## <a name="remarks"></a>備註

此函式會建立 SIS 備份結構，由 SIS 備份 API 用來建立和維護磁片區上的檔案連結清單，以及連結所指向的原始檔案連結。 針對每個備份已啟用 SIS 的磁片區，應該只呼叫一次此函數。 指定磁片區中的所有檔案都應該視為一般存放區檔案，而且只有在 SIS 指出應該時，才會進行備份。

*CountOfCommonStoreFilesToBackUp* 和 *commonStoreFilesToBackUp* 參數會一起傳回必須備份的檔案清單，而不論備份的連結為何。

如果 *countOfCommonStoreFilesToBackUp* 為0，則 *CommonStoreFilesToBackUp* 可能是 **Null** 指標。 應忽略 *commonStoreFilesToBackUp* 參數的值。

備份作業完成之後，請呼叫 [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)，將 *commonStoreFilesToBackUp* 字串陣列所使用的記憶體解除配置。

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> </dl>

 

