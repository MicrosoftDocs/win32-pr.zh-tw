---
title: 預設網路設定
description: 預設網路設定
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK，預設網路設定
- Advanced Systems Format (ASF) ，預設網路設定
- ASF (Advanced Systems Format) ，預設網路設定
- Windows Media Format SDK，網路設定
- Advanced Systems Format (ASF) ，網路設定
- ASF (Advanced Systems Format) ，網路設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840808"
---
# <a name="default-networking-settings"></a>預設網路設定

下表描述 Windows Media 格式 SDK （依介面分組）中網路參數的預設設定。



| IWMReaderNetworkConfig                | 預設設定              |
|---------------------------------------|------------------------------|
| 緩衝時間                        | 5 秒                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (無效)                 |
| ProxySetting： HTTP                    | WMT \_ PROXY \_ 設定 \_ 瀏覽器 |
| ProxySetting： MMS                     | WMT \_ PROXY \_ 設定 \_ 無    |
| ProxySetting： RTSP                    | WMT \_ PROXY \_ 設定 \_ 無    |
| ProxyHostName (HTTP、MMS、RTSP)        | ""                           |
| ProxyPort： HTTP                       | 80                           |
| ProxyPort： MMS                        | 1755                         |
| ProxtPort： RTSP                       | 554                          |
| ProxyExceptionList (HTTP、MMS、RTSP)   | ""                           |
| ProxyBypassForLocal (HTTP、MMS、RTSP)  | FALSE                        |
| ForceRerunAutoDetection               | FALSE                        |
| EnableMulticast                       | true                         |
| Update                            | true                         |
| EnableTCP                             | true                         |
| EnableUDP                             | true                         |
| 連接頻寬                  | 0 (自動偵測)               |



 



| IWMReaderNetworkConfig2        | 預設設定        |
|--------------------------------|------------------------|
| 加速串流持續時間 | 100000000 (10 秒)  |
| 啟用內容快取         | true                   |
| 啟用快速快取              | true                   |
| 啟用重新傳送                 | true                   |
| 啟用 content thinning        | true                   |
| 重新連線限制                | 25                     |



 



| IWMWriterNetworkSink | 預設設定         |
|----------------------|-------------------------|
| 最大用戶端      | 5                       |
| 網路通訊協定     | 0 (WMT \_ PROTOCOL \_ HTTP)  |
| 主機 URL             | 0 (無效)            |



 



| IWMWriterAdvanced2  | 預設設定             |
|---------------------|-----------------------------|
| 封包大小上限 | 1400                        |
| 記錄用戶端識別碼       | FALSE                       |
| 播放模式           | WMT \_ 播放 \_ 模式的 \_ 自選 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行網路功能**](implementing-network-functionality.md)
</dt> </dl>

 

 




