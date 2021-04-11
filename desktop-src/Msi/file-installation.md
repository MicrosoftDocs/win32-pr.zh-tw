---
description: 一旦完成檔案成本計算，安裝程式就會包含處理兩個檔案操作動作所需的所有資訊： DuplicateFiles 和 MoveFiles。
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: 檔案安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115669"
---
# <a name="file-installation"></a><span data-ttu-id="a2853-103">檔案安裝</span><span class="sxs-lookup"><span data-stu-id="a2853-103">File Installation</span></span>

<span data-ttu-id="a2853-104">一旦完成檔案 [成本計算](file-costing.md) ，安裝程式就會包含處理兩個檔案操作動作所需的所有資訊： [DuplicateFiles](duplicatefiles-action.md) 和 [MoveFiles](movefiles-action.md)。</span><span class="sxs-lookup"><span data-stu-id="a2853-104">Once [file costing](file-costing.md) has been completed, the installer has all the information required to process the two file manipulation actions: [DuplicateFiles](duplicatefiles-action.md) and [MoveFiles](movefiles-action.md).</span></span>

<span data-ttu-id="a2853-105">您可以使用 [DuplicateFiles 動作](duplicatefiles-action.md) 來指定安裝程式要在 [DuplicateFile 資料表](duplicatefile-table.md)中複製的檔案。</span><span class="sxs-lookup"><span data-stu-id="a2853-105">Use the [DuplicateFiles action](duplicatefiles-action.md) to specify the files the installer is to duplicate in the [DuplicateFile table](duplicatefile-table.md).</span></span> <span data-ttu-id="a2853-106">您可以使用 [MoveFiles 動作](movefiles-action.md)，藉由查詢 [MoveFile 資料表](movefile-table.md)來判斷要移動的檔案。</span><span class="sxs-lookup"><span data-stu-id="a2853-106">Use the [MoveFiles action](movefiles-action.md)to determine which files to move by querying the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="a2853-107">請注意， [MoveFile 資料表](movefile-table.md) 的 Options 欄位會指定是否要從目前的位置刪除原始檔案。</span><span class="sxs-lookup"><span data-stu-id="a2853-107">Note that the Options field of the [MoveFile table](movefile-table.md) specifies whether or not the original file is to be deleted from its current location.</span></span> <span data-ttu-id="a2853-108">卸載產品時，不會刪除 MoveFiles 動作所移動或複製的檔案。</span><span class="sxs-lookup"><span data-stu-id="a2853-108">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

<span data-ttu-id="a2853-109">當所有其他檔案操作作業完成之後，就會呼叫 [InstallFiles 動作](installfiles-action.md) 。</span><span class="sxs-lookup"><span data-stu-id="a2853-109">The [InstallFiles action](installfiles-action.md) is called once all other file manipulation operations have completed.</span></span> <span data-ttu-id="a2853-110">InstallFiles 動作會處理 [媒體資料表](media-table.md)、檔案 [資料表](file-table.md)和 [元件表格](component-table.md) ，以判斷哪些檔案將從來源複製到目的地。</span><span class="sxs-lookup"><span data-stu-id="a2853-110">The InstallFiles action processes the [Media table](media-table.md), the [File table](file-table.md), and the [Component table](component-table.md) to determine which files will be copied from the source to the destination.</span></span>

<span data-ttu-id="a2853-111">[InstallFiles 動作](installfiles-action.md)會建立安裝所有檔案所需的目錄結構。</span><span class="sxs-lookup"><span data-stu-id="a2853-111">The [InstallFiles action](installfiles-action.md) creates the directory structure necessary to install all files.</span></span> <span data-ttu-id="a2853-112">如果需要安裝明確的空資料夾，則可以呼叫 [CreateFolders 動作](createfolders-action.md) 來建立它。</span><span class="sxs-lookup"><span data-stu-id="a2853-112">If an explicitly empty folder is required to be installed, the [CreateFolders action](createfolders-action.md) may be called to create it.</span></span>

 

 



