---
description: 使用 Netstat 計算額外負荷
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: 使用 Netstat 計算額外負荷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998239"
---
# <a name="calculating-overhead-with-netstat"></a>使用 Netstat 計算額外負荷

使用 Netstat 計算額外負荷應該在無訊息的網路上執行，以避免其他網路流量扭曲資料，例如廣播或多播流量。

**使用 Netstat 計算應用程式的網路額外負荷**

1.  使用 Netstat 取出目前的介面統計資料。
2.  執行應用程式。
3.  使用 Netstat 再次取得介面統計資料。
4.  計算兩個 Netstat 度量之間接收的位元組數目。

## <a name="example"></a>範例

下列範例示範這些步驟，使用 TTCP 傳送10個位元組的資料，一次一個位元組。

首先，會計算應用程式的理論負擔。 針對此測試，所有封包都是60位元組 (Ethernet 最小) 。 這項傳輸需要三封封包來設定連線、10個數據封包、10個認可封包 (延遲的 ACK 幾乎每次都會觸發) ，而四個封包則可正常地關閉連接。

這相當於27個60位元組的封包，或1620個位元組 (3 + 4 + 10 + 10) \* 60 = 1620) 。 由於只會傳送10個位元組的資料，因此額外負荷為1610個位元組，超過99% 的通訊協定額外負荷。

### <a name="commands"></a>命令

**netstat-e**

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

**ttcp-t-h0-D-l1-n10-p9 172.31.71.99**

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

**netstat-e**

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a>計算

**已傳送：** 816 位元組

**收到：** 674 位元組

**位元組總計：** 1490

**使用者位元組：** 10

**額外負荷：** 1480/1490 = 99.3%

* * Goodput： * * = 5 個位元組/秒 (或40位/秒) 

> [!Note]  
> 因為 Netstat 值中未納入填補位元組，所以傳送的實際位元組數不符合理論值。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式行為](application-behavior-2.md)
</dt> <dt>

[高效能的 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



