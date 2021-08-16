---
title: 'DsBackupGetDatabaseNames 函式 (Ntdsbcli) '
description: 取得要針對指定的備份內容備份的資料庫檔案清單。
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- DsBackupGetDatabaseNames 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620ad77f84aa2cb52a7bd99a96a22e7de560b53b2c3ba2022598609dde3737fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191854"
---
# <a name="dsbackupgetdatabasenames-function"></a>DsBackupGetDatabaseNames 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsBackupGetDatabaseNames** 函式會取得要針對指定的備份內容備份的資料庫檔案清單。

## <a name="syntax"></a>語法


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。

</dd> <dt>

*pszAttachmentInfo* \[擴展\]
</dt> <dd>

字串指標的指標，該指標會以 UNC 路徑的形式接收資料庫檔案名的清單。 在呼叫 **DsBackupGetDatabaseNames** 之前，必須將此值初始化為 **Null** 。

這份清單會接收以雙 null 結束的單一 null 結束字串清單。

這個緩衝區是由 **DsBackupGetDatabaseNames** 函式所配置，且必須在呼叫 [**DsBackupFree**](dsbackupfree.md) 函式不再需要時釋放。

每個檔案名的第一個字元都包含一個識別名稱類型的 [**BFT 常數**](bft-constants.md) 。 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)函數只會提供下列類型的名稱。

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ 資料庫**


</dt> <dd>

檔案是 NTDS 資料庫檔案。 當還原資料時，應該將此檔案複製到識別為 **BFT \_ NTDS \_ 資料庫** 的檔案。

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ 記錄檔**


</dt> <dd>

檔案是記錄檔。 還原資料時，會將所有記錄檔複製到識別為 **BFT \_ 記錄 \_** 檔的目錄。

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT \_ 修補 \_ 檔案**


</dt> <dd>

檔案是修補檔案。 還原資料時，會將所有修補檔案複製到識別為 **BFT \_ 檢查點 \_** 目錄的目錄。

</dd> </dl> </dd> <dt>

*pcbSize* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，此值會接收 *pszAttachmentInfo* 緩衝區的大小（以位元組為單位）。

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

*hbc*、 *pszAttachmentInfo* 或 *pcbSize* 無效。

</dd> <dt>

**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**
</dt> <dd>

發生記憶體配置失敗。

</dd> </dl>

## <a name="remarks"></a>備註

**DsBackupGetDatabaseNames** 函數會提供備份所需的資料庫檔案清單。 完整備份是由 [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) 函數所提供的資料庫檔案和記錄檔所組成。 不支援 Active Directory 伺服器的增量備份。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Unicode 與 ANSI 名稱<br/>   | **DsBackupGetDatabaseNamesW** (Unicode) 和 **DsBackupGetDatabaseNamesA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**BFT 常數**](bft-constants.md)
</dt> <dt>

[備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

