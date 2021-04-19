---
description: 乘法指派運算子。
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: operator * = 運算子
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 486e85ae8f541c802e50c38d29cd16beb746b587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969251"
---
# <a name="operator--operators"></a><span data-ttu-id="65a5a-103">operator \* = 運算子</span><span class="sxs-lookup"><span data-stu-id="65a5a-103">operator \*= operators</span></span>

<span data-ttu-id="65a5a-104">乘法指派運算子</span><span class="sxs-lookup"><span data-stu-id="65a5a-104">Multiplication assignment operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="65a5a-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="65a5a-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="65a5a-106">運算子</span><span class="sxs-lookup"><span data-stu-id="65a5a-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="65a5a-107">描述</span><span class="sxs-lookup"><span data-stu-id="65a5a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="65a5a-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR：： operator \* = (XMVECTOR&，float) </strong></a></span><span class="sxs-lookup"><span data-stu-id="65a5a-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="65a5a-109">將 <code>XMVECTOR</code> 實例乘以浮點值，並傳回更新的實例的參考。</span><span class="sxs-lookup"><span data-stu-id="65a5a-109">Multiplies an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="65a5a-110">會將 <code>operator \*=</code> <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之目前實例的每個元件乘以指定的浮點值，並傳回更新的目前實例的參考。</span><span class="sxs-lookup"><span data-stu-id="65a5a-110">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="65a5a-111">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="65a5a-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="65a5a-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR：： operator \* = (XMVECTOR&，XMVECTOR) </strong></a></span><span class="sxs-lookup"><span data-stu-id="65a5a-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="65a5a-113">將一個 <code>XMVECTOR</code> 實例乘以第二個實例，並傳回已更新之初始實例的參考。</span><span class="sxs-lookup"><span data-stu-id="65a5a-113">Multiplies one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="65a5a-114">會將 <code>operator \*=</code> <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之目前實例的每個元件乘以第二個指定之實例中的對應元件 <code>XMVECTOR</code> ，並傳回已更新之初始實例的參考。</span><span class="sxs-lookup"><span data-stu-id="65a5a-114">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="65a5a-115">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="65a5a-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="65a5a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65a5a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a5a-117">XMVECTOR 運算子</span><span class="sxs-lookup"><span data-stu-id="65a5a-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="65a5a-118">**參考**</span><span class="sxs-lookup"><span data-stu-id="65a5a-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="65a5a-119">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="65a5a-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
