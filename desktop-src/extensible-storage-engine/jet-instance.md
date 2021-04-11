---
description: 深入瞭解： JET_INSTANCE
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944795"
---
# <a name="jet_instance"></a><span data-ttu-id="891eb-103">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="891eb-103">JET_INSTANCE</span></span>


<span data-ttu-id="891eb-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="891eb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance"></a><span data-ttu-id="891eb-105">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="891eb-105">JET_INSTANCE</span></span>

<span data-ttu-id="891eb-106">**JET_INSTANCE** 資料類型包含資料庫實例的控制碼，可用於呼叫 JET API。</span><span class="sxs-lookup"><span data-stu-id="891eb-106">The **JET_INSTANCE** data type contains a handle to the instance of the database to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a><span data-ttu-id="891eb-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="891eb-107">Data Types</span></span>

<span data-ttu-id="891eb-108">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="891eb-108">JET_INSTANCE</span></span>

<span data-ttu-id="891eb-109">**Null** 或 [JET_instanceNil](./invalid-handle-constants.md)可以用來表示不正確實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="891eb-109">Either **NULL** or [JET_instanceNil](./invalid-handle-constants.md) can be used to indicate an invalid instance handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="891eb-110">備註</span><span class="sxs-lookup"><span data-stu-id="891eb-110">Remarks</span></span>

<span data-ttu-id="891eb-111">當您藉由呼叫 [JetCreateInstance](./jetcreateinstance-function.md)、 [JetCreateInstance2](./jetcreateinstance2-function.md)、 [JetInit](./jetinit-function.md)或 [JetInit2](./jetinit2-function.md) 函式來建立資料庫的實例時，就會取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="891eb-111">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="891eb-112">**WINDOWS XP：**  只有 Windows XP 和更新版本才支援明確使用實例。</span><span class="sxs-lookup"><span data-stu-id="891eb-112">**Windows XP:**  The explicit use of instances is only supported on Windows XP and later releases.</span></span>

<span data-ttu-id="891eb-113">**Windows 2000：**  每個進程只支援一個全域實例。</span><span class="sxs-lookup"><span data-stu-id="891eb-113">**Windows 2000:**  Only one global instance is supported per process.</span></span>

### <a name="requirements"></a><span data-ttu-id="891eb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="891eb-114">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="891eb-115"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="891eb-115"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="891eb-116">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="891eb-116">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="891eb-117"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="891eb-117"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="891eb-118">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="891eb-118">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="891eb-119"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="891eb-119"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="891eb-120">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="891eb-120">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="891eb-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="891eb-121">See Also</span></span>

[<span data-ttu-id="891eb-122">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="891eb-122">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="891eb-123">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="891eb-123">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="891eb-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="891eb-124">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="891eb-125">JetInit2</span><span class="sxs-lookup"><span data-stu-id="891eb-125">JetInit2</span></span>](./jetinit2-function.md)
