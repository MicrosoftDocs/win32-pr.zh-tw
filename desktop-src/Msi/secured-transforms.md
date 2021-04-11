---
description: 基於安全性考慮，有時需要安全的轉換。
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: 安全的轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852924"
---
# <a name="secured-transforms"></a><span data-ttu-id="f4a43-103">安全的轉換</span><span class="sxs-lookup"><span data-stu-id="f4a43-103">Secured Transforms</span></span>

<span data-ttu-id="f4a43-104">基於安全性考慮，有時需要安全的轉換。</span><span class="sxs-lookup"><span data-stu-id="f4a43-104">Secured transforms are sometimes necessary for security reasons.</span></span> <span data-ttu-id="f4a43-105">安全的轉換會儲存在使用者電腦本機的位置，在安全的檔案系統上，使用者沒有寫入權限。</span><span class="sxs-lookup"><span data-stu-id="f4a43-105">Secured transforms are stored locally on the user's computer in a location where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="f4a43-106">在安裝或公告封裝期間，此位置會快取這類轉換。</span><span class="sxs-lookup"><span data-stu-id="f4a43-106">Such transforms are cached in this location during the installation or advertisement of the package.</span></span> <span data-ttu-id="f4a43-107">只有系統管理員和本機系統具有這個位置的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="f4a43-107">Only administrators and local system have write access to this location.</span></span> <span data-ttu-id="f4a43-108">非管理使用者無法修改轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="f4a43-108">A non-admin user would not be able to modify the transform file.</span></span> <span data-ttu-id="f4a43-109">在後續 [安裝隨選安裝](installation-on-demand.md) 或封裝的 [維護安裝](maintenance-installation.md) 期間，安裝程式會使用快取的轉換。</span><span class="sxs-lookup"><span data-stu-id="f4a43-109">During subsequent [installation-on-demand](installation-on-demand.md) or [maintenance installations](maintenance-installation.md) of the package, the installer uses the cached transforms.</span></span>

<span data-ttu-id="f4a43-110">若要指定安全的轉換儲存區，請設定 [TransformsSecure 原則](transformssecure-policy.md)、設定 [**TransformsSecure**](transformssecure.md) 屬性，或 \| 在轉換清單中傳遞 @ 或符號。</span><span class="sxs-lookup"><span data-stu-id="f4a43-110">To specify secured transform storage, set the [TransformsSecure policy](transformssecure-policy.md), set the [**TRANSFORMSSECURE**](transformssecure.md) property, or pass the @ or \| symbol in the transforms list.</span></span> <span data-ttu-id="f4a43-111">請注意，您不能在相同的轉換清單中包含安全且不安全的轉換。</span><span class="sxs-lookup"><span data-stu-id="f4a43-111">Note that you cannot include secured and unsecured transforms in the same transforms list.</span></span> <span data-ttu-id="f4a43-112">請參閱套用 [轉換](applying-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="f4a43-112">See [Applying Transforms](applying-transforms.md).</span></span>

<span data-ttu-id="f4a43-113">任何使用者移除產品時，都會從使用者的電腦移除該產品的所有安全轉換。</span><span class="sxs-lookup"><span data-stu-id="f4a43-113">The removal of the product by any user removes all secured transforms for that product from the user's computer.</span></span>

<span data-ttu-id="f4a43-114">如果安裝程式發現安全的轉換無法在本機使用，則會嘗試從來源還原轉換快取。</span><span class="sxs-lookup"><span data-stu-id="f4a43-114">If the installer finds that a secured transform is not locally available, it then attempts to restore the transform cache from a source.</span></span> <span data-ttu-id="f4a43-115">安全轉換可以是安全的來源或安全的-完整路徑：</span><span class="sxs-lookup"><span data-stu-id="f4a43-115">Secure transforms can be secure-at-source or secure-full-path:</span></span>

-   <span data-ttu-id="f4a43-116">本機轉換快取中遺失的[安全來源轉換](secure-at-source-transforms.md)會從 .msi 檔案來源的根目錄還原。</span><span class="sxs-lookup"><span data-stu-id="f4a43-116">[Secure-at-source transforms](secure-at-source-transforms.md) that are missing from the local transform cache are restored from the root of the source of the .msi file.</span></span>
-   <span data-ttu-id="f4a43-117">本機轉換快取中遺失的[安全-完整路徑轉換](secure-full-path-transforms.md)會從轉換清單所指定的原始完整路徑還原。</span><span class="sxs-lookup"><span data-stu-id="f4a43-117">[Secure-full-path transforms](secure-full-path-transforms.md) that are missing from the local transform cache are restored from the original full path specified by the transforms list.</span></span>

 

 



