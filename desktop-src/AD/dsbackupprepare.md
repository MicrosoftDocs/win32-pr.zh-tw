---
title: 'DsBackupPrepare 函式 (Ntdsbcli) '
description: 準備指定伺服器上的目錄以進行線上備份，並傳回後續呼叫其他備份函式時所使用的備份內容控制碼。
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- DsBackupPrepare 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea1f24c6cbf3f05ce69d8a71900bfe4d1b08899b98590dc75410b9d5ed92d90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191834"
---
# <a name="dsbackupprepare-function"></a>DsBackupPrepare 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsBackupPrepare** 函式會在指定的伺服器上準備線上備份的目錄，並傳回後續呼叫其他備份函式時所使用的備份內容控制碼。

## <a name="syntax"></a>語法


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szBackupServer* \[在\]
</dt> <dd>

以 null 終止的字串指標，其中包含要備份的伺服器名稱。 前面的反斜線是選擇性的。 伺服器必須是呼叫此函式的同一部電腦。 伺服器名稱不能包含底線 (\_) 字元。 伺服器名稱的範例是「server1」 \\ \\ 。

</dd> <dt>

*grbit* \[在\]
</dt> <dd>

判斷是否會備份記錄檔。 此值應該一律為0，因為不支援增量備份。

</dd> <dt>

*btBackupType* \[在\]
</dt> <dd>

指定備份的類型。 這可以是下列其中一個值。

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**備份 \_ 類型已 \_ 滿**


</dt> <dd>

指定完整備份。 備份) 的完整目錄 (DIT、記錄檔和更新檔案。 備份所有資料，並截斷交易記錄檔。 只支援完整備份。

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_僅備份類型 \_ 記錄 \_**


</dt> <dd>

不支援這個值。 指定只備份資料庫記錄，而不是資料庫本身。 這通常會在執行差異或增量備份時使用。

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**備份 \_ 類型 \_ 增量**


</dt> <dd>

不支援這個值。 **DsBackupPrepare** 傳回 **錯誤 \_ 不正確 \_ 參數**。

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[擴展\]
</dt> <dd>

**PVOID** 值的指標，此值會接收與此備份相關聯的到期權杖指標。 *pcbExpiryTokenSize* 會接收此資料的大小（以位元組為單位）。 呼叫端必須儲存此權杖的內容與備份，因為在嘗試還原資料時，權杖必須傳遞至 [**DsRestorePrepare**](dsrestoreprepare.md) 。 儲存並不再需要權杖之後，呼叫端應該使用 [**DsBackupFree**](dsbackupfree.md)釋放配置的記憶體。

</dd> <dt>

*pcbExpiryTokenSize* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，此值會接收 *ppvExpiryToken* 中權杖的大小（以位元組為單位）。

</dd> <dt>

*phbc* \[擴展\]
</dt> <dd>

**HBC** 值的指標，此值會接收備份的控制碼。 呼叫其他目錄服務備份功能（例如 [**DsBackupOpenFile**](dsbackupopenfile.md) 和 [**DsBackupEnd**](dsbackupend.md)）時，會使用這個控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回錯誤碼。 下列清單列出其他可能的錯誤代碼。

<dl> <dt>

**\_拒絕存取 \_ 錯誤**
</dt> <dd>

呼叫端沒有適當的存取權限可呼叫此函式。 [**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。

</dd> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

*szBackupServer* 或 *phbcBackupCoNtext* 無效。

</dd> <dt>

**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**
</dt> <dd>

發生記憶體配置失敗。

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

找不到 *szBackupServer* 中的伺服器、不是網域控制站，或 *szBackupServer* 的格式不正確。 此值定義于 ntdsbmsg 中。

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* 和/或 *pcbExpiryTokenSize* 無效。 此值定義于 Ntdsbmsg 中。

</dd> <dt>

**RPC \_ S \_ 不正確系結 \_**
</dt> <dd>

此函數會從遠端呼叫，或 *szServerName* 中的伺服器不是網域控制站。

</dd> </dl>

## <a name="remarks"></a>備註

此函式需要呼叫端具有 **SE \_ 備份 \_ 名稱** 許可權。 [**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來變更用來呼叫此函數的安全性內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsBackupPrepareW** (Unicode) 和 **DsBackupPrepareA** (ANSI) <br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupEnd**](dsbackupend.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

