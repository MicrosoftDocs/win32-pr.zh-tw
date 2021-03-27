---
description: 在嚮導中啟用裝載的伺服器端頁面，以確認使用者已通過 Microsoft 帳戶驗證。
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: 'NewWDEvents. PassportAuthenticate 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695651"
---
# <a name="newwdeventspassportauthenticate-method"></a>NewWDEvents. PassportAuthenticate 方法

在嚮導中啟用裝載的伺服器端頁面，以確認使用者已通過 Microsoft 帳戶驗證。

## <a name="syntax"></a>語法


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrSignInUrl* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

字串，包含重新導向至 Microsoft 帳戶的登入 UI 之網頁的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **布林值**

如果驗證成功，則設定為 **true** ，否則為 **false** 。

## <a name="remarks"></a>備註

即使使用者已登入 Microsoft 帳戶，也可以呼叫這個方法。 在此情況下，方法會傳回 **true** ，而不會在 UI 上顯示 Microsoft 帳戶的登入。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (6.0 版或更新版本) </dt> </dl> |



 

 
