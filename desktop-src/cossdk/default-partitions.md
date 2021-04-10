---
description: 預設分割區
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: 預設分割區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191030"
---
# <a name="default-partitions"></a><span data-ttu-id="e6b30-103">預設分割區</span><span class="sxs-lookup"><span data-stu-id="e6b30-103">Default Partitions</span></span>

<span data-ttu-id="e6b30-104">當預設分割區指派給使用者時，COM + 會先嘗試啟動該分割區中的元件。</span><span class="sxs-lookup"><span data-stu-id="e6b30-104">When a default partition is assigned to a user, COM+ attempts to activate components in that partition first.</span></span> <span data-ttu-id="e6b30-105">如果啟用失敗，COM + 會在全域分割區搜尋要啟用的元件。</span><span class="sxs-lookup"><span data-stu-id="e6b30-105">If the activation fails, COM+ searches the global partition for the component to activate.</span></span> <span data-ttu-id="e6b30-106">當 COM + 元件包含分割區標記時（明確指定元件所在的分割區），就會發生此進程的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e6b30-106">The exception to this process occurs when the COM+ component includes a partition moniker, which explicitly specifies the partition in which the component is located.</span></span> <span data-ttu-id="e6b30-107">在此情況下，資料分割的名字優先于任何預設分割區設定。</span><span class="sxs-lookup"><span data-stu-id="e6b30-107">In this case, the partition moniker takes precedence over any default partition configuration.</span></span>

<span data-ttu-id="e6b30-108">使用本機資料分割時，會使用應用程式伺服器上 [元件服務] 系統管理工具中的 [ **Com + 磁碟分割使用者** ] 資料夾，將預設分割區指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="e6b30-108">When using local partitions, the default partition is assigned to users using the **COM+ Partition Users** folder in the Component Services administrative tool on the application server.</span></span> <span data-ttu-id="e6b30-109">使用 Active Directory 中的資料分割集時，使用者的預設分割區是由使用者的資料分割集所決定。</span><span class="sxs-lookup"><span data-stu-id="e6b30-109">When using partition sets in the Active Directory, the user's default partition is determined by the user's partition set.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6b30-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6b30-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b30-111">本機分割區</span><span class="sxs-lookup"><span data-stu-id="e6b30-111">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="e6b30-112">分割區屬性</span><span class="sxs-lookup"><span data-stu-id="e6b30-112">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="e6b30-113">磁碟分割和 Active Directory</span><span class="sxs-lookup"><span data-stu-id="e6b30-113">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="e6b30-114">全域分割區</span><span class="sxs-lookup"><span data-stu-id="e6b30-114">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



