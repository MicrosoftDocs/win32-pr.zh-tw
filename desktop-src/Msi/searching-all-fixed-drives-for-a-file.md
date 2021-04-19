---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋檔案的所有固定磁片磁碟機。
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: 搜尋檔案的所有固定磁片磁碟機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983737"
---
# <a name="searching-all-fixed-drives-for-a-file"></a><span data-ttu-id="c5283-103">搜尋檔案的所有固定磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="c5283-103">Searching All Fixed Drives for a File</span></span>

<span data-ttu-id="c5283-104">**搜尋檔案的所有固定磁片磁碟機**</span><span class="sxs-lookup"><span data-stu-id="c5283-104">**To search all fixed drives for a file**</span></span>

1.  <span data-ttu-id="c5283-105">在簽章 [資料表](signature-table.md)中輸入檔案簽章和名稱。</span><span class="sxs-lookup"><span data-stu-id="c5283-105">Enter the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="c5283-106">此記錄中的其餘欄位可以是 null，以搜尋任何版本的 MyApp.exe。</span><span class="sxs-lookup"><span data-stu-id="c5283-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="c5283-107">[簽名表](signature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="c5283-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="c5283-108">簽名</span><span class="sxs-lookup"><span data-stu-id="c5283-108">Signature</span></span>          | <span data-ttu-id="c5283-109">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="c5283-109">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="c5283-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="c5283-110">AppFile</span></span><br/> | <span data-ttu-id="c5283-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="c5283-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="c5283-112">如果已安裝 MyApp.exe，請輸入安裝程式要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="c5283-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    [<span data-ttu-id="c5283-113">AppSearch 資料表</span><span class="sxs-lookup"><span data-stu-id="c5283-113">AppSearch Table</span></span>](appsearch-table.md)

    

    | <span data-ttu-id="c5283-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c5283-114">Property</span></span>         | <span data-ttu-id="c5283-115">簽名</span><span class="sxs-lookup"><span data-stu-id="c5283-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="c5283-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="c5283-116">MYAPP</span></span><br/> | <span data-ttu-id="c5283-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="c5283-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="c5283-118">使用 [DrLocator 資料表](drlocator-table.md)。</span><span class="sxs-lookup"><span data-stu-id="c5283-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="c5283-119">將 [父系] 和 [路徑] 欄位保留空白，以搜尋使用者系統的所有固定磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c5283-119">Leave the Parent and Path fields empty to search all fixed drives of the user system.</span></span> <span data-ttu-id="c5283-120">在 [深度] 資料行中指定要搜尋的子目錄層級數目。</span><span class="sxs-lookup"><span data-stu-id="c5283-120">Specify in the Depth column the number of subdirectory levels to search.</span></span> <span data-ttu-id="c5283-121">例如，將 Depth 設定為0會偵測到 c： \\MyApp.exe，但不會在深度2偵測到檔案，例如： c： \\ Program Files \\ MyApps \\MyApp.exe。</span><span class="sxs-lookup"><span data-stu-id="c5283-121">For example, setting Depth to 0 detects c:\\MyApp.exe, but does not detect the file at a depth of 2, for example: c:\\Program Files\\MyApps\\MyApp.exe.</span></span>

    [<span data-ttu-id="c5283-122">DrLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="c5283-122">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="c5283-123">簽名</span><span class="sxs-lookup"><span data-stu-id="c5283-123">Signature</span></span>          | <span data-ttu-id="c5283-124">父代</span><span class="sxs-lookup"><span data-stu-id="c5283-124">Parent</span></span> | <span data-ttu-id="c5283-125">路徑</span><span class="sxs-lookup"><span data-stu-id="c5283-125">Path</span></span> | <span data-ttu-id="c5283-126">深度</span><span class="sxs-lookup"><span data-stu-id="c5283-126">Depth</span></span>        |
    |--------------------|--------|------|--------------|
    | <span data-ttu-id="c5283-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="c5283-127">AppFile</span></span><br/> |        |      | <span data-ttu-id="c5283-128">3</span><span class="sxs-lookup"><span data-stu-id="c5283-128">3</span></span><br/> |

    

     

4.  <span data-ttu-id="c5283-129">在動作順序中包含 AppSearch 動作。</span><span class="sxs-lookup"><span data-stu-id="c5283-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="c5283-130">如果已安裝 MyApp.exe，安裝程式會將屬性 MYAPP 設定為檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="c5283-130">If MyApp.exe is installed, the Installer sets the property MYAPP to the location of the file.</span></span> <span data-ttu-id="c5283-131">如果已安裝檔案，MYAPP 會在條件運算式中評估為 True。</span><span class="sxs-lookup"><span data-stu-id="c5283-131">If the file is installed, MYAPP evaluates as True in a conditional expression.</span></span>

 

 




