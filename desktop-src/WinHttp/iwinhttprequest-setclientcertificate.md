---
description: 選取要傳送至安全超文字傳輸通訊協定 (HTTPS) 伺服器的用戶端憑證。
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: IWinHttpRequest：： SetClientCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319859"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>IWinHttpRequest：： SetClientCertificate 方法

**SetClientCertificate** 方法會選取要傳送至安全超文字傳輸通訊協定 (HTTPS) server 的用戶端憑證。

## <a name="syntax"></a>語法


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientCertificate* \[在\]
</dt> <dd>

指定用戶端憑證的位置、 [*憑證存放區*](glossary.md)和主體。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。

## <a name="remarks"></a>備註

*ClientCertificate* 參數中指定的字串包含以反斜線分隔的憑證位置、憑證存放區和主體名稱。 如需有關憑證字串元件的詳細資訊，請參閱 [用戶端憑證](ssl-in-winhttp.md)。

憑證存放區名稱和位置是選擇性的。 但是，如果您指定憑證存放區，您也必須指定該憑證存放區的位置。 預設位置是 [目前 \_ 使用者]，預設憑證存放區為 [我的]。 空白的主旨表示應使用憑證存放區中的第一個憑證。

呼叫 **SetClientCertificate** 來選取憑證，然後再呼叫 [**send**](iwinhttprequest-send.md) 以傳送要求。

Microsoft Windows HTTP Services (WinHTTP) 不提供用戶端憑證給要求憑證進行驗證的 proxy 伺服器。

> [!Note]  
> 針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。

 

## <a name="examples"></a>範例

下列腳本範例示範如何選取要隨要求傳送的用戶端憑證。 在 **HKEY \_ 本機 \_ 電腦** 的登錄中，從登錄中的 [個人] 憑證存放區選擇具有「我的 Middle-Tier 憑證」主體的憑證。 因為此程式碼範例是 Microsoft JScript 專屬的，使用反斜線作為 escape 字元，所以需要兩個連續的反斜線來分隔憑證字串的元件。


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

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

[WinHTTP 中的 SSL](ssl-in-winhttp.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




