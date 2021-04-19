---
description: 當資料可從回應中取得時，就會發生。
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: IWinHttpRequestEvents：： OnResponseDataAvailable 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988266"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>IWinHttpRequestEvents：： OnResponseDataAvailable 事件

當資料可從回應中取得時，就會發生 **OnResponseDataAvailable** 事件。

## <a name="syntax"></a>語法


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*資料* \[在\]
</dt> <dd>

以零為基底的位元組陣列，這個陣列會接收 Microsoft Windows HTTP 服務所收到的回應資料 (WinHTTP) 直到發生此事件為止。 這是 VT  \_ 陣列 \| Vt UI1 類型的變異 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

因為資料是以位元組為單位，所以在放置於寬字元 (Unicode) 字串時，必須將其轉換成寬字元。

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

 

 




