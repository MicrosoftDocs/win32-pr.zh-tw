---
description: 瞭解以字母 T 開頭的 Windows Installer 概念，例如交易處理和轉換。
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: 'T (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9489455f880ba558e5a9f8584be19718823035
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011261"
---
# <a name="t-windows-installer"></a><span data-ttu-id="e8cdf-103">T (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="e8cdf-103">T (Windows Installer)</span></span>

<span data-ttu-id="e8cdf-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T W](u-gly.md) [](v-gly.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e8cdf-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e8cdf-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**交易處理**</span><span class="sxs-lookup"><span data-stu-id="e8cdf-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="e8cdf-106">一或多個作業會一起處理為單一不可分割，稱為「交易」。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="e8cdf-107">所有組成的作業都必須成功，交易才會成功，否則所有作業都會回復為原始狀態。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="e8cdf-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**變換**</span><span class="sxs-lookup"><span data-stu-id="e8cdf-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="e8cdf-109">您可以套用的兩個 [*安裝程式資料庫*](i-gly.md) 之間的差異範本，以在其他資料庫產生類似的變更。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="e8cdf-110">例如，當地語系化轉換可以用來變更應用程式的語言。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="e8cdf-111">如需詳細資訊，請參閱 [合併和轉換](merges-and-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8cdf-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**轉換錯誤條件旗標**</span><span class="sxs-lookup"><span data-stu-id="e8cdf-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="e8cdf-113">用來標示 [*轉換*](/windows)之錯誤狀況的屬性集。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="e8cdf-114">如需詳細資訊，請參閱 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="e8cdf-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**轉換驗證旗標**</span><span class="sxs-lookup"><span data-stu-id="e8cdf-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="e8cdf-116">用來確認 [*轉換*](/windows) 可以套用至資料庫的屬性集。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="e8cdf-117">如需這些屬性的清單，請參閱 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)。</span><span class="sxs-lookup"><span data-stu-id="e8cdf-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
