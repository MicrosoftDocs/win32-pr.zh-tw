---
description: 乘法運算子。
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: operator * 運算子
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114465"
---
# <a name="operator--operators"></a><span data-ttu-id="30126-103">運算子 \* 運算子</span><span class="sxs-lookup"><span data-stu-id="30126-103">operator \* operators</span></span>

<span data-ttu-id="30126-104">乘法運算子</span><span class="sxs-lookup"><span data-stu-id="30126-104">Multiplication operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="30126-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="30126-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="30126-106">運算子</span><span class="sxs-lookup"><span data-stu-id="30126-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="30126-107">描述</span><span class="sxs-lookup"><span data-stu-id="30126-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="30126-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR：： operator \* (float，XMVECTOR) </strong></a></span><span class="sxs-lookup"><span data-stu-id="30126-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator \* (float,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="30126-109">將浮點值乘以的實例，並傳回 <code>XMVECTOR</code> 新實例的結果 <code>XMVECTOR</code> 。</span><span class="sxs-lookup"><span data-stu-id="30126-109">Multiply a floating point value by an instance of <code>XMVECTOR</code>, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="30126-110">會將 <code>operator \*</code> 浮點值乘以 <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a>之實例的每個元件，以傳回 <code>XMVECTOR</code> 其元件包含結果的新實例。</span><span class="sxs-lookup"><span data-stu-id="30126-110">The <code>operator \*</code> multiplies a floating point value against each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a>, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="30126-111">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="30126-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="30126-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR：： operator \* (XMVECTOR，float) </strong></a></span><span class="sxs-lookup"><span data-stu-id="30126-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="30126-113">將實例乘以 <code>XMVECTOR</code> 浮點數，並傳回新實例的結果 <code>XMVECTOR</code> 。</span><span class="sxs-lookup"><span data-stu-id="30126-113">Multiply an instance of <code>XMVECTOR</code> by a floating point value, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="30126-114">會以 <code>operator \*</code> 浮點值乘以 <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之實例的每個元件，以傳回 <code>XMVECTOR</code> 其元件包含結果的新實例。</span><span class="sxs-lookup"><span data-stu-id="30126-114">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a floating point value, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="30126-115">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="30126-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="30126-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR：： operator \* (XMVECTOR，XMVECTOR) </strong></a></span><span class="sxs-lookup"><span data-stu-id="30126-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="30126-117">將一個實例乘以 <code>XMVECTOR</code> 第二個實例，並在第三個實例中傳回結果。</span><span class="sxs-lookup"><span data-stu-id="30126-117">Multiplies one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.</span></span> <br/> <span data-ttu-id="30126-118">會將 <code>operator \*</code> <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之實例的每個元件乘以第二個實例中的對應元件 <code>XMVECTOR</code> ，並傳回包含結果的新 <code>XMVECTOR</code> 實例。</span><span class="sxs-lookup"><span data-stu-id="30126-118">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="30126-119">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="30126-119">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="30126-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30126-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30126-121">XMVECTOR 運算子</span><span class="sxs-lookup"><span data-stu-id="30126-121">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="30126-122">**參考**</span><span class="sxs-lookup"><span data-stu-id="30126-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30126-123">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="30126-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
