---
description: 深入瞭解： JET_SIGNATURE 結構
title: JET_SIGNATURE 結構
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972255"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="20e07-103">JET_SIGNATURE 結構</span><span class="sxs-lookup"><span data-stu-id="20e07-103">JET_SIGNATURE Structure</span></span>


<span data-ttu-id="20e07-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20e07-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_signature-structure"></a><span data-ttu-id="20e07-105">JET_SIGNATURE 結構</span><span class="sxs-lookup"><span data-stu-id="20e07-105">JET_SIGNATURE Structure</span></span>

<span data-ttu-id="20e07-106">**JET_SIGNATURE** 結構包含可唯一識別資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="20e07-106">The **JET_SIGNATURE** structure contains information that uniquely identifies a database.</span></span>

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a><span data-ttu-id="20e07-107">成員</span><span class="sxs-lookup"><span data-stu-id="20e07-107">Members</span></span>

<span data-ttu-id="20e07-108">**ulRandom**</span><span class="sxs-lookup"><span data-stu-id="20e07-108">**ulRandom**</span></span>

<span data-ttu-id="20e07-109">隨機指派的數位。</span><span class="sxs-lookup"><span data-stu-id="20e07-109">A randomly assigned number.</span></span>

<span data-ttu-id="20e07-110">**logtimeCreate**</span><span class="sxs-lookup"><span data-stu-id="20e07-110">**logtimeCreate**</span></span>

<span data-ttu-id="20e07-111">執行[JetCreateDatabase](./jetcreatedatabase-function.md)時的[JET_LOGTIME](./jet-logtime-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="20e07-111">The [JET_LOGTIME](./jet-logtime-structure.md) at the time of [JetCreateDatabase](./jetcreatedatabase-function.md) is executed.</span></span>

<span data-ttu-id="20e07-112">**szComputerName**</span><span class="sxs-lookup"><span data-stu-id="20e07-112">**szComputerName**</span></span>

<span data-ttu-id="20e07-113">電腦之 NetBIOS 名稱的選擇性字串值。</span><span class="sxs-lookup"><span data-stu-id="20e07-113">The optional string value of the NetBIOS name for the computer.</span></span> <span data-ttu-id="20e07-114">可能無法設定這個值。</span><span class="sxs-lookup"><span data-stu-id="20e07-114">This value may not be set.</span></span>

### <a name="remarks"></a><span data-ttu-id="20e07-115">備註</span><span class="sxs-lookup"><span data-stu-id="20e07-115">Remarks</span></span>

<span data-ttu-id="20e07-116">您可以使用 [JET_DBINFOMISC](./jet-dbinfomisc-structure.md)的元素來找到這個專案。</span><span class="sxs-lookup"><span data-stu-id="20e07-116">This can be found as an element of [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="20e07-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="20e07-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20e07-118"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="20e07-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20e07-119">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="20e07-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20e07-120"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="20e07-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20e07-121">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="20e07-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20e07-122"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="20e07-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20e07-123">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="20e07-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="20e07-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20e07-124">See Also</span></span>

[<span data-ttu-id="20e07-125">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="20e07-125">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="20e07-126">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="20e07-126">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="20e07-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="20e07-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)
