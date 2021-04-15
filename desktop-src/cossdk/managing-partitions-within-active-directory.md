---
description: 除了透過 Active Directory 消費者和電腦系統管理工具來管理 Active Directory 分割區之外，您還可以透過在 Active Directory 系統介面 (ADSI) 中使用一組 COM + 物件，以程式設計方式管理 COM + 分割。
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: 管理 Active Directory 內的磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510705"
---
# <a name="managing-partitions-within-active-directory"></a><span data-ttu-id="e0ad0-103">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="e0ad0-103">Managing Partitions Within Active Directory</span></span>

<span data-ttu-id="e0ad0-104">除了透過 Active Directory 消費者和電腦系統管理工具來管理 Active Directory 分割區之外，您還可以透過在 Active Directory 系統介面 (ADSI) 中使用一組 COM + 物件，以程式設計方式管理 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-104">As an alternative to managing Active Directory partitions through the Active Directory Users and Computers administrative tool, you can manage COM+ partitions programmatically through the use of a set of COM+ objects within Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="e0ad0-105">無論您選擇用來管理 COM + 分割的管理技術為何，系統管理員都必須遵循一般的步驟順序：</span><span class="sxs-lookup"><span data-stu-id="e0ad0-105">Regardless of the administrative technique you choose for managing COM+ partitions, there is a general sequence of steps that administrators must follow:</span></span>

1.  <span data-ttu-id="e0ad0-106">在您的網域 Active Directory 內建立新的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-106">Create the new COM+ partitions within Active Directory for your domain.</span></span>
2.  <span data-ttu-id="e0ad0-107">在 Active Directory 中建立 COM + 分割集，並將它們對應到新建立的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-107">Create COM+ partition sets within Active Directory, and map them to your newly created COM+ partitions.</span></span>
3.  <span data-ttu-id="e0ad0-108">使用適當的 COM + 物件，在本機電腦上設定 Active Directory 的資料分割。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-108">Configure your Active Directory partitions on your local machine, using the appropriate COM+ object.</span></span> <span data-ttu-id="e0ad0-109">當您在本機電腦上設定 Active Directory 分割區時，會自動在該分割區資料夾中建立 **Com + 應用程式** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-109">When you configure an Active Directory partition on a local machine, a **COM+ Applications** folder is automatically created in that partition folder.</span></span>
4.  <span data-ttu-id="e0ad0-110">將您的 COM + 應用程式安裝在適當的 COM + 分割中。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-110">Install your COM+ applications in the appropriate COM+ partitions.</span></span>

<span data-ttu-id="e0ad0-111">您可以使用一組稱為 ADSI 的 Active Directory 介面，以程式設計的方式完成上述所有步驟。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-111">All of the preceding steps can be done programmatically, using a set of Active Directory interfaces called ADSI.</span></span> <span data-ttu-id="e0ad0-112">可用來管理 ADSI 中可用之分割區的物件如下所示：</span><span class="sxs-lookup"><span data-stu-id="e0ad0-112">The objects available for managing partitions that are available within ADSI are as follows:</span></span>

-   <span data-ttu-id="e0ad0-113">DS \_ USERPARTITIONSETLINK \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e0ad0-113">DS\_USERPARTITIONSETLINK\_NAME</span></span>
-   <span data-ttu-id="e0ad0-114">DS \_ PARTITIONLINK \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e0ad0-114">DS\_PARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="e0ad0-115">DS \_ OBJECTID \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e0ad0-115">DS\_OBJECTID\_NAME</span></span>
-   <span data-ttu-id="e0ad0-116">DS \_ DEFAULTPARTITIONLINK \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e0ad0-116">DS\_DEFAULTPARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="e0ad0-117">DS \_ USERLINK \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e0ad0-117">DS\_USERLINK\_NAME</span></span>
-   <span data-ttu-id="e0ad0-118">DS \_ PARTITIONSET \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e0ad0-118">DS\_PARTITIONSET\_NAME</span></span>
-   <span data-ttu-id="e0ad0-119">DS \_ 磁碟分割 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e0ad0-119">DS\_PARTITION\_NAME</span></span>

<span data-ttu-id="e0ad0-120">如需使用 Active Directory 消費者和電腦和元件服務系統管理工具來建立和管理 COM + 分割的相關資訊，請參閱每個工具中的可用線上說明。</span><span class="sxs-lookup"><span data-stu-id="e0ad0-120">For information on creating and managing COM+ partitions through the use of the Active Directory Users and Computers and Component Services administrative tools, see the online help available from within each tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0ad0-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0ad0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ad0-122">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="e0ad0-122">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="e0ad0-123">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="e0ad0-123">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="e0ad0-124">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="e0ad0-124">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="e0ad0-125">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="e0ad0-125">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="e0ad0-126">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="e0ad0-126">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



