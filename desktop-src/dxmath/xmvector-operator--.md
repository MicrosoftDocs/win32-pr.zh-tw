---
description: 減法和負運算子。
ms.assetid: b3a3da02-4fba-4f76-90d8-15f605c73f16
title: operator-運算子
ms.topic: reference
ms.date: 12/06/2018
ms.openlocfilehash: 21c10490db92a335f07f298876d838f2152d17b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512673"
---
# <a name="operator---operators"></a><span data-ttu-id="a251a-103">operator-運算子</span><span class="sxs-lookup"><span data-stu-id="a251a-103">operator - operators</span></span>

<span data-ttu-id="a251a-104">減法和負運算子</span><span class="sxs-lookup"><span data-stu-id="a251a-104">Subtraction and negation operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="a251a-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="a251a-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a251a-106">運算子</span><span class="sxs-lookup"><span data-stu-id="a251a-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a251a-107">描述</span><span class="sxs-lookup"><span data-stu-id="a251a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a251a-108"><a href="/previous-versions/windows/desktop/legacy/ee421383(v=vs.85)"><strong>XMVECTOR：： operator- (XMVECTOR) </strong></a></span><span class="sxs-lookup"><span data-stu-id="a251a-108"><a href="/previous-versions/windows/desktop/legacy/ee421383(v=vs.85)"><strong>XMVECTOR::operator - (XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a251a-109">計算實例的否定 <code>XMVECTOR</code> 。</span><span class="sxs-lookup"><span data-stu-id="a251a-109">Computes the negation of an <code>XMVECTOR</code> instance.</span></span><br/> <span data-ttu-id="a251a-110"><code>operator -</code>會採用<a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a>的實例，並傳回的新實例 <code>XMVECTOR</code> ，每個元件都是否定的。</span><span class="sxs-lookup"><span data-stu-id="a251a-110">The <code>operator -</code> takes an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> and returns a new instance of <code>XMVECTOR</code>, with each component negated.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a251a-111">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="a251a-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a251a-112"><a href="/previous-versions/windows/desktop/legacy/ee421385(v=vs.85)"><strong>XMVECTOR：： operator- (XMVECTOR、XMVECTOR) </strong></a></span><span class="sxs-lookup"><span data-stu-id="a251a-112"><a href="/previous-versions/windows/desktop/legacy/ee421385(v=vs.85)"><strong>XMVECTOR::operator - (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a251a-113"><code>XMVECTOR</code>從第二個實例減去一個的實例，並在新的實例中傳回結果 <code>XMVECTOR</code> 。</span><span class="sxs-lookup"><span data-stu-id="a251a-113">Subtracts one instance of <code>XMVECTOR</code> from a second instance, returning the result in a new instance of <code>XMVECTOR</code>.</span></span> <br/> <span data-ttu-id="a251a-114">會 <code>operator -</code> 從另一個實例的每個元件減去 <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之實例的每個元件，並傳回 <code>XMVECTOR</code> <code>XMVECTOR</code> 包含結果的新實例。</span><span class="sxs-lookup"><span data-stu-id="a251a-114">The <code>operator -</code> subtracts each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> from each component of another instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a251a-115">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="a251a-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="a251a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a251a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a251a-117">XMVECTOR 運算子</span><span class="sxs-lookup"><span data-stu-id="a251a-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="a251a-118">**參考**</span><span class="sxs-lookup"><span data-stu-id="a251a-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a251a-119">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="a251a-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
