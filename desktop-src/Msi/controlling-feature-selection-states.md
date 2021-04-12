---
description: 您可以藉由撰寫 Feature 資料表和元件表格，來控制可供使用者和應用程式選取的功能安裝選項。
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: 控制特徵選取狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194948"
---
# <a name="controlling-feature-selection-states"></a><span data-ttu-id="2e2aa-103">控制特徵選取狀態</span><span class="sxs-lookup"><span data-stu-id="2e2aa-103">Controlling Feature Selection States</span></span>

<span data-ttu-id="2e2aa-104">您可以藉由撰寫 [feature 資料表](feature-table.md) 和 [元件表格](component-table.md)，來控制可供使用者和應用程式選取的功能安裝選項。</span><span class="sxs-lookup"><span data-stu-id="2e2aa-104">You can control which feature installation options are available for users and applications to select by authoring the [Feature table](feature-table.md) and [Component table](component-table.md).</span></span>

-   <span data-ttu-id="2e2aa-105">若要防止選取某項功能的公告狀態，請在 [功能資料表](feature-table.md)的 [屬性] 欄位中包含 **msidbFeatureAttributesDisallowAdvertise** 。</span><span class="sxs-lookup"><span data-stu-id="2e2aa-105">To prevent selection of the advertise state for a feature, include **msidbFeatureAttributesDisallowAdvertise** in the feature's Attributes field in the [Feature table](feature-table.md).</span></span>
-   <span data-ttu-id="2e2aa-106">若要防止針對某個功能選取 [從來源執行] 或 [從網路執行] 狀態，請在 [元件資料表](component-table.md)的 [屬性] 欄位中，針對屬於該功能的每個元件包含 **msidbComponentAttributesLocalOnly** 。</span><span class="sxs-lookup"><span data-stu-id="2e2aa-106">To prevent selection of the run-from-source or run-from-network states for a feature, include **msidbComponentAttributesLocalOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="2e2aa-107">如果某項功能沒有元件，則此功能一律會有從來源執行和可執行檔「我的電腦」選項。</span><span class="sxs-lookup"><span data-stu-id="2e2aa-107">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="2e2aa-108">若要防止選取某項功能的 [從我的電腦] 狀態，請在 [元件資料表](component-table.md)的 [屬性] 欄位中，針對屬於該功能的每個元件包含 **msidbComponentAttributesSourceOnly** 。</span><span class="sxs-lookup"><span data-stu-id="2e2aa-108">To prevent selection of the run-from-my-computer state for a feature, include **msidbComponentAttributesSourceOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="2e2aa-109">如果某項功能沒有元件，則此功能一律會有從來源執行和可執行檔「我的電腦」選項。</span><span class="sxs-lookup"><span data-stu-id="2e2aa-109">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="2e2aa-110">您可以在 [功能資料表](feature-table.md)的 [屬性] 欄位中包含 **msidbFeatureAttributesFollowParent** 和 **msidbFeatureAttributesUIDisallowAbsent** ，以撰寫新的子功能。</span><span class="sxs-lookup"><span data-stu-id="2e2aa-110">New child features can be authored by including **msidbFeatureAttributesFollowParent** and **msidbFeatureAttributesUIDisallowAbsent** in the Attributes field of the [Feature table](feature-table.md).</span></span>

 

 



