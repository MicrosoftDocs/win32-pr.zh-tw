---
title: 'DsRestorePrepare 函式 (Ntdsbcli) '
description: 連接到指定的目錄伺服器，並將它準備好進行還原作業。
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- DsRestorePrepare 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11b844919cc459788bbd8acda722a68344ae16807e45be9bd6dcd5780b09d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191804"
---
# <a name="dsrestoreprepare-function"></a>DsRestorePrepare 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsRestorePrepare** 函式會連接到指定的目錄伺服器，並將它準備好進行還原作業。

## <a name="syntax"></a>語法


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szServerName* \[在\]
</dt> <dd>

以 null 終止的字串指標，其中包含要還原的伺服器名稱。 前面的反斜線是選擇性的。 伺服器必須是呼叫此函式的同一部電腦。 伺服器名稱不能包含任何底線 (\_) 字元。 伺服器名稱的範例是「server1」 \\ \\ 。

</dd> <dt>

*rtFlag* \[在\]
</dt> <dd>

指定要執行的還原類型。 這可以是零或下列其中一個值。

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**還原 \_ 類型 \_ 追捕**


</dt> <dd>

預設值。 還原的版本會透過標準對帳邏輯進行協調，讓還原的 DIT 可以與其他企業伺服器電腦進行同步處理。

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**還原 \_ 類型 \_ AUTHORATATIVE**


</dt> <dd>

不支援。

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**\_線上還原類型 \_**


</dt> <dd>

不支援。 當 NTDS 處於線上狀態時，就會執行還原。

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[在\]
</dt> <dd>

與要還原之備份相關聯的到期權杖指標。 當備份目錄時，會從 [**DsBackupPrepare**](dsbackupprepare.md) 函式取得此權杖。

如果此參數為 **Null**，則 *phbc* 中傳回的控制碼只能用來取得具有 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) 函數的還原目錄。 控制碼無法用於任何其他還原函數。

</dd> <dt>

*cbExpiryTokenSize* \[在\]
</dt> <dd>

包含 *pvExpiryToken* 中到期權杖的大小（以位元組為單位）。

</dd> <dt>

*phbc* \[擴展\]
</dt> <dd>

**HBC** 值的指標，此值會接收還原的控制碼。 呼叫其他目錄服務還原功能（例如 [**DsBackupOpenFile**](dsbackupopenfile.md) 和 [**DsRestoreEnd**](dsrestoreend.md)）時，會使用這個控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回標準 **HRESULT** 代碼;否則，會傳回失敗碼。

## <a name="remarks"></a>備註

**DsRestorePrepare** 函式要求呼叫端必須是伺服器上 Administrators 群組的成員。

**DsRestorePrepare** 可搭配或未提供權杖使用。 如果已提供權杖，則會檢查其是否到期，並允許在傳回的內容上執行所有作業。 如果未提供權杖，則會限制傳回的內容，而且只能用於 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) 函數。 它可能不會用於 [**DsRestoreRegister**](dsrestoreregister.md) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsRestorePrepareW** (Unicode) 和 **DsRestorePrepareA** (ANSI) <br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[還原 Active Directory 伺服器](restoring-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> </dl>

 

