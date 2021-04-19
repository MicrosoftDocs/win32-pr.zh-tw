---
description: 提供 Microsoft Windows HTTP Services (WinHTTP) 的事件。
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: IWinHttpRequestEvents 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985319"
---
# <a name="iwinhttprequestevents-interface"></a>IWinHttpRequestEvents 介面

**IWinHttpRequestEvents** 介面提供 [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md)的事件。 它只會使用事件方法。

## <a name="members"></a>成員

**IWinHttpRequestEvents** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWinHttpRequestEvents** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWinHttpRequestEvents** 介面具有這些方法。



| 方法                                                                           | 描述                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | 當應用程式中發生執行階段錯誤時發生。<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | 當資料可從回應中取得時，就會發生。<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | 當回應資料完成時發生。<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | 在開始接收回應資料時發生。<br/>      |



 

## <a name="remarks"></a>備註

下列程式說明如何註冊通知。

1.  藉由在 [**IWinHttpRequest**](iwinhttprequest-interface.md)物件上呼叫 **QueryInterface** 來取得 [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)介面。
2.  在傳回的介面上呼叫 [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) ，並將 **IID \_ IWinHttpRequestEvents** 傳遞給 *riid*。
3.  呼叫所傳回連接點上的 [建議](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise)，並在執行 **IWinHttpRequestEvents** 至 *pUnk* 的物件上，將指標傳遞至 **IUnknown** 介面。

您可以在步驟2傳回的連接點上呼叫 [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) ，以終止通知。

若要查看一些註冊 COM 通知的程式碼，請參閱 [Com 連接點](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) 一文的用戶端一節。

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

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

