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
# <a name="connection-sequence"></a><span data-ttu-id="c2b7b-103">連接順序</span><span class="sxs-lookup"><span data-stu-id="c2b7b-103">Connection Sequence</span></span>

<span data-ttu-id="c2b7b-104">下圖顯示在用戶端連接順序期間，遠端桌面服務服務與您的通訊協定之間所進行的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="c2b7b-104">The following illustration shows the method calls made between the Remote Desktop Services service and your protocol during the client connection sequence.</span></span> <span data-ttu-id="c2b7b-105">此處顯示的動作會遵循 [開始順序](start-sequence.md)。</span><span class="sxs-lookup"><span data-stu-id="c2b7b-105">The actions shown here follow the [Start Sequence](start-sequence.md).</span></span> <span data-ttu-id="c2b7b-106">服務與 [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) 物件之間的互動表示用戶端的授權交握。</span><span class="sxs-lookup"><span data-stu-id="c2b7b-106">The interaction between the service and the [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) object represents the licensing handshake for the client.</span></span>

![用戶端連接順序](images/protocol-connectionsequence.png)

## <a name="related-topics"></a><span data-ttu-id="c2b7b-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2b7b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2b7b-109">方法呼叫順序</span><span class="sxs-lookup"><span data-stu-id="c2b7b-109">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="c2b7b-110">重新連接順序</span><span class="sxs-lookup"><span data-stu-id="c2b7b-110">Reconnect Sequence</span></span>](reconnect-sequence.md)
</dt> <dt>

[<span data-ttu-id="c2b7b-111">開始順序</span><span class="sxs-lookup"><span data-stu-id="c2b7b-111">Start Sequence</span></span>](start-sequence.md)
</dt> </dl>

 

 




