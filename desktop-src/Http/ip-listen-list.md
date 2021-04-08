---
title: IP 接聽清單
description: HTTP 伺服器 Api 在使用者註冊 UrlPrefix 之前，不會系結至任何 IP 位址和 TCP 通訊埠配對。
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932538"
---
# <a name="ip-listen-list"></a>IP 接聽清單

HTTP 伺服器 Api 在使用者註冊 UrlPrefix 之前，不會系結至任何 IP 位址和 TCP 通訊埠配對。 根據預設，一旦在要求佇列中輸入註冊，HTTP 伺服器 API 就會系結至 UrlPrefix (中指定的埠，例如，所有 IP 位址的埠 80)  (INADDR \_ 任何或 INADDR6 \_ 電腦上可用的任何) 。 當協力廠商應用程式 (不使用 HTTP 伺服器 Api 時，) 系結至電腦上的 IP 位址和埠80配對，就會發生問題。 HTTP 伺服器 API 提供一種方式來設定它所系結的 IP 位址清單，並解決這個共存問題。 系統管理員會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函數，並將 *ConfigId* 參數設定為 HttpServiceConfigIPListenList 值，以指定 IP 接聽清單。 IPv4 和 IPv6 位址都可以新增至清單。 輸入的 IP 位址會套用至電腦上使用 HTTP 伺服器 API 的所有應用程式，並在機器重新開機時持續保存。 不過，IP 接聽清單設定的任何變更都不會以動態方式進行;在大部分的情況下，可能需要重新開機系統。

 

 




