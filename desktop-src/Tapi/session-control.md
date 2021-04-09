---
description: 會話或呼叫代表兩個或更多位址之間的連接。
ms.assetid: f598c1cd-2b50-4ac6-a05e-4fd8eeb5e3e1
title: 會話控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09250a90f978bde9be4f20aad6ee38f5e9766818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695839"
---
# <a name="session-control"></a><span data-ttu-id="0f1e6-103">會話控制項</span><span class="sxs-lookup"><span data-stu-id="0f1e6-103">Session Control</span></span>

<span data-ttu-id="0f1e6-104">會話或呼叫代表兩個或更多位址之間的連接。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-104">A session or call represents a connection between two or more addresses.</span></span> <span data-ttu-id="0f1e6-105">此連接是動態的，且必須在必要時建立、操作和釋放相關聯的程式設計物件。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-105">This connection is dynamic, and the associated programming objects must be created, manipulated, and released as needed.</span></span> <span data-ttu-id="0f1e6-106">在最簡單的情況下，這表示會進行通話並中斷連線。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-106">In the simplest case, this means making and disconnecting a phone call.</span></span> <span data-ttu-id="0f1e6-107">針對先進的應用程式，會話控制可能牽涉到透過 IP 網路管理多媒體會議到個別參與者的層級。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-107">For advanced applications, session control may involve managing multimedia conferences over an IP network down to the level of individual participants.</span></span>

<span data-ttu-id="0f1e6-108">會話控制項牽涉到兩個基本區域：</span><span class="sxs-lookup"><span data-stu-id="0f1e6-108">Session control involves two basic areas:</span></span>

-   <span data-ttu-id="0f1e6-109">[會話作業](session-operations-ovr.md) 是初始化、維護和終止通訊會話的控制項。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-109">[Session Operations](session-operations-ovr.md) are controls that initiate, maintain, and terminate a communications session.</span></span>
-   <span data-ttu-id="0f1e6-110">[會話資訊](session-information-ovr.md) 描述可針對通訊會話取得的資料。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-110">[Session Information](session-information-ovr.md) describes data that can be obtained concerning a communications session.</span></span>

<span data-ttu-id="0f1e6-111">本節未涵蓋兩種特製化的會話控制項類型。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-111">Two specialized types of session control are not covered in this section.</span></span> <span data-ttu-id="0f1e6-112">如需自動通話配送中心的相關資訊，請參閱 (TAPI 2.x 的 [電話中心控制](./call-center-control.md)) 或 (TAPI 3.X 的 [電話中心控制項](about-call-center-controls.md)) 。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-112">For information on Automatic Call Distribution Centers, see [Call Center Control](./call-center-control.md) (TAPI 2.x) or [About Call Center Controls](about-call-center-controls.md) (TAPI 3.x).</span></span> <span data-ttu-id="0f1e6-113">如需 IP 會議的相關資訊，請參閱 [關於會合 Ip 電話語音會議](about-rendezvous-ip-telephony-conferencing.md)。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-113">For information on IP conferencing, see [About Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).</span></span>

 

 
