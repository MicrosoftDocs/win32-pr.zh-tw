---
description: 深入瞭解： JET_INDEXCREATE 屬性
title: JET_INDEXCREATE 屬性
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945091"
---
# <a name="jet_indexcreate-properties"></a><span data-ttu-id="df842-103">JET_INDEXCREATE 屬性</span><span class="sxs-lookup"><span data-stu-id="df842-103">JET_INDEXCREATE properties</span></span>

<span data-ttu-id="df842-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="df842-104">Include protected members</span></span>  
<span data-ttu-id="df842-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="df842-105">Include inherited members</span></span>  

<span data-ttu-id="df842-106">[JET_INDEXCREATE](./jet-indexcreate-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="df842-106">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="df842-107">屬性</span><span class="sxs-lookup"><span data-stu-id="df842-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="df842-108">名稱</span><span class="sxs-lookup"><span data-stu-id="df842-108">Name</span></span></th>
<th><span data-ttu-id="df842-109">描述</span><span class="sxs-lookup"><span data-stu-id="df842-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="df842-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="df842-112">取得或設定 szKey 的長度（以字元為單位），包括兩個終止的 null。</span><span class="sxs-lookup"><span data-stu-id="df842-112">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="df842-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="df842-115">取得或設定索引中索引鍵允許的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="df842-115">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="df842-116">最小支援的金鑰大小為 JET_cbKeyMostMin (255) 這是舊版的最大金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="df842-116">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="df842-117">最大索引鍵大小取決於資料庫頁面大小 <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>。</span><span class="sxs-lookup"><span data-stu-id="df842-117">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="df842-118">您可以使用 <a href="dn351156(v=exchg.10).md">KeyMost</a>抓取最大的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="df842-118">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="df842-119">Windows XP 和 Windows Server 2003 會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="df842-119">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="df842-120">不同于非受控 API，不需要 <strong>IndexKeyMost () </strong> (JET_bitIndexKeyMost) ，它會自動加入。</span><span class="sxs-lookup"><span data-stu-id="df842-120">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="df842-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="df842-123">取得或設定要儲存在索引中之每個資料行的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="df842-123">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="df842-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="df842-126">取得或設定條件式資料行的數目。</span><span class="sxs-lookup"><span data-stu-id="df842-126">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-128"><a href="dn335157(v=exchg.10).md">犯 錯</a></span><span class="sxs-lookup"><span data-stu-id="df842-128"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="df842-129">取得或設定建立此索引的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="df842-129">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-131"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="df842-131"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="df842-132">取得或設定索引建立選項。</span><span class="sxs-lookup"><span data-stu-id="df842-132">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="df842-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="df842-135">取得或設定選擇性的 unicode 比較選項。</span><span class="sxs-lookup"><span data-stu-id="df842-135">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="df842-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="df842-138">取得或設定空間配置、維護和使用方式提示。</span><span class="sxs-lookup"><span data-stu-id="df842-138">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="df842-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="df842-141">取得或設定選擇性的條件式資料行。</span><span class="sxs-lookup"><span data-stu-id="df842-141">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="df842-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="df842-144">取得或設定要建立之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="df842-144">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-146"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="df842-146"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="df842-147">取得或設定索引鍵的描述。</span><span class="sxs-lookup"><span data-stu-id="df842-147">Gets or sets the description of the index key.</span></span> <span data-ttu-id="df842-148">這是以 null 分隔之標記的雙 null 結束字串。</span><span class="sxs-lookup"><span data-stu-id="df842-148">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="df842-149">每個標記的格式都是 [方向規範] [資料行名稱]，其中的方向規格為 &quot; + &quot; 或 &quot; - &quot; 。</span><span class="sxs-lookup"><span data-stu-id="df842-149">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="df842-150">例如， &quot; + abc\0-def\0 + ghi\0 的 szKey 會以 &quot; 遞增順序)  (的三個數據行來編制索引 &quot; &quot; ， &quot; &quot; 而 def (以遞減順序) 和 &quot; ghi &quot; (遞增順序) 。</span><span class="sxs-lookup"><span data-stu-id="df842-150">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="df842-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="df842-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="df842-153">取得或設定索引的密度。</span><span class="sxs-lookup"><span data-stu-id="df842-153">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="df842-154">頁首</span><span class="sxs-lookup"><span data-stu-id="df842-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="df842-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df842-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="df842-156">參考</span><span class="sxs-lookup"><span data-stu-id="df842-156">Reference</span></span>

[<span data-ttu-id="df842-157">JET_INDEXCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="df842-157">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="df842-158">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="df842-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
