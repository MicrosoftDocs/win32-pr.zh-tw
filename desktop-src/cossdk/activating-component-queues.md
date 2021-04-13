---
description: 啟用元件佇列
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: 啟用元件佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385921"
---
# <a name="activating-component-queues"></a><span data-ttu-id="642ac-103">啟用元件佇列</span><span class="sxs-lookup"><span data-stu-id="642ac-103">Activating Component Queues</span></span>

<span data-ttu-id="642ac-104">在已排入佇列的元件上進行方法呼叫，並不會直接執行方法。</span><span class="sxs-lookup"><span data-stu-id="642ac-104">Making method calls on a queued component does not directly execute the method.</span></span> <span data-ttu-id="642ac-105">相反地， [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 會將方法呼叫和參數封送處理並儲存在佇列中，而佇列中的這些呼叫和參數稍後會由佇列元件進行抓取和執行</span><span class="sxs-lookup"><span data-stu-id="642ac-105">Rather, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshals and stores method calls and parameters in a queue where they are later retrieved and executed by the queued component.</span></span> <span data-ttu-id="642ac-106">與啟動遠端 DCOM 物件不同的是，在呼叫方法時，不會具現化已排入佇列的元件。</span><span class="sxs-lookup"><span data-stu-id="642ac-106">Unlike activating a remote DCOM object, the queued component is not instantiated when a method is called.</span></span> <span data-ttu-id="642ac-107">這是使用已排入佇列之元件背後的基本概念，佇列元件不需要與呼叫應用程式同時具現化。</span><span class="sxs-lookup"><span data-stu-id="642ac-107">This is the basic idea behind using queued components—queued components need not be instantiated at the same time as the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="642ac-108">啟用佇列應用程式的描述會假設應用程式已標示為已排入佇列，而且已啟用 [接聽程式] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="642ac-108">The descriptions for activating a queued application assume that the application is marked as queued and that the listener check box is enabled.</span></span>

 

<span data-ttu-id="642ac-109">您可以使用腳本來啟動和停止已排入佇列的應用程式。</span><span class="sxs-lookup"><span data-stu-id="642ac-109">You can use scripting to start and stop a queued application.</span></span> <span data-ttu-id="642ac-110">您可以將腳本放在工作排程器的控制項底下，以視需要執行。</span><span class="sxs-lookup"><span data-stu-id="642ac-110">You can put the script under the control of the task scheduler to run it as required.</span></span> <span data-ttu-id="642ac-111">例如，如果應用程式是可永久提供的，則腳本可以在系統重新開機時執行。</span><span class="sxs-lookup"><span data-stu-id="642ac-111">For example, the script can be run on system reboot if the applications are to be permanently available.</span></span> <span data-ttu-id="642ac-112">如果應用程式是以批次模式處理交易，則可以在每天的特定時間執行腳本，並搭配關機腳本，以確保批次處理會在特定時間停止。</span><span class="sxs-lookup"><span data-stu-id="642ac-112">If the application is to process transactions in batch mode, the script can be run at a certain time each day in conjunction with a shutdown script to be sure the batch processing stops at a specific time.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="642ac-113">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="642ac-113">Component Services Administrative Tool</span></span>

<span data-ttu-id="642ac-114">若要啟動已排入佇列的應用程式，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="642ac-114">To start a queued application, use the following steps:</span></span>

1.  <span data-ttu-id="642ac-115">在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="642ac-115">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="642ac-116">以滑鼠右鍵按一下您想要啟用其佇列的應用程式。</span><span class="sxs-lookup"><span data-stu-id="642ac-116">Right-click the application whose queue you want to activate.</span></span>

3.  <span data-ttu-id="642ac-117">按一下 [啟動]。</span><span class="sxs-lookup"><span data-stu-id="642ac-117">Click **Start**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="642ac-118">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="642ac-118">Visual Basic</span></span>

<span data-ttu-id="642ac-119">請參閱 COMAdminCatalog. StartApplication 範例。</span><span class="sxs-lookup"><span data-stu-id="642ac-119">See the COMAdminCatalog.StartApplication example.</span></span>

## <a name="cc"></a><span data-ttu-id="642ac-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="642ac-120">C/C++</span></span>

<span data-ttu-id="642ac-121">請參閱 [**ICOMAdminCatalog：： StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) 範例。</span><span class="sxs-lookup"><span data-stu-id="642ac-121">See the [**ICOMAdminCatalog::StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="642ac-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="642ac-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="642ac-123">使用佇列的標記</span><span class="sxs-lookup"><span data-stu-id="642ac-123">Using the Queue Moniker</span></span>](using-the-queue-moniker.md)
</dt> </dl>

 

 



