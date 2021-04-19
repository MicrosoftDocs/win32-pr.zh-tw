---
Description: 本主題提供有關搭配使用 WinHTTP WinHttpRequest COM 物件與指令碼語言的資訊。
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: WinHttpRequest 物件
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995305"
---
# <a name="winhttprequest-object"></a>WinHttpRequest 物件

本主題提供有關搭配使用 WinHTTP **WinHttpRequest** COM 物件與指令碼語言的資訊。 如需詳細資訊，包括 c + + API (WinHTTP) 請參閱 [關於 winHTTP](about-winhttp.md)。 如需這些介面的比較，請參閱 [選擇 WinHTTP 介面](choosing-a-winhttp-interface.md) 。

## <a name="example"></a>範例

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

取自 [IWinHttpRequest：： Status 屬性](iwinhttprequest-status.md)的程式碼範例。



## <a name="members"></a>成員

**WinHttpRequest** 物件具有下列類型的成員：

-   [事件](#events)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**WinHttpRequest** 物件具有這些事件。



| 事件                                                                            | 描述                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | 當應用程式中發生執行階段錯誤時發生。<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | 當資料可從回應中取得時，就會發生。<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | 當回應資料完成時發生。<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | 在開始接收回應資料時發生。<br/>      |



 

### <a name="methods"></a>方法

**WinHttpRequest** 物件有這些方法。



| 方法                                                                 | 描述                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**中止**](iwinhttprequest-abort.md)                                 | 中止 [WinHTTP](about-winhttp.md) [**傳送**](iwinhttprequest-send.md) 方法。<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | 抓取所有 HTTP 回應標頭。<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | 抓取 HTTP 回應標頭。<br/>                                                                                                            |
| [**打開**](iwinhttprequest-open.md)                                   | 開啟 HTTP 資源的 HTTP 連接。<br/>                                                                                                   |
| [**傳送**](iwinhttprequest-send.md)                                   | 將 HTTP 要求傳送至 HTTP 伺服器。<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | 設定目前的 [自動登入原則](authentication-in-winhttp.md)。<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | 選取要傳送至安全超文字傳輸通訊協定 (HTTPS) 伺服器的用戶端憑證。<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | 設定要與 HTTP 伺服器（來源或 proxy 伺服器）搭配使用的認證。<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | 設定 proxy 伺服器資訊。<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | 新增、變更或刪除 HTTP 要求標頭。<br/>                                                                                               |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | 指定傳送/接收作業的個別超時元件（以毫秒為單位）。<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | 以秒為單位，指定非同步 [**傳送**](iwinhttprequest-send.md) 方法完成的等候時間（以秒為單位），並提供選擇性的超時值。<br/> |



 

### <a name="properties"></a>屬性

**WinHttpRequest** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | Description                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**選項**](iwinhttprequest-option.md)<br/>                 | 讀取/寫入<br/> | 設定或抓取 WinHTTP 選項值。<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | 唯讀<br/>  | 以不帶正負號的位元組陣列形式捕獲回應實體主體。<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | 唯讀<br/>  | 以 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)形式抓取回應實體主體。<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | 唯讀<br/>  | 以文字形式抓取回應實體主體。<br/>                          |
| [**狀態**](iwinhttprequest-status.md)<br/>                 | 唯讀<br/>  | 從上一個回應中抓取 HTTP 狀態碼。<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | 唯讀<br/>  | 抓取 HTTP 狀態文字。<br/>                                          |



 

## <a name="remarks"></a>備註

**WinHttpRequest** 物件會使用 [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo)介面來提供錯誤資料。 您可以使用 Microsoft Visual Basic Scripting Edition (VBScript) 中的 [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件和 microsoft JScript 中的 [error](https://msdn.microsoft.com/library/dww52sbt.aspx) 物件，取得描述和數值錯誤值。 錯誤號碼的較低16位會對應到在 [**錯誤訊息**](error-messages.md)中找到的值。

> [!Note]  
> 針對 Windows XP 和 Windows 2000，請參閱 [執行時間需求](winhttp-start-page.md)。

 

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

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

