---
description: 除法指派運算子。
ms.assetid: 59dee8a1-48c5-4748-8eca-1d0939e90fe0
title: operator/= 運算子
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4d0c20975a93215a62bdb6b08dedc839ca8d079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943750"
---
# <a name="operator--operators"></a><span data-ttu-id="8d883-103">operator/= 運算子</span><span class="sxs-lookup"><span data-stu-id="8d883-103">operator /= operators</span></span>

<span data-ttu-id="8d883-104">除法指派運算子。</span><span class="sxs-lookup"><span data-stu-id="8d883-104">Division Assignment operator.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8d883-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="8d883-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8d883-106">運算子</span><span class="sxs-lookup"><span data-stu-id="8d883-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8d883-107">描述</span><span class="sxs-lookup"><span data-stu-id="8d883-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8d883-108"><a href="/previous-versions/windows/desktop/legacy/ee421377(v=vs.85)"><strong>XMVECTOR：： operator/= (XMVECTOR&，float) </strong></a></span><span class="sxs-lookup"><span data-stu-id="8d883-108"><a href="/previous-versions/windows/desktop/legacy/ee421377(v=vs.85)"><strong>XMVECTOR::operator /= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8d883-109">將 <code>XMVECTOR</code> 實例除以浮點值，並傳回更新的實例的參考。</span><span class="sxs-lookup"><span data-stu-id="8d883-109">Divides an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="8d883-110">會將 <code>operator /=</code> <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之目前實例的每個元件除以指定的浮點值，並傳回更新的目前實例的參考。</span><span class="sxs-lookup"><span data-stu-id="8d883-110">The <code>operator /=</code> divides each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8d883-111">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="8d883-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8d883-112"><a href="/previous-versions/windows/desktop/legacy/ee421378(v=vs.85)"><strong>XMVECTOR：： operator/= (XMVECTOR&，XMVECTOR) </strong></a></span><span class="sxs-lookup"><span data-stu-id="8d883-112"><a href="/previous-versions/windows/desktop/legacy/ee421378(v=vs.85)"><strong>XMVECTOR::operator /= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8d883-113">將一個 <code>XMVECTOR</code> 實例除以第二個實例，並傳回已更新之初始實例的參考。</span><span class="sxs-lookup"><span data-stu-id="8d883-113">Divides one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="8d883-114">將 <code>operator /=</code> <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之目前實例的每個元件除以第二個指定之實例中的對應元件 <code>XMVECTOR</code> ，並傳回已更新之初始實例的參考。</span><span class="sxs-lookup"><span data-stu-id="8d883-114">The <code>operator /=</code> divides each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8d883-115">此運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="8d883-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="8d883-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d883-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d883-117">XMVECTOR 運算子</span><span class="sxs-lookup"><span data-stu-id="8d883-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="8d883-118">**參考**</span><span class="sxs-lookup"><span data-stu-id="8d883-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d883-119">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="8d883-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
