---
description: TAPI 伺服器 (TAPISRV) 是使用者電腦上電話語音資料的中央存放庫。
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: TAPI 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850796"
---
# <a name="tapi-server"></a><span data-ttu-id="c0ec8-103">TAPI 伺服器</span><span class="sxs-lookup"><span data-stu-id="c0ec8-103">TAPI Server</span></span>

<span data-ttu-id="c0ec8-104">TAPI 伺服器 (TAPISRV) 是使用者電腦上電話語音資料的中央存放庫。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-104">The TAPI server (TAPISRV) is the central repository of telephony data on a user computer.</span></span> <span data-ttu-id="c0ec8-105">此服務處理常式會追蹤本機和遠端電話語音資源、註冊用來處理輔助電話語音要求的應用程式，以及擱置中的非同步函式，也會啟用與電話語音服務提供者一致的介面， (Tsp) 。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-105">This service process tracks local and remote telephony resources, applications registered to handle Assisted Telephony requests, and pending asynchronous functions, and it also enables a consistent interface with telephony service providers (TSPs).</span></span> <span data-ttu-id="c0ec8-106">如需詳細資訊以及說明 TAPI 伺服器與其他元件的關係以及其角色總覽的圖表，請參閱 [Microsoft 電話語音程式設計模型](microsoft-telephony-programming-model.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-106">For more information and a diagram that illustrates the relationship of the TAPI Server to other components and an overview of their roles, see [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span></span>

<span data-ttu-id="c0ec8-107">針對在 Windows Server 2003 作業系統、Windows XP 及 Windows 2000 上執行的電腦，TAPISRV 會在 Svchost.exe 的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-107">For computers running on Windows Server 2003 operating systems, Windows XP, and Windows 2000, TAPISRV runs within the context of Svchost.exe.</span></span> <span data-ttu-id="c0ec8-108">針對在 Windows NT 上執行的電腦，它會以個別的服務程式執行。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-108">For computers running on Windows NT, it runs as a separate service process.</span></span> <span data-ttu-id="c0ec8-109">當應用程式將 TAPI DLL 載入其進程空間並執行初始化操作時，DLL 會建立與 TAPI 伺服器的 RPC 連結。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-109">When an application loads a TAPI DLL into its process space and performs an initialization operation, the DLL establishes an RPC link to the TAPI Server.</span></span> <span data-ttu-id="c0ec8-110">TAPI 伺服器會將電話服務提供者 (Tsp) 載入其進程空間中。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-110">The TAPI Server loads telephone service providers (TSPs) into its process space.</span></span> <span data-ttu-id="c0ec8-111">無論有多少應用程式存取指定提供者的裝置，都只會有一個指定之 TSP 的實例存在。</span><span class="sxs-lookup"><span data-stu-id="c0ec8-111">Regardless of how many applications access a given provider's devices, only one instance of a given TSP will exist.</span></span>

 

 



