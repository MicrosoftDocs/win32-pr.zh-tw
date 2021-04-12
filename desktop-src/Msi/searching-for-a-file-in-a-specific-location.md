---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋使用者系統上特定位置中的檔案。
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: 搜尋特定位置中的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513660"
---
# <a name="searching-for-a-file-in-a-specific-location"></a><span data-ttu-id="80cea-103">搜尋特定位置中的檔案</span><span class="sxs-lookup"><span data-stu-id="80cea-103">Searching for a File in a Specific Location</span></span>

<span data-ttu-id="80cea-104">**搜尋使用者系統上特定位置的檔案**</span><span class="sxs-lookup"><span data-stu-id="80cea-104">**To search for a file in a specific location on a user system**</span></span>

1.  <span data-ttu-id="80cea-105">列出 [簽名表](signature-table.md)中的檔案簽章和名稱。</span><span class="sxs-lookup"><span data-stu-id="80cea-105">List the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="80cea-106">此記錄中的其餘欄位可以是 null，以搜尋任何版本的 MyApp.exe。</span><span class="sxs-lookup"><span data-stu-id="80cea-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    [<span data-ttu-id="80cea-107">簽名表</span><span class="sxs-lookup"><span data-stu-id="80cea-107">Signature Table</span></span>](signature-table.md)

    

    | <span data-ttu-id="80cea-108">簽名</span><span class="sxs-lookup"><span data-stu-id="80cea-108">Signature</span></span>          | <span data-ttu-id="80cea-109">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="80cea-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="80cea-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="80cea-110">AppFile</span></span><br/> | <span data-ttu-id="80cea-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="80cea-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="80cea-112">如果已安裝 MyApp.exe，請輸入安裝程式要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="80cea-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="80cea-113">[AppSearch 資料表](appsearch-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="80cea-113">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="80cea-114">屬性</span><span class="sxs-lookup"><span data-stu-id="80cea-114">Property</span></span>         | <span data-ttu-id="80cea-115">簽名</span><span class="sxs-lookup"><span data-stu-id="80cea-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="80cea-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="80cea-116">MYAPP</span></span><br/> | <span data-ttu-id="80cea-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="80cea-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="80cea-118">使用 [DrLocator 資料表](drlocator-table.md)。</span><span class="sxs-lookup"><span data-stu-id="80cea-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="80cea-119">在 [路徑] 欄位中，輸入使用者系統上檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="80cea-119">Enter the full path to the file on the user system in the Path field.</span></span> <span data-ttu-id="80cea-120">在 [深度] 資料行中輸入0值，以搜尋 bin 資料夾。</span><span class="sxs-lookup"><span data-stu-id="80cea-120">Enter a value of 0 into the Depth column to search the bin folder.</span></span>

    [<span data-ttu-id="80cea-121">DrLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="80cea-121">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="80cea-122">簽名</span><span class="sxs-lookup"><span data-stu-id="80cea-122">Signature</span></span>          | <span data-ttu-id="80cea-123">父代</span><span class="sxs-lookup"><span data-stu-id="80cea-123">Parent</span></span> | <span data-ttu-id="80cea-124">路徑</span><span class="sxs-lookup"><span data-stu-id="80cea-124">Path</span></span>                                                    | <span data-ttu-id="80cea-125">深度</span><span class="sxs-lookup"><span data-stu-id="80cea-125">Depth</span></span>        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | <span data-ttu-id="80cea-126">AppFile</span><span class="sxs-lookup"><span data-stu-id="80cea-126">AppFile</span></span><br/> |        | <span data-ttu-id="80cea-127">C： \\ Program Files \\ MyProducts \\ Projects \\ bin</span><span class="sxs-lookup"><span data-stu-id="80cea-127">C:\\Program Files\\MyProducts\\Projects\\bin</span></span><br/> | <span data-ttu-id="80cea-128">0</span><span class="sxs-lookup"><span data-stu-id="80cea-128">0</span></span><br/> |

    

     

4.  <span data-ttu-id="80cea-129">在動作順序中包含 AppSearch 動作。</span><span class="sxs-lookup"><span data-stu-id="80cea-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="80cea-130">如果 MyApp.exe 安裝在 C： \\ Program Files \\ MyProducts \\ Projects Bin 中 \\ ，安裝程式會將屬性 MYAPP 設定為檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="80cea-130">If MyApp.exe is installed in C:\\Program Files\\MyProducts\\Projects\\bin, the Installer sets the property MYAPP to the location of file.</span></span>

 

 




