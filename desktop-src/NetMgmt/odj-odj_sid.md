---
title: ODJ_SID
description: ODJ_SID IDL 定義
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104024283"
---
# <a name="odj_sid-structure"></a><span data-ttu-id="c7c26-103">ODJ_SID 結構</span><span class="sxs-lookup"><span data-stu-id="c7c26-103">ODJ_SID structure</span></span>

<span data-ttu-id="c7c26-104">包含 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7c26-104">Contains a Security Identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c26-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7c26-105">Syntax</span></span>

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a><span data-ttu-id="c7c26-106">成員</span><span class="sxs-lookup"><span data-stu-id="c7c26-106">Members</span></span>

### <a name="revision"></a><span data-ttu-id="c7c26-107">修訂版</span><span class="sxs-lookup"><span data-stu-id="c7c26-107">Revision</span></span>

<span data-ttu-id="c7c26-108">必須設定為 SID 修訂。</span><span class="sxs-lookup"><span data-stu-id="c7c26-108">Must be set to the SID revision.</span></span>

### <a name="subauthoritycount"></a><span data-ttu-id="c7c26-109">SubAuthorityCount</span><span class="sxs-lookup"><span data-stu-id="c7c26-109">SubAuthorityCount</span></span>

<span data-ttu-id="c7c26-110">必須設定為 SubAuthority 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c7c26-110">Must be set to the number of elements in SubAuthority.</span></span>

### <a name="identifierauthority"></a><span data-ttu-id="c7c26-111">IdentifierAuthority</span><span class="sxs-lookup"><span data-stu-id="c7c26-111">IdentifierAuthority</span></span>

<span data-ttu-id="c7c26-112">必須設定為 SID 授權單位識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7c26-112">Must be set to the SID authority identifier.</span></span>

### <a name="subauthority"></a><span data-ttu-id="c7c26-113">SubAuthority</span><span class="sxs-lookup"><span data-stu-id="c7c26-113">SubAuthority</span></span>

<span data-ttu-id="c7c26-114">必須包含 SID 子授權陣列。</span><span class="sxs-lookup"><span data-stu-id="c7c26-114">Must contain an array of SID sub authorities.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7c26-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7c26-115">See also</span></span>

[<span data-ttu-id="c7c26-116">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="c7c26-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="c7c26-117">**ODJ \_ SID \_ 識別碼 \_ 授權單位**</span><span class="sxs-lookup"><span data-stu-id="c7c26-117">**ODJ\_SID\_IDENTIFIER\_AUTHORITY**</span></span>](odj-sid_identifier_authority.md)
