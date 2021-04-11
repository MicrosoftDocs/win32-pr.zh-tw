---
description: 深入瞭解： JET_ERRINFOBASIC_W 結構
title: JET_ERRINFOBASIC_W 結構
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103946278"
---
# <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="e974a-103">JET_ERRINFOBASIC_W 結構</span><span class="sxs-lookup"><span data-stu-id="e974a-103">JET_ERRINFOBASIC_W Structure</span></span>


<span data-ttu-id="e974a-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e974a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="e974a-105">JET_ERRINFOBASIC_W 結構</span><span class="sxs-lookup"><span data-stu-id="e974a-105">JET_ERRINFOBASIC_W Structure</span></span>

<span data-ttu-id="e974a-106">**JET_ERRINFOBASIC_W** 結構會定義傳入 JET_ErrorInfoSpecificErr InfoLevel 時，從 [JetGetErrorInfo ()](./jetgeterrorinfow-function.md)方法傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="e974a-106">The **JET_ERRINFOBASIC_W** structure defines the data that is returned from the [JetGetErrorInfo()](./jetgeterrorinfow-function.md) method when the JET_ErrorInfoSpecificErr InfoLevel is passed in.</span></span>

<span data-ttu-id="e974a-107">注意：本檔是以可延伸儲存引擎的初步發行版本為基礎。</span><span class="sxs-lookup"><span data-stu-id="e974a-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="e974a-108">此資訊可能隨時變更。</span><span class="sxs-lookup"><span data-stu-id="e974a-108">This information is subject to change.</span></span>

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a><span data-ttu-id="e974a-109">成員</span><span class="sxs-lookup"><span data-stu-id="e974a-109">Members</span></span>

<span data-ttu-id="e974a-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e974a-110">**cbStruct**</span></span>

<span data-ttu-id="e974a-111">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e974a-111">The size of the structure, in bytes.</span></span> <span data-ttu-id="e974a-112">它必須設定為 sizeof ( JET_ERRINFOBASIC ) 。</span><span class="sxs-lookup"><span data-stu-id="e974a-112">It must be set to sizeof( JET_ERRINFOBASIC ).</span></span>

<span data-ttu-id="e974a-113">**errValue**</span><span class="sxs-lookup"><span data-stu-id="e974a-113">**errValue**</span></span>

<span data-ttu-id="e974a-114">針對 [JetGetErrorInfo ()](./jetgeterrorinfow-function.md)的 *pvResult* 引數所傳遞的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="e974a-114">The error value that was evaluated, as passed in for the *pvResult* argument to [JetGetErrorInfo()](./jetgeterrorinfow-function.md).</span></span>

<span data-ttu-id="e974a-115">**errcatMostSpecific**</span><span class="sxs-lookup"><span data-stu-id="e974a-115">**errcatMostSpecific**</span></span>

<span data-ttu-id="e974a-116">與錯誤相關聯的最低層級 [JET_ERRCAT](./jet-errcat.md) 常數;亦即，在 [JET_ERRCAT](./jet-errcat.md)中記載的類別目錄階層中的分葉層級類別。</span><span class="sxs-lookup"><span data-stu-id="e974a-116">The lowest-level [JET_ERRCAT](./jet-errcat.md) constant that is associated with the error; that is, the leaf-level category in the category hierarchy documented in [JET_ERRCAT](./jet-errcat.md).</span></span>

<span data-ttu-id="e974a-117">**rgCategoricalHierarchy \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="e974a-117">**rgCategoricalHierarchy\[8\]**</span></span>

<span data-ttu-id="e974a-118">與錯誤相關聯的錯誤類別目錄階層。</span><span class="sxs-lookup"><span data-stu-id="e974a-118">The hierarchy of error categories that is associated with the error.</span></span> <span data-ttu-id="e974a-119">位置0是 [JET_ERRCAT](./jet-errcat.md)階層中的最高層級，其餘則是子類別，直到設定了最特定的類別為止，之後所有的類別都是 JET_errcatUnknown。</span><span class="sxs-lookup"><span data-stu-id="e974a-119">Position 0 is the highest level in the hierarchy of [JET_ERRCAT](./jet-errcat.md), and the rest are subcategories until the most specific category is set, after which all categories are JET_errcatUnknown.</span></span>

<span data-ttu-id="e974a-120">**lSourceLine**</span><span class="sxs-lookup"><span data-stu-id="e974a-120">**lSourceLine**</span></span>

<span data-ttu-id="e974a-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="e974a-121">Reserved.</span></span>

<span data-ttu-id="e974a-122">**rgszSourceFile \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="e974a-122">**rgszSourceFile\[64\]**</span></span>

<span data-ttu-id="e974a-123">保留的。</span><span class="sxs-lookup"><span data-stu-id="e974a-123">Reserved.</span></span>

### <a name="requirements"></a><span data-ttu-id="e974a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e974a-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e974a-125"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e974a-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e974a-126">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="e974a-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e974a-127"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e974a-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e974a-128">需要 Windows 8 Server。</span><span class="sxs-lookup"><span data-stu-id="e974a-128">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e974a-129"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e974a-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e974a-130">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e974a-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
