---
description: 深入瞭解： JET_COLTYP
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851948"
---
# <a name="jet_coltyp"></a><span data-ttu-id="7aa0c-103">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="7aa0c-103">JET_COLTYP</span></span>


<span data-ttu-id="7aa0c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7aa0c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_coltyp"></a><span data-ttu-id="7aa0c-105">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="7aa0c-105">JET_COLTYP</span></span>

<span data-ttu-id="7aa0c-106">**JET_COLTYP** 的常數群組描述可在資料表中找到的所有可能資料行類型。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-106">The **JET_COLTYP** group of constants describe all possible column types that can be found in a table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7aa0c-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="7aa0c-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="7aa0c-108">Description</span><span class="sxs-lookup"><span data-stu-id="7aa0c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-109">JET_coltypNil</span><span class="sxs-lookup"><span data-stu-id="7aa0c-109">JET_coltypNil</span></span><br />
<span data-ttu-id="7aa0c-110">0</span><span class="sxs-lookup"><span data-stu-id="7aa0c-110">0</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-111">不正確資料行類型。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-111">An invalid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-112">JET_coltypBit</span><span class="sxs-lookup"><span data-stu-id="7aa0c-112">JET_coltypBit</span></span><br />
<span data-ttu-id="7aa0c-113">1</span><span class="sxs-lookup"><span data-stu-id="7aa0c-113">1</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-114">允許三個值的資料行類型： <strong>True</strong>、 <strong>False</strong>或 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-114">A column type that allows three values: <strong>True</strong>, <strong>False</strong>, or <strong>NULL</strong>.</span></span> <span data-ttu-id="7aa0c-115">這種類型的資料行是長度的一個位元組，而且是固定的大小。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-115">This type of column is one byte in length and is a fixed size.</span></span> <span data-ttu-id="7aa0c-116"><strong>False</strong> 會在 <strong>True</strong>之前排序。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-116"><strong>False</strong> sorts before <strong>True</strong>.</span></span> <span data-ttu-id="7aa0c-117">請注意，這個類型的大小不符合 variant 布林值類型的大小。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-117">Note that the size of this type does not match the size of the variant Boolean type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-118">JET_coltypUnsignedByte</span><span class="sxs-lookup"><span data-stu-id="7aa0c-118">JET_coltypUnsignedByte</span></span><br />
<span data-ttu-id="7aa0c-119">2</span><span class="sxs-lookup"><span data-stu-id="7aa0c-119">2</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-120">1位元組不帶正負號的整數，可採用 0 (零) 和255之間的值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-120">A 1-byte unsigned integer that can take on values between 0 (zero) and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-121">JET_coltypShort</span><span class="sxs-lookup"><span data-stu-id="7aa0c-121">JET_coltypShort</span></span><br />
<span data-ttu-id="7aa0c-122">3</span><span class="sxs-lookup"><span data-stu-id="7aa0c-122">3</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-123">2位元組帶正負號的整數，可採用-32768 和32767之間的值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-123">A 2-byte signed integer that can take on values between -32768 and 32767.</span></span> <span data-ttu-id="7aa0c-124">負數值會在正值之前排序。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-124">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-125">JET_coltypLong</span><span class="sxs-lookup"><span data-stu-id="7aa0c-125">JET_coltypLong</span></span><br />
<span data-ttu-id="7aa0c-126">4</span><span class="sxs-lookup"><span data-stu-id="7aa0c-126">4</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-127">4位元組帶正負號的整數，可採用-2147483648 和2147483647之間的值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-127">A 4-byte signed integer that can take on values between - 2147483648 and 2147483647.</span></span> <span data-ttu-id="7aa0c-128">負數值會在正值之前排序。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-128">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-129">JET_coltypCurrency</span><span class="sxs-lookup"><span data-stu-id="7aa0c-129">JET_coltypCurrency</span></span><br />
<span data-ttu-id="7aa0c-130">5</span><span class="sxs-lookup"><span data-stu-id="7aa0c-130">5</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-131">8位元組帶正負號的整數，可採用-9223372036854775808 和9223372036854775807之間的值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-131">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="7aa0c-132">負數值會在正值之前排序。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-132">Negative values sort before positive values.</span></span> <span data-ttu-id="7aa0c-133">此資料行類型與 variant 貨幣類型相同。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-133">This column type is identical to the variant currency type.</span></span> <span data-ttu-id="7aa0c-134">此資料行類型也可以用來當做原生8位元組帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-134">This column type can also be used as a native 8-byte signed integer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-135">JET_coltypIEEESingle</span><span class="sxs-lookup"><span data-stu-id="7aa0c-135">JET_coltypIEEESingle</span></span><br />
<span data-ttu-id="7aa0c-136">6</span><span class="sxs-lookup"><span data-stu-id="7aa0c-136">6</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-137">單精確度 (4 位元組) 浮點數。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-137">A single-precision (4-byte) floating point number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-138">JET_coltypIEEEDouble</span><span class="sxs-lookup"><span data-stu-id="7aa0c-138">JET_coltypIEEEDouble</span></span><br />
<span data-ttu-id="7aa0c-139">7</span><span class="sxs-lookup"><span data-stu-id="7aa0c-139">7</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-140">雙精確度 (8 位元組的) 浮點數。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-140">A double-precision (8-byte) floating point number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-141">JET_coltypDateTime</span><span class="sxs-lookup"><span data-stu-id="7aa0c-141">JET_coltypDateTime</span></span><br />
<span data-ttu-id="7aa0c-142">8</span><span class="sxs-lookup"><span data-stu-id="7aa0c-142">8</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-143">雙精確度 (8 位元組) 浮點數，表示自1900年起算的日期（以小數天為單位）。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-143">A double-precision (8-byte) floating point number that represents a date in fractional days since the year 1900.</span></span> <span data-ttu-id="7aa0c-144">此資料行類型與 variant 日期類型相同。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-144">This column type is identical to the variant date type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-145">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="7aa0c-145">JET_coltypBinary</span></span><br />
<span data-ttu-id="7aa0c-146">9</span><span class="sxs-lookup"><span data-stu-id="7aa0c-146">9</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-147">固定或可變長度的原始二進位資料行，長度最多可達255個位元組。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-147">A fixed or variable length, raw binary column that can be up to 255 bytes in length.</span></span></p>
<p><span data-ttu-id="7aa0c-148">如果設定為固定長度的16位元組二進位資料行，此資料行類型可以用來執行 GUID。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-148">This column type can be used to implement a GUID if configured as a fixed length, 16-byte binary column.</span></span> <span data-ttu-id="7aa0c-149">唯一要注意的是，在這類資料行的索引中，值的相對順序，不會比對 GUID (之標準登錄字串轉譯的相對順序，也就是 &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-149">The only caveat is that the relative ordering of values in an index over such a column will not match the relative ordering of the standard registry-string rendering of a GUID (that is &quot;{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-150">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="7aa0c-150">JET_coltypText</span></span><br />
<span data-ttu-id="7aa0c-151">10</span><span class="sxs-lookup"><span data-stu-id="7aa0c-151">10</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-152">固定或可變長度的文字資料行，長度最多可達255個 ASCII 字元或127個 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-152">A fixed or variable length text column that can be up to 255 ASCII characters in length or 127 Unicode characters in length.</span></span></p>
<p><span data-ttu-id="7aa0c-153">所有字串都會儲存為計數的字元數。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-153">All strings are stored as a counted number of characters.</span></span> <span data-ttu-id="7aa0c-154">字串不需要是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-154">The strings need not be null terminated.</span></span> <span data-ttu-id="7aa0c-155">此外，count 不需要包含 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-155">Further, it is not necessary for the count to include a null terminator.</span></span> <span data-ttu-id="7aa0c-156">最後，可以儲存內嵌的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-156">Finally, embedded null characters can be stored.</span></span></p>
<p><span data-ttu-id="7aa0c-157">針對排序和搜尋用途，系統一律會將 ASCII 字串視為不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-157">ASCII strings are always treated as case insensitive for sorting and searching purposes.</span></span> <span data-ttu-id="7aa0c-158">此外，如果有任何) 被視為排序和搜尋，則只有第一個 null 字元前面的字元 (。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-158">Further, only the characters preceding the first null character (if any) are considered for sorting and searching.</span></span></p>
<p><span data-ttu-id="7aa0c-159">Unicode 字串會使用 WIN32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> 來建立排序索引鍵，之後用來排序和搜尋該資料。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-159">Unicode strings use the Win32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> to create sort keys that are subsequently used for sorting and searching that data.</span></span> <span data-ttu-id="7aa0c-160">根據預設，Unicode 字串會被視為美國英文地區設定，並使用下列正規化旗標進行排序和搜尋： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-160">By default, Unicode strings are considered to be in the U.S. English locale and are sorted and searched using the following normalization flags: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="7aa0c-161">在 Windows 2000 中，您可以自訂每個索引的這些旗標，以同時包含 NORM_IGNORENONSPACE。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-161">In Windows 2000, it is possible to customize these flags per index to also include NORM_IGNORENONSPACE.</span></span> <span data-ttu-id="7aa0c-162">在 Windows XP 和更新版本中，每個索引都可以要求下列正規化旗標的任意組合： LCMAP_SORTKEY、LCMAP_BYTEREV、NORM_IGNORECASE、NORM_IGNORENONSPACE、NORM_IGNORESYMBOLS、NORM_IGNOREKANATYPE、NORM_IGNOREWIDTH 和 SORT_STRINGSORT。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-162">In Windows XP and later releases, it is possible to request any combination of the following normalization flags per index: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH, and SORT_STRINGSORT.</span></span></p>
<p><span data-ttu-id="7aa0c-163">在所有版本中，都可以自訂每個索引的地區設定。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-163">In all releases, it is possible to customize the locale per index.</span></span> <span data-ttu-id="7aa0c-164">只要電腦上已安裝適當的語言套件，即可使用任何地區設定。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-164">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="7aa0c-165">最後，會完全忽略在 Unicode 字串中遇到的任何 null 字元。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-165">Finally, any null characters encountered in a Unicode string are completely ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-166">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="7aa0c-166">JET_coltypLongBinary</span></span><br />
<span data-ttu-id="7aa0c-167">11</span><span class="sxs-lookup"><span data-stu-id="7aa0c-167">11</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-168">固定或可變長度的原始二進位資料行，長度最多可達2147483647個位元組。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-168">A fixed or variable length, raw binary column that can be up to 2147483647 bytes in length.</span></span> <span data-ttu-id="7aa0c-169">此類型被視為 Long 值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-169">This type is considered to be a Long Value.</span></span> <span data-ttu-id="7aa0c-170">Long 值是特殊值，因為它可能很大，而且可以存取為數據流。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-170">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="7aa0c-171">此類型也與 JET_coltypBinary 相同。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-171">This type is otherwise identical to JET_coltypBinary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-172">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="7aa0c-172">JET_coltypLongText</span></span><br />
<span data-ttu-id="7aa0c-173">12</span><span class="sxs-lookup"><span data-stu-id="7aa0c-173">12</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-174">固定或可變長度的文字資料行，長度最多可達2147483647個 ASCII 字元或1073741823個 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-174">A fixed or variable length, text column that can be up to 2147483647 ASCII characters in length or 1073741823 Unicode characters in length.</span></span> <span data-ttu-id="7aa0c-175">此類型被視為 Long 值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-175">This type is considered to be a Long Value.</span></span> <span data-ttu-id="7aa0c-176">Long 值是特殊值，因為它可能很大，而且可以存取為數據流。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-176">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="7aa0c-177">此類型也與 JET_coltypText 相同。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-177">This type is otherwise identical to JET_coltypText.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-178">JET_coltypSLV</span><span class="sxs-lookup"><span data-stu-id="7aa0c-178">JET_coltypSLV</span></span><br />
<span data-ttu-id="7aa0c-179">13</span><span class="sxs-lookup"><span data-stu-id="7aa0c-179">13</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-180">此資料行類型已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-180">This column type is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-181">JET_coltypUnsignedLong</span><span class="sxs-lookup"><span data-stu-id="7aa0c-181">JET_coltypUnsignedLong</span></span><br />
<span data-ttu-id="7aa0c-182">14</span><span class="sxs-lookup"><span data-stu-id="7aa0c-182">14</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-183">4位元組不帶正負號的整數，可採用 0 (零) 和4294967295之間的值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-183">A 4-byte unsigned integer that can take on values between 0 (zero) and 4294967295.</span></span></p>
<p><span data-ttu-id="7aa0c-184"><strong>Windows Vista 和 Windows Server 2008：</strong>  Windows Vista、Windows Server 2008 及更新版本支援此資料行類型。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-184"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-185">JET_coltypLongLong</span><span class="sxs-lookup"><span data-stu-id="7aa0c-185">JET_coltypLongLong</span></span><br />
<span data-ttu-id="7aa0c-186">15</span><span class="sxs-lookup"><span data-stu-id="7aa0c-186">15</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-187">8位元組帶正負號的整數，可採用-9223372036854775808 和9223372036854775807之間的值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-187">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="7aa0c-188">負數值會在正值之前排序。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-188">Negative values sort before positive values.</span></span></p>
<p><span data-ttu-id="7aa0c-189"><strong>Windows Vista 和 Windows Server 2008：</strong>  Windows Vista、Windows Server 2008 及更新版本支援此資料行類型。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-189"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-190">JET_coltypGUID</span><span class="sxs-lookup"><span data-stu-id="7aa0c-190">JET_coltypGUID</span></span><br />
<span data-ttu-id="7aa0c-191">16</span><span class="sxs-lookup"><span data-stu-id="7aa0c-191">16</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-192">固定長度16位元組的二進位資料行，原生表示 GUID 資料類型。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-192">A fixed length 16 byte binary column that natively represents the GUID data type.</span></span> <span data-ttu-id="7aa0c-193">GUID 資料行值的排序方式與在標準格式 (（例如 {4999b5c0-7657-42d9-bdc1-4b779784e013} ) ）中，這些值會以字串排序。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-193">GUID column values sort in the same way that those values would sort as strings when in standard form (i.e. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span></span></p>
<p><span data-ttu-id="7aa0c-194"><strong>Windows Vista 和 Windows Server 2008：</strong>  Windows Vista、Windows Server 2008 及更新版本支援此資料行類型。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-194"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-195">JET_coltypUnsignedShort</span><span class="sxs-lookup"><span data-stu-id="7aa0c-195">JET_coltypUnsignedShort</span></span><br />
<span data-ttu-id="7aa0c-196">17</span><span class="sxs-lookup"><span data-stu-id="7aa0c-196">17</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-197">2位元組不帶正負號的整數，可採用0到65535之間的值。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-197">A 2-byte unsigned integer that can take on values between 0 and 65535.</span></span></p>
<p><span data-ttu-id="7aa0c-198"><strong>Windows Vista 和 Windows Server 2008：</strong>  Windows Vista、Windows Server 2008 及更新版本支援此資料行類型。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-198"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-199">JET_coltypMax</span><span class="sxs-lookup"><span data-stu-id="7aa0c-199">JET_coltypMax</span></span><br />
<span data-ttu-id="7aa0c-200">18</span><span class="sxs-lookup"><span data-stu-id="7aa0c-200">18</span></span></p></td>
<td><p><span data-ttu-id="7aa0c-201">常數，描述最大 (，也就是引擎所支援的最大有效) 資料行類型之一。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-201">A constant describing the maximum (that is, one beyond the largest valid) column type supported by the engine.</span></span></p>
<p><span data-ttu-id="7aa0c-202">此值應謹慎使用，因為它會隨著支援新的資料行類型而變更。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-202">This value should be used with care because it will change as new column types are supported.</span></span> <span data-ttu-id="7aa0c-203">例如，它在 Windows 2000 上的常值與在 Windows XP 和更新版本上的值不同。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-203">For example, it has a different literal value on Windows 2000 than it does on Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="7aa0c-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="7aa0c-204">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-205"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0c-205"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7aa0c-206">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-206">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aa0c-207"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0c-207"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7aa0c-208">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-208">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aa0c-209"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0c-209"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7aa0c-210">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="7aa0c-210">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7aa0c-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7aa0c-211">See Also</span></span>

[<span data-ttu-id="7aa0c-212">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="7aa0c-212">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="7aa0c-213">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="7aa0c-213">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)
