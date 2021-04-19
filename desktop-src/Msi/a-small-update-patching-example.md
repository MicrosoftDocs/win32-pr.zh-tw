---
description: 此範例說明如何建立修補程式套件，以將小型更新套用至安裝範例中所討論的範例安裝套件。
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: 小型更新修補範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995832"
---
# <a name="a-small-update-patching-example"></a><span data-ttu-id="30ac8-103">小型更新修補範例</span><span class="sxs-lookup"><span data-stu-id="30ac8-103">A Small Update Patching Example</span></span>

<span data-ttu-id="30ac8-104">此範例說明如何建立 [修補程式套件](patch-packages.md) ，以將 [小型更新](small-updates.md) 套用至 [安裝範例](an-installation-example.md)中所討論的範例安裝套件。</span><span class="sxs-lookup"><span data-stu-id="30ac8-104">This example illustrates how to create a [patch package](patch-packages.md) that applies a [small update](small-updates.md) to the sample installation package discussed in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="30ac8-105">小規模的更新會變更一個或多個應用程式檔，而這些應用程式檔會被判定為太小而無法保證變更產品代碼。</span><span class="sxs-lookup"><span data-stu-id="30ac8-105">A small update makes changes to one or more application files that are judged to be too minor to warrant changing the product code.</span></span> <span data-ttu-id="30ac8-106">如需詳細資訊，請參閱 [修補和升級](patching-and-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="30ac8-106">For more information see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="30ac8-107">此範例說明如何建立 Windows Installer 修補程式套件，以更新假設產品 MNP2000 的協同功能，以修正原始產品中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="30ac8-107">This example illustrates how to create a Windows Installer patch package that updates the Concert feature of the hypothetical product MNP2000 to fix an error in the original product.</span></span> <span data-ttu-id="30ac8-108">範例修補套件會將小型更新套用至不需要變更產品代碼的產品。</span><span class="sxs-lookup"><span data-stu-id="30ac8-108">The example patch package applies a small update to the product that does not require changing the product code.</span></span> <span data-ttu-id="30ac8-109">如需有關主要升級的詳細資訊，請參閱[修補和升級](patching-and-upgrades.md)一節中的[重大升級](major-upgrades.md)主題。</span><span class="sxs-lookup"><span data-stu-id="30ac8-109">See the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section for more information about major upgrades.</span></span>

<span data-ttu-id="30ac8-110">範例升級套件具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="30ac8-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="30ac8-111">它會更正協同功能所顯示的協同排程中的次要錯誤。</span><span class="sxs-lookup"><span data-stu-id="30ac8-111">It corrects a minor error in the Concert schedule displayed by the Concert feature.</span></span>
-   <span data-ttu-id="30ac8-112">它會更新套件程式碼，以反映安裝套件已變更。</span><span class="sxs-lookup"><span data-stu-id="30ac8-112">It updates the package code to reflect the installation package has changed.</span></span>
-   <span data-ttu-id="30ac8-113">您可以修補產品的本機安裝，以套用 small update。</span><span class="sxs-lookup"><span data-stu-id="30ac8-113">The small update can be applied by patching the local installation of the product.</span></span>

[<span data-ttu-id="30ac8-114">繼續</span><span class="sxs-lookup"><span data-stu-id="30ac8-114">Continue</span></span>](planning-a-small-update-patch.md)

 

 



