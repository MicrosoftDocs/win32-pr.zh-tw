---
description: 深入瞭解： JET_coltyp 列舉
title: JET_coltyp 列舉
TOCTitle: JET_coltyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_coltyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_coltyp(v=EXCHG.10)
ms:contentKeyID: 39511169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 616dc80d835e22502b6781355a2eff35a6375e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975463"
---
# <a name="jet_coltyp-enumeration"></a><span data-ttu-id="517ab-103">JET_coltyp 列舉</span><span class="sxs-lookup"><span data-stu-id="517ab-103">JET_coltyp enumeration</span></span>

<span data-ttu-id="517ab-104">ESENT 資料行類型。</span><span class="sxs-lookup"><span data-stu-id="517ab-104">ESENT column types.</span></span>

<span data-ttu-id="517ab-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="517ab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="517ab-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="517ab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="517ab-107">語法</span><span class="sxs-lookup"><span data-stu-id="517ab-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_coltyp
'Usage
Dim instance As JET_coltyp
```

``` csharp
public enum JET_coltyp
```

## <a name="members"></a><span data-ttu-id="517ab-108">成員</span><span class="sxs-lookup"><span data-stu-id="517ab-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="517ab-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="517ab-109">Member name</span></span></th>
<th><span data-ttu-id="517ab-110">說明</span><span class="sxs-lookup"><span data-stu-id="517ab-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="517ab-111">零</span><span class="sxs-lookup"><span data-stu-id="517ab-111">Nil</span></span></td>
<td><span data-ttu-id="517ab-112">Null 資料行類型。</span><span class="sxs-lookup"><span data-stu-id="517ab-112">Null column type.</span></span> <span data-ttu-id="517ab-113">建立資料行時無效。</span><span class="sxs-lookup"><span data-stu-id="517ab-113">Invalid for column creation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="517ab-114">bit</span><span class="sxs-lookup"><span data-stu-id="517ab-114">Bit</span></span></td>
<td><span data-ttu-id="517ab-115">True、False 或 Null。</span><span class="sxs-lookup"><span data-stu-id="517ab-115">True, False or NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="517ab-116">UnsignedByte</span><span class="sxs-lookup"><span data-stu-id="517ab-116">UnsignedByte</span></span></td>
<td><span data-ttu-id="517ab-117">1位元組整數，不帶正負號。</span><span class="sxs-lookup"><span data-stu-id="517ab-117">1-byte integer, unsigned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="517ab-118">Short</span><span class="sxs-lookup"><span data-stu-id="517ab-118">Short</span></span></td>
<td><span data-ttu-id="517ab-119">2位元組整數，已簽署。</span><span class="sxs-lookup"><span data-stu-id="517ab-119">2-byte integer, signed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="517ab-120">long</span><span class="sxs-lookup"><span data-stu-id="517ab-120">Long</span></span></td>
<td><span data-ttu-id="517ab-121">4位元組整數，已簽署。</span><span class="sxs-lookup"><span data-stu-id="517ab-121">4-byte integer, signed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="517ab-122">貨幣</span><span class="sxs-lookup"><span data-stu-id="517ab-122">Currency</span></span></td>
<td><span data-ttu-id="517ab-123">8個位元組的整數（帶正負號）。</span><span class="sxs-lookup"><span data-stu-id="517ab-123">8-byte integer, signed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="517ab-124">IEEESingle</span><span class="sxs-lookup"><span data-stu-id="517ab-124">IEEESingle</span></span></td>
<td><span data-ttu-id="517ab-125">4位元組 IEEE 單一精確度。</span><span class="sxs-lookup"><span data-stu-id="517ab-125">4-byte IEEE single-precisions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="517ab-126">IEEEDouble</span><span class="sxs-lookup"><span data-stu-id="517ab-126">IEEEDouble</span></span></td>
<td><span data-ttu-id="517ab-127">8位元組 IEEE 雙精確度。</span><span class="sxs-lookup"><span data-stu-id="517ab-127">8-byte IEEE double-precision.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="517ab-128">Datetime</span><span class="sxs-lookup"><span data-stu-id="517ab-128">DateTime</span></span></td>
<td><span data-ttu-id="517ab-129">整數日期、小數時間。</span><span class="sxs-lookup"><span data-stu-id="517ab-129">Integral date, fractional time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="517ab-130">Binary</span><span class="sxs-lookup"><span data-stu-id="517ab-130">Binary</span></span></td>
<td><span data-ttu-id="517ab-131">二進位資料，最多255個位元組。</span><span class="sxs-lookup"><span data-stu-id="517ab-131">Binary data, up to 255 bytes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="517ab-132">Text</span><span class="sxs-lookup"><span data-stu-id="517ab-132">Text</span></span></td>
<td><span data-ttu-id="517ab-133">文字資料，最多255個位元組。</span><span class="sxs-lookup"><span data-stu-id="517ab-133">Text data, up to 255 bytes.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="517ab-134">LongBinary</span><span class="sxs-lookup"><span data-stu-id="517ab-134">LongBinary</span></span></td>
<td><span data-ttu-id="517ab-135">二進位資料，最多 2 GB。</span><span class="sxs-lookup"><span data-stu-id="517ab-135">Binary data, up to 2GB.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="517ab-136">LongText</span><span class="sxs-lookup"><span data-stu-id="517ab-136">LongText</span></span></td>
<td><span data-ttu-id="517ab-137">文字資料，最多 2 GB。</span><span class="sxs-lookup"><span data-stu-id="517ab-137">Text data, up to 2GB.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="517ab-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="517ab-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="517ab-139">參考</span><span class="sxs-lookup"><span data-stu-id="517ab-139">Reference</span></span>

[<span data-ttu-id="517ab-140">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="517ab-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
