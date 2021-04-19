---
description: 您可以為升級的產品安裝新的安裝套件，以套用主要升級。
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: 藉由安裝產品來套用主要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974417"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a><span data-ttu-id="148ef-103">藉由安裝產品來套用主要升級</span><span class="sxs-lookup"><span data-stu-id="148ef-103">Applying Major Upgrades by Installing the Product</span></span>

<span data-ttu-id="148ef-104">您可以為升級的產品安裝新的安裝套件，以套用主要升級。</span><span class="sxs-lookup"><span data-stu-id="148ef-104">A major upgrade can be applied by installing the new installation package for the upgraded product.</span></span> <span data-ttu-id="148ef-105">因為主要升級所取得的產品代碼與原始產品不同，所以安裝升級必須視為新產品的安裝。</span><span class="sxs-lookup"><span data-stu-id="148ef-105">Because major upgrades get a different product code than the original product, installing the upgrade must be treated as an installation of a new product.</span></span> <span data-ttu-id="148ef-106">升級可以像是另一個產品一樣安裝。</span><span class="sxs-lookup"><span data-stu-id="148ef-106">The upgrade can simply be installed like another product.</span></span> <span data-ttu-id="148ef-107">您可以藉由加入 [升級資料表](upgrade-table.md) 和 [FindRelatedProducts 動作](findrelatedproducts-action.md) 和 [RemoveExistingProducts 動作](removeexistingproducts-action.md)，讓新的安裝套件處理舊產品的移除。</span><span class="sxs-lookup"><span data-stu-id="148ef-107">You can have the new installation package handle the removal of the old product by including the [Upgrade table](upgrade-table.md) and the [FindRelatedProducts action](findrelatedproducts-action.md) and [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

<span data-ttu-id="148ef-108">**從命令列將主要升級傳播至目前的使用者**</span><span class="sxs-lookup"><span data-stu-id="148ef-108">**To propagate a major upgrade to current users from the command line**</span></span>

-   <span data-ttu-id="148ef-109">從命令列，使用： **msiexec/i \[**_路徑來更新 msi_ 檔案 *_\]_*</span><span class="sxs-lookup"><span data-stu-id="148ef-109">From the command line, use: **msiexec /i \[**_path to updated msi file_*_\]_*</span></span>

<span data-ttu-id="148ef-110">**從程式將主要升級傳播至目前的使用者**</span><span class="sxs-lookup"><span data-stu-id="148ef-110">**To propagate a major upgrade to current users from a program**</span></span>

-   <span data-ttu-id="148ef-111">從程式中，呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 並指定更新的 msi 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="148ef-111">From a program, call [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) and specify the path to the updated msi file.</span></span>

 

 



