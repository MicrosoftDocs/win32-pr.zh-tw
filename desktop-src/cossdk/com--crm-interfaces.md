---
description: 需要 CRM 介面，才能為使用 Visual Basic 和 Visual C++ 開發的 CRM 工作者和 CRM Compensators 提供支援。
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: COM + CRM 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689180"
---
# <a name="com-crm-interfaces"></a><span data-ttu-id="b327e-103">COM + CRM 介面</span><span class="sxs-lookup"><span data-stu-id="b327e-103">COM+ CRM Interfaces</span></span>

<span data-ttu-id="b327e-104">需要 CRM 介面，才能為使用 Visual Basic 和 Visual C++ 開發的 CRM 工作者和 CRM Compensators 提供支援。</span><span class="sxs-lookup"><span data-stu-id="b327e-104">The CRM interfaces are required to provide support for CRM Workers and CRM Compensators developed using Visual Basic and Visual C++.</span></span>

<span data-ttu-id="b327e-105">您可以使用 COM + 補償 Resource Manager (CRM) 快速輕鬆地整合應用程式資源與 Microsoft Distributed Transaction Coordinator (DTC) 交易。</span><span class="sxs-lookup"><span data-stu-id="b327e-105">You can use the COM+ Compensating Resource Manager (CRM) to quickly and easily integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span>

<span data-ttu-id="b327e-106">使用 Visual Basic 撰寫的元件更容易將記錄檔記錄建立為變數集合。</span><span class="sxs-lookup"><span data-stu-id="b327e-106">It is easier for components written with Visual Basic to build up a log record as a collection of Variants.</span></span> <span data-ttu-id="b327e-107">此外，Visual Basic 元件是以執行緒為單位，這表示必須能夠將多執行緒單元的介面封送處理至單一執行緒的單元。</span><span class="sxs-lookup"><span data-stu-id="b327e-107">Also, Visual Basic components are apartment threaded, which implies that it must be possible to marshal the interfaces from the multithreaded apartment to a single-threaded apartment.</span></span> <span data-ttu-id="b327e-108">使用 Visual C++ 開發的 CRM 元件也可以使用單元執行緒模型，不過建議您改為使用這兩個執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="b327e-108">CRM components developed with Visual C++ could also use the Apartment threading model, although it is recommended that these use the Both threading model instead.</span></span>

<span data-ttu-id="b327e-109">下表所述的介面提供 COM + Crm 開發人員的詳細參考資訊。</span><span class="sxs-lookup"><span data-stu-id="b327e-109">The interfaces described in the following table provide detailed reference information for developers of COM+ CRMs.</span></span>



| <span data-ttu-id="b327e-110">CRM 介面</span><span class="sxs-lookup"><span data-stu-id="b327e-110">CRM interfaces</span></span>                                             | <span data-ttu-id="b327e-111">Description</span><span class="sxs-lookup"><span data-stu-id="b327e-111">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b327e-112">**ICrmCompensator**</span><span class="sxs-lookup"><span data-stu-id="b327e-112">**ICrmCompensator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | <span data-ttu-id="b327e-113">此介面會在 Visual C++ 中傳遞非結構化記錄。</span><span class="sxs-lookup"><span data-stu-id="b327e-113">This interface delivers unstructured log records in Visual C++.</span></span>                                                           |
| [<span data-ttu-id="b327e-114">**ICrmCompensatorVariants**</span><span class="sxs-lookup"><span data-stu-id="b327e-114">**ICrmCompensatorVariants**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | <span data-ttu-id="b327e-115">使用 Visual Basic 時，這個介面會將結構化記錄檔記錄傳遞給 CRM 補償器。</span><span class="sxs-lookup"><span data-stu-id="b327e-115">This interface delivers structured log records to the CRM Compensator when using Visual Basic.</span></span>                            |
| [<span data-ttu-id="b327e-116">**ICrmFormatLogRecords**</span><span class="sxs-lookup"><span data-stu-id="b327e-116">**ICrmFormatLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | <span data-ttu-id="b327e-117">這個介面會將記錄檔記錄轉換成可看見的格式，讓它們可以使用一般監視工具來呈現。</span><span class="sxs-lookup"><span data-stu-id="b327e-117">This interface converts the log records to viewable format so that they can be presented using a generic monitoring tool.</span></span> |
| [<span data-ttu-id="b327e-118">**ICrmLogControl**</span><span class="sxs-lookup"><span data-stu-id="b327e-118">**ICrmLogControl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | <span data-ttu-id="b327e-119">CRM 工作者和 CRM 補償器會使用這個介面將記錄寫入記錄檔，並使其成為持久的。</span><span class="sxs-lookup"><span data-stu-id="b327e-119">This interface is used by the CRM Worker and CRM Compensator to write records to the log and make them durable.</span></span>           |
| [<span data-ttu-id="b327e-120">**ICrmMonitor**</span><span class="sxs-lookup"><span data-stu-id="b327e-120">**ICrmMonitor**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | <span data-ttu-id="b327e-121">此介面會捕獲 CRM 目前狀態的快照集，並保留特定的 CRM 職員。</span><span class="sxs-lookup"><span data-stu-id="b327e-121">This interface captures a snapshot of the current state of a CRM and holds a specific CRM clerk.</span></span>                          |
| [<span data-ttu-id="b327e-122">**ICrmMonitorClerks**</span><span class="sxs-lookup"><span data-stu-id="b327e-122">**ICrmMonitorClerks**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | <span data-ttu-id="b327e-123">此介面會取得 clerk 狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b327e-123">This interface obtains information about the state of clerks.</span></span>                                                             |
| [<span data-ttu-id="b327e-124">**ICrmMonitorLogRecords**</span><span class="sxs-lookup"><span data-stu-id="b327e-124">**ICrmMonitorLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | <span data-ttu-id="b327e-125">此介面會監視特定 CRM 職員針對指定交易所維護的個別記錄檔記錄。</span><span class="sxs-lookup"><span data-stu-id="b327e-125">This interface monitors the individual log records maintained by a specific CRM clerk for a given transaction.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="b327e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="b327e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b327e-127">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="b327e-127">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



