---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA IDL 定義
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "106991114"
---
# <a name="odj_provision_data-structure"></a><span data-ttu-id="97a0a-103">ODJ_PROVISION_DATA 結構</span><span class="sxs-lookup"><span data-stu-id="97a0a-103">ODJ_PROVISION_DATA structure</span></span>

<span data-ttu-id="97a0a-104">指定離線網域加入 api 所使用的最外層序列化結構。</span><span class="sxs-lookup"><span data-stu-id="97a0a-104">Specifies the outermost serialization structure used by the offline domain join apis.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="97a0a-105">Syntax</span></span>

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a><span data-ttu-id="97a0a-106">成員</span><span class="sxs-lookup"><span data-stu-id="97a0a-106">Members</span></span>

### <a name="ulversion"></a><span data-ttu-id="97a0a-107">ulVersion</span><span class="sxs-lookup"><span data-stu-id="97a0a-107">ulVersion</span></span>

<span data-ttu-id="97a0a-108">這必須設定為1。</span><span class="sxs-lookup"><span data-stu-id="97a0a-108">This must be set to 1.</span></span>

### <a name="ulcblobs"></a><span data-ttu-id="97a0a-109">ulcBlobs</span><span class="sxs-lookup"><span data-stu-id="97a0a-109">ulcBlobs</span></span>

<span data-ttu-id="97a0a-110">這必須設定為 pBlobs 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="97a0a-110">This must be set to the number of elements in the pBlobs array.</span></span>

### <a name="pblobs"></a><span data-ttu-id="97a0a-111">pBlobs</span><span class="sxs-lookup"><span data-stu-id="97a0a-111">pBlobs</span></span>

<span data-ttu-id="97a0a-112">指向 ODJ_BLOB 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="97a0a-112">Points to an array of ODJ_BLOB structures.</span></span>

## <a name="see-also"></a><span data-ttu-id="97a0a-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97a0a-113">See also</span></span>

[<span data-ttu-id="97a0a-114">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="97a0a-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="97a0a-115">**ODJ \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="97a0a-115">**ODJ\_BLOB**</span></span>](odj-odj_blob.md)


