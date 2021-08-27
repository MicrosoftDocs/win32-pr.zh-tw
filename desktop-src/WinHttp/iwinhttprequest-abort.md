---
description: Abort 方法會中止 WinHTTP 傳送方法。
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: IWinHttpRequest：： Abort 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ca70917139059e8b0d038797ad61b137a259d615f6098a52bc86466f8054c7b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071768"
---
# <a name="iwinhttprequestabort-method"></a>IWinHttpRequest：： Abort 方法

**Abort** 方法會中止 [WinHTTP](about-winhttp.md) [**傳送**](iwinhttprequest-send.md)方法。

## <a name="syntax"></a>語法


```C++
HRESULT Abort();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。

## <a name="remarks"></a>備註

您可以中止非同步和同步的 [**傳送**](iwinhttprequest-send.md) 方法。 若要中止同步 [**傳送**](iwinhttprequest-send.md)方法，您必須從 [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)事件內呼叫 **abort** 。

> [!Note]  
> 如 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的[執行時間需求](winhttp-start-page.md)一節。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WinHTTP .lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




