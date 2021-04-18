---
description: 每個 Windows Installer 功能都會使用一或多個 Windows Installer 元件，而功能可以共用元件。
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: 指定 Feature-Component 關聯性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971430"
---
# <a name="specifying-feature-component-relationships"></a><span data-ttu-id="8e82e-103">指定 Feature-Component 關聯性</span><span class="sxs-lookup"><span data-stu-id="8e82e-103">Specifying Feature-Component Relationships</span></span>

<span data-ttu-id="8e82e-104">每個 [Windows Installer 功能](windows-installer-features.md) 都會使用一或多個 [Windows Installer 元件](windows-installer-components.md)，而功能可以共用元件。</span><span class="sxs-lookup"><span data-stu-id="8e82e-104">Each [Windows Installer Feature](windows-installer-features.md) uses one or more [Windows Installer Components](windows-installer-components.md), and features may share components.</span></span> <span data-ttu-id="8e82e-105">[FeatureComponents 資料表](featurecomponents-table.md)會定義功能和元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="8e82e-105">The [FeatureComponents table](featurecomponents-table.md) defines the relationship between features and components.</span></span> <span data-ttu-id="8e82e-106">請參閱 Windows Installer 總覽中的 [核心資料表群組](core-tables-group.md) 和 [元件和功能](components-and-features.md) 。</span><span class="sxs-lookup"><span data-stu-id="8e82e-106">See the [Core Tables Group](core-tables-group.md) and [Components and Features](components-and-features.md) in the Windows Installer overview.</span></span> <span data-ttu-id="8e82e-107">在本節中，您會將資訊新增至「記事本」範例的 FeatureComponents 資料表。</span><span class="sxs-lookup"><span data-stu-id="8e82e-107">In this section you add information to the FeatureComponents table of the Notepad sample.</span></span>

<span data-ttu-id="8e82e-108">使用資料庫編輯器開啟 MNP2000.msi，並將下列資料輸入空白的 FeatureComponents 資料表中。</span><span class="sxs-lookup"><span data-stu-id="8e82e-108">Use your database editor to open MNP2000.msi and enter the following data into the empty FeatureComponents table.</span></span>

[<span data-ttu-id="8e82e-109">FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="8e82e-109">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="8e82e-110">功能\_</span><span class="sxs-lookup"><span data-stu-id="8e82e-110">Feature\_</span></span> | <span data-ttu-id="8e82e-111">元件\_</span><span class="sxs-lookup"><span data-stu-id="8e82e-111">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="8e82e-112">棒球</span><span class="sxs-lookup"><span data-stu-id="8e82e-112">Baseball</span></span>  | <span data-ttu-id="8e82e-113">棒球</span><span class="sxs-lookup"><span data-stu-id="8e82e-113">Baseball</span></span>    |
| <span data-ttu-id="8e82e-114">演唱會</span><span class="sxs-lookup"><span data-stu-id="8e82e-114">Concert</span></span>   | <span data-ttu-id="8e82e-115">演唱會</span><span class="sxs-lookup"><span data-stu-id="8e82e-115">Concert</span></span>     |
| <span data-ttu-id="8e82e-116">舞蹈</span><span class="sxs-lookup"><span data-stu-id="8e82e-116">Dance</span></span>     | <span data-ttu-id="8e82e-117">舞蹈</span><span class="sxs-lookup"><span data-stu-id="8e82e-117">Dance</span></span>       |
| <span data-ttu-id="8e82e-118">足球</span><span class="sxs-lookup"><span data-stu-id="8e82e-118">Football</span></span>  | <span data-ttu-id="8e82e-119">足球</span><span class="sxs-lookup"><span data-stu-id="8e82e-119">Football</span></span>    |
| <span data-ttu-id="8e82e-120">Help</span><span class="sxs-lookup"><span data-stu-id="8e82e-120">Help</span></span>      | <span data-ttu-id="8e82e-121">Help</span><span class="sxs-lookup"><span data-stu-id="8e82e-121">Help</span></span>        |
| <span data-ttu-id="8e82e-122">一月</span><span class="sxs-lookup"><span data-stu-id="8e82e-122">January</span></span>   | <span data-ttu-id="8e82e-123">一月</span><span class="sxs-lookup"><span data-stu-id="8e82e-123">January</span></span>     |
| <span data-ttu-id="8e82e-124">NewYears</span><span class="sxs-lookup"><span data-stu-id="8e82e-124">NewYears</span></span>  | <span data-ttu-id="8e82e-125">NewYears</span><span class="sxs-lookup"><span data-stu-id="8e82e-125">NewYears</span></span>    |
| <span data-ttu-id="8e82e-126">[記事本]</span><span class="sxs-lookup"><span data-stu-id="8e82e-126">Notepad</span></span>   | <span data-ttu-id="8e82e-127">[記事本]</span><span class="sxs-lookup"><span data-stu-id="8e82e-127">Notepad</span></span>     |
| <span data-ttu-id="8e82e-128">讀我檔案</span><span class="sxs-lookup"><span data-stu-id="8e82e-128">Readme</span></span>    | <span data-ttu-id="8e82e-129">[記事本]</span><span class="sxs-lookup"><span data-stu-id="8e82e-129">Notepad</span></span>     |



 

[<span data-ttu-id="8e82e-130">繼續</span><span class="sxs-lookup"><span data-stu-id="8e82e-130">Continue</span></span>](adding-registry-information.md)

 

 



