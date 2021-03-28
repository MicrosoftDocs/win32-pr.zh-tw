---
description: IUserIdentityManager：： ManageIdentities 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'IUserIdentityManager：： ManageIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317951"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>IUserIdentityManager：： ManageIdentities 方法

\[**IUserIdentityManager：： ManageIdentities** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

向使用者顯示 UI，讓使用者可以管理使用者身分識別。

## <a name="syntax"></a>語法


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

**HWND** 值，這個值會識別在關閉 UI 之後將會進入前景的視窗。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

類型： **DWORD**

定義 UI 行為方式的選擇性旗標。 設定為 UIMI \_ 建立 \_ 新 \_ 的身分識別，以提示使用者建立新的身分識別。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

管理作業的結果。 如果成功，則會傳回 \_ [確定]。 否則，它會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                            | Description                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E 身分識別 \_ \_ 已停用**</dt> </dl> | 系統上的身分識別管理已停用。<br/> |
| <dl> <dt>**E \_ 使用者已 \_ 取消**</dt> </dl>      | 使用者已取消對話方塊。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager：： Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager：：登出**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




