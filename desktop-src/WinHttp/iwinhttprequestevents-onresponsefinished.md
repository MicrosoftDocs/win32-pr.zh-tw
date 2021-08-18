---
description: 當回應資料完成時發生。
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: IWinHttpRequestEvents：： OnResponseFinished 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2114135c17f3e2eb2f9d60a7044f7441271f257fe099de31ea70c6030de769df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744248"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a>IWinHttpRequestEvents：： OnResponseFinished 事件

完成回應資料時，就會發生 **OnResponseFinished** 事件。

## <a name="syntax"></a>語法


```C++
void OnResponseFinished();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件表示已收到所有與最近要求相關的回應資料。 在下一個要求之前， [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md)不會再次發生。

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

 

 




