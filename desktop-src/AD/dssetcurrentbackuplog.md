---
title: 'DsSetCurrentBackupLog 函式 (Ntdsbcli) '
description: 設定成功還原後的目前備份記錄檔編號。
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- DsSetCurrentBackupLog 函式 Active Directory
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843828"
---
# <a name="dssetcurrentbackuplog-function"></a>DsSetCurrentBackupLog 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsSetCurrentBackupLog** 函式會在成功還原之後設定目前的備份記錄檔編號。 由於 Active Directory Domain Services 僅支援迴圈記錄，因此通常不會使用此函數。

## <a name="syntax"></a>語法


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szServerName* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含要設定備份記錄檔編號的伺服器名稱。 前面的反斜線是選擇性的。 伺服器必須是呼叫此函式的同一部電腦。 伺服器名稱不能包含任何底線 (\_) 字元。 伺服器名稱的範例是「server1」 \\ \\ 。

</dd> <dt>

*dwCurrentLog* \[在\]
</dt> <dd>

包含要設定的備份記錄檔編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。 下列清單列出可能的錯誤代碼。

<dl> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

一或多個參數無效。

</dd> <dt>

**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**
</dt> <dd>

發生記憶體配置失敗。

</dd> </dl>

## <a name="remarks"></a>備註

通常不需要呼叫 **DsSetCurrentBackupLog** 函數。 備份功能會自動判斷並設定最後備份的記錄檔編號。 您可以使用 **DsSetCurrentBackupLog** 來防止另一個增量備份在執行完整備份之前進行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsSetCurrentBackupLogW** (Unicode) 和 **DsSetCurrentBackupLogA** (ANSI) <br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[備份與還原 Active Directory 伺服器](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

