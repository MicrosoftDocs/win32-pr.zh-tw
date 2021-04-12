---
title: 'DsBackupOpenFile 函式 (Ntdsbcli) '
description: 開啟指定的檔案，並執行準備檔案以進行備份所需的用戶端和伺服器作業。
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- DsBackupOpenFile 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104057"
---
# <a name="dsbackupopenfile-function"></a>DsBackupOpenFile 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsBackupOpenFile** 函式會開啟指定的檔案，並執行準備檔案以進行備份所需的用戶端和伺服器作業。

## <a name="syntax"></a>語法


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。

</dd> <dt>

*szAttachmentName* \[在\]
</dt> <dd>

指標，指向以 null 終止的字串，指定要開啟之備份檔案的名稱。

</dd> <dt>

*cbReadHintSize* \[在\]
</dt> <dd>

包含在 [**DsBackupRead**](dsbackupread.md)函數中傳遞為 *pvBuffer* 引數的緩衝區可能大小（以位元組為單位）。 備份函式會使用此值作為將網路流量優化的提示。 此值必須是8192的倍數，且必須大於或等於24576。

</dd> <dt>

*pliFileSize* \[擴展\]
</dt> <dd>

以位元組為單位的 **大型 \_ 整數** 值的指標，此值會接收備份檔案的大小（以位元組為單位）。

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

*hbc*、 *szAttachmentName* 或 *pliFileSize* 無效。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsBackupOpenFileW** (Unicode) 和 **DsBackupOpenFileA** (ANSI) <br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

