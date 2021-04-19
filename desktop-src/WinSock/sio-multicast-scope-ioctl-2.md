---
description: 使用 SIO \_ 多播 \_ 領域命令程式碼來指定應進行多播的範圍。
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE Ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987708"
---
# <a name="sio_multicast_scope-ioctl"></a><span data-ttu-id="0a289-103">SIO \_ 多播 \_ 範圍 Ioctl</span><span class="sxs-lookup"><span data-stu-id="0a289-103">SIO\_MULTICAST\_SCOPE Ioctl</span></span>

<span data-ttu-id="0a289-104">當採用多播時，通常必須指定應進行多播的範圍。</span><span class="sxs-lookup"><span data-stu-id="0a289-104">When multicasting is employed, it is usually necessary to specify the scope over which the multicast should occur.</span></span> <span data-ttu-id="0a289-105">這裡的範圍定義為要涵蓋的路由網路區段數目。</span><span class="sxs-lookup"><span data-stu-id="0a289-105">Here scope is defined to be the number of routed network segments to be covered.</span></span> <span data-ttu-id="0a289-106">適用于 \_ WSPIoctl 的 SIO 多播 \_ 領域[](/previous-versions/windows/hardware/network/ff566296(v=vs.85))命令程式碼可用來控制此項。</span><span class="sxs-lookup"><span data-stu-id="0a289-106">The SIO\_MULTICAST\_SCOPE command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to control this.</span></span> <span data-ttu-id="0a289-107">範圍為零會指出多播傳輸不會放置在網路上，但是可以跨本機主機內的通訊端簡易性。</span><span class="sxs-lookup"><span data-stu-id="0a289-107">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="0a289-108">一個範圍值 (預設) 表示傳輸將放置在網路上，但不會跨越任何路由器。</span><span class="sxs-lookup"><span data-stu-id="0a289-108">A scope value of one (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="0a289-109">範圍較高的值會決定可跨越的路由器數目。</span><span class="sxs-lookup"><span data-stu-id="0a289-109">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="0a289-110">請注意，這會對應至 IP 多播中的存留時間 (TTL) 參數。</span><span class="sxs-lookup"><span data-stu-id="0a289-110">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

 

 
