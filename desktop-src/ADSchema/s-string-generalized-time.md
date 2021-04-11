---
title: " (一般化時間) 語法的字串"
description: 由 ASN. 1 標準定義的時間字串格式。 | (一般化時間) 語法的字串
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- 字串 (一般化時間) 語法 AD 架構
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195945"
---
# <a name="stringgeneralized-time-syntax"></a><span data-ttu-id="25426-105"> (一般化時間) 語法的字串</span><span class="sxs-lookup"><span data-stu-id="25426-105">String(Generalized-Time) syntax</span></span>

<span data-ttu-id="25426-106">由 ASN. 1 標準定義的時間字串格式。</span><span class="sxs-lookup"><span data-stu-id="25426-106">A time string format defined by ASN.1 standards.</span></span> <span data-ttu-id="25426-107">使用此語法，以 Generalized-Time 格式儲存時間值。</span><span class="sxs-lookup"><span data-stu-id="25426-107">Use this syntax for storing time values in Generalized-Time format.</span></span>

<span data-ttu-id="25426-108">Generalized-Time 語法的格式為 "YYYYMMDDHHMMSS.FFFFFF. 0Z"。</span><span class="sxs-lookup"><span data-stu-id="25426-108">The format for the Generalized-Time syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="25426-109">可接受值的範例是「20010928060000.0 Z」。</span><span class="sxs-lookup"><span data-stu-id="25426-109">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="25426-110">"Z" 表示沒有時間差異。</span><span class="sxs-lookup"><span data-stu-id="25426-110">The "Z" indicates no time differential.</span></span> <span data-ttu-id="25426-111">Active Directory 將日期/時間儲存為格林威治標準時間 (GMT) 。</span><span class="sxs-lookup"><span data-stu-id="25426-111">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="25426-112">如果未指定時間差異，則預設值為 GMT。</span><span class="sxs-lookup"><span data-stu-id="25426-112">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="25426-113">如果時間是在 GMT 以外的時區中指定，則時區與 gmt 之間的差異會附加至字串，而不是 "yyyymmddhhmmss.ffffff. 0 HHMM" 格式的 "Z" \[ +/- \] 。</span><span class="sxs-lookup"><span data-stu-id="25426-113">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="25426-114">可接受值的範例是 "20010928060000.0 + 0200"。</span><span class="sxs-lookup"><span data-stu-id="25426-114">An example of an acceptable value is "20010928060000.0+0200".</span></span> <span data-ttu-id="25426-115">差異是以公式： GMT = Local + 差異為基礎。</span><span class="sxs-lookup"><span data-stu-id="25426-115">The differential is based on the formula: GMT=Local+differential.</span></span>

<span data-ttu-id="25426-116">如需詳細資訊，請參閱 ISO 8601 和 X680。</span><span class="sxs-lookup"><span data-stu-id="25426-116">For more information, see ISO 8601 and X680.</span></span>



| <span data-ttu-id="25426-117">進入</span><span class="sxs-lookup"><span data-stu-id="25426-117">Entry</span></span> | <span data-ttu-id="25426-118">值</span><span class="sxs-lookup"><span data-stu-id="25426-118">Value</span></span> |
|--------------|----------------------------------------------------------------------------|
| <span data-ttu-id="25426-119">名稱</span><span class="sxs-lookup"><span data-stu-id="25426-119">Name</span></span>         | <span data-ttu-id="25426-120">String(Generalized-Time)</span><span class="sxs-lookup"><span data-stu-id="25426-120">String(Generalized-Time)</span></span>                                                   |
| <span data-ttu-id="25426-121">語法識別碼</span><span class="sxs-lookup"><span data-stu-id="25426-121">Syntax ID</span></span>    | <span data-ttu-id="25426-122">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="25426-122">2.5.5.11</span></span>                                                                   |
| <span data-ttu-id="25426-123">OM 識別碼</span><span class="sxs-lookup"><span data-stu-id="25426-123">OM ID</span></span>        | <span data-ttu-id="25426-124">24</span><span class="sxs-lookup"><span data-stu-id="25426-124">24</span></span>                                                                         |
| <span data-ttu-id="25426-125">MAPI 類型</span><span class="sxs-lookup"><span data-stu-id="25426-125">MAPI Type</span></span>    | <span data-ttu-id="25426-126">SYSTIME</span><span class="sxs-lookup"><span data-stu-id="25426-126">SYSTIME</span></span>                                                                    |
| <span data-ttu-id="25426-127">ADS 類型</span><span class="sxs-lookup"><span data-stu-id="25426-127">ADS Type</span></span>     | <span data-ttu-id="25426-128">ADSTYPE \_ UTC \_ 時間</span><span class="sxs-lookup"><span data-stu-id="25426-128">ADSTYPE\_UTC\_TIME</span></span>                                                         |
| <span data-ttu-id="25426-129">Variant 類型</span><span class="sxs-lookup"><span data-stu-id="25426-129">Variant Type</span></span> | <span data-ttu-id="25426-130">VT \_ 日期</span><span class="sxs-lookup"><span data-stu-id="25426-130">VT\_DATE</span></span>                                                                   |
| <span data-ttu-id="25426-131">SDS 類型</span><span class="sxs-lookup"><span data-stu-id="25426-131">SDS Type</span></span>     | [<span data-ttu-id="25426-132">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="25426-132">System.DateTime</span></span>](/dotnet/api/system.datetime) |



## <a name="see-also"></a><span data-ttu-id="25426-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25426-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25426-134">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="25426-134">System.DateTime</span></span>](/dotnet/api/system.datetime)
</dt> </dl>

 

 
