---
description: TcpIp 類別-此類別是 TCP/IP 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0782db83d5c92a0e39578bc4e0d46e2c1d41432feb418a08bceb2e3548a45b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069518"
---
# <a name="tcpip-class"></a>TcpIp 類別

這個類別是 TCP/IP 事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**TcpIp** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用 TCP/IP 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 網路 \_ TCPIP** 旗標。

事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**TcpIpGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，來執行 tcp/ip 事件的特殊處理。 使用事件時，請使用下列事件種類來識別實際的網路 (TCP/IP) 事件。



| 事件類型                                                            | 描述                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ 接受** (事件種類值為 15) <br/>     | 接受 IPv4 通訊協定的事件。 [**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF 類別會定義此事件的事件資料。                                                            |
| **活動 \_追蹤 \_ 類型 \_ 連接** (事件種類值為 12) <br/>    | IPv4 通訊協定的連線事件。 [**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF 類別會定義此事件的事件資料。                                                           |
| **活動 \_追蹤 \_ 類型 \_ 中斷** (事件種類值為 13) <br/> | IPv4 通訊協定的中斷線上活動。 [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                        |
| **活動 \_追蹤 \_ 類型 \_ 接收** (事件種類值為 11) <br/>    | IPv4 通訊協定的接收事件。 [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                           |
| **活動 \_追蹤 \_ 類型 \_ 重新連接** (事件種類值為 16) <br/>  | IPv4 通訊協定的重新連接事件。  (連線嘗試失敗，並嘗試進行其他嘗試。 ) [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別定義此事件的事件資料。 |
| **活動 \_追蹤 \_ 類型重新 \_ 傳輸** (事件種類值為 14) <br/> | IPv4 通訊協定的重新傳輸事件。 [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                        |
| **活動 \_追蹤 \_ 類型 \_ 傳送** (事件種類值為 10) <br/>       | 傳送 IPv4 通訊協定的事件。 [**TcpIp \_ SendIPV4**](tcpip-sendipv4.md) MOF 類別會定義此事件的事件資料。                                                                  |
| 事件種類值17                                                  | Fail 事件。 [**TcpIp \_ 失敗**](tcpip-fail.md)MOF 類別會定義此事件的事件資料。                                                                                            |
| 事件種類值，18                                                  | IPv4 通訊協定的 TCP 複製事件。 [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                          |
| 事件種類值，26                                                  | IPv6 通訊協定的傳送事件。 [**TcpIp \_ SendIPV6**](tcpip-sendipv6.md) MOF 類別會定義此事件的事件資料。                                                                  |
| 事件種類值，27                                                  | IPv6 通訊協定的接收事件。 [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。                                                           |
| 事件種類值28                                                  | IPv6 通訊協定的連線事件。 [**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF 類別會定義此事件的事件資料。                                                           |
| 事件種類值，29                                                  | IPv6 通訊協定的中斷線上活動。 [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。                                                        |
| 事件種類值30                                                  | IPv6 通訊協定的重新傳輸事件。 [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。                                                        |
| 事件種類值，31                                                  | 接受 IPv6 通訊協定的事件。 [**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF 類別會定義此事件的事件資料。                                                            |
| 事件種類值，32                                                  | IPv6 通訊協定的重新連接事件。  (連線嘗試失敗，並嘗試進行其他嘗試。 ) [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別定義此事件的事件資料。 |
| 事件種類值，34                                                  | IPv6 通訊協定的 TCP 複製事件。 [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF 類別會定義此事件的事件資料。                                                          |



 

您可以使用 **ProcessId** 屬性，將網路事件追蹤至來源和目的地進程。 由於部分網路事件是由個別的執行緒所記錄，因此您可能無法使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員來識別產生網路活動的進程或執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**TcpIp \_ 失敗**](tcpip-fail.md)
</dt> <dt>

[**TcpIp \_ SendIPV4**](tcpip-sendipv4.md)
</dt> <dt>

[**TcpIp \_ SendIPV6**](tcpip-sendipv6.md)
</dt> <dt>

[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md)
</dt> <dt>

[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md)
</dt> <dt>

[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md)
</dt> <dt>

[**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md)
</dt> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ V1**](tcpip-v1.md)
</dt> </dl>

 

 
