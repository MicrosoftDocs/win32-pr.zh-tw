---
title: 'DsRestoreRegister 函式 (Ntdsbcli) '
description: 註冊還原作業。
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- DsRestoreRegister 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e878a5d2b9567ae7a483344a2240d3480620ea00706db1ed0c834fd2c5553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962457"
---
# <a name="dsrestoreregister-function"></a>DsRestoreRegister 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsRestoreRegister** 函數會註冊還原作業。此函式會 interlocks 所有後續的還原作業，並防止還原目標啟動，直到呼叫 [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)函數為止。

## <a name="syntax"></a>語法


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsRestorePrepare**](dsrestoreprepare.md) 函數取得的還原內容控制碼。

</dd> <dt>

*szCheckPointFilePath* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含檢查點檔案的路徑。 此路徑是由 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)函式所提供，且具有 **BFT \_ 檢查點 \_ 目錄** 的 **BFT** 值。 這通常與系統資料庫路徑相同。 這是正確的備份還原功能所需的路徑。 此參數不可以是 **Null**。 在此參數中傳遞 **Null** 會在還原過程中造成錯誤。

</dd> <dt>

*szLogPath* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含將還原記錄檔的路徑。 此路徑是由 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)函式所提供，且具有 **BFT 記錄檔 \_ \_ 目錄** 的 **BFT** 值。 如果路徑指向空白目錄，就會在該處建立新的記錄檔。 此參數不可以是 **Null**。

</dd> <dt>

*rgrstmap* \[在\]
</dt> <dd>

[**EDB \_ RSTMAP**](edb-rstmap.md)結構的陣列，其中包含每個資料庫的舊路徑和新路徑。 每個資料庫都有一個結構。 針對目錄，有一個適用于系統資料庫的結構，還有另一個適用于目錄資料庫的結構。 陣列中的元素順序並不重要。 *Crstmap* 參數包含陣列中的元素數目。

</dd> <dt>

*crstmap* \[在\]
</dt> <dd>

包含 *rgrstmap* 陣列中的元素數目。

</dd> <dt>

*szBackupLogPath* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含備份記錄檔目前所在的路徑。 此參數不可以是 **Null**。

</dd> <dt>

*genLow* \[在\]
</dt> <dd>

包含此還原會話中要還原的最低記錄檔編號。 這是從0x00000 到0xFFFFF 的範圍內的十六進位數位。

</dd> <dt>

*genHigh* \[在\]
</dt> <dd>

包含此還原會話中要還原的最高記錄檔編號。 這是從0x00000 到0xFFFFF 的範圍內的十六進位數位。

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

一或多個參數無效。

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

提供給 [**DsRestorePrepare**](dsrestoreprepare.md) 的到期權杖無效。 此值定義于 Ntdsbmsg 中。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsRestoreRegisterW** (Unicode) 和 **DsRestoreRegisterA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> <dt>

[**EDB \_ RSTMAP**](edb-rstmap.md)
</dt> <dt>

[還原 Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

