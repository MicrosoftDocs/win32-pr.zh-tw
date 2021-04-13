---
description: 交易式 NTFS (TxF) 將交易整合至 NTFS 檔案系統，讓應用程式開發人員和系統管理員可以更輕鬆地處理錯誤並保持資料完整性。
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: 關於交易式 NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318432"
---
# <a name="about-transactional-ntfs"></a><span data-ttu-id="52c5e-103">關於交易式 NTFS</span><span class="sxs-lookup"><span data-stu-id="52c5e-103">About Transactional NTFS</span></span>

<span data-ttu-id="52c5e-104">\[Microsoft 強烈建議開發人員利用替代方法來達成您的應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="52c5e-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="52c5e-105">針對 TxF 開發的許多案例，都可以透過更簡單且更容易使用的技術來達成。</span><span class="sxs-lookup"><span data-stu-id="52c5e-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="52c5e-106">此外，Microsoft Windows 的未來版本可能不提供 TxF。</span><span class="sxs-lookup"><span data-stu-id="52c5e-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="52c5e-107">如需詳細資訊以及 TxF 的替代方案，請參閱 [使用交易式 NTFS 的替代方案](deprecation-of-txf.md)。\]</span><span class="sxs-lookup"><span data-stu-id="52c5e-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

<span data-ttu-id="52c5e-108">交易式 NTFS (TxF) 將交易整合至 NTFS 檔案系統，讓應用程式開發人員和系統管理員可以更輕鬆地處理錯誤並保持資料完整性。</span><span class="sxs-lookup"><span data-stu-id="52c5e-108">Transactional NTFS (TxF) integrates transactions into the NTFS file system, which makes it easier for application developers and administrators to gracefully handle errors and preserve data integrity.</span></span>

<span data-ttu-id="52c5e-109">TxF 可以參與 [分散式交易協調器 (DTC) ](/previous-versions/windows/desktop/ms684146(v=vs.85)) 協調的分散式交易，這可讓您針對下列各項使用 TxF：</span><span class="sxs-lookup"><span data-stu-id="52c5e-109">TxF can participate in distributed transactions that the [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordinates, which allows you to use TxF for the following:</span></span>

-   <span data-ttu-id="52c5e-110">跨多個資料存放區的交易，例如，檔案和 SQL 作業的單一交易</span><span class="sxs-lookup"><span data-stu-id="52c5e-110">Transactions that span multiple data stores, for example, a single transaction for file and SQL operations</span></span>
-   <span data-ttu-id="52c5e-111">跨多部電腦的交易（例如，在多部電腦上進行檔案更新的單一交易）</span><span class="sxs-lookup"><span data-stu-id="52c5e-111">Transactions that span multiple computers, for example, a single transaction for file updates on multiple computers</span></span>

## <a name="in-this-section"></a><span data-ttu-id="52c5e-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="52c5e-112">In this section</span></span>



| <span data-ttu-id="52c5e-113">主題</span><span class="sxs-lookup"><span data-stu-id="52c5e-113">Topic</span></span>                                                                                                                 | <span data-ttu-id="52c5e-114">描述</span><span class="sxs-lookup"><span data-stu-id="52c5e-114">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52c5e-115">使用交易式 NTFS 的時機</span><span class="sxs-lookup"><span data-stu-id="52c5e-115">When to Use Transactional NTFS</span></span>](when-to-use-transactional-ntfs.md)<br/>                                       | <span data-ttu-id="52c5e-116">使用交易式 NTFS 來維護資料完整性。</span><span class="sxs-lookup"><span data-stu-id="52c5e-116">Use Transactional NTFS to maintain data integrity.</span></span><br/>                                                                        |
| [<span data-ttu-id="52c5e-117">部署交易式 NTFS</span><span class="sxs-lookup"><span data-stu-id="52c5e-117">Deploying Transactional NTFS</span></span>](deploying-transactional-ntfs.md)<br/>                                           | <span data-ttu-id="52c5e-118">在交易式 NTFS 中快取控制項。</span><span class="sxs-lookup"><span data-stu-id="52c5e-118">Caching control in Transactional NTFS.</span></span><br/>                                                                                    |
| [<span data-ttu-id="52c5e-119">如何使用交易式 NTFS</span><span class="sxs-lookup"><span data-stu-id="52c5e-119">How to Use Transactional NTFS</span></span>](how-to-use-transactional-ntfs.md)<br/>                                         | <span data-ttu-id="52c5e-120">管理交易式 NTFS 中的交易式檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="52c5e-120">Managing transacted file handles in Transactional NTFS.</span></span><br/>                                                                   |
| [<span data-ttu-id="52c5e-121">基本 TxF 概念</span><span class="sxs-lookup"><span data-stu-id="52c5e-121">Basic TxF Concepts</span></span>](txf-basic-concepts.md)<br/>                                                               | <span data-ttu-id="52c5e-122">描述交易式 NTFS 中的讀取認可一致性、讀取認可隔離和交易鎖定概念。</span><span class="sxs-lookup"><span data-stu-id="52c5e-122">Describes read-committed consistency, read-committed isolation, and transactional locking concepts in Transactional NTFS.</span></span><br/> |
| [<span data-ttu-id="52c5e-123">交易式 NTFS 的程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="52c5e-123">Programming Considerations for Transactional NTFS</span></span>](programming-considerations-for-transacted-fileio-.md)<br/> | <span data-ttu-id="52c5e-124">描述交易式 NTFS 的各種程式設計考慮。</span><span class="sxs-lookup"><span data-stu-id="52c5e-124">Describes various programming considerations for Transactional NTFS.</span></span><br/>                                                      |
| [<span data-ttu-id="52c5e-125">交易式 NTFS 的效能考慮</span><span class="sxs-lookup"><span data-stu-id="52c5e-125">Performance Considerations for Transactional NTFS</span></span>](performance-considerations-for-transactional-ntfs.md)<br/> | <span data-ttu-id="52c5e-126">最佳檔案系統交易的建議。</span><span class="sxs-lookup"><span data-stu-id="52c5e-126">Recommendations for optimal file system transactions.</span></span><br/>                                                                     |



 

 

