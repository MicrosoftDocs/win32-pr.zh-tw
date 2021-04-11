---
description: 來源安全轉換的來源必須位於套件來源的根目錄。」
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: 安全來源轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852927"
---
# <a name="secure-at-source-transforms"></a><span data-ttu-id="513d7-103">安全來源轉換</span><span class="sxs-lookup"><span data-stu-id="513d7-103">Secure-At-Source Transforms</span></span>

<span data-ttu-id="513d7-104">來源安全轉換的來源必須位於套件來源的根目錄。」</span><span class="sxs-lookup"><span data-stu-id="513d7-104">Secure-at-source transforms must have a source located at the root of the source for the package.</span></span> <span data-ttu-id="513d7-105">安裝或公告封裝之後，安裝程式會將轉換儲存在快取中，而在安全的檔案系統上，使用者沒有寫入權限。</span><span class="sxs-lookup"><span data-stu-id="513d7-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="513d7-106">如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。</span><span class="sxs-lookup"><span data-stu-id="513d7-106">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="513d7-107">方法與搜尋 .msi 檔案的來源清單相同。</span><span class="sxs-lookup"><span data-stu-id="513d7-107">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="513d7-108">如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="513d7-108">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="513d7-109">由任何使用者移除產品時，會從使用者的電腦移除該產品的所有安全轉換。</span><span class="sxs-lookup"><span data-stu-id="513d7-109">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="513d7-110">若要在安裝封裝時套用安全來源轉換，請設定 [TransformsSecure 原則](transformssecure-policy.md) 或 [**TransformsSecure**](transformssecure.md) 屬性，或將 @ 轉換清單中傳遞的第一個字元。</span><span class="sxs-lookup"><span data-stu-id="513d7-110">To apply secure-at-source transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property, or make @ the first character passed in the transform list.</span></span> <span data-ttu-id="513d7-111">每個轉換都必須以檔案名表示，而且必須位於封裝來源的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="513d7-111">Each transform must be indicated by a file name and must be located at the root of the source for the package.</span></span> <span data-ttu-id="513d7-112">如果有任何轉換不在套件來源的根目錄中，安裝就會失敗。</span><span class="sxs-lookup"><span data-stu-id="513d7-112">If any of the transforms are not located at the root of the package source, the installation fails.</span></span> <span data-ttu-id="513d7-113">如需詳細資訊，請參閱套用 [轉換](applying-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="513d7-113">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



