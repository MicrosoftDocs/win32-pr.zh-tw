---
description: 將修補程式和一或多個自訂轉換安裝到應用程式時，通常會先安裝修補程式，然後再安裝自訂轉換。
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: 修補自訂應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319196"
---
# <a name="patching-customized-applications"></a><span data-ttu-id="71528-103">修補自訂應用程式</span><span class="sxs-lookup"><span data-stu-id="71528-103">Patching Customized Applications</span></span>

<span data-ttu-id="71528-104">將修補程式和一或多個自訂轉換安裝到應用程式時，通常會先安裝修補程式，然後再安裝自訂轉換。</span><span class="sxs-lookup"><span data-stu-id="71528-104">When installing a patch and one or more customization transforms to an application, the patch is typically installed first, followed by the customization transforms.</span></span> <span data-ttu-id="71528-105">根據設計，自訂的後續安裝不會中斷修補程式。</span><span class="sxs-lookup"><span data-stu-id="71528-105">By design, the patch is not broken by the subsequent installation of the customization.</span></span> <span data-ttu-id="71528-106">不過，先安裝轉換，然後再安裝修補程式，可能會中斷自訂作業。</span><span class="sxs-lookup"><span data-stu-id="71528-106">However, installing the transforms first, and then the patch, may break the customization.</span></span>

<span data-ttu-id="71528-107">例如，當使用修補程式將產品從第1版更新為第2版，而針對第1版運作的自訂轉換無法在第2版運作時，可能會發生自訂中斷。</span><span class="sxs-lookup"><span data-stu-id="71528-107">For example, a break in the customization could occur when a patch is used to update a product from version 1 to version 2 and a customization transform that works for version 1 does not work for version 2.</span></span> <span data-ttu-id="71528-108">在此情況下，您必須先卸載再重新安裝原始產品，才能將版本更新修補程式套用至自訂產品。</span><span class="sxs-lookup"><span data-stu-id="71528-108">In this case, the version update patch cannot be applied to a customized product without first uninstalling and then reinstalling the original product.</span></span>

 

 



