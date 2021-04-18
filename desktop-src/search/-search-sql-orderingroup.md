---
description: ORDER IN GROUP 子句會搭配 GROUP ON 語句使用，後者會傳回群組中的結果集。
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: ORDER IN GROUP 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318156"
---
# <a name="order-in-group-clause"></a><span data-ttu-id="e209b-103">ORDER IN GROUP 子句</span><span class="sxs-lookup"><span data-stu-id="e209b-103">ORDER IN GROUP Clause</span></span>

<span data-ttu-id="e209b-104">ORDER IN GROUP 子句會搭配 [GROUP ON](-search-sql-group-on-over.md) 語句使用，後者會傳回群組中的結果集。</span><span class="sxs-lookup"><span data-stu-id="e209b-104">The ORDER IN GROUP clause is used in conjunction with the [GROUP ON](-search-sql-group-on-over.md) statement, which returns result sets in groups.</span></span> <span data-ttu-id="e209b-105">ORDER IN GROUP 子句可讓您以不同的方式排序每個傳回的群組。</span><span class="sxs-lookup"><span data-stu-id="e209b-105">The ORDER IN GROUP clause enables you to sort each returned group in a different way.</span></span> <span data-ttu-id="e209b-106">例如，如果您以 system.string 分組，則可以 System.Doc>ument 來排序所有檔。LastAuthor，AlbumArtist 的所有音樂檔案，以及所有的電子郵件 FromName。</span><span class="sxs-lookup"><span data-stu-id="e209b-106">If you group on System.Kind, for example, you can then sort all documents by System.Document.LastAuthor, all music files by System.Music.AlbumArtist, and all emails by System.Message.FromName.</span></span>

## <a name="syntax"></a><span data-ttu-id="e209b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e209b-107">Syntax</span></span>

<span data-ttu-id="e209b-108">以下是 GROUP 子句中 ORDER IN 的語法：</span><span class="sxs-lookup"><span data-stu-id="e209b-108">The following is the syntax of the ORDER IN GROUP clause:</span></span>


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



<span data-ttu-id="e209b-109">組名規範是群組資料行中的範圍或已知值（如 GROUP ON 語句中所指定）。</span><span class="sxs-lookup"><span data-stu-id="e209b-109">The group name specifier is a range or known value from the group column, as specified in the GROUP ON statement.</span></span> <span data-ttu-id="e209b-110">例如，ISOSpeed 的已知值會包含 ' ISO-100 '、' ISO-200 ' 等等。</span><span class="sxs-lookup"><span data-stu-id="e209b-110">For example, known values for System.Photo.ISOSpeed would include 'ISO-100', 'ISO-200', and so on.</span></span> <span data-ttu-id="e209b-111">DateTaken 的範圍會包含 ' 2006-1-1 ' 和 ' 2007-1-1 ' 的語句，例如 ItemDate \[ ' 2006-1-1 '、' 2007-1-1 ' 上的群組 \] 。</span><span class="sxs-lookup"><span data-stu-id="e209b-111">A range for System.Photo.DateTaken would include '2006-1-1' and '2007-1-1' for a statement like GROUP ON System.ItemDate \['2006-1-1', '2007-1-1'\].</span></span>

<span data-ttu-id="e209b-112">資料行規范必須是在群組 ON 或 SELECT 語句中指定的有效資料行。</span><span class="sxs-lookup"><span data-stu-id="e209b-112">The column specifier must be a valid column specified in either the GROUP ON or the SELECT statement.</span></span> <span data-ttu-id="e209b-113">您可以包含一個以上的資料行，並以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="e209b-113">You can include more than one column, separated by commas.</span></span> <span data-ttu-id="e209b-114">例如，如果您將 ISOSpeed 群組在一起，您可以先 ShutterSpeed 所有的 ISO-100 相片，然後再按 []，然後再按 []。</span><span class="sxs-lookup"><span data-stu-id="e209b-114">For example, if you group on System.Photo.ISOSpeed, you can sort all ISO-100 photos, first by System.Photo.ShutterSpeed, and then by System.Photo.Aperture.</span></span>

<span data-ttu-id="e209b-115">選擇性的方向規範可以是 ASC 的遞增 (低至高) 或 DESC （遞減 (高至低) ）。</span><span class="sxs-lookup"><span data-stu-id="e209b-115">The optional direction specifier can be either ASC for ascending (low to high) or DESC for descending (high to low).</span></span> <span data-ttu-id="e209b-116">如果您未提供方向規範，則會使用預設值 [遞增]。</span><span class="sxs-lookup"><span data-stu-id="e209b-116">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="e209b-117">如果您指定一個以上的資料行，但未指定所有方向，則您指定的最後一個方向會套用至每個連續的資料行，直到您明確變更方向為止。</span><span class="sxs-lookup"><span data-stu-id="e209b-117">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each successive column until you explicitly change the direction.</span></span>

<span data-ttu-id="e209b-118">未在 ORDER 群組 IN 子句中明確指定的範圍或值，會依 [群組依據] 資料行中的值，以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="e209b-118">Ranges or values that are not explicitly specified in an ORDER GROUP IN clause are sorted in ascending order by the values in the GROUP ON column.</span></span>

## <a name="examples"></a><span data-ttu-id="e209b-119">範例</span><span class="sxs-lookup"><span data-stu-id="e209b-119">Examples</span></span>

<span data-ttu-id="e209b-120">下列範例會依 System.object 屬性將結果分組。</span><span class="sxs-lookup"><span data-stu-id="e209b-120">The following example groups results by the System.Kind property.</span></span> <span data-ttu-id="e209b-121">此查詢會依應用程式名稱和「音樂」群組依專輯標題和曲目編號來排序「程式」群組。</span><span class="sxs-lookup"><span data-stu-id="e209b-121">The query would order the 'program' group by the application name and the 'music' group by album title and track number.</span></span> <span data-ttu-id="e209b-122">**Null** 群組將依專案名稱排序。</span><span class="sxs-lookup"><span data-stu-id="e209b-122">The **NULL** group would be ordered by the item name.</span></span> <span data-ttu-id="e209b-123">所有其他群組會依專案日期排序。</span><span class="sxs-lookup"><span data-stu-id="e209b-123">All other groups would by ordered by the item date.</span></span>


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



<span data-ttu-id="e209b-124">下列範例會依 ItemDate 屬性將結果分組，然後依專案 URL、種類或名稱來排序每個群組。</span><span class="sxs-lookup"><span data-stu-id="e209b-124">The following example groups results by the System.ItemDate property, and then sorts each group by item URL, kind, or name.</span></span>


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



<span data-ttu-id="e209b-125">上述查詢的結果會以五個群組傳回，並依下表所述進行排序。</span><span class="sxs-lookup"><span data-stu-id="e209b-125">The results of the preceding query would be returned in five groups and sorted as described in the following table.</span></span>



| <span data-ttu-id="e209b-126">群組</span><span class="sxs-lookup"><span data-stu-id="e209b-126">Group</span></span>    | <span data-ttu-id="e209b-127">描述</span><span class="sxs-lookup"><span data-stu-id="e209b-127">Description</span></span>                                               | <span data-ttu-id="e209b-128">排序依據</span><span class="sxs-lookup"><span data-stu-id="e209b-128">Sorted by</span></span>                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="e209b-129">MINVALUE</span><span class="sxs-lookup"><span data-stu-id="e209b-129">MINVALUE</span></span> | <span data-ttu-id="e209b-130">日期早于2006-1-1 的專案</span><span class="sxs-lookup"><span data-stu-id="e209b-130">Items with dates before 2006-1-1</span></span>                          | <span data-ttu-id="e209b-131">依專案的 URL 排序（以遞增順序）</span><span class="sxs-lookup"><span data-stu-id="e209b-131">Sorted by the item's URL, in ascending order</span></span> |
| <span data-ttu-id="e209b-132">2006-1-1</span><span class="sxs-lookup"><span data-stu-id="e209b-132">2006-1-1</span></span> | <span data-ttu-id="e209b-133">日期等於或晚于2006-1-1 但在2007-1-1 之前的專案</span><span class="sxs-lookup"><span data-stu-id="e209b-133">Items with dates on or after 2006-1-1 but before 2007-1-1</span></span> | <span data-ttu-id="e209b-134">依專案日期以遞增順序排序</span><span class="sxs-lookup"><span data-stu-id="e209b-134">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="e209b-135">2007-1-1</span><span class="sxs-lookup"><span data-stu-id="e209b-135">2007-1-1</span></span> | <span data-ttu-id="e209b-136">日期等於或晚于2007-1-1 但在2008-1-1 之前的專案</span><span class="sxs-lookup"><span data-stu-id="e209b-136">Items with dates on or after 2007-1-1 but before 2008-1-1</span></span> | <span data-ttu-id="e209b-137">依種類值以遞增順序排序</span><span class="sxs-lookup"><span data-stu-id="e209b-137">Sorted by kind value, in ascending order</span></span>     |
| <span data-ttu-id="e209b-138">2008-1-1</span><span class="sxs-lookup"><span data-stu-id="e209b-138">2008-1-1</span></span> | <span data-ttu-id="e209b-139">日期等於或晚于2008-1-1 的專案</span><span class="sxs-lookup"><span data-stu-id="e209b-139">Items with dates on or after 2008-1-1</span></span>                     | <span data-ttu-id="e209b-140">依專案日期以遞增順序排序</span><span class="sxs-lookup"><span data-stu-id="e209b-140">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="e209b-141">**NULL**</span><span class="sxs-lookup"><span data-stu-id="e209b-141">**NULL**</span></span> | <span data-ttu-id="e209b-142">ItemDate 資料行中沒有值的專案</span><span class="sxs-lookup"><span data-stu-id="e209b-142">Items with no value in the System.ItemDate column</span></span>         | <span data-ttu-id="e209b-143">依專案名稱以遞增順序排序</span><span class="sxs-lookup"><span data-stu-id="e209b-143">Sorted by item name, in ascending order</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="e209b-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="e209b-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e209b-145">**參考**</span><span class="sxs-lookup"><span data-stu-id="e209b-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e209b-146">分組依據 .。。OVER .。。聲明</span><span class="sxs-lookup"><span data-stu-id="e209b-146">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
</dt> <dt>

[<span data-ttu-id="e209b-147">ORDER BY 子句</span><span class="sxs-lookup"><span data-stu-id="e209b-147">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> </dl>

 

 



