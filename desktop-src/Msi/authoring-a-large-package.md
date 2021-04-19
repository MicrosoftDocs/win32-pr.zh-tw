---
description: 您可以使用此指導方針來撰寫包含32767以上檔案的 Windows Installer 套件。
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: 撰寫大型封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992447"
---
# <a name="authoring-a-large-package"></a><span data-ttu-id="1d475-103">撰寫大型封裝</span><span class="sxs-lookup"><span data-stu-id="1d475-103">Authoring a Large Package</span></span>

<span data-ttu-id="1d475-104">您可以使用此指導方針來撰寫包含32767以上檔案的 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="1d475-104">Use this guideline to author a Windows Installer package that contains more than 32767 files.</span></span>

<span data-ttu-id="1d475-105">如果您的 Windows Installer 封裝包含32767個以上的檔案，您必須變更資料庫的架構，以增加下列資料行的限制：</span><span class="sxs-lookup"><span data-stu-id="1d475-105">If your Windows Installer package contains more than 32767 files, you must change the schema of the database to increase the limit of the following columns:</span></span>

-   <span data-ttu-id="1d475-106">[File 資料表](file-table.md)的 Sequence 資料行。</span><span class="sxs-lookup"><span data-stu-id="1d475-106">The Sequence column of the [File table](file-table.md).</span></span>
-   <span data-ttu-id="1d475-107">[媒體資料表](media-table.md)的 LastSequence 資料行。</span><span class="sxs-lookup"><span data-stu-id="1d475-107">The LastSequence column of the [Media table](media-table.md).</span></span>
-   <span data-ttu-id="1d475-108">[Patch 資料表](patch-table.md)的 Sequence 資料行。</span><span class="sxs-lookup"><span data-stu-id="1d475-108">The Sequence column of the [Patch table](patch-table.md).</span></span>

<span data-ttu-id="1d475-109">如需詳細資訊，請參閱資料 [行定義格式](column-definition-format.md)。</span><span class="sxs-lookup"><span data-stu-id="1d475-109">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

<span data-ttu-id="1d475-110">**若要增加資料庫資料行的限制**</span><span class="sxs-lookup"><span data-stu-id="1d475-110">**To increase the limit of a database column**</span></span>

1.  <span data-ttu-id="1d475-111">將資料表匯出至 idt 檔案。</span><span class="sxs-lookup"><span data-stu-id="1d475-111">Export the table to an .idt file.</span></span> <span data-ttu-id="1d475-112">如需詳細資訊，請參閱 [Msidb.exe](msidb-exe.md)、 [匯出](export-files.md)檔案，以及匯 [入和匯出](importing-and-exporting.md)。</span><span class="sxs-lookup"><span data-stu-id="1d475-112">For details, see [Msidb.exe](msidb-exe.md), [Export Files](export-files.md), and [Importing and Exporting](importing-and-exporting.md).</span></span>
2.  <span data-ttu-id="1d475-113">編輯 idt 檔案，將資料行類型從 i2 變更為 i4，或從 I2 變更為 I4。</span><span class="sxs-lookup"><span data-stu-id="1d475-113">Edit the .idt file to change the column type from i2 to i4, or from I2 to I4.</span></span>
3.  <span data-ttu-id="1d475-114">將[ \_ 驗證](-validation-table.md)資料表匯出至 idt 檔案。</span><span class="sxs-lookup"><span data-stu-id="1d475-114">Export the [\_Validation](-validation-table.md) table to an .idt file.</span></span>
4.  <span data-ttu-id="1d475-115">編輯 idt 檔案，以變更 [ [ \_ 驗證](-validation-table.md)] 資料表的 [int32.maxvalue] 資料行中的值，以容納增加的資料行寬度。</span><span class="sxs-lookup"><span data-stu-id="1d475-115">Edit the .idt file to change the values in the MaxValue column of the [\_Validation](-validation-table.md) table to accommodate the increased column widths.</span></span>
5.  <span data-ttu-id="1d475-116">將 idt 檔案匯入回資料庫。</span><span class="sxs-lookup"><span data-stu-id="1d475-116">Import the .idt files back into the database.</span></span>

<span data-ttu-id="1d475-117">請注意，無法在具有不同資料行類型的兩個封裝之間建立轉換和修補程式。</span><span class="sxs-lookup"><span data-stu-id="1d475-117">Note that transforms and patches cannot be created between two packages with different column types.</span></span>

 

 



