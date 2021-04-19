---
description: 包含至少一個 queuable 元件的應用程式，可以使用 [元件服務] 系統管理工具標示為已排入佇列。
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: 建立元件佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972556"
---
# <a name="creating-component-queues"></a><span data-ttu-id="3f360-103">建立元件佇列</span><span class="sxs-lookup"><span data-stu-id="3f360-103">Creating Component Queues</span></span>

<span data-ttu-id="3f360-104">包含至少一個 queuable 元件的應用程式，可以使用 [元件服務] 系統管理工具標示為已排入佇列。</span><span class="sxs-lookup"><span data-stu-id="3f360-104">An application that contains at least one queuable component can be marked as queued using the component services administrative tool.</span></span>

<span data-ttu-id="3f360-105">當應用程式標示為已排入佇列時，COM + 會自動為其建立訊息佇列的佇列。</span><span class="sxs-lookup"><span data-stu-id="3f360-105">When an application is marked as queued, COM+ automatically creates a message queuing queue for it.</span></span> <span data-ttu-id="3f360-106">佇列名稱是應用程式的名稱;如果佇列名稱與現有佇列的名稱相符，COM + 將會使用現有的佇列。</span><span class="sxs-lookup"><span data-stu-id="3f360-106">The queue name is the name of the application; if the queue name matches the name of an existing queue, COM+ will use the existing queue.</span></span>

> [!Note]  
> <span data-ttu-id="3f360-107">訊息佇列 *路徑* 名稱參數是遠端伺服器名稱 (RSN) 和 com + 應用程式名稱的組合。</span><span class="sxs-lookup"><span data-stu-id="3f360-107">The Message Queuing *PathName* parameter is a combination of the Remote Server Name (RSN) and the COM+ application name.</span></span> <span data-ttu-id="3f360-108">RSN 指的是遠端啟用的目標。</span><span class="sxs-lookup"><span data-stu-id="3f360-108">The RSN refers to the target of a remote activation.</span></span> <span data-ttu-id="3f360-109">您可以在用戶端電腦上安裝用戶端可匯出的應用程式期間指定 RSN。</span><span class="sxs-lookup"><span data-stu-id="3f360-109">You specify an RSN during the installation of a client exportable application on a client computer.</span></span> <span data-ttu-id="3f360-110">此安裝程式會使用 RSN，將啟用直接導向至指定的用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="3f360-110">The installation procedure uses the RSN to direct activation to a specified client computer.</span></span> <span data-ttu-id="3f360-111">如需有關佇列名稱的詳細資訊，請參閱 [使用佇列](using-the-queue-moniker.md)的「佇列標記參數」一節中的參數表格。</span><span class="sxs-lookup"><span data-stu-id="3f360-111">For more information about queue names, refer to the table of parameters in the "Queue Moniker Parameters" section in [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3f360-112">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="3f360-112">Component Services Administrative Tool</span></span>

<span data-ttu-id="3f360-113">若要將 COM + 應用程式指定為已排入佇列，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="3f360-113">To specify a COM+ application as queued, use the following steps:</span></span>

1.  <span data-ttu-id="3f360-114">在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="3f360-114">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="3f360-115">以滑鼠右鍵按一下您要建立佇列的應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="3f360-115">Right-click the application for which you wish to create a queue, and then click **Properties**.</span></span>

3.  <span data-ttu-id="3f360-116">在 [屬性] 對話方塊中，選取 [ **佇列** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="3f360-116">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="3f360-117">啟用標示為 [已 **排入佇列] 的核取方塊–此應用程式可由 MSMQ 佇列達成**。</span><span class="sxs-lookup"><span data-stu-id="3f360-117">Activate the check box labeled **Queued – This application can be reached by MSMQ queues**.</span></span>

    > [!Note]  
    > <span data-ttu-id="3f360-118">如果 [已 **排入佇列** ] 核取方塊呈現灰色，則應用程式不會包含任何 queuable 元件。</span><span class="sxs-lookup"><span data-stu-id="3f360-118">If the **Queued** check box is grayed out, the application contains no queuable components.</span></span>

     

5.  <span data-ttu-id="3f360-119">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="3f360-119">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3f360-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3f360-120">Visual Basic</span></span>

<span data-ttu-id="3f360-121">不適用。</span><span class="sxs-lookup"><span data-stu-id="3f360-121">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="3f360-122">C/C++</span><span class="sxs-lookup"><span data-stu-id="3f360-122">C/C++</span></span>

<span data-ttu-id="3f360-123">不適用。</span><span class="sxs-lookup"><span data-stu-id="3f360-123">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f360-124">備註</span><span class="sxs-lookup"><span data-stu-id="3f360-124">Remarks</span></span>

<span data-ttu-id="3f360-125">COM + 系統管理程式庫或 [元件服務] 系統管理工具所建立的佇列，會以訊息佇列的交易屬性標記。</span><span class="sxs-lookup"><span data-stu-id="3f360-125">Queues created by the COM+ Administration Library or the Component Services administrative tool are marked with the Message Queuing transactional attribute.</span></span>

<span data-ttu-id="3f360-126">在伺服器上安裝佇列應用程式之後，用戶端可以藉由匯出應用程式，然後在每個用戶端匯入應用程式，讓用戶端可以使用該應用程式。</span><span class="sxs-lookup"><span data-stu-id="3f360-126">After a queued application is installed at the server, it can be made available to clients by exporting the application and then importing the application at each client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f360-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f360-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f360-128">建立 Queuable 元件</span><span class="sxs-lookup"><span data-stu-id="3f360-128">Creating Queuable Components</span></span>](creating-queuable-components.md)
</dt> <dt>

[<span data-ttu-id="3f360-129">已排入佇列的元件架構</span><span class="sxs-lookup"><span data-stu-id="3f360-129">Queued Components Architecture</span></span>](queued-components-architecture.md)
</dt> </dl>

 

 



