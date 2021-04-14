---
title: OP_BLOB
description: OP_BLOB IDL 定義
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383177"
---
# <a name="op_blob-structure"></a><span data-ttu-id="74252-103">OP_BLOB 結構</span><span class="sxs-lookup"><span data-stu-id="74252-103">OP_BLOB structure</span></span>

<span data-ttu-id="74252-104">包含不透明的位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="74252-104">Contains an opaque byte buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="74252-105">語法</span><span class="sxs-lookup"><span data-stu-id="74252-105">Syntax</span></span>

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a><span data-ttu-id="74252-106">成員</span><span class="sxs-lookup"><span data-stu-id="74252-106">Members</span></span>

### <a name="cbblob"></a><span data-ttu-id="74252-107">cbBlob</span><span class="sxs-lookup"><span data-stu-id="74252-107">cbBlob</span></span>

<span data-ttu-id="74252-108">指定 pBlob 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="74252-108">Specifies the the size of pBlob in bytes.</span></span>

### <a name="pblob"></a><span data-ttu-id="74252-109">pBlob</span><span class="sxs-lookup"><span data-stu-id="74252-109">pBlob</span></span>

<span data-ttu-id="74252-110">指向位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="74252-110">Points to a byte buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="74252-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74252-111">See also</span></span>

[<span data-ttu-id="74252-112">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="74252-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
