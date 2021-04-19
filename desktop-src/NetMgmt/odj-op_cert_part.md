---
title: OP_CERT_PART
description: OP_CERT_PART IDL 定義
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "106966482"
---
# <a name="op_cert_part-structure"></a><span data-ttu-id="ef053-103">OP_CERT_PART 結構</span><span class="sxs-lookup"><span data-stu-id="ef053-103">OP_CERT_PART structure</span></span>

<span data-ttu-id="ef053-104">包含已序列化的 PFX 和憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="ef053-104">Contains serialized PFX and certificate stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef053-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef053-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a><span data-ttu-id="ef053-106">成員</span><span class="sxs-lookup"><span data-stu-id="ef053-106">Members</span></span>

### <a name="cpfxstores"></a><span data-ttu-id="ef053-107">cPfxStores</span><span class="sxs-lookup"><span data-stu-id="ef053-107">cPfxStores</span></span>

<span data-ttu-id="ef053-108">包含 pPfxStores 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="ef053-108">Contains the number of elements in pPfxStores.</span></span>

### <a name="ppfxstores"></a><span data-ttu-id="ef053-109">pPfxStores</span><span class="sxs-lookup"><span data-stu-id="ef053-109">pPfxStores</span></span>

<span data-ttu-id="ef053-110">包含 OP_CERT_PFX_STORE 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="ef053-110">Contains an array of OP_CERT_PFX_STORE structures.</span></span>

### <a name="csststores"></a><span data-ttu-id="ef053-111">cSstStores</span><span class="sxs-lookup"><span data-stu-id="ef053-111">cSstStores</span></span>

<span data-ttu-id="ef053-112">包含 pSstStores 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="ef053-112">Contains the number of elements in pSstStores.</span></span>

### <a name="psststores"></a><span data-ttu-id="ef053-113">pSstStores</span><span class="sxs-lookup"><span data-stu-id="ef053-113">pSstStores</span></span>

<span data-ttu-id="ef053-114">包含 OP_CERT_SST_STORE 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="ef053-114">Contains an array of OP_CERT_SST_STORE structures.</span></span>

### <a name="extension"></a><span data-ttu-id="ef053-115">分機</span><span class="sxs-lookup"><span data-stu-id="ef053-115">Extension</span></span>

<span data-ttu-id="ef053-116">保留供日後使用，且必須包含所有的零。</span><span class="sxs-lookup"><span data-stu-id="ef053-116">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef053-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef053-117">See also</span></span>

[<span data-ttu-id="ef053-118">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="ef053-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="ef053-119">**OP \_ CERT \_ PFX \_ 存放區**</span><span class="sxs-lookup"><span data-stu-id="ef053-119">**OP\_CERT\_PFX\_STORE**</span></span>](odj-op_cert_pfx_store.md)

[<span data-ttu-id="ef053-120">**OP \_ CERT \_ .SST \_ STORE**</span><span class="sxs-lookup"><span data-stu-id="ef053-120">**OP\_CERT\_SST\_STORE**</span></span>](odj-op_cert_sst_store.md)

[<span data-ttu-id="ef053-121">**OP \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="ef053-121">**OP\_BLOB**</span></span>](odj-op_blob.md)

