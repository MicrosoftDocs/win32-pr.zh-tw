---
title: ODJ_BLOB
description: ODJ_BLOB IDL 定義
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104463889"
---
# <a name="odj_blob-structure"></a><span data-ttu-id="9667f-103">ODJ_BLOB 結構</span><span class="sxs-lookup"><span data-stu-id="9667f-103">ODJ_BLOB structure</span></span>

<span data-ttu-id="9667f-104">指定包含序列化 ODJ_WIN7BLOB 結構或序列化 OP_PACKAGE 結構的結構。</span><span class="sxs-lookup"><span data-stu-id="9667f-104">Specifies a structure containing either a serialized ODJ_WIN7BLOB structure or a serialized OP_PACKAGE structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9667f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9667f-105">Syntax</span></span>

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a><span data-ttu-id="9667f-106">成員</span><span class="sxs-lookup"><span data-stu-id="9667f-106">Members</span></span>

### <a name="ulodjformat"></a><span data-ttu-id="9667f-107">ulODJFormat</span><span class="sxs-lookup"><span data-stu-id="9667f-107">ulODJFormat</span></span>

<span data-ttu-id="9667f-108">指定結構的邏輯版本，且必須設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="9667f-108">Specifies the logical version of the structure and must be set to one of the following values:</span></span>

|<span data-ttu-id="9667f-109">值</span><span class="sxs-lookup"><span data-stu-id="9667f-109">Value</span></span>|<span data-ttu-id="9667f-110">意義</span><span class="sxs-lookup"><span data-stu-id="9667f-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="9667f-111">ODJ_WIN7_FORMAT (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="9667f-111">ODJ_WIN7_FORMAT (0x00000001)</span></span>|<span data-ttu-id="9667f-112">PBlob 中包含的位元組必須包含序列化的 ODJ_WIN7_BLOB 結構。</span><span class="sxs-lookup"><span data-stu-id="9667f-112">The bytes contained in pBlob must contain a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="9667f-113">ODJ_WIN8_FORMAT (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="9667f-113">ODJ_WIN8_FORMAT (0x00000002)</span></span>|<span data-ttu-id="9667f-114">PBlob 中包含的位元組必須包含序列化的 OP_PACKAGE 結構。</span><span class="sxs-lookup"><span data-stu-id="9667f-114">The bytes contained in pBlob must contain a serialized OP_PACKAGE structure.</span></span>|

### <a name="cbblob"></a><span data-ttu-id="9667f-115">cbBlob</span><span class="sxs-lookup"><span data-stu-id="9667f-115">cbBlob</span></span>

<span data-ttu-id="9667f-116">這必須設定為 pBlob 陣列中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9667f-116">This must be set to the number of bytes in the pBlob array.</span></span>

### <a name="pblob"></a><span data-ttu-id="9667f-117">pBlob</span><span class="sxs-lookup"><span data-stu-id="9667f-117">pBlob</span></span>

<span data-ttu-id="9667f-118">指向包含序列化結構的位元組緩衝區（如上述 ulODJFormat 所指定）。</span><span class="sxs-lookup"><span data-stu-id="9667f-118">Points to a byte buffer containing a serialized structure as specified by ulODJFormat above.</span></span>

## <a name="see-also"></a><span data-ttu-id="9667f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9667f-119">See also</span></span>

[<span data-ttu-id="9667f-120">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="9667f-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

