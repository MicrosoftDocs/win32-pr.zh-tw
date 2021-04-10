---
description: 刪除用於連線身分識別的使用者認證。
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: 'DeleteConnectedIdentity 函式 (Indentitystore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026098"
---
# <a name="deleteconnectedidentity-function"></a>DeleteConnectedIdentity 函式

刪除用於連線身分識別的使用者認證。

## <a name="syntax"></a>語法


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProviderHandle* \[在\]
</dt> <dd>

身分識別提供者控制碼。

</dd> <dt>

*UserToken* \[在中，選擇性\]
</dt> <dd>

已連線使用者的權杖，其帳戶將會轉換為本機帳戶。 如果 *UserToken* 不是 **Null**，則身分識別提供者會使用此權杖來載入使用者設定檔，並清除連接的狀態。 如果 *UserToken* 為 **Null**，LSA 會強制中斷連接。 身分識別提供者應清除此使用者的任何全域線上狀態，但提供者不需要清除使用者設定檔中的線上狀態。

</dd> <dt>

*UserSid* \[在\]
</dt> <dd>

已連線使用者的主要 SID。 如果 *UserToken* 不是 **Null**，這個參數就是 token 的使用者 SID。 如果 *UserToken* 為 **Null**，則會使用此參數來識別已連接的使用者，並清除該使用者的全域連接狀態。

</dd> <dt>

*IdentityUserName* \[在\]
</dt> <dd>

身分識別的使用者名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則函式會傳回 SEC \_ E \_ OK。

如果函式失敗，函數可能會傳回下列其中一個錯誤碼。



| 傳回值                                                                                               | 描述                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>狀態 \_ 不正確 \_ 參數</dt> </dl>      | 參數無效。<br/>                                                                                                                        |
| <dl> <dt>\_沒有 \_ 這類 \_ 使用者的狀態</dt> </dl>          | *UserSid* 所識別的使用者不存在、目前尚未連接，或沒有使用者名稱符合 *IdentityUserName* 的身分識別。<br/> |
| <dl> <dt>狀態 \_ 不足的 \_ 資源</dt> </dl> | 沒有足夠的記憶體可處理要求。<br/>                                                                                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Indentitystore。h</dt> </dl> |



 

 




