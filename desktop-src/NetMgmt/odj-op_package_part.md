---
title: OP_PACKAGE_PART
description: OP_PACKAGE_PART IDL 定義
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104186645"
---
# <a name="op_package_part-structure"></a><span data-ttu-id="95232-103">OP_PACKAGE_PART 結構</span><span class="sxs-lookup"><span data-stu-id="95232-103">OP_PACKAGE_PART structure</span></span>

<span data-ttu-id="95232-104">定義結構，其中包含 GUID 所識別的資料集。</span><span class="sxs-lookup"><span data-stu-id="95232-104">Defines a structure that contains a data set identified by a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="95232-105">語法</span><span class="sxs-lookup"><span data-stu-id="95232-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a><span data-ttu-id="95232-106">成員</span><span class="sxs-lookup"><span data-stu-id="95232-106">Members</span></span>

### <a name="parttype"></a><span data-ttu-id="95232-107">PartType</span><span class="sxs-lookup"><span data-stu-id="95232-107">PartType</span></span>

<span data-ttu-id="95232-108">識別包含在下表部分的序列化結構：</span><span class="sxs-lookup"><span data-stu-id="95232-108">Identifies the serialized structure contained in Part per the following table:</span></span>

|<span data-ttu-id="95232-109">PartType</span><span class="sxs-lookup"><span data-stu-id="95232-109">PartType</span></span>|<span data-ttu-id="95232-110">意義</span><span class="sxs-lookup"><span data-stu-id="95232-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="95232-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span><span class="sxs-lookup"><span data-stu-id="95232-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span></span>|<span data-ttu-id="95232-112">包含序列化的 ODJ_WIN7_BLOB 結構。</span><span class="sxs-lookup"><span data-stu-id="95232-112">Contains a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="95232-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span><span class="sxs-lookup"><span data-stu-id="95232-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span></span>|<span data-ttu-id="95232-114">包含序列化的 OP_JOIN_PROV2_PART 結構。</span><span class="sxs-lookup"><span data-stu-id="95232-114">Contains a serialized OP_JOIN_PROV2_PART structure.</span></span>|
|<span data-ttu-id="95232-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span><span class="sxs-lookup"><span data-stu-id="95232-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span></span>|<span data-ttu-id="95232-116">包含序列化的 OP_JOIN_PROV3_PART 結構。</span><span class="sxs-lookup"><span data-stu-id="95232-116">Contains a serialized OP_JOIN_PROV3_PART structure.</span></span>|
|<span data-ttu-id="95232-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span><span class="sxs-lookup"><span data-stu-id="95232-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span></span>|<span data-ttu-id="95232-118">包含序列化的 OP_CERT_PART 結構。</span><span class="sxs-lookup"><span data-stu-id="95232-118">Contains a serialized OP_CERT_PART structure.</span></span>|
|<span data-ttu-id="95232-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span><span class="sxs-lookup"><span data-stu-id="95232-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span></span>|<span data-ttu-id="95232-120">包含序列化的 OP_POLICY_PART 結構。</span><span class="sxs-lookup"><span data-stu-id="95232-120">Contains a serialized OP_POLICY_PART structure.</span></span>|

### <a name="ulflags"></a><span data-ttu-id="95232-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="95232-121">ulFlags</span></span>

<span data-ttu-id="95232-122">必須設定為零或多個下列旗標：</span><span class="sxs-lookup"><span data-stu-id="95232-122">Must be set to zero or more of the following flags:</span></span>

|<span data-ttu-id="95232-123">值</span><span class="sxs-lookup"><span data-stu-id="95232-123">Value</span></span>|<span data-ttu-id="95232-124">意義</span><span class="sxs-lookup"><span data-stu-id="95232-124">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="95232-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="95232-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span></span>|<span data-ttu-id="95232-126">此封裝部分視為必要。</span><span class="sxs-lookup"><span data-stu-id="95232-126">This package part is considered essential.</span></span> <span data-ttu-id="95232-127">如果取用者無法辨識此封裝部分或無法成功處理，則整體作業必須失敗。</span><span class="sxs-lookup"><span data-stu-id="95232-127">If the consumer does not recognize this package part or fails to successfully process it, the overall operation must fail.</span></span>|

### <a name="part"></a><span data-ttu-id="95232-128">部分</span><span class="sxs-lookup"><span data-stu-id="95232-128">Part</span></span>

<span data-ttu-id="95232-129">包含 OP_BLOB 結構中的序列化結構。</span><span class="sxs-lookup"><span data-stu-id="95232-129">Contains a serialized structure in an OP_BLOB structure.</span></span> <span data-ttu-id="95232-130">特定結構取決於 PartType。</span><span class="sxs-lookup"><span data-stu-id="95232-130">The specific structure is determined by PartType.</span></span>

### <a name="extension"></a><span data-ttu-id="95232-131">分機</span><span class="sxs-lookup"><span data-stu-id="95232-131">Extension</span></span>

<span data-ttu-id="95232-132">保留供日後使用，且必須設定為全部為零。</span><span class="sxs-lookup"><span data-stu-id="95232-132">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="95232-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95232-133">See also</span></span>

[<span data-ttu-id="95232-134">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="95232-134">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="95232-135">**OP \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="95232-135">**OP\_BLOB**</span></span>](odj-op_blob.md)
