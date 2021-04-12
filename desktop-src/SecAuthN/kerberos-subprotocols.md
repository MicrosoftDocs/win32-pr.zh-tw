---
description: Kerberos 通訊協定是由三個 subprotocols 所組成。
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Kerberos Subprotocols
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193085"
---
# <a name="kerberos-subprotocols"></a><span data-ttu-id="eddde-103">Kerberos Subprotocols</span><span class="sxs-lookup"><span data-stu-id="eddde-103">Kerberos Subprotocols</span></span>

<span data-ttu-id="eddde-104">[*Kerberos 通訊協定*](../secgloss/k-gly.md)是由三個 subprotocols 所組成。</span><span class="sxs-lookup"><span data-stu-id="eddde-104">The [*Kerberos protocol*](../secgloss/k-gly.md) is composed of three subprotocols.</span></span>



| <span data-ttu-id="eddde-105">子通訊協定</span><span class="sxs-lookup"><span data-stu-id="eddde-105">Subprotocol</span></span>                                                                         | <span data-ttu-id="eddde-106">意義</span><span class="sxs-lookup"><span data-stu-id="eddde-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eddde-107">驗證服務交換</span><span class="sxs-lookup"><span data-stu-id="eddde-107">Authentication Service Exchange</span></span>](authentication-service-exchange.md)<br/>   | <span data-ttu-id="eddde-108">在此子通訊協定中， [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) 會為用戶端提供登入 [*工作階段金鑰*](../secgloss/s-gly.md) 和票證授權票證 (TGT) 。</span><span class="sxs-lookup"><span data-stu-id="eddde-108">In this subprotocol, the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) gives the client a logon [*session key*](../secgloss/s-gly.md) and a ticket-granting ticket (TGT).</span></span><br/> |
| [<span data-ttu-id="eddde-109">票證授權服務交換</span><span class="sxs-lookup"><span data-stu-id="eddde-109">Ticket-Granting Service Exchange</span></span>](ticket-granting-service-exchange.md)<br/> | <span data-ttu-id="eddde-110">在此子通訊協定中，KDC 會散發服務工作階段金鑰和服務的票證。</span><span class="sxs-lookup"><span data-stu-id="eddde-110">In this subprotocol, the KDC distributes a service session key and a ticket for the service.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="eddde-111">用戶端/伺服器交換</span><span class="sxs-lookup"><span data-stu-id="eddde-111">Client/Server Exchange</span></span>](client-server-exchange.md)<br/>                     | <span data-ttu-id="eddde-112">在此子通訊協定中，用戶端會提供服務的許可票證。</span><span class="sxs-lookup"><span data-stu-id="eddde-112">In this subprotocol, the client presents the ticket for admission to a service.</span></span><br/>                                                                                                                                                                                                                         |



 

 

 
