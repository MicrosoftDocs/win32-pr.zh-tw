---
title: 'DsBackupTruncateLogs 函式 (Ntdsbcli) '
description: 截斷先前讀取的備份記錄。
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- DsBackupTruncateLogs 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef435214248d8b7972e62419ce60626f7dd6ec9f6dc27a8813598e623d7a156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191844"
---
# <a name="dsbackuptruncatelogs-function"></a>DsBackupTruncateLogs 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsBackupTruncateLogs** 函式會截斷先前讀取的備份記錄。

## <a name="syntax"></a>語法


```C++
HRESULT DsBackupTruncateLogs(
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

**\_拒絕存取 \_ 錯誤**
</dt> <dd>

呼叫端沒有適當的存取權限可呼叫此函式。 [**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。

</dd> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

*hbc* 無效。

</dd> </dl>

## <a name="remarks"></a>備註

當完整或增量備份順利完成時，請使用 **DsBackupTruncateLogs** 函數。

> [!Caution]  
> 如果在差異備份之後呼叫這個函式，將會遺失所有增量備份資訊。

 

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

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**DsSetCurrentBackupLog**](dssetcurrentbackuplog.md)
</dt> <dt>

[備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

