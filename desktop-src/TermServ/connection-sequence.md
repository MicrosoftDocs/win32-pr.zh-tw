---
title: 連接順序
description: 此圖顯示在用戶端連接順序期間，遠端桌面服務服務和通訊協定之間所進行的方法呼叫。
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372537"
---
# <a name="connection-sequence"></a>連接順序

下圖顯示在用戶端連接順序期間，遠端桌面服務服務與您的通訊協定之間所進行的方法呼叫。 此處顯示的動作會遵循 [開始順序](start-sequence.md)。 服務與 [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) 物件之間的互動表示用戶端的授權交握。

![用戶端連接順序](images/protocol-connectionsequence.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[方法呼叫順序](method-call-sequence.md)
</dt> <dt>

[重新連接順序](reconnect-sequence.md)
</dt> <dt>

[開始順序](start-sequence.md)
</dt> </dl>

 

 




