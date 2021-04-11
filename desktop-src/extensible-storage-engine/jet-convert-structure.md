---
description: 深入瞭解： JET_CONVERT 結構
title: JET_CONVERT 結構
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848324"
---
# <a name="jet_convert-structure"></a><span data-ttu-id="9c51b-103">JET_CONVERT 結構</span><span class="sxs-lookup"><span data-stu-id="9c51b-103">JET_CONVERT Structure</span></span>


<span data-ttu-id="9c51b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c51b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_convert-structure"></a><span data-ttu-id="9c51b-105">JET_CONVERT 結構</span><span class="sxs-lookup"><span data-stu-id="9c51b-105">JET_CONVERT Structure</span></span>

<span data-ttu-id="9c51b-106">**JET_CONVERT** 結構包含舊版 ESE 版本 DLL 的名稱，此 DLL 是用來讀取使用舊版所建立的資料庫。</span><span class="sxs-lookup"><span data-stu-id="9c51b-106">The **JET_CONVERT** structure contains the name of an earlier ESE version DLL that is used for reading a databases that are created with that earlier version.</span></span> <span data-ttu-id="9c51b-107">此外，還提供其他旗標來控制轉換的本質。</span><span class="sxs-lookup"><span data-stu-id="9c51b-107">In addition, other flags are provided to control the nature of the conversion.</span></span>

<span data-ttu-id="9c51b-108">**Windows Server 2003：**[JetCompact](./jetcompact-function.md)中執行轉換的功能已從 Windows Server 2003 中的產品中移除。</span><span class="sxs-lookup"><span data-stu-id="9c51b-108">**Windows Server 2003:** The feature in [JetCompact](./jetcompact-function.md) that performed a conversion was removed from the product in Windows Server 2003.</span></span> <span data-ttu-id="9c51b-109">只有在 Windows 2000 和 Windows XP 中才支援此功能。</span><span class="sxs-lookup"><span data-stu-id="9c51b-109">It is only supported in Windows 2000 and Windows XP.</span></span>

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a><span data-ttu-id="9c51b-110">成員</span><span class="sxs-lookup"><span data-stu-id="9c51b-110">Members</span></span>

<span data-ttu-id="9c51b-111">**SzOldDll**</span><span class="sxs-lookup"><span data-stu-id="9c51b-111">**SzOldDll**</span></span>

<span data-ttu-id="9c51b-112">較早版本的 ESE DLL 名稱，包括路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="9c51b-112">The name, including path information, to the earlier version of the ESE DLL.</span></span>

<span data-ttu-id="9c51b-113">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="9c51b-113">**fFlags**</span></span>

<span data-ttu-id="9c51b-114">保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c51b-114">Reserved for system use.</span></span>

<span data-ttu-id="9c51b-115">**fSchemaChangesOnly**</span><span class="sxs-lookup"><span data-stu-id="9c51b-115">**fSchemaChangesOnly**</span></span>

<span data-ttu-id="9c51b-116">保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="9c51b-116">Reserved for system use.</span></span>

### <a name="requirements"></a><span data-ttu-id="9c51b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c51b-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c51b-118"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9c51b-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c51b-119">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="9c51b-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c51b-120"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9c51b-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c51b-121">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="9c51b-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c51b-122"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9c51b-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c51b-123">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9c51b-123">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c51b-124"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9c51b-124"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9c51b-125">實作為 <strong>JET_CONVERT_W</strong> (Unicode) 和 <strong>JET_CONVERT_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="9c51b-125">Implemented as <strong>JET_CONVERT_W</strong> (Unicode) and <strong>JET_CONVERT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9c51b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c51b-126">See Also</span></span>

[<span data-ttu-id="9c51b-127">JetCompact</span><span class="sxs-lookup"><span data-stu-id="9c51b-127">JetCompact</span></span>](./jetcompact-function.md)
