---
description: 深入瞭解： JET_DATESERIAL
title: JET_DATESERIAL
TOCTitle: JET_DATESERIAL
ms:assetid: 8fe0abcc-6e63-4877-a74f-5b7f12dc15a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269338(v=EXCHG.10)
ms:contentKeyID: 32765627
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
ms.openlocfilehash: 8d2b5e0c7a5bd6352cc28761a20915e16ed550f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691292"
---
# <a name="jet_dateserial"></a><span data-ttu-id="ed015-103">JET_DATESERIAL</span><span class="sxs-lookup"><span data-stu-id="ed015-103">JET_DATESERIAL</span></span>


<span data-ttu-id="ed015-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ed015-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dateserial"></a><span data-ttu-id="ed015-105">JET_DATESERIAL</span><span class="sxs-lookup"><span data-stu-id="ed015-105">JET_DATESERIAL</span></span>

<span data-ttu-id="ed015-106">**JET_DATESERIAL** 資料類型代表從100年起算的日期（以小數天為單位）。</span><span class="sxs-lookup"><span data-stu-id="ed015-106">The **JET_DATESERIAL** data type represents a date in fractional days since the year 100.</span></span>

```cpp
    typedef double JET_DATESERIAL;
```

### <a name="data-types"></a><span data-ttu-id="ed015-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ed015-107">Data Types</span></span>

<span data-ttu-id="ed015-108">JET_DATESERIAL</span><span class="sxs-lookup"><span data-stu-id="ed015-108">JET_DATESERIAL</span></span>

<span data-ttu-id="ed015-109">將雙精確度 (8 個位元組) 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ed015-109">Holds a double-precision (8-byte) floating point number.</span></span> <span data-ttu-id="ed015-110">這與 c + + [日期](https://msdn.microsoft.com/library/82ab7w69(VS.71).aspx) 類型相同。</span><span class="sxs-lookup"><span data-stu-id="ed015-110">This is the same as the C++ [DATE](https://msdn.microsoft.com/library/82ab7w69(VS.71).aspx) type.</span></span>

### <a name="requirements"></a><span data-ttu-id="ed015-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed015-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed015-112"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ed015-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ed015-113">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="ed015-113">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed015-114"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ed015-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ed015-115">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="ed015-115">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed015-116"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ed015-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ed015-117">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ed015-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ed015-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed015-118">See Also</span></span>

<span data-ttu-id="ed015-119">[DATE](https://msdn.microsoft.com/library/82ab7w69(VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="ed015-119">[DATE](https://msdn.microsoft.com/library/82ab7w69(VS.71).aspx)</span></span>

