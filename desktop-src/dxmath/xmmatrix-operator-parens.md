---
description: 從目前的 XMMATRIX 實例存取資料列和資料行所參考的特定矩陣元素。
ms.assetid: 917d44b0-4625-412f-b3ad-5955856689d5
title: XMMATRIX 運算子 () 運算子
ms.topic: reference
ms.date: 12/06/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 900af391208505d862bc1861534c8e3f1c34faf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998083"
---
# <a name="xmmatrix-operator--operators"></a><span data-ttu-id="c8df4-103">XMMATRIX 運算子 () 運算子</span><span class="sxs-lookup"><span data-stu-id="c8df4-103">XMMATRIX operator () operators</span></span>

<span data-ttu-id="c8df4-104">從目前的實例存取資料列和資料行所參考的特定矩陣元素 `XMMATRIX` 。</span><span class="sxs-lookup"><span data-stu-id="c8df4-104">Accesses specific matrix elements referenced by row and column from the current instance of `XMMATRIX`.</span></span>

<span data-ttu-id="c8df4-105">從目前的 XMMATRIX 實例存取資料列和資料行所參考的特定矩陣元素[ ](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)</span><span class="sxs-lookup"><span data-stu-id="c8df4-105">Accesses specific matrix elements referenced by row and column from the current instance of [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)</span></span>

### <a name="overload-list"></a><span data-ttu-id="c8df4-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="c8df4-106">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c8df4-107">運算子</span><span class="sxs-lookup"><span data-stu-id="c8df4-107">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c8df4-108">描述</span><span class="sxs-lookup"><span data-stu-id="c8df4-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c8df4-109"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>XMMATRIX：： operator ()  (size_t，size_t) </strong></a></span><span class="sxs-lookup"><span data-stu-id="c8df4-109"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>XMMATRIX::operator () (size_t,size_t)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c8df4-110">將傳回 <code>reference</code> 至實例的矩陣元素， <code>XMMATRIX</code> 如資料列和資料行引數所指定。</span><span class="sxs-lookup"><span data-stu-id="c8df4-110">Returns a <code>reference</code> to a matrix element of an instance <code>XMMATRIX</code> as specified by row and column arguments.</span></span><br/> <span data-ttu-id="c8df4-111">這個運算子會將加入 <code>reference</code> 至實例 <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> 的矩陣元素，如資料列和資料行引數所指定。</span><span class="sxs-lookup"><span data-stu-id="c8df4-111">This operator returns a <code>reference</code> to a matrix element of an instance <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> as specified by row and column arguments.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c8df4-112">只有在使用 c + + 進行開發時，才能使用這個運算子。</span><span class="sxs-lookup"><span data-stu-id="c8df4-112">This operator is only available when developing with C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c8df4-113"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>XMMATRIX：： operator ()  (size_t，size_t) </strong></a></span><span class="sxs-lookup"><span data-stu-id="c8df4-113"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>XMMATRIX::operator () (size_t,size_t)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c8df4-114">傳回實例中矩陣元素的值，如資料 <code>XMMATRIX</code> 列和資料行引數所指定。</span><span class="sxs-lookup"><span data-stu-id="c8df4-114">Return the value of a matrix element in an instance <code>XMMATRIX</code> as specified by row and column arguments.</span></span><br/> <span data-ttu-id="c8df4-115">這個運算子會傳回實例 <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> 的矩陣元素值，如資料列和資料行引數所指定。</span><span class="sxs-lookup"><span data-stu-id="c8df4-115">This operator returns the value of a matrix element of an instance <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> as specified by row and column arguments.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c8df4-116">只有在使用 c + + 進行開發時，才能使用這個運算子。</span><span class="sxs-lookup"><span data-stu-id="c8df4-116">This operator is only available when developing with C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="c8df4-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8df4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8df4-118">XMMATRIX 運算子</span><span class="sxs-lookup"><span data-stu-id="c8df4-118">XMMATRIX Operators</span></span>](ovw-xmmatrix-operators.md)
</dt> <dt>

<span data-ttu-id="c8df4-119">**參考**</span><span class="sxs-lookup"><span data-stu-id="c8df4-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8df4-120">**XMMATRIX**</span><span class="sxs-lookup"><span data-stu-id="c8df4-120">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)
</dt> </dl>

 

 
