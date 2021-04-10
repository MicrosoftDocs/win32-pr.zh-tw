---
title: 'SisRestoredCommonStoreFile 函式 (Sisbkup) '
description: 報告已寫入一般存放區檔案的 SIS 架構。
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- SisRestoredCommonStoreFile 函式備份
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934104"
---
# <a name="sisrestoredcommonstorefile-function"></a>SisRestoredCommonStoreFile 函式

**SisRestoredCommonStoreFile** 函式會向已寫入一般存放區檔案的 SIS 架構報告。

## <a name="syntax"></a>語法


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sisRestoreStructure* \[在\]
</dt> <dd>

從 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)傳回的 SIS 還原結構指標。

</dd> <dt>

*commonStoreFileName* \[在\]
</dt> <dd>

已還原之一般存放區檔案的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。 呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。

## <a name="remarks"></a>備註

當您還原一般存放區檔案之後，應該呼叫此函式。 它會通知 SIS 架構已撰寫新的一般存放區檔案，以便 SIS 架構可以執行內部維護工作，例如初始化其內部資料結構或修正一般存放區檔案的連結。

您的還原作業應該只還原 [**SisRestoredLink**](sisrestoredlink.md)所報告的一般存放區檔案，即使備份媒體上有其他一般存放區檔案也一樣。 您的還原作業可以依所選的任何順序還原 SIS 連結和一般存放區檔案;不過，它必須在還原任何連結之後呼叫 **SisRestoredLink** ，而且它必須在還原任何一般存放區檔案之後呼叫此函式。 由於還原作業無法識別將會還原的一般存放區檔案，直到將檔案名回報給它，因為還原連結之後，您的還原作業將一律會還原一般存放區檔案，但至少有一個連結指向它會還原。 不過，您可以接著還原指向該一般存放區檔案的其他 SIS 連結。

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

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

