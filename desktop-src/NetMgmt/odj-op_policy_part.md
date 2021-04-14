---
title: OP_POLICY_PART
description: OP_POLICY_PART IDL 定義
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383174"
---
# <a name="op_policy_part-structure"></a><span data-ttu-id="26ab8-103">OP_POLICY_PART 結構</span><span class="sxs-lookup"><span data-stu-id="26ab8-103">OP_POLICY_PART structure</span></span>

<span data-ttu-id="26ab8-104">包含 OP_POLICY_ELEMENT_LIST 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="26ab8-104">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ab8-105">語法</span><span class="sxs-lookup"><span data-stu-id="26ab8-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a><span data-ttu-id="26ab8-106">成員</span><span class="sxs-lookup"><span data-stu-id="26ab8-106">Members</span></span>

### <a name="celementlists"></a><span data-ttu-id="26ab8-107">cElementLists</span><span class="sxs-lookup"><span data-stu-id="26ab8-107">cElementLists</span></span>

<span data-ttu-id="26ab8-108">包含 pElementLists 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="26ab8-108">Contains the number of elements in pElementLists.</span></span>

### <a name="pelementlists"></a><span data-ttu-id="26ab8-109">pElementLists</span><span class="sxs-lookup"><span data-stu-id="26ab8-109">pElementLists</span></span>

<span data-ttu-id="26ab8-110">包含 OP_POLICY_ELEMENT_LIST 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="26ab8-110">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

### <a name="extension"></a><span data-ttu-id="26ab8-111">分機</span><span class="sxs-lookup"><span data-stu-id="26ab8-111">Extension</span></span>

<span data-ttu-id="26ab8-112">保留供日後使用，且必須包含所有的零。</span><span class="sxs-lookup"><span data-stu-id="26ab8-112">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="26ab8-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26ab8-113">See also</span></span>

[<span data-ttu-id="26ab8-114">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="26ab8-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="26ab8-115">**OP \_ 原則 \_ 元素 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="26ab8-115">**OP\_POLICY\_ELEMENT\_LIST**</span></span>](odj-op_policy_element_list.md)
