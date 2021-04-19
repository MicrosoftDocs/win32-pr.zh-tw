---
description: 深入瞭解： JET_GRBIT
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106997431"
---
# <a name="jet_grbit"></a><span data-ttu-id="cc97f-103">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cc97f-103">JET_GRBIT</span></span>


<span data-ttu-id="cc97f-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cc97f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_grbit"></a><span data-ttu-id="cc97f-105">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cc97f-105">JET_GRBIT</span></span>

<span data-ttu-id="cc97f-106">**JET_GRBIT** 資料類型是一組位，其中包含所使用之函式和結構的特定常數。</span><span class="sxs-lookup"><span data-stu-id="cc97f-106">The **JET_GRBIT** data type is a group of bits that contain constants that are specific to the functions and structures in which it is used.</span></span>

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a><span data-ttu-id="cc97f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="cc97f-107">Data Types</span></span>

<span data-ttu-id="cc97f-108">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cc97f-108">JET_GRBIT</span></span>

<span data-ttu-id="cc97f-109">一般情況下，用來做為此資料類型之值的常數會反映其使用所在的 API 元素名稱。</span><span class="sxs-lookup"><span data-stu-id="cc97f-109">In general, the constants that are used as values for this data type reflect the name of the API element in which they are used.</span></span> <span data-ttu-id="cc97f-110">例如，所有傳遞給 [JetRetrieveColumn](./jetretrievecolumn-function.md) 的常數都以 "JET_bitRetrieve" 開頭。</span><span class="sxs-lookup"><span data-stu-id="cc97f-110">For example, all constants passed to [JetRetrieveColumn](./jetretrievecolumn-function.md) begin with "JET_bitRetrieve".</span></span> <span data-ttu-id="cc97f-111">同樣地，傳遞給 [JetSetColumn](./jetsetcolumn-function.md) 的所有常數都以 "JET_bitSet" 開頭。</span><span class="sxs-lookup"><span data-stu-id="cc97f-111">Similarly, all constants passed to [JetSetColumn](./jetsetcolumn-function.md) begin with "JET_bitSet".</span></span>

<span data-ttu-id="cc97f-112">值為零會導致忽略參數。</span><span class="sxs-lookup"><span data-stu-id="cc97f-112">A value of zero causes the parameter to be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="cc97f-113">備註</span><span class="sxs-lookup"><span data-stu-id="cc97f-113">Remarks</span></span>

<span data-ttu-id="cc97f-114">如需詳細資訊，請參閱特定的函數或結構。</span><span class="sxs-lookup"><span data-stu-id="cc97f-114">For more information, see the specific function or structure.</span></span> <span data-ttu-id="cc97f-115">這些選項通常會以一組可以合併的旗標形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="cc97f-115">The options are usually passed as a set of flags that can be combined.</span></span>

### <a name="requirements"></a><span data-ttu-id="cc97f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc97f-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc97f-117"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="cc97f-117"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc97f-118">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="cc97f-118">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc97f-119"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="cc97f-119"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc97f-120">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="cc97f-120">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc97f-121"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="cc97f-121"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc97f-122">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="cc97f-122">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cc97f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc97f-123">See Also</span></span>

[<span data-ttu-id="cc97f-124">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="cc97f-124">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="cc97f-125">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="cc97f-125">JetSetColumn</span></span>](./jetsetcolumn-function.md)
