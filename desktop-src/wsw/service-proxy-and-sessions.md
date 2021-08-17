---
title: 服務 Proxy 和會話
description: 服務 proxy 具有會話和非會話型通道系結的特殊行為。
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Windows 的服務 Proxy 和會話 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d845bd341f1343338031619a72fd5dbd307fe1a92175b3753d83b373d73c812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962887"
---
# <a name="service-proxy-and-sessions"></a>服務 Proxy 和會話

[服務 proxy](service-proxy.md)具有會話和非會話型通道系結的特殊行為。 如果基礎通道系結是以會話為基礎，服務 proxy 就會提供以會話為基礎的語法。 在此情況下，會使用單一通道來服務呼叫。 但是，如果通道系結不是以會話為基礎，服務 proxy 就會為每個呼叫建立個別的通道。 不過請注意，非會話型的通道是集區，而且可能會重複使用。 在重複使用通道的情況下，如果基礎通道未發生錯誤或通道上的呼叫導致服務 proxy 對通道造成錯誤，服務 proxy 會讓通道保持開啟。 請注意， 除非發生錯誤，否則一旦開啟通道，只要服務 proxy 已開啟，就會保持開啟狀態，而且只有在關閉服務 proxy 時，才會關閉。


如果通道系結是以會話為基礎，而且如果基礎通道發生錯誤，服務 proxy 狀態機器將會轉換為「 [**WS \_ 服務 \_ proxy」 \_ 狀態 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) 的「錯誤」狀態。 在非會話型通道系結的情況下，基礎通道中的錯誤不會導致 proxy 轉換成 **WS \_ 服務 \_ proxy \_ 狀態 \_** 錯誤狀態。

如需服務 proxy 及其狀態的相關詳細資訊，請參閱 [服務 proxy](service-proxy.md) 主題。 如需不同通道系結的範例，請參閱下列範例：

-   非會話通道系結， [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   以會話為基礎的通道系結， [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




