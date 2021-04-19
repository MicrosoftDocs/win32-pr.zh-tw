---
description: COM + CRM 啟動和復原
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: COM + CRM 啟動和復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981128"
---
# <a name="com-crm-startup-and-recovery"></a><span data-ttu-id="da74c-103">COM + CRM 啟動和復原</span><span class="sxs-lookup"><span data-stu-id="da74c-103">COM+ CRM Startup and Recovery</span></span>

<span data-ttu-id="da74c-104">如果伺服器應用程式已使用 [元件服務] 系統管理工具 (選取 [ **啟用補償資源管理員** ] 核取方塊，則在 com + 應用程式的 [屬性] 頁面的 [ **Advanced** ] 索引標籤上) ，第一次啟動時，它會建立 CRM 記錄檔，供該伺服器應用程式進程中的所有 crm 使用。</span><span class="sxs-lookup"><span data-stu-id="da74c-104">If a server application has the **Enable compensating resource managers** checkbox selected (using the Component Services administrative tool, on the **Advanced** tab of the COM+ application's property page), the first time it starts up it creates a CRM log file to be used by all CRMs in that server application process.</span></span> <span data-ttu-id="da74c-105"> (如需設定 CRM 的詳細指示，請參閱設定 [COM + CRM 元件](configuring-com--crm-components.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="da74c-105">(For detailed instructions about configuring the CRM, see [Configuring COM+ CRM Components](configuring-com--crm-components.md).)</span></span>

<span data-ttu-id="da74c-106">針對伺服器應用程式所建立的 CRM 記錄檔名稱是以伺服器應用程式的 GUID)  (為基礎，而且 CRM 記錄檔會放在與 DTC 記錄檔相同的目錄中， (通常是% SystemRoot% \\ winnt \\ system32 \\ DtcLog 目錄) 。</span><span class="sxs-lookup"><span data-stu-id="da74c-106">The name of the CRM log file created for the server application is based on the AppId (a GUID) of the server application, and the CRM log file is placed in the same directory as the DTC log file (normally your %SystemRoot%\\winnt\\system32\\DtcLog directory).</span></span> <span data-ttu-id="da74c-107">CRM 記錄檔的副檔名為 crmlog。</span><span class="sxs-lookup"><span data-stu-id="da74c-107">CRM log files have the extension .crmlog.</span></span>

> [!Note]  
> <span data-ttu-id="da74c-108">基於效能考慮，可能需要變更 CRM 記錄檔的預設位置， (使 DTC 記錄檔位於與 CRM 記錄檔不同的磁片上) 或可能是因為在叢集環境中使用 CRM。</span><span class="sxs-lookup"><span data-stu-id="da74c-108">It may be necessary to change the default location of a CRM log file due to performance reasons (to have the DTC log file on a different disk than the CRM log file) or perhaps due to use of the CRM in a cluster environment.</span></span> <span data-ttu-id="da74c-109">您可以使用 COM + 系統管理 SDK 變更 CRM 記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="da74c-109">The location of the CRM log files can be changed using the COM+ administration SDK.</span></span> <span data-ttu-id="da74c-110">屬性名稱是 CRMLogFile，而且存在於 [**應用程式**](applications.md) 集合物件上。</span><span class="sxs-lookup"><span data-stu-id="da74c-110">The property name is CRMLogFile, and it exists on the [**Applications**](applications.md) collection object.</span></span>

 

<span data-ttu-id="da74c-111">當啟用 CRM 的伺服器應用程式 () 啟動，併發現該伺服器應用程式已經有 CRM 記錄檔，它會在該 CRM 記錄檔上執行復原。</span><span class="sxs-lookup"><span data-stu-id="da74c-111">When a server application (that is CRM-enabled) starts up and finds that a CRM log file already exists for that server application, it performs recovery on that CRM log file.</span></span> <span data-ttu-id="da74c-112">復原 *是完成* 失敗的任何交易的程式，其中牽涉到 crm 基礎結構讀取 crm 記錄檔，以找出任何未完全完成的交易。</span><span class="sxs-lookup"><span data-stu-id="da74c-112">*Recovery* is the process of completing any transactions that were interrupted by a failure and involves the CRM infrastructure reading the CRM log file for any transactions that were not fully completed.</span></span> <span data-ttu-id="da74c-113">如果找到任何，則會聯繫 DTC 以判斷交易結果。</span><span class="sxs-lookup"><span data-stu-id="da74c-113">If it finds any, it contacts the DTC to determine the transaction outcome.</span></span> <span data-ttu-id="da74c-114">然後，它會建立 CRM 補償器，並視需要將認可或中止通知連同相關聯的記錄檔記錄一起傳遞。</span><span class="sxs-lookup"><span data-stu-id="da74c-114">It then creates the CRM Compensator and passes on the commit or abort notifications as required, together with the associated log records.</span></span>

<span data-ttu-id="da74c-115">在復原期間，CRM 補償器不會收到準備通知。</span><span class="sxs-lookup"><span data-stu-id="da74c-115">Prepare notifications are not received by the CRM Compensator during recovery.</span></span> <span data-ttu-id="da74c-116">CRM 補償器具有旗標，可區別是否在正常作業期間或復原期間呼叫它。</span><span class="sxs-lookup"><span data-stu-id="da74c-116">The CRM Compensator has a flag to distinguish whether it is being called during normal operation or during recovery.</span></span>

<span data-ttu-id="da74c-117">復原通常只會在伺服器應用程式因伺服器應用程式進程損毀或電腦損毀而異常關閉時，才會尋找未完成的交易。</span><span class="sxs-lookup"><span data-stu-id="da74c-117">Recovery will normally find uncompleted transactions only if the server application has been shutdown abnormally, due to either a server application process crash or a computer crash.</span></span> <span data-ttu-id="da74c-118">如果允許伺服器應用程式正常關機，因為閒置超時或透過 [元件服務] 系統管理工具手動關機，則記錄檔將會是乾淨的。</span><span class="sxs-lookup"><span data-stu-id="da74c-118">If the server application is allowed to shut down normally, due either to the idle time-out or to manual shutdown via the Component Services administrative tool, the log file will be clean.</span></span>

<span data-ttu-id="da74c-119">開始進行復原的 CRM 伺服器應用程式不會自動啟動。</span><span class="sxs-lookup"><span data-stu-id="da74c-119">Starting of a CRM server application for recovery is not automatically initiated.</span></span> <span data-ttu-id="da74c-120">必須採取一些外部動作，才能啟動需要復原的 CRM 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="da74c-120">Some external action must be taken to start the CRM server application where recovery is required.</span></span> <span data-ttu-id="da74c-121">通常這會在該伺服器應用程式中建立元件。</span><span class="sxs-lookup"><span data-stu-id="da74c-121">Typically this would be creating a component in that server application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da74c-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="da74c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da74c-123">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="da74c-123">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[<span data-ttu-id="da74c-124">COM + CRM 操作進程</span><span class="sxs-lookup"><span data-stu-id="da74c-124">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
</dt> </dl>

 

 



