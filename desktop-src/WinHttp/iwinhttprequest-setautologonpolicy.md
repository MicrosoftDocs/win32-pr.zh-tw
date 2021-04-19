---
description: 設定目前的自動登入原則。
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: IWinHttpRequest：： SetAutoLogonPolicy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991902"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>IWinHttpRequest：： SetAutoLogonPolicy 方法

**SetAutoLogonPolicy** 方法會設定目前的 [自動登入原則](authentication-in-winhttp.md)。

## <a name="syntax"></a>語法


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AutoLogonPolicy* \[在\]
</dt> <dd>

指定目前的自動登入原則。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。

## <a name="remarks"></a>備註

預設原則是 [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md)。

呼叫 **SetAutoLogonPolicy** ，在呼叫 [**send**](iwinhttprequest-send.md) 以傳送要求之前，設定自動登入原則。

> [!Note]  
> 針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。

 

## <a name="examples"></a>範例

下列腳本範例示範如何將自動登入原則設定為永遠不會使用 NTLM 或協商驗證。


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WinHTTP .lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP 中的驗證](authentication-in-winhttp.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




