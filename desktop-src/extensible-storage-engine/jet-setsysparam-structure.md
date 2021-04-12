---
description: 深入瞭解： JET_SETSYSPARAM 結構
title: JET_SETSYSPARAM 結構
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318172"
---
# <a name="jet_setsysparam-structure"></a><span data-ttu-id="940b3-103">JET_SETSYSPARAM 結構</span><span class="sxs-lookup"><span data-stu-id="940b3-103">JET_SETSYSPARAM Structure</span></span>


<span data-ttu-id="940b3-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="940b3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setsysparam-structure"></a><span data-ttu-id="940b3-105">JET_SETSYSPARAM 結構</span><span class="sxs-lookup"><span data-stu-id="940b3-105">JET_SETSYSPARAM Structure</span></span>

<span data-ttu-id="940b3-106">**JET_SETSYSPARAM** 結構的陣列表示使用 [JetEnableMultiInstance](./jetenablemultiinstance-function.md)函式時，設定為引數的一組特定全域系統參數。</span><span class="sxs-lookup"><span data-stu-id="940b3-106">An array of **JET_SETSYSPARAM** structures indicate a specific set of global system parameters that are set as an argument when using the [JetEnableMultiInstance](./jetenablemultiinstance-function.md) function.</span></span>

<span data-ttu-id="940b3-107">**WINDOWS XP：** 此結構是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="940b3-107">**Windows XP:** This structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a><span data-ttu-id="940b3-108">成員</span><span class="sxs-lookup"><span data-stu-id="940b3-108">Members</span></span>

<span data-ttu-id="940b3-109">**paramid**</span><span class="sxs-lookup"><span data-stu-id="940b3-109">**paramid**</span></span>

<span data-ttu-id="940b3-110">將設定之系統參數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="940b3-110">The ID of the system parameter that will be set.</span></span>

<span data-ttu-id="940b3-111">如需系統參數及其屬性的完整清單，請參閱可延伸 [儲存引擎系統參數](./extensible-storage-engine-system-parameters.md) 。</span><span class="sxs-lookup"><span data-stu-id="940b3-111">See [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="940b3-112">**lParam**</span><span class="sxs-lookup"><span data-stu-id="940b3-112">**lParam**</span></span>

<span data-ttu-id="940b3-113">如果系統參數是整數類型，則為所選取系統參數設定的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="940b3-113">The optional value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="940b3-114">**深圳**</span><span class="sxs-lookup"><span data-stu-id="940b3-114">**sz**</span></span>

<span data-ttu-id="940b3-115">如果系統參數是字串類型，則為所選取系統參數設定的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="940b3-115">The optional value to be set for the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="940b3-116">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="940b3-116">**err**</span></span>

<span data-ttu-id="940b3-117">使用先前指定的參數呼叫 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 所產生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="940b3-117">The error resulting from the call to [JetSetSystemParameter](./jetsetsystemparameter-function.md) with the previously specified parameters.</span></span>

### <a name="requirements"></a><span data-ttu-id="940b3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="940b3-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940b3-119"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="940b3-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="940b3-120">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="940b3-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b3-121"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="940b3-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="940b3-122">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="940b3-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940b3-123"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="940b3-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="940b3-124">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="940b3-124">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940b3-125"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="940b3-125"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="940b3-126">實作為 <strong>JET_ SETSYSPARAM_W</strong> (Unicode) 和 <strong>JET_</strong> SETSYSPARAM_A (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="940b3-126">Implemented as <strong>JET_ SETSYSPARAM_W</strong> (Unicode) and <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="940b3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="940b3-127">See Also</span></span>

[<span data-ttu-id="940b3-128">可擴充儲存引擎系統參數</span><span class="sxs-lookup"><span data-stu-id="940b3-128">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)  
[<span data-ttu-id="940b3-129">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="940b3-129">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="940b3-130">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="940b3-130">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="940b3-131">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="940b3-131">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="940b3-132">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="940b3-132">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
