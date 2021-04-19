---
description: 每當對封裝進行任何變更時，升級套件的作者應該一律先在其封裝上執行驗證，再嘗試第一次安裝封裝並重新執行驗證。
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: 驗證安裝升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cab7f45d3d5c19a71dac8c7a2d0150409b3a45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976377"
---
# <a name="validating-an-installation-upgrade"></a><span data-ttu-id="3703c-103">驗證安裝升級</span><span class="sxs-lookup"><span data-stu-id="3703c-103">Validating an Installation Upgrade</span></span>

<span data-ttu-id="3703c-104">每當對封裝進行任何變更時，升級套件的作者應該一律先在其封裝上執行驗證，再嘗試第一次安裝封裝並重新執行驗證。</span><span class="sxs-lookup"><span data-stu-id="3703c-104">Whenever making any changes to the package, authors of upgrade packages should always run validation on their packages before attempting to install the package for the first time and rerun validation.</span></span> <span data-ttu-id="3703c-105">在升級封裝上執行驗證的方式，與安裝套件的方式相同。</span><span class="sxs-lookup"><span data-stu-id="3703c-105">Run validation on an upgrade package in the same way as for an installation package.</span></span> <span data-ttu-id="3703c-106">如需詳細資訊，請參閱 [驗證安裝資料庫](validating-an-installation-database.md)。</span><span class="sxs-lookup"><span data-stu-id="3703c-106">For details, see [Validating an Installation Database](validating-an-installation-database.md).</span></span>

<span data-ttu-id="3703c-107">這會完成範例升級套件。</span><span class="sxs-lookup"><span data-stu-id="3703c-107">This completes the sample upgrade package.</span></span> <span data-ttu-id="3703c-108">若要安裝升級，請先安裝 MNP2000.msi，然後再安裝 MNP2001.msi。</span><span class="sxs-lookup"><span data-stu-id="3703c-108">To install the upgrade first install MNP2000.msi and then install MNP2001.msi.</span></span> <span data-ttu-id="3703c-109">當您卸載 MNP2001 時，會從電腦移除原始和升級產品。</span><span class="sxs-lookup"><span data-stu-id="3703c-109">When you uninstall MNP2001 both the original and upgrade products are removed from your computer.</span></span>

## <a name="next-example"></a><span data-ttu-id="3703c-110">下一個範例</span><span class="sxs-lookup"><span data-stu-id="3703c-110">Next example</span></span>

[<span data-ttu-id="3703c-111">自訂轉換範例</span><span class="sxs-lookup"><span data-stu-id="3703c-111">A Customization Transform Example</span></span>](a-customization-transform-example.md)

 

 



