---
description: 在開始接收回應資料時發生。
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: IWinHttpRequestEvents：： OnResponseStart 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb08273bfbab92e957b932f463ce4b91ee53e3663dcd886f5e02b73698fff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744221"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>IWinHttpRequestEvents：： OnResponseStart 事件

開始接收回應資料時，就會發生 **OnResponseStart** 事件。

## <a name="syntax"></a>語法


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*狀態* \[在\]
</dt> <dd>

接收回應資料所傳回的標準狀態碼。 狀態碼定義于 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)中。

</dd> <dt>

*ContentType* \[在\]
</dt> <dd>

指定收到的內容類型，例如 "text/html" 或 "image/gif"。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

若要進行此事件，請使用 [ [**開啟**](iwinhttprequest-open.md) ] 以非同步模式傳送 HTTP 連接，然後使用 [ [**傳送**](iwinhttprequest-send.md) ] 將資料要求傳送到網際網路伺服器。

這是在 [**傳送**](iwinhttprequest-send.md)之後第一個發生的 WinHTTP 事件。

> [!Note]  
> 如 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的[執行時間需求](winhttp-start-page.md)一節。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




