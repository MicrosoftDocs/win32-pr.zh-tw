---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋檔案，並建立包含檔案路徑的屬性。
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: 搜尋檔案並建立保存檔案路徑的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849948"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a><span data-ttu-id="fed77-103">搜尋檔案並建立保存檔案路徑的屬性</span><span class="sxs-lookup"><span data-stu-id="fed77-103">Searching for a File and Creating a Property Holding the File's Path</span></span>

<span data-ttu-id="fed77-104">**搜尋檔案並建立保存該檔案路徑的屬性**</span><span class="sxs-lookup"><span data-stu-id="fed77-104">**To search for a file and create a property holding the path of that file**</span></span>

1.  <span data-ttu-id="fed77-105">首先，請在簽章 [資料表](signature-table.md)中列出檔案簽章和名稱，以搜尋檔案。</span><span class="sxs-lookup"><span data-stu-id="fed77-105">First do a search for the file by listing the file signature and name in the [Signature Table](signature-table.md).</span></span>

    <span data-ttu-id="fed77-106">此記錄的其餘欄位可以保留空白，以指定搜尋任何版本的 MyApp.exe。</span><span class="sxs-lookup"><span data-stu-id="fed77-106">The remaining fields of this record can be left empty to specify a search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="fed77-107">[簽名表](signature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="fed77-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="fed77-108">簽名</span><span class="sxs-lookup"><span data-stu-id="fed77-108">Signature</span></span>          | <span data-ttu-id="fed77-109">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="fed77-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="fed77-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="fed77-110">AppFile</span></span><br/> | <span data-ttu-id="fed77-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="fed77-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="fed77-112">接下來，指定要在 [DrLocator 資料表](drlocator-table.md)中搜尋之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="fed77-112">Next, specify the path of the file that is being searched for in the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="fed77-113">因為 AppFolder 不會列在簽章 [資料表](signature-table.md)中，所以安裝程式會判斷 AppFolder 是資料夾而非檔案。</span><span class="sxs-lookup"><span data-stu-id="fed77-113">Because AppFolder is not listed in the [Signature Table](signature-table.md), the Installer determines that AppFolder is a folder rather than a file.</span></span>

    [<span data-ttu-id="fed77-114">DrLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="fed77-114">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="fed77-115">簽名</span><span class="sxs-lookup"><span data-stu-id="fed77-115">Signature</span></span>            | <span data-ttu-id="fed77-116">父代</span><span class="sxs-lookup"><span data-stu-id="fed77-116">Parent</span></span>             | <span data-ttu-id="fed77-117">路徑</span><span class="sxs-lookup"><span data-stu-id="fed77-117">Path</span></span> | <span data-ttu-id="fed77-118">深度</span><span class="sxs-lookup"><span data-stu-id="fed77-118">Depth</span></span> |
    |----------------------|--------------------|------|-------|
    | <span data-ttu-id="fed77-119">AppFile</span><span class="sxs-lookup"><span data-stu-id="fed77-119">AppFile</span></span><br/>   |                    |      |       |
    | <span data-ttu-id="fed77-120">AppFolder</span><span class="sxs-lookup"><span data-stu-id="fed77-120">AppFolder</span></span><br/> | <span data-ttu-id="fed77-121">AppFile</span><span class="sxs-lookup"><span data-stu-id="fed77-121">AppFile</span></span><br/> |      |       |

    

     

3.  <span data-ttu-id="fed77-122">最後，填入 [AppSearch 資料表](appsearch-table.md) ，讓 [AppSearch 動作](appsearch-action.md) 傳回 AppFolder 的路徑。</span><span class="sxs-lookup"><span data-stu-id="fed77-122">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the path of AppFolder.</span></span>

    <span data-ttu-id="fed77-123">在安裝程式執行 AppSearch 動作之後，MYFOLDER 的值是 AppFolder 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fed77-123">After the Installer executes the AppSearch action, the value of MYFOLDER is the full path of AppFolder.</span></span>

    <span data-ttu-id="fed77-124">[AppSearch 資料表](appsearch-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="fed77-124">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="fed77-125">屬性</span><span class="sxs-lookup"><span data-stu-id="fed77-125">Property</span></span>            | <span data-ttu-id="fed77-126">簽名</span><span class="sxs-lookup"><span data-stu-id="fed77-126">Signature</span></span>            |
    |---------------------|----------------------|
    | <span data-ttu-id="fed77-127">MYFOLDER</span><span class="sxs-lookup"><span data-stu-id="fed77-127">MYFOLDER</span></span><br/> | <span data-ttu-id="fed77-128">AppFolder</span><span class="sxs-lookup"><span data-stu-id="fed77-128">AppFolder</span></span><br/> |

    

     

 

 




