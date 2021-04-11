---
description: 您可以使用 COM + 補償 Resource Manager (CRM) 輕鬆快速地整合應用程式資源與 Microsoft Distributed Transaction Coordinator (DTC) 交易。
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: COM + 補償 Resource Manager 概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14206a54ffcb4f7e06ddf7362736a722393b0791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936267"
---
# <a name="com-compensating-resource-manager-concepts"></a><span data-ttu-id="42d05-103">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="42d05-103">COM+ Compensating Resource Manager Concepts</span></span>

<span data-ttu-id="42d05-104">您可以使用 COM + 補償 Resource Manager (CRM) 輕鬆快速地整合應用程式資源與 Microsoft Distributed Transaction Coordinator (DTC) 交易。</span><span class="sxs-lookup"><span data-stu-id="42d05-104">You can use the COM+ Compensating Resource Manager (CRM) to easily and quickly integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span> <span data-ttu-id="42d05-105">您的應用程式資源可以針對交易的結果投票，並可接收其結果的最終通知。</span><span class="sxs-lookup"><span data-stu-id="42d05-105">Your application resources can vote on the outcome of a transaction and can receive final notification of its outcome.</span></span> <span data-ttu-id="42d05-106">系統會產生持久的記錄檔，讓您的應用程式資源可以寫入存留失敗的記錄，而 CRM 會在應用程式重新開機時復原此記錄檔。</span><span class="sxs-lookup"><span data-stu-id="42d05-106">A durable log is generated so that your application resources can write records that survive failures, and the CRM recovers this log file when the application restarts.</span></span>

<span data-ttu-id="42d05-107">CRM 包含下列兩個元件：</span><span class="sxs-lookup"><span data-stu-id="42d05-107">A CRM consists of the following two components:</span></span>

-   <span data-ttu-id="42d05-108">CRM 背景工作角色。</span><span class="sxs-lookup"><span data-stu-id="42d05-108">CRM Worker.</span></span> <span data-ttu-id="42d05-109">此元件會執行特定 CRM 的主要工作，並針對需要執行的工作，執行特定的介面。</span><span class="sxs-lookup"><span data-stu-id="42d05-109">This component performs the main work of the specific CRM and implements an interface specific to the task it needs to perform.</span></span> <span data-ttu-id="42d05-110">CRM 基礎結構為 crm 工作者提供了一個介面，CRM 工作者可以透過此介面將記錄寫入磁片上的持久記錄檔。</span><span class="sxs-lookup"><span data-stu-id="42d05-110">The CRM infrastructure provides an interface to the CRM Worker through which the CRM Worker can write records to a durable log file on disk.</span></span> <span data-ttu-id="42d05-111">CRM 工作者必須將記錄寫入記錄檔，並使其在執行其工作之前保持持久，如此一來，萬一發生損毀時，就可以正確進行復原。</span><span class="sxs-lookup"><span data-stu-id="42d05-111">The CRM Worker must write records to the log and make them durable before it performs its work so that, if a crash occurs, recovery can occur correctly.</span></span> <span data-ttu-id="42d05-112">CRM 背景工作一律需要交易。</span><span class="sxs-lookup"><span data-stu-id="42d05-112">The CRM Worker always requires a transaction.</span></span>
-   <span data-ttu-id="42d05-113">CRM 補償器。</span><span class="sxs-lookup"><span data-stu-id="42d05-113">CRM Compensator.</span></span> <span data-ttu-id="42d05-114">在交易完成時，CRM 基礎結構會建立此元件。</span><span class="sxs-lookup"><span data-stu-id="42d05-114">This component is created by the CRM infrastructure at the completion of the transaction.</span></span> <span data-ttu-id="42d05-115">它會執行已定義的介面，讓 CRM 基礎結構可以傳遞交易完成的通知，以及先前由 CRM 背景工作撰寫的記錄檔記錄。</span><span class="sxs-lookup"><span data-stu-id="42d05-115">It implements a defined interface by which the CRM infrastructure can pass on notifications of transaction completion and the log records that were previously written by the CRM Worker.</span></span>

<span data-ttu-id="42d05-116">COM + CRM 提供不可部分完成性的交易式通知，以及 CRM 記錄檔的持久性，但不提供資源的隔離。</span><span class="sxs-lookup"><span data-stu-id="42d05-116">A COM+ CRM provides atomicity with transactional notifications, and durability with the CRM log, but does not provide isolation of resources.</span></span> <span data-ttu-id="42d05-117">在多執行緒環境中，CRM 開發人員必須負責確保在交易中同時序列化多個 CRM 工作者或外部應用程式的資源存取權。</span><span class="sxs-lookup"><span data-stu-id="42d05-117">In a multithreaded environment, it is the responsibility of the CRM developer to ensure that access to resources, either by multiple CRM Workers or external applications, is serialized while in a transaction.</span></span>

<span data-ttu-id="42d05-118">交易通過準備階段之後，CRM 補償器和 CRM 工作者可以同時執行。</span><span class="sxs-lookup"><span data-stu-id="42d05-118">After the transaction has passed the prepare phase, the CRM Compensator and CRM Workers can be running concurrently.</span></span> <span data-ttu-id="42d05-119">當先前交易的 CRM 補償器仍在處理先前的交易時，新交易的 CRM 背景工作元件可能會變成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="42d05-119">It is possible for the CRM Worker component of a new transaction to become active while the CRM Compensator of a previous transaction is still processing the previous transaction.</span></span>

<span data-ttu-id="42d05-120">在 CRM 伺服器應用程式復原之前的失敗期間，應該將中斷的交易視為使用中且未完成。</span><span class="sxs-lookup"><span data-stu-id="42d05-120">During failures prior to recovery of the CRM server application, an interrupted transaction should be considered active and not complete.</span></span> <span data-ttu-id="42d05-121">在復原 CRM 伺服器進程之前，外部進程應該無法存取此特定交易所變更的資源。</span><span class="sxs-lookup"><span data-stu-id="42d05-121">It should not be possible for external processes to access the resources that were being changed by this particular transaction prior to recovery of the CRM server process.</span></span>

<span data-ttu-id="42d05-122">CRM 定義了基本 CRM 函式的三種介面類別型：</span><span class="sxs-lookup"><span data-stu-id="42d05-122">The CRM defines three interface types for the basic CRM functions:</span></span>

-   <span data-ttu-id="42d05-123">[**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) 會在 crm 員工上執行，並由 Crm 背景工作角色用來將記錄檔記錄寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="42d05-123">[**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) is implemented on the CRM clerk and is used by the CRM Worker to write log records to the log.</span></span> <span data-ttu-id="42d05-124">CRM 補償器也可以使用它。</span><span class="sxs-lookup"><span data-stu-id="42d05-124">It can also used by the CRM Compensator.</span></span>
-   <span data-ttu-id="42d05-125">[**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) 和 [**ICRMCOMPENSATORVARIANTS**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) 會在 CRM 補償器上執行。</span><span class="sxs-lookup"><span data-stu-id="42d05-125">[**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) and [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) are implemented on the CRM Compensator.</span></span> <span data-ttu-id="42d05-126">這些介面是用來將交易結果通知及其相關聯的記錄檔記錄傳遞給 CRM 補償器。</span><span class="sxs-lookup"><span data-stu-id="42d05-126">These interfaces are used to deliver transaction outcome notifications and their associated log records to the CRM Compensator.</span></span> <span data-ttu-id="42d05-127">通常，CRM 補償器只會根據它是否需要非結構化或結構化記錄檔記錄，來執行其中一個介面。</span><span class="sxs-lookup"><span data-stu-id="42d05-127">Normally, the CRM Compensator would implement only one of these interfaces, depending on whether it required unstructured or structured log records.</span></span> <span data-ttu-id="42d05-128">*結構化* 記錄是以 variant 集合的形式建立的記錄，通常可供 Microsoft Visual Basic 使用。</span><span class="sxs-lookup"><span data-stu-id="42d05-128">*Structured log records* are those that are built up as a collection of Variants and are typically for use by Microsoft Visual Basic.</span></span> <span data-ttu-id="42d05-129">*非結構化記錄檔記錄* 只是位元組緩衝區，通常可供 Microsoft Visual C++ 使用。</span><span class="sxs-lookup"><span data-stu-id="42d05-129">*Unstructured log records* are just a buffer of bytes and are typically for use by Microsoft Visual C++.</span></span> <span data-ttu-id="42d05-130">CRM 補償器可以同時執行兩個補償器介面;不過，一次只能有一個用來傳遞記錄檔記錄。</span><span class="sxs-lookup"><span data-stu-id="42d05-130">A CRM Compensator can implement both of the compensator interfaces; however, only one at a time is used to deliver log records.</span></span>
-   <span data-ttu-id="42d05-131">COM + CRM 監視介面可用來監視特定伺服器應用程式內的 Crm。</span><span class="sxs-lookup"><span data-stu-id="42d05-131">The COM+ CRM monitoring interfaces are used for monitoring the CRMs within a particular server application.</span></span> <span data-ttu-id="42d05-132">如需監視介面的詳細資訊，請參閱 [Com + CRM 監視介面](com--crm-monitoring-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="42d05-132">For detailed information about the monitoring interfaces, see [COM+ CRM Monitoring Interfaces](com--crm-monitoring-interfaces.md).</span></span>

<span data-ttu-id="42d05-133">本節中的下列主題提供 COM + CRM 服務的更多詳細資料：</span><span class="sxs-lookup"><span data-stu-id="42d05-133">The following topics in this section provide more detail about the COM+ CRM service:</span></span>

-   [<span data-ttu-id="42d05-134">COM + CRM 安全性考慮</span><span class="sxs-lookup"><span data-stu-id="42d05-134">COM+ CRM Security Considerations</span></span>](com--crm-security-considerations.md)
-   [<span data-ttu-id="42d05-135">COM + CRM 操作進程</span><span class="sxs-lookup"><span data-stu-id="42d05-135">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
-   [<span data-ttu-id="42d05-136">COM + CRM 啟動和復原</span><span class="sxs-lookup"><span data-stu-id="42d05-136">COM+ CRM Startup and Recovery</span></span>](com--crm-startup-and-recovery.md)
-   [<span data-ttu-id="42d05-137">在叢集環境中使用 COM + CRM</span><span class="sxs-lookup"><span data-stu-id="42d05-137">Using the COM+ CRM in a Cluster Environment</span></span>](using-the-com--crm-in-a-cluster-environment.md)
-   [<span data-ttu-id="42d05-138">COM + CRM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="42d05-138">Error Handling in the COM+ CRM</span></span>](error-handling-in-the-com--crm.md)
-   [<span data-ttu-id="42d05-139">COM + CRM 登錄設定</span><span class="sxs-lookup"><span data-stu-id="42d05-139">COM+ CRM Registry Settings</span></span>](com--crm-registry-settings.md)
-   [<span data-ttu-id="42d05-140">COM + CRM 疑難排解</span><span class="sxs-lookup"><span data-stu-id="42d05-140">Troubleshooting the COM+ CRM</span></span>](troubleshooting-the-com--crm.md)
-   [<span data-ttu-id="42d05-141">開發 COM + CRM 的設計建議</span><span class="sxs-lookup"><span data-stu-id="42d05-141">Design Suggestions for Developing a COM+ CRM</span></span>](design-suggestions-for-developing-a-com--crm.md)
-   [<span data-ttu-id="42d05-142">COM + CRM 監視介面</span><span class="sxs-lookup"><span data-stu-id="42d05-142">COM+ CRM Monitoring Interfaces</span></span>](com--crm-monitoring-interfaces.md)
-   [<span data-ttu-id="42d05-143">COM + CRM 介面</span><span class="sxs-lookup"><span data-stu-id="42d05-143">COM+ CRM Interfaces</span></span>](com--crm-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="42d05-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="42d05-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42d05-145">COM + 補償 Resource Manager 工作</span><span class="sxs-lookup"><span data-stu-id="42d05-145">COM+ Compensating Resource Manager Tasks</span></span>](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



