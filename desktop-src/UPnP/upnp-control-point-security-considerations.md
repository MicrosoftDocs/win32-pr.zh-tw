---
title: 控制點安全性考慮
description: 當您在建立控制點時，必須考慮下列安全性問題。
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932428"
---
# <a name="control-point-security-considerations"></a><span data-ttu-id="b36db-103">控制點安全性考慮</span><span class="sxs-lookup"><span data-stu-id="b36db-103">Control Point Security Considerations</span></span>

<span data-ttu-id="b36db-104">當您在建立控制點時，必須考慮下列安全性問題。</span><span class="sxs-lookup"><span data-stu-id="b36db-104">When you are creating a control point, you need to take into consideration the following security issues.</span></span>

-   <span data-ttu-id="b36db-105">所有控制點搜尋預設會以 TTL 1 傳送。</span><span class="sxs-lookup"><span data-stu-id="b36db-105">All control point searches are by default sent with a TTL of 1.</span></span> <span data-ttu-id="b36db-106">這表示只會探索相同子網內的裝置。</span><span class="sxs-lookup"><span data-stu-id="b36db-106">This means that only devices within the same subnet are discovered.</span></span> <span data-ttu-id="b36db-107">您可以在登錄中設定較高的 TTL。</span><span class="sxs-lookup"><span data-stu-id="b36db-107">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="b36db-108">裝置的裝置和服務描述只會在已傳送裝置公告的相同裝置上存在時才會下載。</span><span class="sxs-lookup"><span data-stu-id="b36db-108">A device's device and service description is only downloaded if it is present on the same device which sent the device announcement.</span></span>
-   <span data-ttu-id="b36db-109">如果裝置的控制項和訂用帳戶 Url 位於傳送裝置宣告的相同裝置上，則裝置只會傳送控制權和訂用帳戶要求。</span><span class="sxs-lookup"><span data-stu-id="b36db-109">A device is only sent control and subscription requests if its control and subscription URLs are on the same device that sent the device announcements.</span></span>

 

 




