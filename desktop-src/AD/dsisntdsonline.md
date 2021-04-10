---
title: 'DsIsNTDSOnline 函式 (Ntdsbcli) '
description: 判斷指定的伺服器上 Active Directory Domain Services 是否在線上。
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- DsIsNTDSOnline 函式 Active Directory
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103799"
---
# <a name="dsisntdsonline-function"></a>DsIsNTDSOnline 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsIsNTDSOnline** 函式會判斷指定的伺服器上 Active Directory Domain Services 是否在線上。

## <a name="syntax"></a>語法


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szServerName* \[在\]
</dt> <dd>

以 null 終止的字串指標，其中包含要測試之伺服器的名稱。 前面的反斜線是選擇性的。 伺服器必須是呼叫此函式的同一部電腦。 伺服器名稱不能包含任何底線 (\_) 字元。 伺服器名稱的範例是「server1」 \\ \\ 。

</dd> <dt>

*pfNTDSOnline* \[擴展\]
</dt> <dd>

接收結果之 **BOOL** 值的指標。 如果目錄服務已上線，則會收到 **TRUE** ，如果目錄服務離線，則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **S \_ OK** ，否則傳回錯誤碼。 下列清單列出可能的錯誤代碼。

<dl> <dt>

**\_拒絕存取 \_ 錯誤**
</dt> <dd>

呼叫端沒有適當的存取權限可呼叫此函式。 [**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

找不到 *szServerName* 中的伺服器、不是網域控制站，或 *szServerName* 的格式不正確。 此值定義于 Ntdsbmsg 中。

</dd> <dt>

**RPC \_ S \_ 不正確系結 \_**
</dt> <dd>

正在遠端呼叫 [**DsIsNTDSOnline**](dsisntdsonline.md) 函數，或 *szServerName* 中的伺服器不是網域控制站。

</dd> </dl>

## <a name="remarks"></a>備註

呼叫此函式之前，請先呼叫此函式，再呼叫任何目錄備份或還原功能。 目錄必須在線上，才能執行備份。 目錄必須離線才能執行還原。

這個函式只能從同時也是 *szServerName* 中所指定之目標伺服器的網域控制站呼叫。 無法從遠端呼叫這個函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsIsNTDSOnlineW** (Unicode) 和 **DsIsNTDSOnlineA** (ANSI) <br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> <dt>

[備份與還原 Active Directory 伺服器](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

