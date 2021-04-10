---
description: Windows Installer 資料庫的文字封存檔案會 idt 副檔名。
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: 封存檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848967"
---
# <a name="archive-file-format"></a><span data-ttu-id="f03f8-103">封存檔案格式</span><span class="sxs-lookup"><span data-stu-id="f03f8-103">Archive File Format</span></span>

<span data-ttu-id="f03f8-104">Windows Installer 資料庫的 [文字](text-archive-files.md) 封存檔案會 idt 副檔名。</span><span class="sxs-lookup"><span data-stu-id="f03f8-104">A [text archive file](text-archive-files.md) for a Windows Installer database carries an .idt file name extension.</span></span> <span data-ttu-id="f03f8-105">將整個資料庫匯出至保存檔案時，資料庫中的每個資料表都有個別的 idt 檔案。</span><span class="sxs-lookup"><span data-stu-id="f03f8-105">When an entire database is exported to archive files, each table in the database has a separate .idt file.</span></span> <span data-ttu-id="f03f8-106">如果資料表包含資料流程資料行，資料表中的每個資料流程都會以副檔名為 ibd 的檔案來表示。</span><span class="sxs-lookup"><span data-stu-id="f03f8-106">If a table contains a stream column, each stream in the table is represented by a file with an .ibd file name extension.</span></span> <span data-ttu-id="f03f8-107">Ibd 檔案會儲存在與資料表同名的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="f03f8-107">The .ibd files are stored in a folder with the same name as the table.</span></span>

## <a name="idt-file-format"></a><span data-ttu-id="f03f8-108">idt 檔案格式</span><span class="sxs-lookup"><span data-stu-id="f03f8-108">.idt File Format</span></span>

<span data-ttu-id="f03f8-109">只包含 ASCII 字元之匯出資料庫資料表的 idt 檔案具有下列基本格式。</span><span class="sxs-lookup"><span data-stu-id="f03f8-109">The .idt file of an exported database table that contains only ASCII characters has the following basic format.</span></span>

-   <span data-ttu-id="f03f8-110">第一個資料列包含以定位字元分隔的資料表資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f03f8-110">The first row contains the table column names separated by tabs.</span></span>
-   <span data-ttu-id="f03f8-111">第二個數據列包含以定位字元分隔的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="f03f8-111">The second row contains the column definitions separated by tabs.</span></span>
-   <span data-ttu-id="f03f8-112">如果檔案只包含 ASCII 資料，則第三個數據列是以 tab 分隔的資料表名稱和主鍵資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f03f8-112">If the file contain only ASCII data, the third row is table name and primary key column names separated by tabs.</span></span>
-   <span data-ttu-id="f03f8-113">檔案中的其餘資料列代表資料表中的資料列，資料行是以定位字元分隔。</span><span class="sxs-lookup"><span data-stu-id="f03f8-113">The remaining rows in the file represent rows in the table, with columns separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="f03f8-114">如果檔案包含非 ASCII 資料，則第三個數據列是數值字碼頁，後面接著資料表名稱和主鍵資料行名稱，並以定位字元分隔。</span><span class="sxs-lookup"><span data-stu-id="f03f8-114">If the file contains non-ASCII data, the third row is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span> <span data-ttu-id="f03f8-115">包含非 ASCII 資訊的 idt 檔案應該以 ASCII 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="f03f8-115">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="f03f8-116">例如，文字封存檔案可以包含編碼為 UTF-8 的資料行和資料表名稱，但封存檔案本身應該是 ASCII。</span><span class="sxs-lookup"><span data-stu-id="f03f8-116">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span> <span data-ttu-id="f03f8-117">請參閱 [文字保存檔案中的 ASCII 資料](ascii-data-in-text-archive-files.md)一節。</span><span class="sxs-lookup"><span data-stu-id="f03f8-117">See the section [ASCII Data in Text Archive Files](ascii-data-in-text-archive-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="f03f8-118">特殊的[ \_ ForceCodepage](-forcecodepage.md)和[ \_ SummaryInformation](-summaryinformation.md) idt 檔會使用擴充格式。</span><span class="sxs-lookup"><span data-stu-id="f03f8-118">The special [\_ForceCodepage](-forcecodepage.md) and [\_SummaryInformation](-summaryinformation.md) .idt files use extended formats.</span></span> <span data-ttu-id="f03f8-119">如需 \_ 其格式的說明，請參閱 ForceCodepage 和 \_ SummaryInformation 一節。</span><span class="sxs-lookup"><span data-stu-id="f03f8-119">See the \_ForceCodepage and \_SummaryInformation sections for descriptions of their formats.</span></span>

 

## <a name="column-definitions"></a><span data-ttu-id="f03f8-120">資料行定義</span><span class="sxs-lookup"><span data-stu-id="f03f8-120">Column Definitions</span></span>

<span data-ttu-id="f03f8-121">資料行定義是以字元表示。</span><span class="sxs-lookup"><span data-stu-id="f03f8-121">Column definitions are indicated by characters.</span></span>

-   <span data-ttu-id="f03f8-122">第一個字元表示資料行類型。</span><span class="sxs-lookup"><span data-stu-id="f03f8-122">The first character indicates the column type.</span></span> <span data-ttu-id="f03f8-123">小寫字母表示不可為 null 的資料行，而大寫字母表示資料行可以包含 null 值。</span><span class="sxs-lookup"><span data-stu-id="f03f8-123">A lowercase letter indicates a non-nullable column and an uppercase letter indicates that the column can contain null values.</span></span>

    | <span data-ttu-id="f03f8-124">字元</span><span class="sxs-lookup"><span data-stu-id="f03f8-124">Character</span></span> | <span data-ttu-id="f03f8-125">意義</span><span class="sxs-lookup"><span data-stu-id="f03f8-125">Meaning</span></span>                   |
    |-----------|---------------------------|
    | <span data-ttu-id="f03f8-126">s、S</span><span class="sxs-lookup"><span data-stu-id="f03f8-126">s, S</span></span>      | <span data-ttu-id="f03f8-127">字串資料行</span><span class="sxs-lookup"><span data-stu-id="f03f8-127">String Column</span></span>             |
    | <span data-ttu-id="f03f8-128">l、L</span><span class="sxs-lookup"><span data-stu-id="f03f8-128">l, L</span></span>      | <span data-ttu-id="f03f8-129">可當地語系化的字串資料行</span><span class="sxs-lookup"><span data-stu-id="f03f8-129">Localizable String Column</span></span> |
    | <span data-ttu-id="f03f8-130">v、V</span><span class="sxs-lookup"><span data-stu-id="f03f8-130">v, V</span></span>      | <span data-ttu-id="f03f8-131">二進位資料行</span><span class="sxs-lookup"><span data-stu-id="f03f8-131">Binary Column</span></span>             |
    | <span data-ttu-id="f03f8-132">i、I</span><span class="sxs-lookup"><span data-stu-id="f03f8-132">i, I</span></span>      | <span data-ttu-id="f03f8-133">整數資料行</span><span class="sxs-lookup"><span data-stu-id="f03f8-133">Integer Column</span></span>            |

    

     

-   <span data-ttu-id="f03f8-134">第二個字元表示資料行資料大小。</span><span class="sxs-lookup"><span data-stu-id="f03f8-134">The second character indicates the column data size.</span></span>

    > [!Note]  
    > <span data-ttu-id="f03f8-135">Windows Installer 實際上不會使用指定的資料行大小來限制可在字串資料列欄位中輸入的字串大小。</span><span class="sxs-lookup"><span data-stu-id="f03f8-135">The Windows Installer does not actually use the specified column size to limit the size of the string that can be entered into a string column field.</span></span> <span data-ttu-id="f03f8-136">不過，有些撰寫工具會使用指定的資料行大小來限制有效字串的大小。</span><span class="sxs-lookup"><span data-stu-id="f03f8-136">However, some authoring tools do use the specified column size to limit the size of a valid string.</span></span> <span data-ttu-id="f03f8-137">建議輸入任何資料行中的字串符合指定的大小需求。</span><span class="sxs-lookup"><span data-stu-id="f03f8-137">It is recommended that strings entered into any column meet the specified size requirement.</span></span>

     

    

    | <span data-ttu-id="f03f8-138">資料行定義</span><span class="sxs-lookup"><span data-stu-id="f03f8-138">Column Definition</span></span> | <span data-ttu-id="f03f8-139">意義</span><span class="sxs-lookup"><span data-stu-id="f03f8-139">Meaning</span></span>                                    |
    |-------------------|--------------------------------------------|
    | <span data-ttu-id="f03f8-140">s255</span><span class="sxs-lookup"><span data-stu-id="f03f8-140">s255</span></span>              | <span data-ttu-id="f03f8-141">不可為 Null 的字串資料行 255 long</span><span class="sxs-lookup"><span data-stu-id="f03f8-141">Non-Nullable String Column 255 long</span></span>        |
    | <span data-ttu-id="f03f8-142">L50</span><span class="sxs-lookup"><span data-stu-id="f03f8-142">L50</span></span>               | <span data-ttu-id="f03f8-143">可為 null 的可當地語系化字串資料行 50 long</span><span class="sxs-lookup"><span data-stu-id="f03f8-143">Nullable Localizable String Column 50 long</span></span> |
    | <span data-ttu-id="f03f8-144">i2，I2</span><span class="sxs-lookup"><span data-stu-id="f03f8-144">i2, I2</span></span>            | <span data-ttu-id="f03f8-145">Short 整數資料行</span><span class="sxs-lookup"><span data-stu-id="f03f8-145">Short Integer Column</span></span>                       |
    | <span data-ttu-id="f03f8-146">i4、I4</span><span class="sxs-lookup"><span data-stu-id="f03f8-146">i4, I4</span></span>            | <span data-ttu-id="f03f8-147">長整數資料行</span><span class="sxs-lookup"><span data-stu-id="f03f8-147">Long Integer Column</span></span>                        |

    

     

## <a name="control-character-translation"></a><span data-ttu-id="f03f8-148">控制字元轉譯</span><span class="sxs-lookup"><span data-stu-id="f03f8-148">Control Character Translation</span></span>

<span data-ttu-id="f03f8-149">將資料表匯出到文字封存檔案會轉譯控制字元，以避免與檔案分隔符號發生衝突。</span><span class="sxs-lookup"><span data-stu-id="f03f8-149">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span> <span data-ttu-id="f03f8-150">寫入 idt 檔案時，控制字元會轉譯如下。</span><span class="sxs-lookup"><span data-stu-id="f03f8-150">While writing into the .idt file, the control characters are translated as follows.</span></span>



| <span data-ttu-id="f03f8-151">控制字元</span><span class="sxs-lookup"><span data-stu-id="f03f8-151">Control Character</span></span> | <span data-ttu-id="f03f8-152">Idt 中的翻譯</span><span class="sxs-lookup"><span data-stu-id="f03f8-152">Translation in .idt</span></span> | <span data-ttu-id="f03f8-153">意義</span><span class="sxs-lookup"><span data-stu-id="f03f8-153">Meaning</span></span>         |
|-------------------|---------------------|-----------------|
| <span data-ttu-id="f03f8-154">NULL</span><span class="sxs-lookup"><span data-stu-id="f03f8-154">NULL</span></span>              | <span data-ttu-id="f03f8-155">21</span><span class="sxs-lookup"><span data-stu-id="f03f8-155">21</span></span>                  | <span data-ttu-id="f03f8-156">Null</span><span class="sxs-lookup"><span data-stu-id="f03f8-156">Null</span></span>            |
| <span data-ttu-id="f03f8-157">BS</span><span class="sxs-lookup"><span data-stu-id="f03f8-157">BS</span></span>                | <span data-ttu-id="f03f8-158">27</span><span class="sxs-lookup"><span data-stu-id="f03f8-158">27</span></span>                  | <span data-ttu-id="f03f8-159">背面空間</span><span class="sxs-lookup"><span data-stu-id="f03f8-159">Back Space</span></span>      |
| <span data-ttu-id="f03f8-160">HT</span><span class="sxs-lookup"><span data-stu-id="f03f8-160">HT</span></span>                | <span data-ttu-id="f03f8-161">16</span><span class="sxs-lookup"><span data-stu-id="f03f8-161">16</span></span>                  | <span data-ttu-id="f03f8-162">索引標籤</span><span class="sxs-lookup"><span data-stu-id="f03f8-162">Tab</span></span>             |
| <span data-ttu-id="f03f8-163">如果</span><span class="sxs-lookup"><span data-stu-id="f03f8-163">LF</span></span>                | <span data-ttu-id="f03f8-164">25</span><span class="sxs-lookup"><span data-stu-id="f03f8-164">25</span></span>                  | <span data-ttu-id="f03f8-165">換行字元</span><span class="sxs-lookup"><span data-stu-id="f03f8-165">Line Feed</span></span>       |
| <span data-ttu-id="f03f8-166">FF</span><span class="sxs-lookup"><span data-stu-id="f03f8-166">FF</span></span>                | <span data-ttu-id="f03f8-167">24</span><span class="sxs-lookup"><span data-stu-id="f03f8-167">24</span></span>                  | <span data-ttu-id="f03f8-168">表單摘要</span><span class="sxs-lookup"><span data-stu-id="f03f8-168">Form Feed</span></span>       |
| <span data-ttu-id="f03f8-169">CR</span><span class="sxs-lookup"><span data-stu-id="f03f8-169">CR</span></span>                | <span data-ttu-id="f03f8-170">17</span><span class="sxs-lookup"><span data-stu-id="f03f8-170">17</span></span>                  | <span data-ttu-id="f03f8-171">回車</span><span class="sxs-lookup"><span data-stu-id="f03f8-171">Carriage Return</span></span> |



 

 

 



