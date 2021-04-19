---
description: DirectXMath 程式庫提供下列常數。
ms.assetid: a206fe22-12c8-ac2b-ee37-20cfff35841a
title: DirectXMath 程式庫常數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4809c72fbd5cec27b549be29ebced81839c89723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974359"
---
# <a name="directxmath-library-constants"></a>DirectXMath 程式庫常數

DirectXMath 程式庫提供下列常數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DIRECTXMATH_VERSION<br/></td>
<td>DirectXMath 程式庫的版本。 初始預覽版本為300，Windows 8 最終版本為303，Windows 8.1 版本為305。 硬碟版數學的版本是200、201、202、203、204等等。 這會定義為預處理器符號。<br/></td>
</tr>
<tr class="even">
<td>XM_PI<br/></td>
<td>Π的最佳標記法。<br/></td>
</tr>
<tr class="odd">
<td>XM_2PI<br/></td>
<td>雙 * π的最佳標記法。<br/></td>
</tr>
<tr class="even">
<td>XM_1DIVPI<br/></td>
<td>1/π的最佳標記法。<br/></td>
</tr>
<tr class="odd">
<td>XM_1DIV2PI<br/></td>
<td>雙/π的最佳標記法。<br/></td>
</tr>
<tr class="even">
<td>XM_PIDIV2<br/></td>
<td>Π/2 的最佳標記法。<br/></td>
</tr>
<tr class="odd">
<td>XM_PIDIV4<br/></td>
<td>Π/4 的最佳標記法。<br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_0X<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 的第一個向量引數的 X 元件，會複製到結果向量中對應至指定專案的索引位置。 <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_0Y<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 的第一個向量引數的 Y 元件，會複製到結果向量中對應至指定專案的索引位置。 <br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_0Z<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 的第一個向量引數的 Z 元件，會複製到結果向量中對應于指定專案的索引位置。 <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_0W<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 的第一個向量引數的 W 元件，會複製到結果向量中對應至指定專案的索引位置。 <br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_1X<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 的第二個向量引數的 X 元件，會複製到結果向量中對應至指定專案的索引位置。 <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_1Y<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 之向量引數的第二個 Y 元件，會複製到結果向量中對應于指定專案的索引位置。 <br/></td>
</tr>
<tr class="even">
<td>XM_PERMUTE_1Z<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 之向量引數的第二個 Z 元件，會複製到結果向量中對應于指定專案的索引位置。 <br/></td>
</tr>
<tr class="odd">
<td>XM_PERMUTE_1W<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute"><strong>XMVectorPermute</strong></a>做為元素索引的常數。 這表示要 <strong>XMVectorPermute</strong> 之向量引數第二個的 W 元件，會複製到結果向量中對應于指定專案的索引位置。 <br/></td>
</tr>
<tr class="even">
<td>XM_SELECT_0<br/></td>
<td>常數，用來建立與 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect"><strong>XMVectorSelect</strong></a>搭配使用的控制向量。 表示要將 <strong>XMVectorSelect</strong> 的第一個向量引數的元件複製到結果向量中的索引位置，其對應至其在控制向量中的索引。<br/> 例如，以 XM_SELECT_0 做為第二個元件的控制向量，會將第一個向量的第二個元件複製到結果向量的第二個元件。 <br/></td>
</tr>
<tr class="odd">
<td>XM_SELECT_1<br/></td>
<td>常數，用來建立與 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect"><strong>XMVectorSelect</strong></a>搭配使用的控制向量。 表示要將 <strong>XMVectorSelect</strong> 之向量引數的第二個元件複製到結果向量中的索引位置，其對應至其在控制向量中的索引。 <br/> 例如，以 XM_SELECT_1 做為第二個元件的控制向量，會將第二個向量的第二個元件複製到結果向量的第二個元件。 <br/></td>
</tr>
<tr class="even">
<td>XM_SWIZZLE_X<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle</strong></a>做為元素索引的常數。 這表示要將 <strong>XMVectorSwizzle</strong> 的向量引數 X 元件複製到對應至指定專案的結果向量中的索引位置。<br/></td>
</tr>
<tr class="odd">
<td>XM_SWIZZLE_Y<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle</strong></a>做為元素索引的常數。 這表示將 <strong>XMVectorSwizzle</strong> 向量引數的 Y 元件複製到對應至指定專案的結果向量中的索引位置。 <br/></td>
</tr>
<tr class="even">
<td>XM_SWIZZLE_Z<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle</strong></a>做為元素索引的常數。 這表示將 <strong>XMVectorSwizzle</strong> 向量引數的 Z 元件複製到對應至指定專案的結果向量中的索引位置。 <br/></td>
</tr>
<tr class="odd">
<td>XM_SWIZZLE_W<br/></td>
<td>使用 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorswizzle"><strong>XMVectorSwizzle</strong></a>做為元素索引的常數。 這表示要將 <strong>XMVectorSwizzle</strong> 向量引數的 W 元件複製到對應至指定專案的結果向量中的索引位置。 <br/></td>
</tr>
<tr class="even">
<td>XM_CRMASK_CR6<br/></td>
<td>遮罩以取得比較結果，通常是使用 DirectXMath 函式（例如 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>XMVector4EqualR</strong></a>）的記錄版本來抓取。 下列範例會從變數 CR 取得比較結果：
<pre class="syntax" data-space="preserve"><code>uint32_t val = ((CR) & XM_CRMASK_CR6);</code></pre>
<br/></td>
</tr>
<tr class="odd">
<td>XM_CRMASK_CR6TRUE<br/></td>
<td>遮罩以取得比較結果，並確認它是否為邏輯 true。 通常會使用 DirectXMath 函式的記錄版本（例如 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>XMVector4EqualR</strong></a>）來抓取此值。 此範例會檢查 variableq CR 是否為 true：
<pre class="syntax" data-space="preserve"><code>bool val = (((CR) & XM_CRMASK_CR6FALSE) == XM_CRMASK_CR6FALSE);</code></pre>
另請參閱 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonanytrue"><strong>XMComparisonAnyTrue</strong></a>、 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonalltrue"><strong>XMComparisonAllTrue</strong></a>和 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonmixed"><strong>XMComparisonMixed</strong></a><br/></td>
</tr>
<tr class="even">
<td>XM_CRMASK_CR6FALSE<br/></td>
<td>遮罩以取得比較結果，並確認它是否為邏輯 false。 通常會使用 DirectXMath 數學函式的錄製版本（例如 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>XMVector4EqualR</strong></a>）來抓取此值。 此範例會檢查變數 CR 是否為 false：
<pre class="syntax" data-space="preserve"><code>bool val = (((CR) & XM_CRMASK_CR6FALSE) == XM_CRMASK_CR6FALSE);</code></pre>
另請參閱 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonanyfalse"><strong>XMComparisonAnyFalse</strong></a>、 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonallfalse"><strong>XMComparisonAllFalse</strong></a> 和 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonmixed"><strong>XMComparisonMixed</strong></a><br/></td>
</tr>
<tr class="odd">
<td>XM_CRMASK_CR6BOUNDS<br/></td>
<td>遮罩以取得比較結果，並確認結果是否指出部分輸入超出範圍。 通常會使用 DirectXMath 函式的記錄版本（例如 <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr"><strong>XMVector4EqualR</strong></a>）來抓取此值。 此範例會檢查變數 CR 是否指出和超出範圍狀態。
<pre class="syntax" data-space="preserve"><code>bool val = (((CR) & XM_CRMASK_CR6BOUNDS) == XM_CRMASK_CR6BOUNDS);</code></pre>
另請參閱 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonallinbounds"><strong>XMComparisonAllInBounds</strong></a> 和 <a href="/windows/desktop/api/DirectXMath/nf-directxmath-xmcomparisonanyoutofbounds"><strong>XMComparisonAnyOutOfBounds</strong></a><br/></td>
</tr>
<tr class="even">
<td>色彩：： AliceBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： AntiqueWhite</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：淺綠色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：青綠色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： Azure</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：米色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：淡黃</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：黑色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： BlanchedAlmond</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Blue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：藍紫</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：棕色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： BurlyWood</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： CadetBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： Chartreuse</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：巧克力</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：珊瑚</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： [Cornflowerblue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： Cornsilk</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Crimson</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：青色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkCyan</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkGoldenrod</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkGray</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkKhaki</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkMagenta</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkOliveGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkOrange</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkOrchid</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkRed</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkSalmon</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkSeaGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkSlateBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkSlateGray</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D arkTurquoise</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D arkViolet</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D eepPink</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D eepSkyBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:D imGray</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:D odgerBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： Firebrick</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： FloralWhite</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： ForestGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Fuchsia</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： Gainsboro</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： GhostWhite</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：金級</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：金黃</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：灰色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：綠色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： >greenyellow</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Honeydew</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： HotPink</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： IndianRed</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：靛藍色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：象牙海岸</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：卡其色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：紫色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LavenderBlush</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LawnGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LemonChiffon</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LightBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LightCoral</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LightCyan</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LightGoldenrodYellow</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LightGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LightGray</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LightPink</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LightSalmon</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LightSeaGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LightSkyBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LightSlateGray</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： LightSteelBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： LightYellow</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：橙色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：暗綠</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： Linen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：洋紅</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：褐紅色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： MediumAquamarine</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： MediumBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： MediumOrchid</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： MediumPurple</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： MediumSeaGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： MediumSlateBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： MediumSpringGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： MediumTurquoise</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： MediumVioletRed</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： MidnightBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： MintCream</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： MistyRose</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Moccasin</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： NavajoWhite</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Navy</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： OldLace</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：橄欖色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： OliveDrab</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：橙色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： OrangeRed</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：蘭花</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:P aleGoldenrod</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:P aleGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:P aleTurquoise</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:P aleVioletRed</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:P apayaWhip</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:P eachPuff</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:P eru</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:P 筆墨</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:P 的亮度</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：:P owderBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：:P urple</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Red</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： RosyBrown</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： RoyalBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： SaddleBrown</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：橙紅</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： SandyBrown</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： SeaGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：貝殼</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Sienna</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：銀</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： SkyBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： SlateBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：青灰</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：雪</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： SpringGreen</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： SteelBlue</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Tan</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：青色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：： Thistle</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：蕃茄紅</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：透明</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：青</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：紫羅蘭</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：： Wheat</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：白色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：白霧色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="odd">
<td>色彩：：黃色</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
<tr class="even">
<td>色彩：：黃綠</td>
<td>標準 .NET 色彩定義的常數。 這些值是 R、G、B 資料，可用來做為 XMVECTOR，或直接傳遞給 Direct3D 10. x/Direct3D 11 API 的 Clear 方法。</td>
</tr>
</tbody>
</table>



 

> [!Note]
>
> 所有色彩常數都定義于標準 [sRGB](https://en.wikipedia.org/wiki/SRGB) 色彩空間 (如 .net 色彩和 HTML web 安全色彩) 。 若要使用線性色彩空間進行 gamma 正確轉譯，必須稍微調整這些值。

 

## <a name="related-topics"></a>[相關主題]

<dl> <dt>

<span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath 程式設計參考](ovw-xnamath-reference.md)
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計參考](ovw-xnamath-reference.md)
</dt> </dl>

 

 
