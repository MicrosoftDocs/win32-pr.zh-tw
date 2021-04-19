---
description: AllocateRegistrySpace 動作可確保登錄中的 AVAILABLEFREEREG 屬性所指定的可用登錄空間量是否存在。
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: AllocateRegistrySpace 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986890"
---
# <a name="allocateregistryspace-action"></a><span data-ttu-id="14258-103">AllocateRegistrySpace 動作</span><span class="sxs-lookup"><span data-stu-id="14258-103">AllocateRegistrySpace Action</span></span>

<span data-ttu-id="14258-104">AllocateRegistrySpace 動作可確保登錄中的 [**AVAILABLEFREEREG**](availablefreereg.md) 屬性所指定的可用登錄空間量是否存在。</span><span class="sxs-lookup"><span data-stu-id="14258-104">The AllocateRegistrySpace action ensures that the amount of free registry space specified by the [**AVAILABLEFREEREG**](availablefreereg.md) property exists in the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="14258-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="14258-105">Sequence Restrictions</span></span>

<span data-ttu-id="14258-106">您必須在 [InstallInitialize](installinitialize-action.md)之後呼叫 AllocateRegistrySpace 動作。</span><span class="sxs-lookup"><span data-stu-id="14258-106">The AllocateRegistrySpace action must be called after [InstallInitialize](installinitialize-action.md).</span></span> <span data-ttu-id="14258-107">建議您在所有其他動作之前排程 AllocateRegistrySpace，以確保有足夠的登錄空間可繼續。</span><span class="sxs-lookup"><span data-stu-id="14258-107">It is advisable to schedule the AllocateRegistrySpace before all other actions to ensure there is enough registry space available to continue.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="14258-108">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="14258-108">ActionData Messages</span></span>



| <span data-ttu-id="14258-109">欄位</span><span class="sxs-lookup"><span data-stu-id="14258-109">Field</span></span> | <span data-ttu-id="14258-110">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="14258-110">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="14258-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="14258-111">\[1\]</span></span> | <span data-ttu-id="14258-112">需要登錄空間，以 KB 為單位。</span><span class="sxs-lookup"><span data-stu-id="14258-112">Registry space required in KB.</span></span> |



 

 

 



