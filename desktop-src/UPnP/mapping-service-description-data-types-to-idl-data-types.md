---
title: 將服務描述資料類型對應至 IDL 資料類型
description: 下表顯示在服務描述中指定的 XML 資料類型與 IDL 中所使用之對應資料類型的對應。
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021911"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a><span data-ttu-id="1af4b-103">將服務描述資料類型對應至 IDL 資料類型</span><span class="sxs-lookup"><span data-stu-id="1af4b-103">Mapping Service Description Data Types to IDL Data Types</span></span>

<span data-ttu-id="1af4b-104">下表顯示在服務描述中指定的 XML 資料類型與 IDL 中所使用之對應資料類型的對應。</span><span class="sxs-lookup"><span data-stu-id="1af4b-104">The following table shows the mapping of XML data types specified in a service description to the corresponding data types used in IDL.</span></span>



| <span data-ttu-id="1af4b-105">XML 資料類型</span><span class="sxs-lookup"><span data-stu-id="1af4b-105">XML Data Type</span></span> | <span data-ttu-id="1af4b-106">IDL 資料類型</span><span class="sxs-lookup"><span data-stu-id="1af4b-106">IDL Data Type</span></span>  |
|---------------|----------------|
| <span data-ttu-id="1af4b-107">bin.base64</span><span class="sxs-lookup"><span data-stu-id="1af4b-107">bin.base64</span></span>    | <span data-ttu-id="1af4b-108">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="1af4b-108">SAFEARRAY</span></span>      |
| <span data-ttu-id="1af4b-109">bin.hex</span><span class="sxs-lookup"><span data-stu-id="1af4b-109">bin.hex</span></span>       | <span data-ttu-id="1af4b-110">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="1af4b-110">SAFEARRAY</span></span>      |
| <span data-ttu-id="1af4b-111">boolean</span><span class="sxs-lookup"><span data-stu-id="1af4b-111">boolean</span></span>       | <span data-ttu-id="1af4b-112">VARIANT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="1af4b-112">VARIANT\_BOOL</span></span>  |
| <span data-ttu-id="1af4b-113">char</span><span class="sxs-lookup"><span data-stu-id="1af4b-113">char</span></span>          | <span data-ttu-id="1af4b-114">wchar \_ t</span><span class="sxs-lookup"><span data-stu-id="1af4b-114">wchar\_t</span></span>       |
| <span data-ttu-id="1af4b-115">date</span><span class="sxs-lookup"><span data-stu-id="1af4b-115">date</span></span>          | <span data-ttu-id="1af4b-116">日期</span><span class="sxs-lookup"><span data-stu-id="1af4b-116">DATE</span></span>           |
| <span data-ttu-id="1af4b-117">dateTime</span><span class="sxs-lookup"><span data-stu-id="1af4b-117">dateTime</span></span>      | <span data-ttu-id="1af4b-118">日期</span><span class="sxs-lookup"><span data-stu-id="1af4b-118">DATE</span></span>           |
| <span data-ttu-id="1af4b-119">dateTime.tz</span><span class="sxs-lookup"><span data-stu-id="1af4b-119">dateTime.tz</span></span>   | <span data-ttu-id="1af4b-120">日期</span><span class="sxs-lookup"><span data-stu-id="1af4b-120">DATE</span></span>           |
| <span data-ttu-id="1af4b-121">fixed.14.4</span><span class="sxs-lookup"><span data-stu-id="1af4b-121">fixed.14.4</span></span>    | <span data-ttu-id="1af4b-122">CY</span><span class="sxs-lookup"><span data-stu-id="1af4b-122">CY</span></span>             |
| <span data-ttu-id="1af4b-123">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1af4b-123">float</span></span>         | <span data-ttu-id="1af4b-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1af4b-124">float</span></span>          |
| <span data-ttu-id="1af4b-125">i1</span><span class="sxs-lookup"><span data-stu-id="1af4b-125">i1</span></span>            | <span data-ttu-id="1af4b-126">char</span><span class="sxs-lookup"><span data-stu-id="1af4b-126">char</span></span>           |
| <span data-ttu-id="1af4b-127">i2</span><span class="sxs-lookup"><span data-stu-id="1af4b-127">i2</span></span>            | <span data-ttu-id="1af4b-128">short</span><span class="sxs-lookup"><span data-stu-id="1af4b-128">short</span></span>          |
| <span data-ttu-id="1af4b-129">i4</span><span class="sxs-lookup"><span data-stu-id="1af4b-129">i4</span></span>            | <span data-ttu-id="1af4b-130">long</span><span class="sxs-lookup"><span data-stu-id="1af4b-130">long</span></span>           |
| <span data-ttu-id="1af4b-131">int</span><span class="sxs-lookup"><span data-stu-id="1af4b-131">int</span></span>           | <span data-ttu-id="1af4b-132">long</span><span class="sxs-lookup"><span data-stu-id="1af4b-132">long</span></span>           |
| <span data-ttu-id="1af4b-133">number</span><span class="sxs-lookup"><span data-stu-id="1af4b-133">number</span></span>        | <span data-ttu-id="1af4b-134">BSTR</span><span class="sxs-lookup"><span data-stu-id="1af4b-134">BSTR</span></span>           |
| <span data-ttu-id="1af4b-135">r4</span><span class="sxs-lookup"><span data-stu-id="1af4b-135">r4</span></span>            | <span data-ttu-id="1af4b-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1af4b-136">float</span></span>          |
| <span data-ttu-id="1af4b-137">r8</span><span class="sxs-lookup"><span data-stu-id="1af4b-137">r8</span></span>            | <span data-ttu-id="1af4b-138">double</span><span class="sxs-lookup"><span data-stu-id="1af4b-138">double</span></span>         |
| <span data-ttu-id="1af4b-139">字串</span><span class="sxs-lookup"><span data-stu-id="1af4b-139">string</span></span>        | <span data-ttu-id="1af4b-140">BSTR</span><span class="sxs-lookup"><span data-stu-id="1af4b-140">BSTR</span></span>           |
| <span data-ttu-id="1af4b-141">time</span><span class="sxs-lookup"><span data-stu-id="1af4b-141">time</span></span>          | <span data-ttu-id="1af4b-142">日期</span><span class="sxs-lookup"><span data-stu-id="1af4b-142">DATE</span></span>           |
| <span data-ttu-id="1af4b-143">time.tz</span><span class="sxs-lookup"><span data-stu-id="1af4b-143">time.tz</span></span>       | <span data-ttu-id="1af4b-144">日期</span><span class="sxs-lookup"><span data-stu-id="1af4b-144">DATE</span></span>           |
| <span data-ttu-id="1af4b-145">ui1</span><span class="sxs-lookup"><span data-stu-id="1af4b-145">ui1</span></span>           | <span data-ttu-id="1af4b-146">unsigned char</span><span class="sxs-lookup"><span data-stu-id="1af4b-146">unsigned char</span></span>  |
| <span data-ttu-id="1af4b-147">ui2</span><span class="sxs-lookup"><span data-stu-id="1af4b-147">ui2</span></span>           | <span data-ttu-id="1af4b-148">unsigned short</span><span class="sxs-lookup"><span data-stu-id="1af4b-148">unsigned short</span></span> |
| <span data-ttu-id="1af4b-149">ui4</span><span class="sxs-lookup"><span data-stu-id="1af4b-149">ui4</span></span>           | <span data-ttu-id="1af4b-150">unsigned long</span><span class="sxs-lookup"><span data-stu-id="1af4b-150">unsigned long</span></span>  |
| <span data-ttu-id="1af4b-151">uri</span><span class="sxs-lookup"><span data-stu-id="1af4b-151">uri</span></span>           | <span data-ttu-id="1af4b-152">BSTR</span><span class="sxs-lookup"><span data-stu-id="1af4b-152">BSTR</span></span>           |
| <span data-ttu-id="1af4b-153">uuid</span><span class="sxs-lookup"><span data-stu-id="1af4b-153">uuid</span></span>          | <span data-ttu-id="1af4b-154">BSTR</span><span class="sxs-lookup"><span data-stu-id="1af4b-154">BSTR</span></span>           |



 

 

 




