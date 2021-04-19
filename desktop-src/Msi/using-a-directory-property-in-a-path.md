---
description: 目錄資料表中的目錄會指定安裝的版面配置。
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: 使用路徑中的目錄屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991937"
---
# <a name="using-a-directory-property-in-a-path"></a><span data-ttu-id="16e3b-103">使用路徑中的目錄屬性</span><span class="sxs-lookup"><span data-stu-id="16e3b-103">Using a Directory Property in a Path</span></span>

<span data-ttu-id="16e3b-104">[目錄資料表](directory-table.md)中的目錄會指定安裝的版面配置。</span><span class="sxs-lookup"><span data-stu-id="16e3b-104">The directories in the [Directory table](directory-table.md) specify the layout of an installation.</span></span> <span data-ttu-id="16e3b-105">當 Windows Installer 在 [CostFinalize 動作](costfinalize-action.md)期間解析這些目錄時，目錄資料表中的索引鍵會變成將 [屬性](properties.md) 設為目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="16e3b-105">When the Windows Installer resolves these directories during the [CostFinalize action](costfinalize-action.md), the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span> <span data-ttu-id="16e3b-106">安裝程式也一律會將一些標準 [系統資料夾屬性](property-reference.md) 設定為系統資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="16e3b-106">The installer also always sets a number of standard [System Folder Properties](property-reference.md) to system folder paths.</span></span>

<span data-ttu-id="16e3b-107">[系統資料夾屬性](property-reference.md)的值保證會以目錄分隔符號結尾。</span><span class="sxs-lookup"><span data-stu-id="16e3b-107">The values of the [System Folder Properties](property-reference.md) are guaranteed to end in a directory separator.</span></span> <span data-ttu-id="16e3b-108">在安裝程式執行[CostFinalize 動作](costfinalize-action.md)之後，才保證在[目錄資料表](directory-table.md)中輸入的所有其他屬性值都能以目錄分隔符號結束。</span><span class="sxs-lookup"><span data-stu-id="16e3b-108">The values of all other properties entered in the [Directory table](directory-table.md) are only guaranteed to end in a directory separator after the installer has run the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="16e3b-109">在完成成本評估之前，不是 [系統資料夾屬性](property-reference.md) 的目錄資料表中輸入的屬性值，不能以目錄分隔符號結尾。</span><span class="sxs-lookup"><span data-stu-id="16e3b-109">Before costing has completed, the values of properties entered in the Directory table which are not [System Folder Properties](property-reference.md) may not end in a directory separator.</span></span> <span data-ttu-id="16e3b-110">因此，如果您的安裝在封裝中使用 [自訂動作](custom-actions.md) 來設定目錄屬性，則參考上的值可能不會以目錄分隔符號結尾。</span><span class="sxs-lookup"><span data-stu-id="16e3b-110">Therefore, if your installation sets directory properties using [custom actions](custom-actions.md) in the package, the values on reference might not end with a directory separator.</span></span>

<span data-ttu-id="16e3b-111">因此，以目錄分隔符號結尾的目錄屬性可以在路徑字串中使用，而不需要明確包含目錄分隔符號。</span><span class="sxs-lookup"><span data-stu-id="16e3b-111">Directory properties ending with a directory separator can therefore be used in a path string without explicitly including the directory separator.</span></span> <span data-ttu-id="16e3b-112">例如，如果 DirectoryProperty 的值以目錄分隔符號結尾，下列字串會 *正確地指定* 檔案在 *子目錄* 中的路徑。</span><span class="sxs-lookup"><span data-stu-id="16e3b-112">For example, if the value of DirectoryProperty ends with a directory separator, the following string correctly specifies the path to *file* in *subdirectory*</span></span>

``` syntax
[DirectoryProperty]subdirectory\file
```

<span data-ttu-id="16e3b-113">下列路徑字串不正確。</span><span class="sxs-lookup"><span data-stu-id="16e3b-113">and the following path string is incorrect.</span></span>

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



