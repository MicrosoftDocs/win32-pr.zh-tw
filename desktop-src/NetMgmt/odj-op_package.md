---
title: OP_PACKAGE
description: OP_PACKAGE IDL 定義
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "106991113"
---
# <a name="op_package-structure"></a><span data-ttu-id="fba9d-103">OP_PACKAGE 結構</span><span class="sxs-lookup"><span data-stu-id="fba9d-103">OP_PACKAGE structure</span></span>

<span data-ttu-id="fba9d-104">包含包含序列化 OP_PACKAGE_COLLECTION 的結構。</span><span class="sxs-lookup"><span data-stu-id="fba9d-104">Contains a structure that contains a serialized OP_PACKAGE_COLLECTION.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba9d-105">語法</span><span class="sxs-lookup"><span data-stu-id="fba9d-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a><span data-ttu-id="fba9d-106">成員</span><span class="sxs-lookup"><span data-stu-id="fba9d-106">Members</span></span>

### <a name="encryptiontype"></a><span data-ttu-id="fba9d-107">EncryptionType</span><span class="sxs-lookup"><span data-stu-id="fba9d-107">EncryptionType</span></span>

<span data-ttu-id="fba9d-108">保留供日後使用，且必須設定為 GUID_Null。</span><span class="sxs-lookup"><span data-stu-id="fba9d-108">Reserved for future use and MUST be set to GUID_NULL.</span></span>

### <a name="encryptioncontext"></a><span data-ttu-id="fba9d-109">EncryptionCoNtext</span><span class="sxs-lookup"><span data-stu-id="fba9d-109">EncryptionContext</span></span>

<span data-ttu-id="fba9d-110">保留供日後使用，且必須設定為全部為零。</span><span class="sxs-lookup"><span data-stu-id="fba9d-110">Reserved for future use and MUST be set to all zeros.</span></span>

### <a name="wrappedpartcollection"></a><span data-ttu-id="fba9d-111">WrappedPartCollection</span><span class="sxs-lookup"><span data-stu-id="fba9d-111">WrappedPartCollection</span></span>

<span data-ttu-id="fba9d-112">包含序列化 OP_PACKAGE_COLLECTION 結構的 OP_BLOB 結構。</span><span class="sxs-lookup"><span data-stu-id="fba9d-112">An OP_BLOB structure that contains a serialized OP_PACKAGE_COLLECTION structure.</span></span>

### <a name="cbdecryptedpartcollection"></a><span data-ttu-id="fba9d-113">cbDecryptedPartCollection</span><span class="sxs-lookup"><span data-stu-id="fba9d-113">cbDecryptedPartCollection</span></span>

<span data-ttu-id="fba9d-114">保留供日後使用，且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="fba9d-114">Reserved for future use and MUST be set to zero.</span></span>

### <a name="extension"></a><span data-ttu-id="fba9d-115">分機</span><span class="sxs-lookup"><span data-stu-id="fba9d-115">Extension</span></span>

<span data-ttu-id="fba9d-116">保留供日後使用，且必須設定為全部為零。</span><span class="sxs-lookup"><span data-stu-id="fba9d-116">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="fba9d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fba9d-117">See also</span></span>

[<span data-ttu-id="fba9d-118">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="fba9d-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="fba9d-119">**OP \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="fba9d-119">**OP\_BLOB**</span></span>](odj-op_blob.md)

[<span data-ttu-id="fba9d-120">**OP \_ 套件 \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="fba9d-120">**OP\_PACKAGE\_COLLECTION**</span></span>](odj-op_package_collection.md)
