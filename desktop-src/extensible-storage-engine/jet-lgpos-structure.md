---
description: 深入瞭解： JET_LGPOS 結構
title: JET_LGPOS 結構
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: 25f00c73a4bb922a8152335babe222b539c70ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027153"
---
# <a name="jet_lgpos-structure"></a><span data-ttu-id="fb5d1-103">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="fb5d1-103">JET_LGPOS Structure</span></span>


<span data-ttu-id="fb5d1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fb5d1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_lgpos-structure"></a><span data-ttu-id="fb5d1-105">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="fb5d1-105">JET_LGPOS Structure</span></span>

<span data-ttu-id="fb5d1-106">**JET_LGPOS** 結構會保存資料庫引擎記錄機制內部的資料。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-106">The **JET_LGPOS** structure holds data that is internal to the logging mechanism of the database engine.</span></span> <span data-ttu-id="fb5d1-107">此結構會被視為內部。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-107">This structure is considered internal.</span></span>

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a><span data-ttu-id="fb5d1-108">成員</span><span class="sxs-lookup"><span data-stu-id="fb5d1-108">Members</span></span>

<span data-ttu-id="fb5d1-109">**Ib**</span><span class="sxs-lookup"><span data-stu-id="fb5d1-109">**ib**</span></span>

<span data-ttu-id="fb5d1-110">支援 ESE 基礎結構，無法從您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-110">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="fb5d1-111">**isec**</span><span class="sxs-lookup"><span data-stu-id="fb5d1-111">**isec**</span></span>

<span data-ttu-id="fb5d1-112">支援 ESE 基礎結構，無法從您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-112">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="fb5d1-113">**lGeneration**</span><span class="sxs-lookup"><span data-stu-id="fb5d1-113">**lGeneration**</span></span>

<span data-ttu-id="fb5d1-114">支援 ESE 基礎結構，無法從您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-114">Supports the ESE infrastructure and cannot be used from your code.</span></span>

### <a name="requirements"></a><span data-ttu-id="fb5d1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb5d1-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb5d1-116"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="fb5d1-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fb5d1-117">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb5d1-118"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="fb5d1-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fb5d1-119">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb5d1-120"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="fb5d1-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fb5d1-121">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="fb5d1-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fb5d1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb5d1-122">See Also</span></span>

[<span data-ttu-id="fb5d1-123">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="fb5d1-123">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="fb5d1-124">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="fb5d1-124">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
