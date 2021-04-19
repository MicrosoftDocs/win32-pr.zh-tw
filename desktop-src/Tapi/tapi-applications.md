---
description: 下列內容提供使用 TAPI 撰寫終端使用者或伺服器通訊應用程式的指導方針。 這項資訊也與服務提供者程式設計師高度相關。
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: TAPI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984701"
---
# <a name="tapi-applications"></a><span data-ttu-id="6b4b5-104">TAPI 應用程式</span><span class="sxs-lookup"><span data-stu-id="6b4b5-104">TAPI Applications</span></span>

<span data-ttu-id="6b4b5-105">下列內容提供使用 TAPI 撰寫終端使用者或伺服器通訊應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-105">The following material provides guidelines on using TAPI to write end-user or server communications applications.</span></span> <span data-ttu-id="6b4b5-106">這項資訊也與服務提供者程式設計師高度相關。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-106">This information is also highly relevant to service provider programmers.</span></span>

<span data-ttu-id="6b4b5-107">程式設計師需要使用 TAPI 進行的第一個決策是需要的服務層級。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-107">The first decision a programmer needs to make in using TAPI is the level of service required.</span></span> <span data-ttu-id="6b4b5-108">例如，如果應用程式需要可撥電話號碼的功能表選取專案，則可能不需要完整的 TAPI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-108">For example, if an application requires a menu selection that can dial a phone number, a full TAPI application is probably not required.</span></span> <span data-ttu-id="6b4b5-109">輔助電話語音可以快速且單純地啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-109">Assisted Telephony can enable this option quickly and simply.</span></span> <span data-ttu-id="6b4b5-110">如需完整 TAPI 應用程式和輔助電話語音之間差異的詳細資訊，請參閱 [服務的 TAPI 等級](tapi-levels-of-service.md) 。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-110">Please see [TAPI Levels of Service](tapi-levels-of-service.md) for more information on the distinction between full TAPI applications and Assisted Telephony.</span></span>

<span data-ttu-id="6b4b5-111">第二個重要的決定是要使用 TAPI 2.x、以 C 為基礎的 API，或 TAPI 3.x （以 COM 為基礎）。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-111">The second important decision is whether to use TAPI 2.x, the C-based API, or TAPI 3.x, which is based on COM.</span></span> <span data-ttu-id="6b4b5-112">請參閱 [tapi 3.x 與 tapi](tapi-3-x-versus-tapi-2-x.md) 2.x，以瞭解決定要使用哪一項的重要考慮。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-112">Please see [TAPI 3.x vs. TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) for a discussion of important considerations in deciding which one to use.</span></span>

<span data-ttu-id="6b4b5-113">下圖說明完整 TAPI 應用程式的基本組建區塊。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-113">The following diagram illustrates the basic building blocks of a full TAPI application.</span></span> <span data-ttu-id="6b4b5-114">TAPI 2.x 和 TAPI 3.x 都在這些章節中解決。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-114">TAPI 2.x and TAPI 3.x are both addressed in these sections.</span></span> <span data-ttu-id="6b4b5-115">在 TAPI 2.x 或 TAPI 3.x 的總覽章節中，將會說明高度特定的材質。</span><span class="sxs-lookup"><span data-stu-id="6b4b5-115">Material that is highly specific to one is addressed in the overview sections for TAPI 2.x or TAPI 3.x.</span></span>

![tapi 應用程式的建立區塊](images/tapior3.png)

<span data-ttu-id="6b4b5-117">下列連結提供的內容對應至上圖中的圖表：</span><span class="sxs-lookup"><span data-stu-id="6b4b5-117">The following links provide content that corresponds to the figures in the above image:</span></span>

| <span data-ttu-id="6b4b5-118">圖</span><span class="sxs-lookup"><span data-stu-id="6b4b5-118">Figure</span></span> | <span data-ttu-id="6b4b5-119">文件</span><span class="sxs-lookup"><span data-stu-id="6b4b5-119">Documentation</span></span>                                                                    |
|--------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b4b5-120">1</span><span class="sxs-lookup"><span data-stu-id="6b4b5-120">1</span></span>      | [<span data-ttu-id="6b4b5-121">TAPI 初始化</span><span class="sxs-lookup"><span data-stu-id="6b4b5-121">TAPI Initialization</span></span>](tapi-initialization.md)                                   |
| <span data-ttu-id="6b4b5-122">2</span><span class="sxs-lookup"><span data-stu-id="6b4b5-122">2</span></span>      | [<span data-ttu-id="6b4b5-123">會話控制項</span><span class="sxs-lookup"><span data-stu-id="6b4b5-123">Session Control</span></span>](session-control.md)                                           |
| <span data-ttu-id="6b4b5-124">3</span><span class="sxs-lookup"><span data-stu-id="6b4b5-124">3</span></span>      | [<span data-ttu-id="6b4b5-125">裝置控制</span><span class="sxs-lookup"><span data-stu-id="6b4b5-125">Device Control</span></span>](device-control.md)                                             |
| <span data-ttu-id="6b4b5-126">4</span><span class="sxs-lookup"><span data-stu-id="6b4b5-126">4</span></span>      | [<span data-ttu-id="6b4b5-127">媒體控制項</span><span class="sxs-lookup"><span data-stu-id="6b4b5-127">Media Control</span></span>](media-control.md)                                               |
| <span data-ttu-id="6b4b5-128">5</span><span class="sxs-lookup"><span data-stu-id="6b4b5-128">5</span></span>      | [<span data-ttu-id="6b4b5-129">關於撥置中心控制項</span><span class="sxs-lookup"><span data-stu-id="6b4b5-129">About Call Center Controls</span></span>](about-call-center-controls.md)                     |
| <span data-ttu-id="6b4b5-130">6</span><span class="sxs-lookup"><span data-stu-id="6b4b5-130">6</span></span>      | [<span data-ttu-id="6b4b5-131">彙集 IP 電話語音會議</span><span class="sxs-lookup"><span data-stu-id="6b4b5-131">Rendezvous IP Telephony Conferencing</span></span>](rendezvous-ip-telephony-conferencing.md) |
| <span data-ttu-id="6b4b5-132">7</span><span class="sxs-lookup"><span data-stu-id="6b4b5-132">7</span></span>      | [<span data-ttu-id="6b4b5-133">TAPI 關機</span><span class="sxs-lookup"><span data-stu-id="6b4b5-133">TAPI Shutdown</span></span>](tapi-shutdown.md)                                               |



 

 

 



