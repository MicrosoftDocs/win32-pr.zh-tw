---
description: 當封裝包含隔離的元件時，Windows Installer 在移除應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: 移除隔離的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000298"
---
# <a name="removal-of-isolated-components"></a><span data-ttu-id="ff71a-104">移除隔離的元件</span><span class="sxs-lookup"><span data-stu-id="ff71a-104">Removal of Isolated Components</span></span>

<span data-ttu-id="ff71a-105">當封裝包含隔離的元件時，Windows Installer 在移除應用程式期間執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="ff71a-105">Windows Installer performs the following actions during the removal of an application when the package contains isolated components.</span></span> <span data-ttu-id="ff71a-106">通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。</span><span class="sxs-lookup"><span data-stu-id="ff71a-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="uninstall"></a><span data-ttu-id="ff71a-107">解除安裝</span><span class="sxs-lookup"><span data-stu-id="ff71a-107">Uninstall</span></span>

-   <span data-ttu-id="ff71a-108">\_ \_ 只有在同時移除元件應用程式時，才移除包含元件應用程式之資料夾中共用的元件檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff71a-108">Remove the files of Component\_Shared from the folder containing Component\_Application only if Component\_Application is also being removed.</span></span>
-   <span data-ttu-id="ff71a-109">如果 msidbComponentAttributesSharedDllRefCount 位設定在 [元件資料表](component-table.md) 中，則會遞減 SharedDLL refcount。</span><span class="sxs-lookup"><span data-stu-id="ff71a-109">If the msidbComponentAttributesSharedDllRefCount bit is set in the [Component table](component-table.md) decrement the SharedDLL refcount.</span></span>
-   <span data-ttu-id="ff71a-110">移除。包含元件應用程式之資料夾中的本機零位元組檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff71a-110">Remove the .LOCAL zero-byte file from the folder containing Component\_Application.</span></span>
-   <span data-ttu-id="ff71a-111">\_從共用的元件用戶端清單中移除元件應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff71a-111">Remove Component\_Application from the client list of Component\_Shared.</span></span>
-   <span data-ttu-id="ff71a-112">照常移除元件應用程式的所有資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff71a-112">Remove all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="ff71a-113">如果已共用元件的用戶端清單中剩餘其他產品 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ff71a-113">If there are other products remaining on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="ff71a-114">從共用的元件共用位置移除沒有任何檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff71a-114">Remove no files from the shared location of Component\_Shared.</span></span>

<span data-ttu-id="ff71a-115">如果共用元件的 SharedDLL refcount 在 \_ 遞減之後為0，或者，如果沒有其他剩餘的元件共用用戶端 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ff71a-115">If the SharedDLL refcount for Component\_Shared is 0 after being decremented, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="ff71a-116">移除共用位置共用的元件檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff71a-116">Remove the files of Component\_Shared from the shared location.</span></span>
-   <span data-ttu-id="ff71a-117">處理與此元件相關的所有卸載動作。</span><span class="sxs-lookup"><span data-stu-id="ff71a-117">Process all uninstall actions with respect to this component.</span></span>

 

 



