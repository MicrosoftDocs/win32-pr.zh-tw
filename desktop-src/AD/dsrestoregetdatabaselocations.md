---
title: 'DsRestoreGetDatabaseLocations 函式 (Ntdsbcli) '
description: 取得還原作業期間應該複本備份檔的位置。
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- DsRestoreGetDatabaseLocations 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c5626e2e0dc679a4669bb5d8be8096b6ae0629aeed7c833f397b5f9bca45db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429990"
---
# <a name="dsrestoregetdatabaselocations-function"></a>DsRestoreGetDatabaseLocations 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsRestoreGetDatabaseLocations** 函式會取得還原作業期間應該複本備份檔的位置。

## <a name="syntax"></a>語法


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsRestorePrepare**](dsrestoreprepare.md) 函數取得的還原內容控制碼。

</dd> <dt>

*pszDatabaseLocationList* \[擴展\]
</dt> <dd>

字串指標的指標，該指標會以 UNC 路徑的形式接收資料庫位置清單。 這份清單會接收以雙 null 結束的單一 null 結束字串清單。

這個緩衝區是由 **DsRestoreGetDatabaseLocations** 函式所配置，且必須在呼叫 [**DsBackupFree**](dsbackupfree.md) 函式不再需要時釋放。

每個檔案名的第一個字元都包含識別名稱類型的其中一個 [**BFT 常數**](bft-constants.md) 。 **DsRestoreGetDatabaseLocations** 函式只會提供下列名稱類型。

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ 資料庫**


</dt> <dd>

應該將 NTDS 資料庫檔案複製到此檔案。 這是在執行備份時識別為 **BFT \_ NTDS \_ 資料庫** 的檔案。

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ 記錄檔 \_ 目錄**


</dt> <dd>

所有記錄檔都會複製到這個目錄。 執行備份時，會將記錄檔識別為 **BFT \_ 記錄** 檔。

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ 檢查點 \_ 目錄**


</dt> <dd>

所有修補檔都會複製到這個目錄。 執行備份時，會將修補檔案識別為 **BFT \_ 修補程式 \_** 檔案。

</dd> </dl> </dd> <dt>

*pcbSize* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，此值會接收 *pszDatabaseLocationList* 緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。 下列清單列出可能的錯誤代碼。

<dl> <dt>

**\_拒絕存取 \_ 錯誤**
</dt> <dd>

呼叫端沒有適當的存取權限可呼叫此函式。 [**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。

</dd> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

*hbc*、 *pszDatabaseLocationList* 或 *pcbSize* 無效。

</dd> <dt>

**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**
</dt> <dd>

發生記憶體配置失敗。

</dd> </dl>

## <a name="remarks"></a>備註

**DsRestoreGetDatabaseLocations** 函數可以用來取得還原目錄，而不需要存取備份的資料。 若要這樣做，請使用 **Null** 來呼叫 *PvExpiryToken* 參數的 [**DsRestorePrepare**](dsrestoreprepare.md) 。 這會導致 **DsRestorePrepare** 傳回受限的內容控制碼，此控制碼只能與 **DsRestoreGetDatabaseLocations** 函數搭配使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                        |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>                 |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Unicode 與 ANSI 名稱<br/>   | **DsRestoreGetDatabaseLocationsW** (Unicode) 和 **DsRestoreGetDatabaseLocationsA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> <dt>

[還原 Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

