---
title: 網際網路連線共用
description: 如果連線共用設定為在網路上的電腦存取網際網路時撥號，則 BITS 可以強制使用 Microsoft 網際網路連線共用的家用網路撥號連線。
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671427"
---
# <a name="internet-connection-sharing"></a><span data-ttu-id="5c298-103">網際網路連線共用</span><span class="sxs-lookup"><span data-stu-id="5c298-103">Internet Connection Sharing</span></span>

<span data-ttu-id="5c298-104">如果連線共用設定為在網路上的電腦存取網際網路時撥號，則 BITS 可以強制使用 Microsoft 網際網路連線共用的家用網路撥號連線。</span><span class="sxs-lookup"><span data-stu-id="5c298-104">BITS can force a dial-up connection for home networks that use Microsoft Internet Connection Sharing if Connection Sharing is configured to dial out when computers on the network access the Internet.</span></span> <span data-ttu-id="5c298-105">若要防止強制撥號連線，請在共用網際網路連線的連線共用主機電腦上，停 **用 [每當網路上的電腦嘗試存取網際網路時建立撥號連線** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="5c298-105">To prevent a forced dial-up connection, disable the **Establish a dial-up connection whenever a computer on my network attempts to access the Internet** option on the Connection Sharing host computer that shares its Internet connection.</span></span>

<span data-ttu-id="5c298-106">連線到連線共用主機電腦的電腦假設它們具有網路連線，因此 BITS 會嘗試傳輸檔案。</span><span class="sxs-lookup"><span data-stu-id="5c298-106">Computers connected to the Connection Sharing host computer assume they have a network connection, so BITS will try to transfer files.</span></span> <span data-ttu-id="5c298-107">如果主機電腦上的撥號選項已停用，而且主機電腦沒有作用中的連線，則傳輸會失敗併發生暫時性錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c298-107">If the dial-up option is disabled on the host computer and the host computer does not have an active connection, the transfers will fail with a transient error.</span></span> <span data-ttu-id="5c298-108">BITS 會定期重試傳輸。</span><span class="sxs-lookup"><span data-stu-id="5c298-108">BITS will retry the transfers periodically.</span></span>

 

 




