---
title: OP_JOINPROV3_PART
description: OP_JOINPROV3_PART IDL 定義
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383169"
---
# <a name="op_joinprov3_part-structure"></a><span data-ttu-id="e8bde-103">OP_JOINPROV3_PART 結構</span><span class="sxs-lookup"><span data-stu-id="e8bde-103">OP_JOINPROV3_PART structure</span></span>

<span data-ttu-id="e8bde-104">包含用來設定加入網域之用戶端的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="e8bde-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bde-105">語法</span><span class="sxs-lookup"><span data-stu-id="e8bde-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a><span data-ttu-id="e8bde-106">成員</span><span class="sxs-lookup"><span data-stu-id="e8bde-106">Members</span></span>

### <a name="rid"></a><span data-ttu-id="e8bde-107">擺脫</span><span class="sxs-lookup"><span data-stu-id="e8bde-107">Rid</span></span>

<span data-ttu-id="e8bde-108">必須設定為電腦帳戶 SID 的相對識別碼</span><span class="sxs-lookup"><span data-stu-id="e8bde-108">Must be set to the Relative Identifier of the machine account’s SID</span></span>

### <a name="lpsid"></a><span data-ttu-id="e8bde-109">lpSid</span><span class="sxs-lookup"><span data-stu-id="e8bde-109">lpSid</span></span>

<span data-ttu-id="e8bde-110">必須設定為字串格式之電腦帳戶的 SID。</span><span class="sxs-lookup"><span data-stu-id="e8bde-110">Must be set to the SID of the machine account in string form.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8bde-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8bde-111">See also</span></span>

[<span data-ttu-id="e8bde-112">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="e8bde-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
