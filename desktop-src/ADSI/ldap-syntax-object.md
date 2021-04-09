---
title: LDAP 語法物件
description: LDAP 提供者會使用 LDAP 語法和 ADSI 語法之間的下列對應。
ms.assetid: a82cf8ab-9591-4489-87a6-ccfab0e01d61
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、服務提供者、將語法對應到 LDAP 語法
- 將 ADSI 語法對應到 LDAP 語法 ADSI
- 從 ADSI 到 LDAP ADSI 的語法和對應
- LDAP 服務提供者 ADSI，將 ADSI 語法對應到 LDAP 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2272a0805ec32fd7ade9c4584feefb64fb1467f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092197"
---
# <a name="ldap-syntax-object"></a><span data-ttu-id="e9f0b-107">LDAP 語法物件</span><span class="sxs-lookup"><span data-stu-id="e9f0b-107">LDAP Syntax Object</span></span>

<span data-ttu-id="e9f0b-108">LDAP 提供者會使用 LDAP 語法和 ADSI 語法之間的下列對應。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-108">The LDAP provider uses the following mapping between the LDAP syntax and ADSI syntax.</span></span>



| <span data-ttu-id="e9f0b-109">LDAP 語法</span><span class="sxs-lookup"><span data-stu-id="e9f0b-109">LDAP Syntax</span></span>   | <span data-ttu-id="e9f0b-110">ADSI 語法 (Automation) </span><span class="sxs-lookup"><span data-stu-id="e9f0b-110">ADSI Syntax (Automation)</span></span>            |
|---------------|-------------------------------------|
| <span data-ttu-id="e9f0b-111">ADsPath</span><span class="sxs-lookup"><span data-stu-id="e9f0b-111">ADsPath</span></span>       | <span data-ttu-id="e9f0b-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-112">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="e9f0b-113">Boolean</span></span>       | <span data-ttu-id="e9f0b-114">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="e9f0b-114">VT\_BOOL</span></span>                            |
| <span data-ttu-id="e9f0b-115">計數器</span><span class="sxs-lookup"><span data-stu-id="e9f0b-115">Counter</span></span>       | <span data-ttu-id="e9f0b-116">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e9f0b-116">VT\_I4</span></span>                              |
| <span data-ttu-id="e9f0b-117">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e9f0b-117">EmailAddress</span></span>  | <span data-ttu-id="e9f0b-118">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-118">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-119">FaxNumber</span><span class="sxs-lookup"><span data-stu-id="e9f0b-119">FaxNumber</span></span>     | <span data-ttu-id="e9f0b-120">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-120">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-121">整數</span><span class="sxs-lookup"><span data-stu-id="e9f0b-121">Integer</span></span>       | <span data-ttu-id="e9f0b-122">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e9f0b-122">VT\_I4</span></span>                              |
| <span data-ttu-id="e9f0b-123">間隔</span><span class="sxs-lookup"><span data-stu-id="e9f0b-123">Interval</span></span>      | <span data-ttu-id="e9f0b-124">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e9f0b-124">VT\_I4</span></span>                              |
| <span data-ttu-id="e9f0b-125">List</span><span class="sxs-lookup"><span data-stu-id="e9f0b-125">List</span></span>          | <span data-ttu-id="e9f0b-126">VT \_ VARIANT (vt \_ BSTR \| vt \_ 陣列) </span><span class="sxs-lookup"><span data-stu-id="e9f0b-126">VT\_VARIANT (VT\_BSTR \| VT\_ARRAY)</span></span> |
| <span data-ttu-id="e9f0b-127">NetAddress</span><span class="sxs-lookup"><span data-stu-id="e9f0b-127">NetAddress</span></span>    | <span data-ttu-id="e9f0b-128">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-128">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-129">OctetString</span><span class="sxs-lookup"><span data-stu-id="e9f0b-129">OctetString</span></span>   | <span data-ttu-id="e9f0b-130">VT \_ 變異</span><span class="sxs-lookup"><span data-stu-id="e9f0b-130">VT\_VARIANT</span></span>                         |
| <span data-ttu-id="e9f0b-131">路徑</span><span class="sxs-lookup"><span data-stu-id="e9f0b-131">Path</span></span>          | <span data-ttu-id="e9f0b-132">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-132">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-133">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="e9f0b-133">PhoneNumber</span></span>   | <span data-ttu-id="e9f0b-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-134">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-135">PostalAddress</span><span class="sxs-lookup"><span data-stu-id="e9f0b-135">PostalAddress</span></span> | <span data-ttu-id="e9f0b-136">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-136">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-137">SmallInterval</span><span class="sxs-lookup"><span data-stu-id="e9f0b-137">SmallInterval</span></span> | <span data-ttu-id="e9f0b-138">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e9f0b-138">VT\_I4</span></span>                              |
| <span data-ttu-id="e9f0b-139">String</span><span class="sxs-lookup"><span data-stu-id="e9f0b-139">String</span></span>        | <span data-ttu-id="e9f0b-140">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e9f0b-140">VT\_BSTR</span></span>                            |
| <span data-ttu-id="e9f0b-141">Time</span><span class="sxs-lookup"><span data-stu-id="e9f0b-141">Time</span></span>          | <span data-ttu-id="e9f0b-142">VT \_ 日期</span><span class="sxs-lookup"><span data-stu-id="e9f0b-142">VT\_DATE</span></span>                            |



 

 

 




