---
description: 深入瞭解： JET_PCWSTR
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 51cd0dab17096fb8f7371a01ebabfca3abc595be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985136"
---
# <a name="jet_pcwstr"></a><span data-ttu-id="fdb47-103">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="fdb47-103">JET_PCWSTR</span></span>


<span data-ttu-id="fdb47-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fdb47-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pcwstr"></a><span data-ttu-id="fdb47-105">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="fdb47-105">JET_PCWSTR</span></span>

<span data-ttu-id="fdb47-106">**JET_PCWSTR** 資料類型包含以 null 終止的常數 **Unicode** 字串 (char \*) 。</span><span class="sxs-lookup"><span data-stu-id="fdb47-106">The **JET_PCWSTR** data type contains a null-terminated, constant **Unicode** string (char \*).</span></span>

<span data-ttu-id="fdb47-107">**Windows vista： JET_PCWSTR** 是在 windows vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="fdb47-107">**Windows Vista:  JET_PCWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a><span data-ttu-id="fdb47-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="fdb47-108">Data Types</span></span>

<span data-ttu-id="fdb47-109">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="fdb47-109">JET_PCWSTR</span></span>

<span data-ttu-id="fdb47-110">以 Null 終止的常數 Unicode 字串 (char \*) 。</span><span class="sxs-lookup"><span data-stu-id="fdb47-110">Null-terminated, constant Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="fdb47-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdb47-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdb47-112"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="fdb47-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fdb47-113">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="fdb47-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdb47-114"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="fdb47-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fdb47-115">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="fdb47-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdb47-116"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="fdb47-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fdb47-117">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="fdb47-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

