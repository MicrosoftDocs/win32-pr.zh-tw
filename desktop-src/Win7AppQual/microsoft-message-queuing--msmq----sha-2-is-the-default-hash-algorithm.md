---
description: Microsoft Message Queuing (MSMQ) -SHA 2 是預設的雜湊演算法
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: Microsoft Message Queuing (MSMQ) -SHA 2 是預設的雜湊演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3c54832d953e50f3b912fdf36374faa8ff9ed0466587f7ac3fed2572eb3b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053036"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ) -SHA 2 是預設的雜湊演算法

## <a name="affected-platforms"></a>受影響的平臺

 **客戶** 端-Windows XP、Windows Vista、Windows 7  
**伺服器**-Windows server 2003、Windows server 2008、Windows Server 2008 R2  










## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>描述

在 Windows 7 中，MSMQ 會使用 SHA-2 做為簽署外寄訊息時的預設值。 此外，所有傳入的訊息都必須使用 SHA-1 簽署。 您可以透過系統管理員可存取的登錄機碼來啟用較低加密演算法的支援。

## <a name="manifestation-of-impact"></a>影響的表現

-   Windows 2003 或以下的 msmq 不會在 Windows 7 中接受源自 MSMQ 的已簽署訊息
-   Windows 7 中的 MSMQ 不會接受源自 Windows 2008 或以下的已簽署訊息

## <a name="mitigation"></a>降低

使用者應考慮升級至 Windows 7，以利用更強的簽署演算法。 若要在 Windows 7 和任何下層作業系統之間啟用無縫簽署的訊息交換，系統管理員必須在 MSMQ 電腦上新增適當的例外狀況。

 

 



