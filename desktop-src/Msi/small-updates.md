---
description: 小型更新會變更一或多個太小的應用程式檔，以保證變更產品代碼。
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: 小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112256"
---
# <a name="small-updates"></a><span data-ttu-id="3d5d8-103">小型更新</span><span class="sxs-lookup"><span data-stu-id="3d5d8-103">Small Updates</span></span>

<span data-ttu-id="3d5d8-104">小型更新會變更一或多個太小的應用程式檔，以保證變更產品代碼。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-104">A small update makes changes to one or more application files that are too minor to warrant changing the product code.</span></span> <span data-ttu-id="3d5d8-105">小型更新通常也稱為快速修正工程， (QFE) 更新。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-105">A small update is also commonly referred to as a quick fix engineering (QFE) update.</span></span> <span data-ttu-id="3d5d8-106">小型更新不允許重組功能元件樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-106">A small update does not permit reorganization of the feature-component tree.</span></span>

<span data-ttu-id="3d5d8-107">一般的小型更新只會變更一或兩個檔案或登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-107">A typical small update changes only one or two files or a registry key.</span></span> <span data-ttu-id="3d5d8-108">因為小型更新會變更 .msi 檔案中的資訊，所以必須變更安裝封裝程式碼。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-108">Because a small update changes the information in the .msi file, the installation package code must be changed.</span></span> <span data-ttu-id="3d5d8-109">封裝程式碼會儲存在 [摘要資訊資料流程](summary-information-stream.md)的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-109">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) property of the [Summary Information Stream](summary-information-stream.md).</span></span>

<span data-ttu-id="3d5d8-110">產品代碼永遠不會隨著小型更新而變更，因此小型更新所引進的所有變更都必須與 [變更產品代碼](changing-the-product-code.md)中所述的指導方針一致。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-110">The product code is never changed with a small update, so all of the changes introduced by a small update have to be consistent with the guidelines described in [Changing the Product Code](changing-the-product-code.md).</span></span> <span data-ttu-id="3d5d8-111">更新需要進行 [重大升級](major-upgrades.md) 以變更 [**ProductCode**](productcode.md)。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-111">An update requires a [major upgrade](major-upgrades.md) to change the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="3d5d8-112">如果需要在不變更產品代碼的情況下區分產品，請使用 [次要升級](minor-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-112">If it is necessary to differentiate between products without changing the product code, use a [minor upgrade](minor-upgrades.md).</span></span>

<span data-ttu-id="3d5d8-113">如需如何將小型更新修補套件套用至 Windows Installer 套件的詳細資訊，請參閱 [建立小型更新修補程式](creating-a-small-update-patch.md)、 [修補產品的本機安裝](applying-small-updates-by-patching-the-local-installation-of-the-product.md)、透過 [重新安裝產品來](applying-small-updates-by-reinstalling-the-product.md)套用小型更新，以及藉 [由修補系統管理映射](applying-small-updates-by-patching-an-administrative-image.md)以套用小型更新。</span><span class="sxs-lookup"><span data-stu-id="3d5d8-113">For information on how to apply a small update patch package to a Windows Installer package, see [Creating a Small Update Patch](creating-a-small-update-patch.md), [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and [Applying Small Updates by Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).</span></span>

 

 



