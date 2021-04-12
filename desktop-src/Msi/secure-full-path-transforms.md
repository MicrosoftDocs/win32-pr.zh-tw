---
description: 安全-完整路徑轉換的來源必須位於 [轉換] 屬性中指定的完整路徑。
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: 安全-完整路徑轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514196"
---
# <a name="secure-full-path-transforms"></a><span data-ttu-id="e9928-103">安全-完整路徑轉換</span><span class="sxs-lookup"><span data-stu-id="e9928-103">Secure-Full-Path Transforms</span></span>

<span data-ttu-id="e9928-104">安全-完整路徑轉換的來源必須位於 [ [**轉換**](transforms.md) ] 屬性中指定的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e9928-104">Secure-full-path transforms must have a source located at the full path specified in the [**TRANSFORMS**](transforms.md) property.</span></span> <span data-ttu-id="e9928-105">安裝或公告封裝之後，安裝程式會將轉換儲存在快取中，而在安全的檔案系統上，使用者沒有寫入權限。</span><span class="sxs-lookup"><span data-stu-id="e9928-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="e9928-106">如果轉換的本機複本變得無法使用，它可能只會使用指定的路徑來還原快取。</span><span class="sxs-lookup"><span data-stu-id="e9928-106">If the local copy of the transform becomes unavailable, it may only restore the cache using the specified path.</span></span> <span data-ttu-id="e9928-107">由任何使用者移除產品時，會從使用者的電腦移除該產品的所有安全轉換。</span><span class="sxs-lookup"><span data-stu-id="e9928-107">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="e9928-108">若要在安裝封裝時套用安全的完整路徑轉換，請設定 [TransformsSecure 原則](transformssecure-policy.md) 或 [**TransformsSecure**](transformssecure.md) 屬性，或將 \| 第一個字元傳遞至轉換清單。</span><span class="sxs-lookup"><span data-stu-id="e9928-108">To apply secure-full-paths transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property or make \| the first character passed in the transform list.</span></span> <span data-ttu-id="e9928-109">每個轉換來源的完整路徑必須在轉換字串中傳遞。</span><span class="sxs-lookup"><span data-stu-id="e9928-109">The full paths to the source of each transform must be passed in the transforms string.</span></span> <span data-ttu-id="e9928-110">如果清單中有任何相對路徑，安裝就會失敗。</span><span class="sxs-lookup"><span data-stu-id="e9928-110">If any relative paths are in the list, the installation fails.</span></span> <span data-ttu-id="e9928-111">轉換來源不需要與封裝的來源位於一起。</span><span class="sxs-lookup"><span data-stu-id="e9928-111">The transform source does not have to be located with the source of the package.</span></span>

 

 



