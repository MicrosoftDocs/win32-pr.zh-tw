---
description: 撥置中心控制項會擴充 TAPI 3 物件模型，以支援 (ACD) 系統的自動呼叫散發需求。
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: 使用撥置中心控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997100"
---
# <a name="using-call-center-controls"></a><span data-ttu-id="5927f-103">使用撥置中心控制項</span><span class="sxs-lookup"><span data-stu-id="5927f-103">Using Call Center Controls</span></span>

<span data-ttu-id="5927f-104">撥置中心控制項會擴充 TAPI 3 物件模型，以支援 (ACD) 系統的自動呼叫散發需求。</span><span class="sxs-lookup"><span data-stu-id="5927f-104">Call center controls extend the TAPI 3 object model to support the requirements of Automatic Call Distribution (ACD) systems.</span></span> <span data-ttu-id="5927f-105">撥接中心是在電話銀行撥打電話或撥入來電的地點。</span><span class="sxs-lookup"><span data-stu-id="5927f-105">A call center is a location with agents or operators at banks of telephones either making outgoing telephone calls or fielding incoming ones.</span></span> <span data-ttu-id="5927f-106">例如，銀行或信用卡公司會使用撥入中心來處理帳戶查詢。</span><span class="sxs-lookup"><span data-stu-id="5927f-106">For example, a bank or credit card company will use a call center to process account inquiries.</span></span>

<span data-ttu-id="5927f-107">電話中心應用程式分成三種基本類型：</span><span class="sxs-lookup"><span data-stu-id="5927f-107">Call center applications are divided into three basic types:</span></span>

-   <span data-ttu-id="5927f-108">[ACD Proxy](acd-proxy.md)：處理伺服器上的傳入或傳出會話，這可以是來自專屬電話交換器到網際網路閘道的任何內容。</span><span class="sxs-lookup"><span data-stu-id="5927f-108">[ACD Proxy](acd-proxy.md): Handles incoming or outgoing sessions at the server, which can be anything from a proprietary telephone switch to an Internet gateway.</span></span>
-   <span data-ttu-id="5927f-109">[ACD 代理程式用戶端](acd-agent-client.md)：服務正在接收或發出呼叫的個別代理程式。</span><span class="sxs-lookup"><span data-stu-id="5927f-109">[ACD Agent Client](acd-agent-client.md): Services an individual agent who is receiving or making calls.</span></span>
-   <span data-ttu-id="5927f-110">ACD 監督員用戶端：提供代理程式和 ACD 作業的整體觀點。</span><span class="sxs-lookup"><span data-stu-id="5927f-110">ACD Supervisor Client: Provides an overall view of agent and ACD operations.</span></span>

> [!Note]  
> <span data-ttu-id="5927f-111">針對 Windows 2000，可使用 TAPI 2.2 提供 proxy 功能，而不會執行監督員功能。</span><span class="sxs-lookup"><span data-stu-id="5927f-111">For Windows 2000, proxy functionality is available using TAPI 2.2, and supervisor functions are not implemented.</span></span>

 

<span data-ttu-id="5927f-112">Windows SDK 的 [範例] 區段包含 Netds \\ tapi \\ Tapi2 \\ ACD 和 Netds \\ tapi \\ Tapi3 \\ ACD 下的 ACD 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="5927f-112">The samples section of the Windows SDK contains ACD code samples under Netds\\Tapi\\Tapi2\\Acd and Netds\\Tapi\\Tapi3\\Acd.</span></span>

 

 



