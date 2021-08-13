---
title: 'DsBackupGetBackupLogs 函式 (Ntdsbcli) '
description: 取得必須針對指定的備份內容備份的記錄檔清單。
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- DsBackupGetBackupLogs 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a240ef514fc62450a04f512f04d985380b79fa20daaee9ff4b27ccb71027a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430100"
---
# <a name="dsbackupgetbackuplogs-function"></a>DsBackupGetBackupLogs 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsBackupGetBackupLogs** 函數會取得必須針對指定的備份內容備份的記錄檔清單。

## <a name="syntax"></a>語法


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。

</dd> <dt>

*pszBackupLogFiles* \[擴展\]
</dt> <dd>

字串指標的指標，該指標會以 UNC 路徑的形式接收記錄檔名稱的清單。 在呼叫 **DsBackupGetBackupLogs** 之前，將此值初始化為 **Null** 。

這份清單會接收以雙 null 結束的單一 null 結束字串清單。

這個緩衝區是由 **DsBackupGetBackupLogs** 函式所配置，且必須在呼叫 [**DsBackupFree**](dsbackupfree.md) 函式不再需要時釋放。

每個檔案名的第一個字元都包含識別名稱類型的其中一個 [**BFT 常數**](bft-constants.md) 。

</dd> <dt>

*pcbSize* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，此值會接收 *pszBackupLogFiles* 緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。 下列清單列出其他可能的錯誤代碼。

<dl> <dt>

**\_拒絕存取 \_ 錯誤**
</dt> <dd>

呼叫端沒有適當的存取權限可呼叫此函式。 [**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。

</dd> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

*hbc*、 *pszBackupLogFiles* 或 *pcbSize* 無效。

</dd> <dt>

**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**
</dt> <dd>

發生記憶體配置失敗。

</dd> </dl>

## <a name="remarks"></a>備註

**DsBackupGetBackupLogs** 函數會提供備份所需的記錄檔清單。 完整備份是由 [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) 函數和記錄檔所提供的資料庫檔案所組成。 不支援 Active Directory 伺服器的增量備份。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsBackupGetBackupLogsW** (Unicode) 和 **DsBackupGetBackupLogsA** (ANSI) <br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**BFT 常數**](bft-constants.md)
</dt> <dt>

[備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

