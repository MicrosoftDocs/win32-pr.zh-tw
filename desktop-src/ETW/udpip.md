---
description: UdpIp 類別-此類別是 UDP/IP 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105386"
---
# <a name="udpip-class"></a>UdpIp 類別

此類別是 UDP/IP 事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**UdpIp** 類別不會定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用 UDP/IP 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 網路 \_ TCPIP** 旗標。

事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**UdpIpGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，以針對 UDP/IP 事件執行特殊處理。 使用下列事件種類來識別使用事件時的實際網路 (UDP/IP) 事件。



| 事件類型                                                         | 描述                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ 接收** (事件種類值為 11) <br/> | IPv4 通訊協定的接收事件。 [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF 類別會定義此事件的事件資料。 |
| **活動 \_追蹤 \_ 類型 \_ 傳送** (事件種類值為 10) <br/>    | 傳送 IPv4 通訊協定的事件。 [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF 類別會定義此事件的事件資料。    |
| 事件種類值17                                               | Fail 事件。 [**UdpIp \_ Fail**](udpip-fail.md) MOF 類別會定義此事件的事件資料。                                  |
| 事件種類值，26                                               | IPv6 通訊協定的傳送事件。 [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF 類別會定義此事件的事件資料。    |
| 事件種類值，27                                               | IPv6 通訊協定的接收事件。 [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF 類別會定義此事件的事件資料。 |



 

您可以使用 **ProcessId** 屬性，將網路事件追蹤至來源和目的地進程。 由於部分網路事件是由個別的執行緒所記錄，因此您可能無法使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員來識別產生網路活動的進程或執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**UdpIp \_ 失敗**](udpip-fail.md)
</dt> <dt>

[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> </dl>

 

 
