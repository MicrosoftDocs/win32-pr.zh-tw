---
title: 'SisFreeAllocatedMemory 函式 (Sisbkup) '
description: 釋出 SIS API 函數所配置的記憶體。
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- SisFreeAllocatedMemory 函式備份
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4510e464c2201952823d144721614caa7b5f1397c68f4f129dac73a4015b86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702178"
---
# <a name="sisfreeallocatedmemory-function"></a>SisFreeAllocatedMemory 函式

**SisFreeAllocatedMemory** 函式會釋出 SIS API 函式所配置的記憶體。

## <a name="syntax"></a>語法


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*allocatedSpace* \[在\]
</dt> <dd>

SIS API 所配置之記憶體的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

呼叫此函式完成之後，呼叫端就無法再存取釋放的記憶體。

此呼叫應該用來解除配置針對 [**SisCreateBackupStructure**](siscreatebackupstructure.md)和 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)所傳回之 *commonStoreRootPathname* 參數字串所配置的記憶體，以及包含從 **SisCreateBackupStructure**、 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)、 **SisCreateRestoreStructure** 和 [**SisRestoredLink**](sisrestoredlink.md)傳回之一般存放區檔案名的字串陣列。 在後者的情況下，也必須藉由呼叫 **SisFreeAllocatedMemory** 來釋放陣列本身。

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

 





