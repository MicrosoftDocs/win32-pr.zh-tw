---
title: 啟動和停止 Microsoft 定位器
description: 必要時，RPC 執行時間程式庫會自動啟動 Microsoft 定位器。 例如，您可以手動停止和啟動定位器，例如，當您在將分散式應用程式進行偵錯工具時，需要清除資料庫時。
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020733"
---
# <a name="starting-and-stopping-microsoft-locator"></a><span data-ttu-id="9be7d-104">啟動和停止 Microsoft 定位器</span><span class="sxs-lookup"><span data-stu-id="9be7d-104">Starting and Stopping Microsoft Locator</span></span>

<span data-ttu-id="9be7d-105">必要時，RPC 執行時間程式庫會自動啟動 Microsoft 定位器。</span><span class="sxs-lookup"><span data-stu-id="9be7d-105">The RPC run-time libraries automatically start Microsoft Locator when necessary.</span></span> <span data-ttu-id="9be7d-106">例如，您可以手動停止和啟動定位器，例如，當您在將分散式應用程式進行偵錯工具時，需要清除資料庫時。</span><span class="sxs-lookup"><span data-stu-id="9be7d-106">You can manually stop and start the Locator if, for example, you need to clear the database while debugging a distributed application.</span></span>

<span data-ttu-id="9be7d-107">**若要停止並啟動 Microsoft 定位器**</span><span class="sxs-lookup"><span data-stu-id="9be7d-107">**To stop and start Microsoft Locator**</span></span>

1.  <span data-ttu-id="9be7d-108">在主控台中，按一下 [服務] 圖示。</span><span class="sxs-lookup"><span data-stu-id="9be7d-108">From Control Panel, click the Services icon.</span></span>

    <span data-ttu-id="9be7d-109">[ **服務** ] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="9be7d-109">The **Services** dialog box appears.</span></span>

2.  <span data-ttu-id="9be7d-110">在 [ **服務** ] 對話方塊中，選取 [ **Microsoft 定位器** ]，然後按一下 [ **啟動** ] 或 [ **停止**]。</span><span class="sxs-lookup"><span data-stu-id="9be7d-110">In the **Service** dialog box, select **Microsoft Locator** and then click **Start** or **Stop**.</span></span>

<span data-ttu-id="9be7d-111">您也可以從命令列啟動和停止 Microsoft 定位器，方法是輸入：</span><span class="sxs-lookup"><span data-stu-id="9be7d-111">You can also start and stop Microsoft Locator from the command line by typing:</span></span>

<span data-ttu-id="9be7d-112">**net \[ start/stop \] rpclocator**</span><span class="sxs-lookup"><span data-stu-id="9be7d-112">**net \[start/stop\] rpclocator**</span></span>

<span data-ttu-id="9be7d-113">只有系統管理員可以在停止後啟動 Microsoft 定位器。</span><span class="sxs-lookup"><span data-stu-id="9be7d-113">Only an administrator can start Microsoft Locator once it is stopped.</span></span> <span data-ttu-id="9be7d-114">如果已停止，則會視 RPC 執行時間程式庫的需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="9be7d-114">If stopped, it will be restarted as necessary by the RPC run-time libraries.</span></span>

 

 




