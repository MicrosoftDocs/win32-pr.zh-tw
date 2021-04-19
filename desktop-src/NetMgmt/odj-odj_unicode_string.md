---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING IDL 定義
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "106966276"
---
# <a name="odj_unicode_string-structure"></a><span data-ttu-id="9a5c2-103">ODJ_UNICODE_STRING 結構</span><span class="sxs-lookup"><span data-stu-id="9a5c2-103">ODJ_UNICODE_STRING structure</span></span>

<span data-ttu-id="9a5c2-104">包含 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="9a5c2-104">Contains a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5c2-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a5c2-105">Syntax</span></span>

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a><span data-ttu-id="9a5c2-106">成員</span><span class="sxs-lookup"><span data-stu-id="9a5c2-106">Members</span></span>

### <a name="length"></a><span data-ttu-id="9a5c2-107">長度</span><span class="sxs-lookup"><span data-stu-id="9a5c2-107">Length</span></span>

<span data-ttu-id="9a5c2-108">必須設定為包含字串的緩衝區中的位元組數目，不包括 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="9a5c2-108">Must be set to the number of bytes in Buffer containing the string, not including the NULL terminator.</span></span>

### <a name="maximumlength"></a><span data-ttu-id="9a5c2-109">MaximumLength</span><span class="sxs-lookup"><span data-stu-id="9a5c2-109">MaximumLength</span></span>

<span data-ttu-id="9a5c2-110">這必須設定為緩衝區中的總位元組數，不包括 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="9a5c2-110">This MUST be set to the total number of bytes in Buffer, not including the NULL terminator.</span></span>

### <a name="buffer"></a><span data-ttu-id="9a5c2-111">Buffer</span><span class="sxs-lookup"><span data-stu-id="9a5c2-111">Buffer</span></span>

<span data-ttu-id="9a5c2-112">必須為 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="9a5c2-112">Must be a Unicode string.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a5c2-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a5c2-113">See also</span></span>

[<span data-ttu-id="9a5c2-114">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="9a5c2-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
