---
description: IUserIdentityManager：： Logon 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'IUserIdentityManager：： Logon 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: e5be9402dbbbf7c46528ceeab944317fa35857f9521db41b621ab246c8da86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821128"
---
# <a name="iuseridentitymanagerlogon-method"></a>IUserIdentityManager：： Logon 方法

\[**IUserIdentityManager：： Logon** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

向使用者顯示 UI，讓使用者可以選擇使用者身分識別。 如果成功，將會登入並取出使用者身分識別。

## <a name="syntax"></a>語法


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

**HWND** 值，這個值會識別在關閉登入 UI 之後將會帶入前景的視窗。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

類型： **DWORD**

定義 UI 行為方式的選擇性旗標。 設定為 UIL \_ 強制 \_ ui 以強制 ui 顯示，即使已經選擇身分識別也一樣。

</dd> <dt>

*ppIdentity* \[擴展\]
</dt> <dd>

類型： **[ **IUserIdentity**](iuseridentity.md)\*\***

接收所選使用者識別之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

登入操作的結果。 如果成功，則會傳回 \_ [確定]。 否則，它會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                            | 描述                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ 使用者已 \_ 取消**</dt> </dl>      | 使用者已從 UI 取消登入操作。<br/>                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | 無法建立使用者身分識別。<br/>                                          |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>           | 作業意外失敗。<br/>                                               |
| <dl> <dt>**E 身分識別 \_ \_ 已停用**</dt> </dl> | 系統上的身分識別管理已停用。<br/>                                   |
| <dl> <dt>**S 身分識別 \_ \_ 已停用**</dt> </dl> | 系統上的身分識別管理已停用。<br/>                                   |
| <dl> <dt>**E 身分 \_ 識別 \_ 變更**</dt> </dl>   | 系統目前正在切換身分識別，因此無法完成操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager：：登出**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




