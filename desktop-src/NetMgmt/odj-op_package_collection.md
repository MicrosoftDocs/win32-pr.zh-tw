---
title: OP_PACKAGE_PART_COLLECTION
description: OP_PACKAGE_PART_COLLECTION IDL 定義
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104024281"
---
# <a name="op_package_part_collection-structure"></a><span data-ttu-id="7d5cc-103">OP_PACKAGE_PART_COLLECTION 結構</span><span class="sxs-lookup"><span data-stu-id="7d5cc-103">OP_PACKAGE_PART_COLLECTION structure</span></span>

<span data-ttu-id="7d5cc-104">指定包含 OP_PACKAGE_PART 結構陣列的結構。</span><span class="sxs-lookup"><span data-stu-id="7d5cc-104">Specifies a structure that contains an array of OP_PACKAGE_PART structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d5cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="7d5cc-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a><span data-ttu-id="7d5cc-106">成員</span><span class="sxs-lookup"><span data-stu-id="7d5cc-106">Members</span></span>

### <a name="cparts"></a><span data-ttu-id="7d5cc-107">cParts</span><span class="sxs-lookup"><span data-stu-id="7d5cc-107">cParts</span></span>

<span data-ttu-id="7d5cc-108">包含 pParts 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="7d5cc-108">Contains the number of elements in pParts.</span></span>

### <a name="pparts"></a><span data-ttu-id="7d5cc-109">pParts</span><span class="sxs-lookup"><span data-stu-id="7d5cc-109">pParts</span></span>

<span data-ttu-id="7d5cc-110">包含 OP_PACKAGE_PART 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="7d5cc-110">Contains an array of OP_PACKAGE_PART structures.</span></span>

### <a name="extension"></a><span data-ttu-id="7d5cc-111">分機</span><span class="sxs-lookup"><span data-stu-id="7d5cc-111">Extension</span></span>

<span data-ttu-id="7d5cc-112">保留供日後使用，且必須設定為全部為零。</span><span class="sxs-lookup"><span data-stu-id="7d5cc-112">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d5cc-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d5cc-113">See also</span></span>

[<span data-ttu-id="7d5cc-114">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="7d5cc-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="7d5cc-115">**OP \_ 套件 \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="7d5cc-115">**OP\_PACKAGE\_PART**</span></span>](odj-op_package_part.md)

[<span data-ttu-id="7d5cc-116">**OP \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="7d5cc-116">**OP\_BLOB**</span></span>](odj-op_blob.md)

