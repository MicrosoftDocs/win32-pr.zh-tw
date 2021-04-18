---
description: IWinHttpRequest 介面提供 Microsoft Windows HTTP Services (WinHTTP) 的所有 nonevent 方法。
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: IWinHttpRequest 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193072"
---
# <a name="iwinhttprequest-interface"></a>IWinHttpRequest 介面

**IWinHttpRequest** 介面提供 [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md)的所有 nonevent 方法。

## <a name="members"></a>成員

**IWinHttpRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWinHttpRequest** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWinHttpRequest** 介面具有這些方法。



| 方法                                                                 | 描述                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**中止**](iwinhttprequest-abort.md)                                 | 中止 [WinHTTP](about-winhttp.md) [**傳送**](iwinhttprequest-send.md) 方法。<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | 抓取所有 HTTP 回應標頭。<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | 抓取 HTTP 回應標頭。<br/>                                                                                         |
| [**打開**](iwinhttprequest-open.md)                                   | 開啟 HTTP 資源的 HTTP 連接。<br/>                                                                                |
| [**傳送**](iwinhttprequest-send.md)                                   | 將 HTTP 要求傳送至 HTTP 伺服器。<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | 設定目前的 [自動登入原則](authentication-in-winhttp.md)。<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | 選取要傳送至安全超文字傳輸通訊協定 (HTTPS) 伺服器的用戶端憑證。<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | 設定要用於 HTTP 伺服器的認證，也就是 proxy 伺服器或源伺服器。<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | 設定 proxy 伺服器資訊。<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | 新增、變更或刪除 HTTP 要求標頭。<br/>                                                                            |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | 指定傳送/接收作業的個別超時元件（以毫秒為單位）。<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | 使用選擇性的超時值（以秒為單位），等候非同步 [**傳送**](iwinhttprequest-send.md) 方法完成。<br/> |



 

### <a name="properties"></a>屬性

**IWinHttpRequest** 介面具有這些屬性。



| 屬性                                                            | 存取類型           | Description                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**選項**](iwinhttprequest-option.md)<br/>                 | 讀取/寫入<br/> | WinHTTP 選項值。<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | 唯讀<br/>  | 以不帶正負號的位元組陣列形式的回應實體主體。<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | 唯讀<br/>  | 作為 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)的回應實體主體。<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | 唯讀<br/>  | 回應實體主體。<br/>                                  |
| [**狀態**](iwinhttprequest-status.md)<br/>                 | 唯讀<br/>  | 上次回應中的 HTTP 狀態碼。<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | 唯讀<br/>  | HTTP 狀態文字。<br/>                                      |



 

## <a name="remarks"></a>備註

Httprequest 中定義的 **IWinHttpRequest** 介面是由具有 **CLSID \_ WinHttpRequest** 識別碼的類別所執行。 應用程式會使用 **CLSID \_ WinHttpRequest** 類別識別碼和 **IID \_ IWinHttpRequest** 的介面識別碼呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來取得這個介面。

> [!Note]  
> 針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。

 

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

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

