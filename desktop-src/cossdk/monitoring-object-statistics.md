---
description: 您可以在應用程式執行時監視物件統計資料。 如此一來，您就可以微調物件集區的特性，以達到您想要的效能和資源平衡。
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: 監視物件統計資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317856"
---
# <a name="monitoring-object-statistics"></a><span data-ttu-id="0a20c-104">監視物件統計資料</span><span class="sxs-lookup"><span data-stu-id="0a20c-104">Monitoring Object Statistics</span></span>

<span data-ttu-id="0a20c-105">您可以在應用程式執行時監視物件統計資料。</span><span class="sxs-lookup"><span data-stu-id="0a20c-105">You can monitor object statistics as an application runs.</span></span> <span data-ttu-id="0a20c-106">如此一來，您就可以微調物件集區的特性，以達到您想要的效能和資源平衡。</span><span class="sxs-lookup"><span data-stu-id="0a20c-106">By doing so, you can fine-tune the object pool characteristics to achieve the balance in performance and resources that you would like to have.</span></span>

<span data-ttu-id="0a20c-107">您可以監視設定為支持對象統計資料和附隨報告之任何物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a20c-107">You can monitor status for any objects that are configured to support object statistics and event reporting.</span></span> <span data-ttu-id="0a20c-108">啟用物件統計資料會稍微降低效能。</span><span class="sxs-lookup"><span data-stu-id="0a20c-108">Enabling object statistics has a very slight performance overhead.</span></span>

<span data-ttu-id="0a20c-109">**啟用物件統計資料**</span><span class="sxs-lookup"><span data-stu-id="0a20c-109">**To enable object statistics**</span></span>

1.  <span data-ttu-id="0a20c-110">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="0a20c-110">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="0a20c-111">在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0a20c-111">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="0a20c-112">若要啟用元件的物件統計資料，請在 [ **啟用內容**] 下，選取 [ **元件支援事件和統計資料]** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="0a20c-112">To enable object statistics for the component, under **Activation Context**, select the **Component supports events and statistics** check box.</span></span>

<span data-ttu-id="0a20c-113">**若要監視物件狀態**</span><span class="sxs-lookup"><span data-stu-id="0a20c-113">**To monitor object status**</span></span>

1.  <span data-ttu-id="0a20c-114">在 [元件服務] 系統管理工具的主控台樹中，開啟包含您要監視之元件的應用程式資料夾。</span><span class="sxs-lookup"><span data-stu-id="0a20c-114">In the console tree of the Component Services administrative tool, open the folder for the application that includes the components you want to monitor.</span></span>

2.  <span data-ttu-id="0a20c-115">以滑鼠右鍵按一下 [ **元件** ] 資料夾，指向 [ **view**]，然後按一下 [ **狀態視圖**]。</span><span class="sxs-lookup"><span data-stu-id="0a20c-115">Right-click the **Components** folder, point to **View**, and then click **Status View**.</span></span> <span data-ttu-id="0a20c-116">[詳細資料] 窗格現在會顯示應用程式中所有元件的狀態視圖。</span><span class="sxs-lookup"><span data-stu-id="0a20c-116">The details pane now displays the status view for all components in the application.</span></span> <span data-ttu-id="0a20c-117">下表描述狀態視圖中的六個數據行。</span><span class="sxs-lookup"><span data-stu-id="0a20c-117">The following table describes the six columns in the status view.</span></span>

    

    | <span data-ttu-id="0a20c-118">Column</span><span class="sxs-lookup"><span data-stu-id="0a20c-118">Column</span></span>                        | <span data-ttu-id="0a20c-119">描述</span><span class="sxs-lookup"><span data-stu-id="0a20c-119">Description</span></span>                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0a20c-120">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="0a20c-120">**ProgID**</span></span><br/>         | <span data-ttu-id="0a20c-121">識別特定元件。</span><span class="sxs-lookup"><span data-stu-id="0a20c-121">Identifies a specific component.</span></span><br/>                                                                                                                                                                                |
    | <span data-ttu-id="0a20c-122">**物件**</span><span class="sxs-lookup"><span data-stu-id="0a20c-122">**Objects**</span></span><br/>        | <span data-ttu-id="0a20c-123">顯示用戶端參考目前保留的物件數目。</span><span class="sxs-lookup"><span data-stu-id="0a20c-123">Shows the number of objects that are currently held by client references.</span></span><br/>                                                                                                                                       |
    | <span data-ttu-id="0a20c-124">**已啟動**</span><span class="sxs-lookup"><span data-stu-id="0a20c-124">**Activated**</span></span><br/>      | <span data-ttu-id="0a20c-125">顯示目前已啟用的物件數目。</span><span class="sxs-lookup"><span data-stu-id="0a20c-125">Shows the number of objects that are currently activated.</span></span> <br/>                                                                                                                                                      |
    | <span data-ttu-id="0a20c-126">**彙集**</span><span class="sxs-lookup"><span data-stu-id="0a20c-126">**Pooled**</span></span><br/>         | <span data-ttu-id="0a20c-127">顯示集區所建立的物件總數，包括使用中的物件以及停用的物件。</span><span class="sxs-lookup"><span data-stu-id="0a20c-127">Shows the total number of objects created by the pool, including objects that are in use and objects that are deactivated.</span></span><br/>                                                                                      |
    | <span data-ttu-id="0a20c-128">**在呼叫中**</span><span class="sxs-lookup"><span data-stu-id="0a20c-128">**In Call**</span></span><br/>        | <span data-ttu-id="0a20c-129">識別呼叫中的物件。</span><span class="sxs-lookup"><span data-stu-id="0a20c-129">Identifies objects in call.</span></span><br/>                                                                                                                                                                                     |
    | <span data-ttu-id="0a20c-130">**呼叫時間 (ms)**</span><span class="sxs-lookup"><span data-stu-id="0a20c-130">**Call Time (ms)**</span></span><br/> | <span data-ttu-id="0a20c-131">顯示在過去20秒內 (的平均通話持續時間，以毫秒為單位)  (最多20個呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="0a20c-131">Shows the average call duration (in milliseconds) of method calls made in the last 20 seconds (up to 20 calls).</span></span> <span data-ttu-id="0a20c-132">呼叫時間是在物件上測量，不包含用來跨越網路的時間。</span><span class="sxs-lookup"><span data-stu-id="0a20c-132">Call time is measured at the object and does not include the time used to traverse the network.</span></span><br/> |

    

     

## <a name="related-topics"></a><span data-ttu-id="0a20c-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a20c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a20c-134">設定要共用的元件</span><span class="sxs-lookup"><span data-stu-id="0a20c-134">Configuring a Component to Be Pooled</span></span>](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




