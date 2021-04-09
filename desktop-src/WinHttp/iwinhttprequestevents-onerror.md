---
description: 當應用程式中發生執行階段錯誤時發生。
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: IWinHttpRequestEvents：： OnError 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945187"
---
# <a name="iwinhttprequesteventsonerror-event"></a>IWinHttpRequestEvents：： OnError 事件

當應用程式中發生執行階段錯誤時，就會發生 **OnError** 事件。

## <a name="syntax"></a>語法


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ErrorNumber* \[在\]
</dt> <dd>

接收錯誤的數值。 此錯誤號碼的較低16位會對應到 [**錯誤訊息**](error-messages.md)中所列的其中一個錯誤。

</dd> <dt>

*ErrorDescription* \[在\]
</dt> <dd>

指定所發生錯誤的簡短描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




