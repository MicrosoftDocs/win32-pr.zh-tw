---
title: NAP 用戶端和伺服器端元件通訊
description: NAP 用戶端和伺服器端元件通訊
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372538"
---
# <a name="nap-client-and-server-side-component-communication"></a><span data-ttu-id="84b39-103">NAP 用戶端和伺服器端元件通訊</span><span class="sxs-lookup"><span data-stu-id="84b39-103">NAP Client and Server-side Component Communication</span></span>

> [!Note]  
> <span data-ttu-id="84b39-104">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="84b39-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="84b39-105">NAP 代理程式元件可以透過下列程式與 NAP 管理伺服器元件通訊：</span><span class="sxs-lookup"><span data-stu-id="84b39-105">The NAP Agent component can communicate with the NAP Administration Server component through the following process:</span></span>

1.  <span data-ttu-id="84b39-106">NAP 代理程式會將 SSoH 傳遞至 NAP EC。</span><span class="sxs-lookup"><span data-stu-id="84b39-106">The NAP Agent passes the SSoH to the NAP EC.</span></span>
2.  <span data-ttu-id="84b39-107">NAP EC 會將 SSoH 傳遞給 NAP ES。</span><span class="sxs-lookup"><span data-stu-id="84b39-107">The NAP EC passes the SSoH to the NAP ES.</span></span>
3.  <span data-ttu-id="84b39-108">NAP ES 會將 SSoH 傳遞至網路原則伺服器 (NPS) 服務。</span><span class="sxs-lookup"><span data-stu-id="84b39-108">The NAP ES passes the SSoH to the Network Policy Server (NPS) service.</span></span>
4.  <span data-ttu-id="84b39-109">NPS 服務會將 SSoH 傳遞給 NAP 管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="84b39-109">The NPS service passes the SSoH to the NAP Administration Server.</span></span>

<span data-ttu-id="84b39-110">SHA 可透過下列進程與其對應的 SHV 通訊：</span><span class="sxs-lookup"><span data-stu-id="84b39-110">An SHA can communicate with its corresponding SHV through the following process:</span></span>

1.  <span data-ttu-id="84b39-111">SHA 會將其 SoH 傳遞給 NAP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="84b39-111">The SHA passes its SoH to the NAP Agent.</span></span>
2.  <span data-ttu-id="84b39-112">NAP 代理程式會將包含在 SSoH 內的 SoH 傳遞至 NAP EC。</span><span class="sxs-lookup"><span data-stu-id="84b39-112">The NAP Agent passes the SoH, contained within the SSoH, to the NAP EC.</span></span>
3.  <span data-ttu-id="84b39-113">NAP EC 會將 SoH 傳遞給 NAP ES。</span><span class="sxs-lookup"><span data-stu-id="84b39-113">The NAP EC passes the SoH to the NAP ES.</span></span>
4.  <span data-ttu-id="84b39-114">NAP ES 將 SoH 傳遞給 NAP 管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="84b39-114">The NAP ES passes the SoH to the NAP Administration Server.</span></span>
5.  <span data-ttu-id="84b39-115">NAP 管理伺服器會將 SoH 傳遞給 SHV。</span><span class="sxs-lookup"><span data-stu-id="84b39-115">The NAP Administration Server passes the SoH to the SHV.</span></span>

<span data-ttu-id="84b39-116">下圖顯示 NAP 用戶端元件與 NAP 伺服器端元件之間的通訊流程。</span><span class="sxs-lookup"><span data-stu-id="84b39-116">The figure below shows the communication process from NAP client components to NAP server-side components.</span></span>

![nap 平臺中用戶端對伺服器通訊的架構](images/nap-client-to-server-comm.png)

<span data-ttu-id="84b39-118">NAP 管理伺服器可以透過下列程式與 NAP 代理程式通訊：</span><span class="sxs-lookup"><span data-stu-id="84b39-118">The NAP Administration Server can communicate with the NAP Agent through the following process:</span></span>

1.  <span data-ttu-id="84b39-119">NAP 管理伺服器會將 Sohr 傳遞給 NPS 服務。</span><span class="sxs-lookup"><span data-stu-id="84b39-119">The NAP Administration Server passes the SoHRs to the NPS service.</span></span>
2.  <span data-ttu-id="84b39-120">NPS 服務會將 SSoHR 傳遞至 NAP ES。</span><span class="sxs-lookup"><span data-stu-id="84b39-120">The NPS service passes the SSoHR to the NAP ES.</span></span>
3.  <span data-ttu-id="84b39-121">NAP ES 會將 SSoHR 傳遞給 NAP EC。</span><span class="sxs-lookup"><span data-stu-id="84b39-121">The NAP ES passes the SSoHR to the NAP EC.</span></span>
4.  <span data-ttu-id="84b39-122">NAP EC 將 SSoHR 傳遞給 NAP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="84b39-122">The NAP EC passes the SSoHR to the NAP Agent.</span></span>

<span data-ttu-id="84b39-123">SHV 可透過下列進程與其對應的 SHA 通訊：</span><span class="sxs-lookup"><span data-stu-id="84b39-123">The SHV can communicate with its corresponding SHA through the following process:</span></span>

1.  <span data-ttu-id="84b39-124">SHV 會將其 SoHR 傳遞給 NAP 管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="84b39-124">The SHV passes its SoHR to the NAP Administration Server.</span></span>
2.  <span data-ttu-id="84b39-125">NAP 管理伺服器會將 SoHR 傳遞給 NPS 服務。</span><span class="sxs-lookup"><span data-stu-id="84b39-125">The NAP Administration Server passes the SoHR to the NPS service.</span></span>
3.  <span data-ttu-id="84b39-126">NPS 服務會將包含在 SSoHR 中的 SoHR 傳遞至 NAP ES。</span><span class="sxs-lookup"><span data-stu-id="84b39-126">The NPS service passes the SoHR, contained within the SSoHR, to the NAP ES.</span></span>
4.  <span data-ttu-id="84b39-127">NAP ES 會將 SoHR 傳遞給 NAP EC。</span><span class="sxs-lookup"><span data-stu-id="84b39-127">The NAP ES passes the SoHR to the NAP EC.</span></span>
5.  <span data-ttu-id="84b39-128">NAP EC 將 SoHR 傳遞給 NAP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="84b39-128">The NAP EC passes the SoHR to the NAP Agent.</span></span>
6.  <span data-ttu-id="84b39-129">NAP 代理程式會將 SoHR 傳遞給 SHA。</span><span class="sxs-lookup"><span data-stu-id="84b39-129">The NAP Agent passes the SoHR to the SHA.</span></span>

<span data-ttu-id="84b39-130">下圖顯示從 NAP 伺服器端元件到 NAP 用戶端元件的通訊流程。</span><span class="sxs-lookup"><span data-stu-id="84b39-130">The figure below shows the communication process from NAP server-side components to NAP client components.</span></span>

![nap 平臺中伺服器對用戶端通訊的架構](images/nap-server-to-client-comm.png)

 

 




