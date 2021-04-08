---
title: 發佈嚮導
description: 本節說明 Windows XP 發佈嚮導。
ms.assetid: 53279837-f57b-447a-8c71-03f635959fdb
keywords:
- 發佈嚮導，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5943c17fdf142e3b68af24aaa34d3eff3a47404
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931784"
---
# <a name="publishing-wizards"></a><span data-ttu-id="b5b58-104">發佈嚮導</span><span class="sxs-lookup"><span data-stu-id="b5b58-104">Publishing Wizards</span></span>

<span data-ttu-id="b5b58-105">本節說明 Windows XP 發佈嚮導。</span><span class="sxs-lookup"><span data-stu-id="b5b58-105">This section describes the Windows XP publishing wizards.</span></span>



| <span data-ttu-id="b5b58-106">主題</span><span class="sxs-lookup"><span data-stu-id="b5b58-106">Topic</span></span>                                               | <span data-ttu-id="b5b58-107">目錄</span><span class="sxs-lookup"><span data-stu-id="b5b58-107">Contents</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5b58-108">用戶端設計</span><span class="sxs-lookup"><span data-stu-id="b5b58-108">Client-Side Design</span></span>](pubwiz-client.md)             | <span data-ttu-id="b5b58-109">伺服器端 HTML 頁面中的腳本會與裝載的線上列印順序 Wizard 用戶端進行通訊。</span><span class="sxs-lookup"><span data-stu-id="b5b58-109">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="b5b58-110">這項通訊是透過 **window** 所存取的方法和屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="b5b58-110">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span><br/>                                 |
| [<span data-ttu-id="b5b58-111">發佈嚮導簡介</span><span class="sxs-lookup"><span data-stu-id="b5b58-111">Publishing Wizards Introduction</span></span>](pubwiz-intro.md) | <span data-ttu-id="b5b58-112">Windows XP 引進了 Web 發佈嚮導和線上列印順序 Wizard。</span><span class="sxs-lookup"><span data-stu-id="b5b58-112">Windows XP introduces the Web Publishing Wizard and Online Print Ordering Wizard.</span></span> <span data-ttu-id="b5b58-113">根據相同的架構，這些嚮導為使用者提供一個簡單的機制，可將內容發佈至網站，或訂購從數位影像檔進行的列印。</span><span class="sxs-lookup"><span data-stu-id="b5b58-113">Based on the same framework, these wizards provide the user with a simple mechanism for publishing content to a website or for ordering prints made from digital image files.</span></span><br/> |
| [<span data-ttu-id="b5b58-114">註冊服務</span><span class="sxs-lookup"><span data-stu-id="b5b58-114">Registering a Service</span></span>](pubwiz-reg.md)             | <span data-ttu-id="b5b58-115">若要將您的服務加入至 [Web 發佈嚮導] 或 [線上列印順序] Wizard 中的提供者清單，您必須將適當的金鑰和其值新增至 Windows 登錄。</span><span class="sxs-lookup"><span data-stu-id="b5b58-115">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span><br/>                                                                  |
| [<span data-ttu-id="b5b58-116">伺服器端設計</span><span class="sxs-lookup"><span data-stu-id="b5b58-116">Server-Side Design</span></span>](pubwiz-server.md)             | <span data-ttu-id="b5b58-117">伺服器端函式會透過 **windows 外部** 物件與用戶端 wizard 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="b5b58-117">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="b5b58-118">伺服器端腳本會提供這些函式來回應 wizard 事件，以及取得有關 wizard 的資訊。</span><span class="sxs-lookup"><span data-stu-id="b5b58-118">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span><br/>                                         |
| [<span data-ttu-id="b5b58-119">使用傳送資訊清單</span><span class="sxs-lookup"><span data-stu-id="b5b58-119">Using the Transfer Manifest</span></span>](pubwiz-manifest.md)  | <span data-ttu-id="b5b58-120">Web 發佈嚮導和線上列印順序 Wizard 會使用傳輸資訊清單來傳達用戶端電腦與伺服器網站之間資料傳輸的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b5b58-120">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span><br/>                                                                                   |



 

 

 





