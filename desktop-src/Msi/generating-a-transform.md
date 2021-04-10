---
description: 下列程式描述的案例會產生可永久隱藏功能的轉換。
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: 產生轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027029"
---
# <a name="generating-a-transform"></a><span data-ttu-id="e186c-103">產生轉換</span><span class="sxs-lookup"><span data-stu-id="e186c-103">Generating a Transform</span></span>

<span data-ttu-id="e186c-104">下列程式描述的案例會產生可永久隱藏功能的轉換。</span><span class="sxs-lookup"><span data-stu-id="e186c-104">The following procedure describes a scenario to generate a transform that permanently hides a feature.</span></span>

<span data-ttu-id="e186c-105">**永久隱藏產品功能**</span><span class="sxs-lookup"><span data-stu-id="e186c-105">**To permanently hide a product feature**</span></span>

1.  <span data-ttu-id="e186c-106">複製原始安裝套件。</span><span class="sxs-lookup"><span data-stu-id="e186c-106">Copy the original installation package.</span></span>
2.  <span data-ttu-id="e186c-107">將 [功能資料表](feature-table.md) 中顯示資料行的值設定為零，以修改複製。</span><span class="sxs-lookup"><span data-stu-id="e186c-107">Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero.</span></span> <span data-ttu-id="e186c-108">這會指定隱藏此功能。</span><span class="sxs-lookup"><span data-stu-id="e186c-108">This specifies hiding the feature.</span></span>
3.  <span data-ttu-id="e186c-109">藉由呼叫 [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)，從原始安裝套件建立轉換至新的安裝套件。</span><span class="sxs-lookup"><span data-stu-id="e186c-109">Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span></span>
4.  <span data-ttu-id="e186c-110">藉由呼叫 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)，在轉換中建立摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="e186c-110">Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

<span data-ttu-id="e186c-111">然後，您就可以在安裝期間套用轉換。</span><span class="sxs-lookup"><span data-stu-id="e186c-111">The transform is then ready to be applied during installation.</span></span> <span data-ttu-id="e186c-112">如需詳細資訊，請參閱套用 [轉換](applying-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="e186c-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



