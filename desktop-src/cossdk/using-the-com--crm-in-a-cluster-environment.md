---
description: 在叢集環境中使用 COM + CRM
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: 在叢集環境中使用 COM + CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317872"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a><span data-ttu-id="0f841-103">在叢集環境中使用 COM + CRM</span><span class="sxs-lookup"><span data-stu-id="0f841-103">Using the COM+ CRM in a Cluster Environment</span></span>

<span data-ttu-id="0f841-104">在開發要在叢集環境中運作的 COM + Crm 時，要考慮的主要因素是，特定 CRM 是否在意其正在操作的叢集節點。</span><span class="sxs-lookup"><span data-stu-id="0f841-104">When developing COM+ CRMs to work in cluster environments, the main factor to consider is whether a specific CRM cares which node of the cluster it is operating on.</span></span> <span data-ttu-id="0f841-105">例如，如果 CRM 所管理的資源是電腦檔案系統或登錄，則所有變更都是 CRM 伺服器應用程式在當時執行的節點所特有。</span><span class="sxs-lookup"><span data-stu-id="0f841-105">For example, if the resource managed by the CRM is the machine file system or registry, any changes are specific to the node that the CRM server application is running on at the time.</span></span> <span data-ttu-id="0f841-106">在此情況下，不需要將 CRM 伺服器應用程式容錯移轉至另一個節點。</span><span class="sxs-lookup"><span data-stu-id="0f841-106">In this case, failover of the CRM server application to another node would not be desirable.</span></span> <span data-ttu-id="0f841-107">在不同的情況下，CRM 會管理叢集的一些資源，而將 CRM 伺服器應用程式容錯移轉至另一個節點會很有用。</span><span class="sxs-lookup"><span data-stu-id="0f841-107">In a different case, where the CRM is managing some resource common to the cluster, failover of the CRM server application to another node is useful.</span></span>

<span data-ttu-id="0f841-108">CRM 記錄檔的預設目錄位置與 DTC 記錄檔的目錄相同。</span><span class="sxs-lookup"><span data-stu-id="0f841-108">The default directory location for CRM log files is the same directory as the DTC log file.</span></span> <span data-ttu-id="0f841-109">在叢集上，DTC 記錄檔會放在叢集節點之間容錯移轉的共用磁片上。</span><span class="sxs-lookup"><span data-stu-id="0f841-109">On clusters, the DTC log file is placed on a shared disk that is failed over between the nodes of the cluster.</span></span> <span data-ttu-id="0f841-110">這表示 CRM 伺服器應用程式的預設行為是在叢集的節點之間進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="0f841-110">This means that the default behavior for CRM server applications is to failover between nodes of the cluster.</span></span> <span data-ttu-id="0f841-111">因此，如果特定 CRM 需要不同的行為，而不是在節點之間進行容錯移轉，則應該變更該特定 CRM 伺服器應用程式之 CRM 記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="0f841-111">Therefore, if a specific CRM requires the alternative behavior of not failing over between nodes, the location of the CRM log file for that particular CRM server application should be changed.</span></span>

<span data-ttu-id="0f841-112">此外，如果 CRM 應用程式需要容錯移轉，則應該將它設定為叢集群組中的一般應用程式。</span><span class="sxs-lookup"><span data-stu-id="0f841-112">In addition, if failover is required for the CRM application, it should be configured as a generic application in a cluster group.</span></span> <span data-ttu-id="0f841-113">其相依性應該是 DTC。</span><span class="sxs-lookup"><span data-stu-id="0f841-113">Its dependency should be DTC.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f841-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f841-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f841-115">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="0f841-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



