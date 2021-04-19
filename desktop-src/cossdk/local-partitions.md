---
description: 本機分割區
ms.assetid: 629c4915-00b8-46da-b52a-2d274056eb6c
title: 本機分割區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f1a8524b0ebada203d6b42ac7b6cae000f5a51
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973159"
---
# <a name="local-partitions"></a><span data-ttu-id="23591-103">本機分割區</span><span class="sxs-lookup"><span data-stu-id="23591-103">Local Partitions</span></span>

<span data-ttu-id="23591-104">分割區可以使用的其中一種方式是在本機應用程式伺服器上。</span><span class="sxs-lookup"><span data-stu-id="23591-104">One way that partitions can be used is locally on an application server.</span></span> <span data-ttu-id="23591-105">在此案例中，系統管理員可以使用 [元件服務] 系統管理工具來建立磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="23591-105">In this scenario, an administrator can create a partition using the Component Services administrative tool.</span></span> <span data-ttu-id="23591-106">本機使用者只能存取在本機執行的資料分割，而不是在 Active Directory 內的資料分割，而不是網域中其他電腦上的使用者。</span><span class="sxs-lookup"><span data-stu-id="23591-106">Partitions implemented locally and not within Active Directory are accessible to local users only, not to users on other computers in the domain.</span></span> <span data-ttu-id="23591-107">建立分割區並在其中安裝 COM + 應用程式之後，系統管理員可以將該磁碟分割指派為該伺服器上一或多個使用者的預設資料分割。</span><span class="sxs-lookup"><span data-stu-id="23591-107">After a partition is created and a COM+ application is installed into it, the administrator can assign that partition as a default partition for one or more users on that server.</span></span> <span data-ttu-id="23591-108">若要將預設分割區指派給使用者，系統管理員可以使用 [元件服務] 系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="23591-108">To assign a default partition to a user, the administrator can use the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23591-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="23591-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23591-110">預設分割區</span><span class="sxs-lookup"><span data-stu-id="23591-110">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="23591-111">分割區屬性</span><span class="sxs-lookup"><span data-stu-id="23591-111">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="23591-112">磁碟分割和 Active Directory</span><span class="sxs-lookup"><span data-stu-id="23591-112">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="23591-113">全域分割區</span><span class="sxs-lookup"><span data-stu-id="23591-113">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



