---
description: 描述在 WQL WHERE 子句中支援使用的日期格式。
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported 日期格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849558"
---
# <a name="wql-supported-date-formats"></a><span data-ttu-id="efe04-103">WQL-Supported 日期格式</span><span class="sxs-lookup"><span data-stu-id="efe04-103">WQL-Supported Date Formats</span></span>

<span data-ttu-id="efe04-104">除了 WMI **DATETIME** 格式之外，還支援下列日期格式以用於 WQL **WHERE** 子句。</span><span class="sxs-lookup"><span data-stu-id="efe04-104">In addition to the WMI **DATETIME** format, the following date formats are supported for use in the WQL **WHERE** clause.</span></span>

<span data-ttu-id="efe04-105">不同地區設定的顯示時間格式不同。</span><span class="sxs-lookup"><span data-stu-id="efe04-105">The displayed time format is different for different locales.</span></span> <span data-ttu-id="efe04-106">連接至遠端電腦的腳本必須以適用于目的電腦地區設定的格式來指定時間。</span><span class="sxs-lookup"><span data-stu-id="efe04-106">Scripts that connect to remote computers must specify time in the format appropriate for the locale of the target computer.</span></span>

<span data-ttu-id="efe04-107">例如，美國日期和時間格式為 MM DD-YYYY。</span><span class="sxs-lookup"><span data-stu-id="efe04-107">For example, the United States date and time format is MM-DD-YYYY.</span></span> <span data-ttu-id="efe04-108">如果美國電腦上的腳本連接到格式為 DD-YYYY 的地區設定中的目的電腦，則查詢會在目的電腦上處理為 DD MM。</span><span class="sxs-lookup"><span data-stu-id="efe04-108">If a script on a US computer connects to a target computer in a locale where the format is DD-MM-YYYY, then queries are processed on the target computer as DD-MM-YYYY.</span></span> <span data-ttu-id="efe04-109">若要避免地區設定之間的不同結果，請使用 [**日期時間**](datetime.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="efe04-109">To avoid different results between locales, use the [**DATETIME**](datetime.md) format.</span></span> <span data-ttu-id="efe04-110">如需詳細資訊，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="efe04-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="efe04-111">格式</span><span class="sxs-lookup"><span data-stu-id="efe04-111">Format</span></span></th>
<th><span data-ttu-id="efe04-112">描述</span><span class="sxs-lookup"><span data-stu-id="efe04-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="efe04-113">週一 [th] dd [，] [yy] yy</span><span class="sxs-lookup"><span data-stu-id="efe04-113">Mon[th] dd[,] [yy]yy</span></span></td>
<td><span data-ttu-id="efe04-114">月份 (拼寫出或縮寫為三個字母) 、日、選擇性的逗號，以及兩個或四位數年份。</span><span class="sxs-lookup"><span data-stu-id="efe04-114">Month (either spelled-out or abbreviated in three letters), day, optional comma, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="efe04-115">1932年1月21日</span><span class="sxs-lookup"><span data-stu-id="efe04-115">January 21, 1932</span></span><br />
<span data-ttu-id="efe04-116">32年1月21日</span><span class="sxs-lookup"><span data-stu-id="efe04-116">January 21, 32</span></span><br />
<span data-ttu-id="efe04-117">Jan 21 1932</span><span class="sxs-lookup"><span data-stu-id="efe04-117">Jan 21 1932</span></span><br />
<span data-ttu-id="efe04-118">Jan 21 32</span><span class="sxs-lookup"><span data-stu-id="efe04-118">Jan 21 32</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-119">週一 [th] [，] yyyy</span><span class="sxs-lookup"><span data-stu-id="efe04-119">Mon[th][,] yyyy</span></span></td>
<td><span data-ttu-id="efe04-120">月份 (拼寫出或縮寫為三個字母) 、選擇性逗號和四位數年份。</span><span class="sxs-lookup"><span data-stu-id="efe04-120">Month (either spelled-out or abbreviated in three letters), optional comma, and four-digit year.</span></span><br/> <dl> <span data-ttu-id="efe04-121">1932年1月</span><span class="sxs-lookup"><span data-stu-id="efe04-121">January 1932</span></span><br />
<span data-ttu-id="efe04-122">Jan 1932</span><span class="sxs-lookup"><span data-stu-id="efe04-122">Jan 1932</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efe04-123">星期一 [th] [yy] yy dd</span><span class="sxs-lookup"><span data-stu-id="efe04-123">Mon[th] [yy]yy dd</span></span></td>
<td><span data-ttu-id="efe04-124">月份 (拼寫出或縮寫為三個字母) 、二或四位數年份和日。</span><span class="sxs-lookup"><span data-stu-id="efe04-124">Month (either spelled-out or abbreviated in three letters), two or four digit year, and day.</span></span><br/> <dl> <span data-ttu-id="efe04-125">1932 21 年1月</span><span class="sxs-lookup"><span data-stu-id="efe04-125">January 1932 21</span></span><br />
<span data-ttu-id="efe04-126">Jan 32 21</span><span class="sxs-lookup"><span data-stu-id="efe04-126">Jan 32 21</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-127">dd 週一 [th] [，] [] [yy] yy</span><span class="sxs-lookup"><span data-stu-id="efe04-127">dd Mon[th][,][ ][yy]yy</span></span></td>
<td><span data-ttu-id="efe04-128">月中的日、月 (拼寫出或縮寫為三個字母) 、選擇性的逗號、選擇性的空格，以及兩個或四位數年份。</span><span class="sxs-lookup"><span data-stu-id="efe04-128">Day of the month, month (either spelled-out or abbreviated in three letters), optional comma, optional space, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="efe04-129">1932年1月21日</span><span class="sxs-lookup"><span data-stu-id="efe04-129">21 January, 1932</span></span><br />
<span data-ttu-id="efe04-130">21 Jan32</span><span class="sxs-lookup"><span data-stu-id="efe04-130">21 Jan32</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efe04-131">dd [yy] yy 週一 [th]</span><span class="sxs-lookup"><span data-stu-id="efe04-131">dd [yy]yy Mon[th]</span></span></td>
<td><span data-ttu-id="efe04-132">月份的日期、兩位數或四位數年份，以及月份 (以三個字母) 拼寫或縮寫。</span><span class="sxs-lookup"><span data-stu-id="efe04-132">Day of the month, two or four-digit year, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="efe04-133">21 1932 年1月</span><span class="sxs-lookup"><span data-stu-id="efe04-133">21 1932 January</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-134">[yy] yy 週一 [th] dd</span><span class="sxs-lookup"><span data-stu-id="efe04-134">[yy]yy Mon[th] dd</span></span></td>
<td><span data-ttu-id="efe04-135">兩位數或四位數年份、月份 (拼出或縮寫為三個字母) 和日。</span><span class="sxs-lookup"><span data-stu-id="efe04-135">Two or four-digit year, month (either spelled-out or abbreviated in three letters), and day.</span></span><br/> <dl> <span data-ttu-id="efe04-136">1932年1月21日</span><span class="sxs-lookup"><span data-stu-id="efe04-136">1932 January 21</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efe04-137">yyyy 週一 [th]</span><span class="sxs-lookup"><span data-stu-id="efe04-137">yyyy Mon[th]</span></span></td>
<td><span data-ttu-id="efe04-138">有兩個或四位數年份和月份 (拼出或縮寫以三個字母為) 。</span><span class="sxs-lookup"><span data-stu-id="efe04-138">Two or four-digit year and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="efe04-139">1932 Jan</span><span class="sxs-lookup"><span data-stu-id="efe04-139">1932 Jan</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-140">yyyy dd 週一 [th]</span><span class="sxs-lookup"><span data-stu-id="efe04-140">yyyy dd Mon[th]</span></span></td>
<td><span data-ttu-id="efe04-141">有兩個或四位數年份、日和月 (拼出或縮寫以三個字母為) 。</span><span class="sxs-lookup"><span data-stu-id="efe04-141">Two or four-digit year, day, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="efe04-142">1932 21 年1月</span><span class="sxs-lookup"><span data-stu-id="efe04-142">1932 21 January</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efe04-143">MM {/-.}dd {/-.}[yy] yy</span><span class="sxs-lookup"><span data-stu-id="efe04-143">[M]M{/-.}dd{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="efe04-144">月、日和兩位數或四位數年份。</span><span class="sxs-lookup"><span data-stu-id="efe04-144">Month, day, and two or four-digit year.</span></span> <span data-ttu-id="efe04-145">請注意，分隔符號必須相同。</span><span class="sxs-lookup"><span data-stu-id="efe04-145">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-146">dd {/-.}MM {/-.}[yy] yy</span><span class="sxs-lookup"><span data-stu-id="efe04-146">dd{/-.}[M]M{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="efe04-147">當月、month 和二或四位數年份的日期。</span><span class="sxs-lookup"><span data-stu-id="efe04-147">Day of the month, month, and two or four-digit year.</span></span> <span data-ttu-id="efe04-148">請注意，分隔符號必須相同。</span><span class="sxs-lookup"><span data-stu-id="efe04-148">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efe04-149">MM {/-.}[yy] yy {/-.}Dd</span><span class="sxs-lookup"><span data-stu-id="efe04-149">[M]M{/-.}[yy]yy{/-.}dd</span></span></td>
<td><span data-ttu-id="efe04-150">Month、二或四位數年份和日。</span><span class="sxs-lookup"><span data-stu-id="efe04-150">Month, two or four-digit year, and day.</span></span> <span data-ttu-id="efe04-151">請注意，分隔符號必須相同。</span><span class="sxs-lookup"><span data-stu-id="efe04-151">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-152">dd {/-.}[yy] yy {/-.}MM</span><span class="sxs-lookup"><span data-stu-id="efe04-152">dd{/-.}[yy]yy{/-.}[M]M</span></span></td>
<td><span data-ttu-id="efe04-153">月份的日期、二或四位數年份和月份。</span><span class="sxs-lookup"><span data-stu-id="efe04-153">Day of the month, two or four-digit year, and month.</span></span> <span data-ttu-id="efe04-154">請注意，分隔符號必須相同。</span><span class="sxs-lookup"><span data-stu-id="efe04-154">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efe04-155">[yy] yy {/-.}dd {/-.}MM</span><span class="sxs-lookup"><span data-stu-id="efe04-155">[yy]yy{/-.}dd{/-.}[M]M</span></span></td>
<td><span data-ttu-id="efe04-156">二或四位數年份、日和月。</span><span class="sxs-lookup"><span data-stu-id="efe04-156">Two or four digit year, day, and month.</span></span> <span data-ttu-id="efe04-157">請注意，分隔符號必須相同。</span><span class="sxs-lookup"><span data-stu-id="efe04-157">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-158">[yy] yy {/-.}MM {/-.}Dd</span><span class="sxs-lookup"><span data-stu-id="efe04-158">[yy]yy{/-.}[M]M{/-.}dd</span></span></td>
<td><span data-ttu-id="efe04-159">二或四位數年份、月份和日。</span><span class="sxs-lookup"><span data-stu-id="efe04-159">Two or four digit year, month, and day.</span></span> <span data-ttu-id="efe04-160">請注意，分隔符號必須相同。</span><span class="sxs-lookup"><span data-stu-id="efe04-160">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efe04-161">[yy] yyMMdd</span><span class="sxs-lookup"><span data-stu-id="efe04-161">[yy]yyMMdd</span></span></td>
<td><span data-ttu-id="efe04-162">沒有空格的兩個或四位數年份、月份和日。</span><span class="sxs-lookup"><span data-stu-id="efe04-162">Two or four digit year, month, and day, without spaces.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efe04-163">yyyy [MM [dd]]</span><span class="sxs-lookup"><span data-stu-id="efe04-163">yyyy[MM[dd]]</span></span></td>
<td><span data-ttu-id="efe04-164">有兩個或四位數年份、選擇性月份和選用日，不含空格。</span><span class="sxs-lookup"><span data-stu-id="efe04-164">Two or four digit year, optional month, and optional day, without spaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="efe04-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="efe04-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efe04-166">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="efe04-166">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




