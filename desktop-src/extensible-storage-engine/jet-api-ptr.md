---
description: 深入瞭解： JET_API_PTR
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
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
ms.openlocfilehash: 687f28fcba3d20c5b72a3089d3a442dd97e2dfb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980494"
---
# <a name="jet_api_ptr"></a><span data-ttu-id="089f3-103">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="089f3-103">JET_API_PTR</span></span>


<span data-ttu-id="089f3-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="089f3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_api_ptr"></a><span data-ttu-id="089f3-105">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="089f3-105">JET_API_PTR</span></span>

<span data-ttu-id="089f3-106">**JET_API_PTR** 資料類型會保存整數或指標值。</span><span class="sxs-lookup"><span data-stu-id="089f3-106">The **JET_API_PTR** data type holds an integer or a pointer value.</span></span>

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="089f3-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="089f3-107">Data Types</span></span>

<span data-ttu-id="089f3-108">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="089f3-108">JET_API_PTR</span></span>

<span data-ttu-id="089f3-109">如同 **DWORD_PTR** 資料類型， **JET_API_PTR** 資料類型在32位電腦上定義為4個位元組，在64位電腦上定義為8個位元組。</span><span class="sxs-lookup"><span data-stu-id="089f3-109">Like a **DWORD_PTR** data type, the **JET_API_PTR** data type is defined as 4 bytes on a 32-bit machine and 8 bytes on a 64-bit machine.</span></span>

### <a name="remarks"></a><span data-ttu-id="089f3-110">備註</span><span class="sxs-lookup"><span data-stu-id="089f3-110">Remarks</span></span>

<span data-ttu-id="089f3-111">**JET_API_PTR** 資料類型是用來定義下列資料類型：</span><span class="sxs-lookup"><span data-stu-id="089f3-111">The **JET_API_PTR** data type is used to define the following data types:</span></span>

  - [<span data-ttu-id="089f3-112">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="089f3-112">JET_HANDLE</span></span>](./jet-handle.md)

  - [<span data-ttu-id="089f3-113">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="089f3-113">JET_INSTANCE</span></span>](./jet-instance.md)

  - [<span data-ttu-id="089f3-114">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="089f3-114">JET_SESID</span></span>](./jet-sesid.md)

  - [<span data-ttu-id="089f3-115">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="089f3-115">JET_TABLEID</span></span>](./jet-tableid.md)

  - [<span data-ttu-id="089f3-116">JET_LS</span><span class="sxs-lookup"><span data-stu-id="089f3-116">JET_LS</span></span>](./jet-ls.md)

### <a name="requirements"></a><span data-ttu-id="089f3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="089f3-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="089f3-118"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="089f3-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="089f3-119">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="089f3-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="089f3-120"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="089f3-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="089f3-121">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="089f3-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="089f3-122"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="089f3-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="089f3-123">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="089f3-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
