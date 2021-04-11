---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART IDL 定義
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104093480"
---
# <a name="op_joinprov2_part-structure"></a><span data-ttu-id="9c131-103">OP_JOINPROV2_PART 結構</span><span class="sxs-lookup"><span data-stu-id="9c131-103">OP_JOINPROV2_PART structure</span></span>

<span data-ttu-id="9c131-104">包含用來設定加入網域之用戶端的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="9c131-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c131-105">語法</span><span class="sxs-lookup"><span data-stu-id="9c131-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a><span data-ttu-id="9c131-106">成員</span><span class="sxs-lookup"><span data-stu-id="9c131-106">Members</span></span>

### <a name="dwflags"></a><span data-ttu-id="9c131-107">dwFlags</span><span class="sxs-lookup"><span data-stu-id="9c131-107">dwFlags</span></span>

<span data-ttu-id="9c131-108">必須設定為零或下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="9c131-108">Must be set to either zero or one of the following values:</span></span>

|<span data-ttu-id="9c131-109">值</span><span class="sxs-lookup"><span data-stu-id="9c131-109">Value</span></span>|<span data-ttu-id="9c131-110">意義</span><span class="sxs-lookup"><span data-stu-id="9c131-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="9c131-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="9c131-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span></span>|<span data-ttu-id="9c131-112">在 lpSiteName 中指定的網站必須被視為用戶端的永久網站。</span><span class="sxs-lookup"><span data-stu-id="9c131-112">The site specified in lpSiteName MUST be considered the permanent site for the client.</span></span>|

### <a name="lpnetbiosname"></a><span data-ttu-id="9c131-113">lpNetbiosName</span><span class="sxs-lookup"><span data-stu-id="9c131-113">lpNetbiosName</span></span>

<span data-ttu-id="9c131-114">包含 Unicode 格式之電腦帳戶的 Netbios 名稱。</span><span class="sxs-lookup"><span data-stu-id="9c131-114">Contains the Netbios name of the machine account in Unicode format.</span></span>

### <a name="lpsitename"></a><span data-ttu-id="9c131-115">lpSiteName</span><span class="sxs-lookup"><span data-stu-id="9c131-115">lpSiteName</span></span>

<span data-ttu-id="9c131-116">包含用戶端應使用之 Active Directory 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c131-116">Contains the name of the Active Directory site that the client should use.</span></span>

### <a name="lpprimarydnsdomain"></a><span data-ttu-id="9c131-117">lpPrimaryDNSDomain</span><span class="sxs-lookup"><span data-stu-id="9c131-117">lpPrimaryDNSDomain</span></span>

<span data-ttu-id="9c131-118">包含用戶端應使用的主要 DNS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="9c131-118">Contains the primary DNS domain name that the client should use.</span></span>

### <a name="dwreserved"></a><span data-ttu-id="9c131-119">>dwreserved</span><span class="sxs-lookup"><span data-stu-id="9c131-119">dwReserved</span></span>

<span data-ttu-id="9c131-120">保留供日後使用，且必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="9c131-120">Reserved for future use and must be set to 0.</span></span>

### <a name="lpreserved"></a><span data-ttu-id="9c131-121">lpReserved</span><span class="sxs-lookup"><span data-stu-id="9c131-121">lpReserved</span></span>

<span data-ttu-id="9c131-122">保留供日後使用，且必須設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="9c131-122">Reserved for future use and must be set to NULL.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c131-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c131-123">See also</span></span>

[<span data-ttu-id="9c131-124">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="9c131-124">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
