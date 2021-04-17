---
title: 'DsBackupClose 函式 (Ntdsbcli) '
description: 關閉以 DsBackupOpenFile 函數開啟的備份檔案。
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- DsBackupClose 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465069"
---
# <a name="dsbackupclose-function"></a>DsBackupClose 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsBackupClose** 函式會關閉以 [**DsBackupOpenFile**](dsbackupopenfile.md)函數開啟的備份檔案。 針對每個備份控制碼，一次只能開啟一個檔案，所以此函式會關閉目前開啟的檔案。

## <a name="syntax"></a>語法


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。 下列清單列出其他可能的錯誤代碼。

<dl> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

*hbc* 無效。

</dd> <dt>

**hrInvalidHandle**
</dt> <dd>

目前未開啟任何檔案。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

