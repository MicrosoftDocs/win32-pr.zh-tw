---
description: 深入瞭解： JET_PSTR
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: 6bbed2cad9f9c7816d010a429b1db8eb5306fc1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980644"
---
# <a name="jet_pstr"></a><span data-ttu-id="bb5d4-103">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="bb5d4-103">JET_PSTR</span></span>


<span data-ttu-id="bb5d4-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bb5d4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pstr"></a><span data-ttu-id="bb5d4-105">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="bb5d4-105">JET_PSTR</span></span>

<span data-ttu-id="bb5d4-106">JET_PSTR 資料類型包含以 null 終止的 ASCII 字串 (char \*) 。</span><span class="sxs-lookup"><span data-stu-id="bb5d4-106">The JET_PSTR data type contains a null-terminated ASCII string (char \*).</span></span>

<span data-ttu-id="bb5d4-107">**Windows vista： JET_PSTR** 是在 windows vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="bb5d4-107">**Windows Vista:  JET_PSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a><span data-ttu-id="bb5d4-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="bb5d4-108">Data Types</span></span>

<span data-ttu-id="bb5d4-109">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="bb5d4-109">JET_PSTR</span></span>

<span data-ttu-id="bb5d4-110">以 Null 終止的 ASCII 字串 (char \*) 。</span><span class="sxs-lookup"><span data-stu-id="bb5d4-110">Null-terminated, ASCII string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="bb5d4-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb5d4-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb5d4-112"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="bb5d4-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bb5d4-113">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="bb5d4-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb5d4-114"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="bb5d4-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb5d4-115">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="bb5d4-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb5d4-116"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="bb5d4-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bb5d4-117">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="bb5d4-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

