---
description: FhManagew.exe 程式會從目前指派的檔案歷程記錄目標裝置刪除超過指定年齡的檔案版本。
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468208"
---
# <a name="fhmanagewexe"></a><span data-ttu-id="67313-103">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="67313-103">FhManagew.exe</span></span>

<span data-ttu-id="67313-104">FhManagew.exe 程式會從目前指派的檔案歷程記錄目標裝置刪除超過指定年齡的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="67313-104">The FhManagew.exe program deletes file versions that exceed a specified age from the currently assigned File History target device.</span></span>

<span data-ttu-id="67313-105">此程式可在 Windows 8 和 Windows Server 2012 及更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="67313-105">This program is available in Windows 8 and Windows Server 2012 and later.</span></span>

<span data-ttu-id="67313-106">若要執行此程式，請移至 [ **開始** ] 功能表，按一下 [ **執行**]，然後輸入下列命令。</span><span class="sxs-lookup"><span data-stu-id="67313-106">To execute this program, go to the **Start** menu, click **Run**, and type the following command.</span></span>

<span data-ttu-id="67313-107">\**FhManagew.exe-清理\*\*\*存留期*</span><span class="sxs-lookup"><span data-stu-id="67313-107">**FhManagew.exe -cleanup** *age*</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67313-108">參數</span><span class="sxs-lookup"><span data-stu-id="67313-108">Parameter</span></span></th>
<th><span data-ttu-id="67313-109">Description</span><span class="sxs-lookup"><span data-stu-id="67313-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67313-110"><span id="age"></span><span id="AGE"></span><em>年齡</em></span><span class="sxs-lookup"><span data-stu-id="67313-110"><span id="age"></span><span id="AGE"></span><em>age</em></span></span><br/></td>
<td><span data-ttu-id="67313-111">此參數會指定可刪除之檔案版本的最小存留期（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="67313-111">This parameter specifies the minimum age, in days, of file versions that can be deleted.</span></span> <span data-ttu-id="67313-112">如果下列兩個條件都成立，則會刪除檔案版本：</span><span class="sxs-lookup"><span data-stu-id="67313-112">A file version is deleted if both of the following conditions are true:</span></span><br/>
<ul>
<li><span data-ttu-id="67313-113">檔案版本比指定的存留期還舊。</span><span class="sxs-lookup"><span data-stu-id="67313-113">The file version is older than the specified age.</span></span></li>
<li><span data-ttu-id="67313-114">檔案已不再包含于保護範圍內，或目標裝置上有較新版本的相同檔案。</span><span class="sxs-lookup"><span data-stu-id="67313-114">The file is no longer included in the protection scope, or there is a newer version of the same file on the target device.</span></span></li>
</ul>
<span data-ttu-id="67313-115">如果 <em>age</em> 參數設定為零，則會刪除所有檔案版本，但目前存在於保護範圍內的每個檔案的最新版本除外。</span><span class="sxs-lookup"><span data-stu-id="67313-115">If the <em>age</em> parameter is set to zero, all file versions are deleted, except for the newest version of each file that is currently present in the protection scope.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="67313-116">若要隱藏此程式的所有輸出，請使用 **-quiet** 命令列選項，如下所示。</span><span class="sxs-lookup"><span data-stu-id="67313-116">To suppress all output from this program, use the **-quiet** command-line option as follows.</span></span>

<span data-ttu-id="67313-117">\**FhManagew.exe-清理\*\*\*存留期* **-安靜**</span><span class="sxs-lookup"><span data-stu-id="67313-117">**FhManagew.exe -cleanup** *age* **-quiet**</span></span>

## <a name="examples"></a><span data-ttu-id="67313-118">範例</span><span class="sxs-lookup"><span data-stu-id="67313-118">Examples</span></span>



| <span data-ttu-id="67313-119">範例</span><span class="sxs-lookup"><span data-stu-id="67313-119">Example</span></span>                                                                                                                                                                                                      | <span data-ttu-id="67313-120">描述</span><span class="sxs-lookup"><span data-stu-id="67313-120">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="67313-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-清除30**</span><span class="sxs-lookup"><span data-stu-id="67313-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**</span></span><br/>                                 | <span data-ttu-id="67313-122">刪除所有早于一個月的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="67313-122">Delete all file versions that are older than one month.</span></span><br/>                        |
| <span data-ttu-id="67313-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-清除 365-quiet**</span><span class="sxs-lookup"><span data-stu-id="67313-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**</span></span><br/> | <span data-ttu-id="67313-124">刪除早于一年的所有檔案版本，並隱藏所有輸出。</span><span class="sxs-lookup"><span data-stu-id="67313-124">Delete all file versions that are older than one year and suppress all output.</span></span><br/> |



 

 

 




