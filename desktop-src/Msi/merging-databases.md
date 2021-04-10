---
description: 您可以使用安裝程式，藉由執行合併來將某個資料庫中的資訊新增至另一個資料庫。
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: 合併資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944841"
---
# <a name="merging-databases"></a><span data-ttu-id="5c32b-103">合併資料庫</span><span class="sxs-lookup"><span data-stu-id="5c32b-103">Merging Databases</span></span>

<span data-ttu-id="5c32b-104">您可以使用安裝程式，藉由執行合併來將某個資料庫中的資訊新增至另一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="5c32b-104">You can use the installer to add the information in one database into another database by performing a merge.</span></span> <span data-ttu-id="5c32b-105">合併[和轉換](merges-and-transforms.md)操作整個資料庫，而合併合併兩個資料庫到一個。</span><span class="sxs-lookup"><span data-stu-id="5c32b-105">[Merges and Transforms](merges-and-transforms.md) operate on an entire database, and a merge combines two databases into one.</span></span> <span data-ttu-id="5c32b-106">合併適用于開發團隊，因為它們可讓大型應用程式的安裝資料庫分成較小的部分，之後再輕易到完整的安裝資料庫中。</span><span class="sxs-lookup"><span data-stu-id="5c32b-106">Merges are useful to development teams because they allow the installation database of large application to be divided into smaller parts and then recombined into the complete installation database later.</span></span>

<span data-ttu-id="5c32b-107">**將數個元件資料庫合併成單一完整資料庫**</span><span class="sxs-lookup"><span data-stu-id="5c32b-107">**To merge several component databases into a single complete database**</span></span>

1.  <span data-ttu-id="5c32b-108">另外開發部分元件資料庫。</span><span class="sxs-lookup"><span data-stu-id="5c32b-108">Develop the partial component databases separately.</span></span>
2.  <span data-ttu-id="5c32b-109">藉由呼叫 [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) 函數，將每個元件資料庫合併到主要產品資料庫。</span><span class="sxs-lookup"><span data-stu-id="5c32b-109">Merge each component database into the main product database by calling the [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function.</span></span>

 

 



