---
description: 全域分割區
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: 全域分割區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468517"
---
# <a name="the-global-partition"></a><span data-ttu-id="fc83d-103">全域分割區</span><span class="sxs-lookup"><span data-stu-id="fc83d-103">The Global Partition</span></span>

<span data-ttu-id="fc83d-104">除了系統管理員定義的磁碟分割和資料分割集之外，每台電腦上都有一個特殊的資料分割，稱為「 *全域分割* 區」。</span><span class="sxs-lookup"><span data-stu-id="fc83d-104">In addition to administrator-defined partitions and partition sets, there is a special partition on each computer called a *global partition*.</span></span> <span data-ttu-id="fc83d-105">安裝 COM + 時，會自動建立全域資料分割。</span><span class="sxs-lookup"><span data-stu-id="fc83d-105">A global partition is automatically created when COM+ is installed.</span></span> <span data-ttu-id="fc83d-106">全域分割區的設計目的是要包含伺服器或網域中的所有使用者都必須能夠存取的全系統應用程式。</span><span class="sxs-lookup"><span data-stu-id="fc83d-106">The global partition is designed to contain system-wide applications that need to be accessible to all users on a server or in the domain.</span></span> <span data-ttu-id="fc83d-107">將應用程式安裝到全域分割區，不需要將應用程式的複本安裝到每個個別使用者的磁碟分割集。</span><span class="sxs-lookup"><span data-stu-id="fc83d-107">Installing an application into the global partition removes the need to install a copy of the application into each individual user's partition set.</span></span>

<span data-ttu-id="fc83d-108">如果使用者的資料分割集未包含使用者嘗試存取的特定應用程式，但該應用程式安裝在全域分割區中，則會從全域分割區啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="fc83d-108">If a user's partition set does not include a specific application that the user is attempting to access, but that application is installed in the global partition, the application is activated from the global partition.</span></span> <span data-ttu-id="fc83d-109">不過，在此情況下，全域磁碟分割中安裝之應用程式的所有元件都必須標示為公用，而非私用元件。</span><span class="sxs-lookup"><span data-stu-id="fc83d-109">In this case, however, all components of the application installed in the global partition must be marked as public, not private, components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc83d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc83d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc83d-111">預設分割區</span><span class="sxs-lookup"><span data-stu-id="fc83d-111">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="fc83d-112">本機分割區</span><span class="sxs-lookup"><span data-stu-id="fc83d-112">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="fc83d-113">分割區屬性</span><span class="sxs-lookup"><span data-stu-id="fc83d-113">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="fc83d-114">磁碟分割和 Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc83d-114">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> </dl>

 

 



