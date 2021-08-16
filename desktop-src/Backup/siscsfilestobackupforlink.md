---
title: 'SisCSFilesToBackupForLink 函式 (Sisbkup) '
description: 傳回描述指定 SIS 連結指向之通用存放區檔案的資訊。
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- SisCSFilesToBackupForLink 函式備份
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e39d4370e68b67a5c05c1f259c52190be3b931dd02164da191bacf879cd6cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835556"
---
# <a name="siscsfilestobackupforlink-function"></a>SisCSFilesToBackupForLink 函式

**SisCSFilesToBackupForLink** 函式會傳回描述指定 SIS 連結指向之通用存放區檔案的資訊。

## <a name="syntax"></a>語法


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sisBackupStructure* \[在\]
</dt> <dd>

從 [**SisCreateBackupStructure**](siscreatebackupstructure.md)傳回之 SIS 備份結構的指標。

</dd> <dt>

*reparseData* \[在\]
</dt> <dd>

SIS 重新分析點內容的指標。 此重新分析點包含描述 SIS 連結的資料。 若要取出檔案的重新分析點資料，請使用 [**FSCTL \_ 取得重新 \_ 分析 \_ 點**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) 控制項程式碼。

</dd> <dt>

*reparseDataSize* \[在\]
</dt> <dd>

*ReparseData* 所指向之 SIS 重新分析點的內容大小（以位元組為單位）。

</dd> <dt>

*thisFileCoNtext* \[擴展\]
</dt> <dd>

呼叫此函式的備份應用程式所提供的內容字串指標。 此內容字串的內容完全由這個備份應用程式所決定，且不會由 SIS 備份 API 來解讀。 這個參數是選擇性的;如果未使用，請將此參數的值設定為 **Null**。 在此情況下，將不會處理此參數的值。

</dd> <dt>

*matchingFileCoNtext* \[擴展\]
</dt> <dd>

在此函式的前四個參數中傳遞的資訊所識別之 SIS 連結的內容字串的雙向間接指標。 這個參數是選擇性的;如果未提供內容字串做為 *thisFileCoNtext* 參數的值，請將此參數的值設定為 **Null**。 在此情況下，將不會處理此參數的值。

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[擴展\]
</dt> <dd>

*CommonStoreFilesToBackUp* 參數中列出的檔案數目。

</dd> <dt>

*commonStoreFilesToBackUp* \[擴展\]
</dt> <dd>

檔案名陣列的指標。 這些檔案應該同時以 [**SisCreateBackupStructure**](siscreatebackupstructure.md)所要求的一般存放區檔案相同的方式進行備份。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。 呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。

## <a name="remarks"></a>備註

備份應用程式應該只針對每個要備份的 SIS 連結檔案呼叫此函數一次。

備份應用程式可以依標記的 IO 重新 \_ 分析標記 sis 來識別 sis 重新分析點 \_ \_ 。 此標記定義于 Winnt. h 中。

如果由 *reparseData* 參數的值所識別的重新分析點描述要備份之檔案的第一個實例，此函式會傳回 **Null** 做為 *matchingFileCoNtext* 參數的值，並將字串的 *commonStoreFilesToBackUp* 陣列值初始化為通用存放區檔案的名稱，或要備份的檔案。 否則，此函式會將 *matchingFileCoNtext* 參數的值設定為對應到指定檔案之第一個實例的內容字串，並將 *countOfCommonStoreFilesToBackUp* 參數的值設定為0。 如果有多個通用存放區檔案對應到指定的連結， *thisFileCoNtext* 參數的值將會是對應于陣列中傳回的第一個通用存放區檔案（commonStoreFilesToBackUp 0）的內容字串 \[ \] 。

此函式的目前版本最多隻會傳回一個通用存放區檔案，但在未來的版本中，可能會有數個常見存放區檔案支援的單一連結，例如，檔案中的每個資料流程各有一個，因此您的備份應用程式應該在每次呼叫此函式時支援多個檔案。 在任何情況下，每個備份階段最多會傳回一次通用存放區檔案。

您的備份應用程式應該備份或還原一般存放區檔案，或是以 *commonStoreFilesToBackUp* 參數中所傳回的檔案名或檔案名所識別的檔案。 無論是否有對應的一般存放區檔案，您的備份應用程式都應該備份存在於磁片上的 SIS 連結檔案，例如重新分析點和稀疏檔案，而且很可能不會填入任何範圍。 您的備份應用程式可能會立即備份或還原一般存放區檔案、延遲備份，或視需要將它們組合在一起。

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

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

