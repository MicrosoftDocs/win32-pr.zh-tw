---
description: 以不帶正負號的位元組陣列形式捕獲回應實體主體。
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: IWinHttpRequest：： ResponseBody 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56eac42d41054cf7c01ff0c69ffcb82353db7182acf15765b25149560d5f7391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563226"
---
# <a name="iwinhttprequestresponsebody-property"></a>IWinHttpRequest：： ResponseBody 屬性

**ResponseBody** 屬性會以不帶正負號的位元組陣列形式抓取回應實體主體。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a>屬性值

以不帶正負號的位元組陣列形式接收回應實體主體的 **變異** 值。 此陣列包含直接從伺服器接收的原始資料。

## <a name="error-codes"></a>錯誤碼

傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。

## <a name="remarks"></a>備註

這個屬性會傳回不帶正負號之位元組陣列中的回應資料。 如果回應沒有回應主體，則會傳回空的 variant。 這個屬性只能在呼叫 [**Send**](iwinhttprequest-send.md) 方法之後叫用。

> [!Note]  
> 如需 Windows XP 和 Windows 2000 之執行的詳細資訊，請參閱[執行時間需求](winhttp-start-page.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>         |
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

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




