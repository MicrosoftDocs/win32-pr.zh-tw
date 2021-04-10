---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ) 改善的佇列處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944454"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ) 改善的佇列處理

## <a name="platforms"></a>平台

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>Description

MSMQ 服務不會對可在系統上建立的佇列數目施加硬性限制。 但是，當建立大量的佇列時，系統的效能會受到影響。 具體來說，當有超過一千個佇列時，MSMQ 服務的啟動時間會以指數方式增加，而產生明顯的影響。

Microsoft 已將 Windows 7 中的 MSMQ 服務優化，以降低將佇列載入至記憶體的查閱負荷。 即使在系統中建立了數千個佇列，這項優化也導致 MSMQ 服務的啟動時間大幅改進。

## <a name="manifestation-of-impact"></a>影響的表現

這項效能改進不會影響任何現有應用程式的功能。

## <a name="leveraging-the-changed-feature"></a>利用變更的功能

在 Windows 7 上使用 MSMQ 的應用程式開發人員現在可以建立其解決方案的架構，而不會限制佇列數目。 請注意，佇列的數目仍會影響 MSMQ 伺服器的整體效能，但效能影響現在是以線性而非指數的比例進行。

## <a name="compatibility-performance-reliability-and-usability-tests"></a>相容性、效能、可靠性和可用性測試

如果您使用大量的佇列，請在測試平臺上模擬生產環境、監視效能，以及分析服務的啟動時間，以及在測試系統中出現大量佇列和訊息的訊息輸送量。

 

 



