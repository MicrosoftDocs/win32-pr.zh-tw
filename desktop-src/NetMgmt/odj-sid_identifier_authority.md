---
title: SID_IDENTIFIER_AUTHORITY
description: SID_IDENTIFIER_AUTHORITY IDL 定義
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104093483"
---
# <a name="sid_identifier_authority-structure"></a><span data-ttu-id="6f0fd-103">SID_IDENTIFIER_AUTHORITY 結構</span><span class="sxs-lookup"><span data-stu-id="6f0fd-103">SID_IDENTIFIER_AUTHORITY structure</span></span>

<span data-ttu-id="6f0fd-104">包含 SID 識別碼授權單位。</span><span class="sxs-lookup"><span data-stu-id="6f0fd-104">Contains a SID identifier authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f0fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="6f0fd-105">Syntax</span></span>

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a><span data-ttu-id="6f0fd-106">成員</span><span class="sxs-lookup"><span data-stu-id="6f0fd-106">Members</span></span>

### <a name="value"></a><span data-ttu-id="6f0fd-107">值</span><span class="sxs-lookup"><span data-stu-id="6f0fd-107">Value</span></span>

<span data-ttu-id="6f0fd-108">必須設定為 SID 識別碼授權單位的六個位元組。</span><span class="sxs-lookup"><span data-stu-id="6f0fd-108">Must be set to the six bytes of the SID identifier authority.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f0fd-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f0fd-109">See also</span></span>

[<span data-ttu-id="6f0fd-110">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="6f0fd-110">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)