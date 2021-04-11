---
description: 隨附檔案的安裝狀態不會相依于自己的檔案版本設定資訊，而是在其附屬父系的版本控制上。
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: 隨附檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944765"
---
# <a name="companion-files"></a><span data-ttu-id="79527-103">隨附檔案</span><span class="sxs-lookup"><span data-stu-id="79527-103">Companion Files</span></span>

<span data-ttu-id="79527-104">隨附檔案的安裝狀態不會相依于自己的檔案版本設定資訊，而是在其附屬父系的版本控制上。</span><span class="sxs-lookup"><span data-stu-id="79527-104">The installation state of a companion file depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="79527-105">請參閱檔案 [版本控制規則](file-versioning-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="79527-105">See the [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="79527-106">若要指定附屬檔案，必須將檔案 [資料表](file-table.md) 中附屬父系的主鍵撰寫到附屬記錄的 [版本] 欄中。</span><span class="sxs-lookup"><span data-stu-id="79527-106">To specify a companion file, the primary key of the companion parent in the [File table](file-table.md) must be authored into the Version column of the record for the companion.</span></span>

<span data-ttu-id="79527-107">在下列範例中，>filea.docx 是隨附的父系，而 >fileb.docx 則是隨附的檔案。</span><span class="sxs-lookup"><span data-stu-id="79527-107">In the following example, FileA is the companion parent and FileB is the companion file.</span></span>

<span data-ttu-id="79527-108">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="79527-108">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="79527-109">檔案</span><span class="sxs-lookup"><span data-stu-id="79527-109">File</span></span>  | <span data-ttu-id="79527-110">版本</span><span class="sxs-lookup"><span data-stu-id="79527-110">Version</span></span> |
|-------|---------|
| <span data-ttu-id="79527-111">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="79527-111">FileA</span></span> | <span data-ttu-id="79527-112">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="79527-112">1.0.0.0</span></span> |
| <span data-ttu-id="79527-113">>fileb.docx</span><span class="sxs-lookup"><span data-stu-id="79527-113">FileB</span></span> | <span data-ttu-id="79527-114">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="79527-114">FileA</span></span>   |



 

<span data-ttu-id="79527-115">在此範例中，>fileb.docx 的安裝狀態取決於檔案 [版本控制規則](file-versioning-rules.md) 和 >filea.docx 的版本設定資訊。</span><span class="sxs-lookup"><span data-stu-id="79527-115">In this example, the installation state of FileB depends on the [File Versioning Rules](file-versioning-rules.md) and the versioning information for FileA.</span></span> <span data-ttu-id="79527-116">如果安裝程式判斷套件中的 >filea.docx 版本應該安裝在使用者電腦上已存在的舊版 >filea.docx 上，它也會從套件安裝 >fileb.docx，不論任何已安裝的 >fileb.docx 版本為何。</span><span class="sxs-lookup"><span data-stu-id="79527-116">If the installer determines that the version of FileA in the package should be installed over an older version of FileA that already exists on the user's computer, it will also install FileB from the package regardless of the version of any installed FileB.</span></span>

<span data-ttu-id="79527-117">請注意，檔案是其元件的金鑰路徑，不能是附屬檔案。</span><span class="sxs-lookup"><span data-stu-id="79527-117">Note that a file that is the key path for its component must not be a companion file.</span></span> <span data-ttu-id="79527-118">這會導致金鑰路徑檔案的版本控制邏輯由隨附的父檔案所決定。</span><span class="sxs-lookup"><span data-stu-id="79527-118">This would result in the versioning logic of the key path file being determined by the companion parent file.</span></span>

 

 



