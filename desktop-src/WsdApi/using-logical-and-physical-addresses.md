---
description: WS-Discovery 使用以 urn： uuid：格式為基礎的 Uri 定義邏輯定址。
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: 使用邏輯與實體位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ddf1dc6fe34325a90f52e43346e507d837ab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973262"
---
# <a name="using-logical-and-physical-addresses"></a>使用邏輯與實體位址

[Ws-management](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 會使用以格式為基礎的 uri 來定義邏輯定址 `urn:uuid:` 。 此定址配置的目的是要區分裝置的身分識別與目前的 IP 位址。 此配置基本上提供 DNS 名稱的功能，而不需要名稱伺服器。 [Web 服務 (DPWS 的裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/)) 建議裝置使用此定址配置。

DPWS 也建議服務使用實體 (也稱為傳輸) 位址。 這可讓原本不支援 WS-Discovery 定址機制的用戶端與 DPWS 服務通訊。 此外，每個服務都可以定義其位址，以針對在較低層管理服務分派的裝置執行，啟用傳輸層級定址。 最後，使用實體位址會將互通性最大化。

實體定址的缺點是，它會增加裝置執行的複雜度，因為必須追蹤目前的 IP 或傳輸位址，而且必須據以修改裝置中繼資料。 基於這個理由，DPWS 不需要服務就能使用傳輸位址。

如果使用邏輯位址，則會在某些情況下未定義執行行為。 WS-Discovery 規格不會描述服務在邏輯位址中的意義。 由於相關聯的網路 chatter，WS-Discovery 規格的 R1001 建議您不要在託管服務上使用 WS-Discovery。

不建議服務位於邏輯位址，因為這樣會降低互通性。 如果實作為絕對必須位於邏輯位址，則服務應該使用與裝置相同的邏輯位址。 如果這對裝置上的分派模型增加了太多複雜性，則建議的解決方案是使用參考參數來區分服務。 如果 WSDAPI 使用與裝置相同的端點位址，則會正確地將訊息傳送至服務。

 

 



