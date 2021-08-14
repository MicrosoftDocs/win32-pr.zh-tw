---
title: 'DsBackupRead 函式 (Ntdsbcli) '
description: 從目前開啟的檔案將資料區塊讀入緩衝區。
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- DsBackupRead 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b5ea4da5b004bb4584eb119419b8c89658f36fed7e8c47514bae47d44e31b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430000"
---
# <a name="dsbackupread-function"></a>DsBackupRead 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsBackupRead** 函式會從目前開啟的檔案，將資料區塊讀入緩衝區。 用戶端應用程式預期會重複呼叫這個函式，直到收到整個備份檔案為止。 [**DsBackupOpenFile**](dsbackupopenfile.md)函式會提供備份檔案的整個大小。

## <a name="syntax"></a>語法


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。

</dd> <dt>

*pvBuffer* \[在\]
</dt> <dd>

接收資料之緩衝區的指標。 此緩衝區的大小必須至少為 *cbBuffer* 個位元組。

</dd> <dt>

*cbBuffer* \[在\]
</dt> <dd>

包含 *pvBuffer* 的緩衝區大小（以位元組為單位）。 此值必須是8192的倍數，且必須大於或等於24576。

</dd> <dt>

*pcbRead* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，此值會接收實際讀取的位元組數目。 這可能小於所要求的位元組數目，因為某些傳輸會將傳輸的緩衝區片段化，而不是以資料填滿整個緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。 可能的錯誤代碼包括下列各項。

<dl> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

一或多個參數無效。

</dd> <dt>

**錯誤 \_ 處理 \_ EOF**
</dt> <dd>

已達到備份檔案的結尾。

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

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

