---
title: 'DsRestoreEnd 函式 (Ntdsbcli) '
description: 呼叫以終止還原作業。
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- DsRestoreEnd 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025003"
---
# <a name="dsrestoreend-function"></a>DsRestoreEnd 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 改為使用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

呼叫 **DsRestoreEnd** 函數，以終止還原作業。

## <a name="syntax"></a>語法


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hbc* \[在\]
</dt> <dd>

包含使用 [**DsRestorePrepare**](dsrestoreprepare.md) 函數取得的還原內容控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。 下列清單列出可能的錯誤代碼。

<dl> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> <dd>

*hbc* 無效。

</dd> </dl>

## <a name="remarks"></a>備註

**DsRestoreEnd** 函式會關閉未完成的系結控制碼，並在嘗試還原之後執行清除作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                               |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                               |
| 伺服器支援結束<br/>    | 都不支援<br/>                                                               |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[還原 Active Directory 伺服器](restoring-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

