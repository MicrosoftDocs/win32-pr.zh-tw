---
title: 將 Active Directory 語法對應至 ADSI 語法
description: 下表會將 Active Directory 語法對應至其對應的 ADSI 語法。
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- 屬性 ADSI、將 Active Directory 語法對應至 ADSI 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966376"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a><span data-ttu-id="57245-104">將 Active Directory 語法對應至 ADSI 語法</span><span class="sxs-lookup"><span data-stu-id="57245-104">Mapping Active Directory Syntax to ADSI Syntax</span></span>

<span data-ttu-id="57245-105">下表會將 Active Directory 語法對應至其對應的 ADSI 語法。</span><span class="sxs-lookup"><span data-stu-id="57245-105">The following table maps the Active Directory syntaxes to their corresponding ADSI syntaxes.</span></span>



| <span data-ttu-id="57245-106">屬性語法識別碼</span><span class="sxs-lookup"><span data-stu-id="57245-106">Attribute syntax ID</span></span> | <span data-ttu-id="57245-107">Active Directory 語法類型</span><span class="sxs-lookup"><span data-stu-id="57245-107">Active Directory syntax type</span></span>             | <span data-ttu-id="57245-108">相等的 ADSI 語法類型</span><span class="sxs-lookup"><span data-stu-id="57245-108">Equivalent ADSI syntax type</span></span>                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="57245-109">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="57245-109">2.5.5.1</span></span><br/>  | <span data-ttu-id="57245-110">DN 字串</span><span class="sxs-lookup"><span data-stu-id="57245-110">DN String</span></span><br/>                     | <span data-ttu-id="57245-111">DN 字串</span><span class="sxs-lookup"><span data-stu-id="57245-111">DN String</span></span><br/>                                                |
| <span data-ttu-id="57245-112">2.5.5.2</span><span class="sxs-lookup"><span data-stu-id="57245-112">2.5.5.2</span></span><br/>  | <span data-ttu-id="57245-113">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="57245-113">Object ID</span></span><br/>                     | <span data-ttu-id="57245-114">CaseIgnore 字串</span><span class="sxs-lookup"><span data-stu-id="57245-114">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="57245-115">2.5.5.3</span><span class="sxs-lookup"><span data-stu-id="57245-115">2.5.5.3</span></span><br/>  | <span data-ttu-id="57245-116">區分大小寫的字串</span><span class="sxs-lookup"><span data-stu-id="57245-116">Case Sensitive String</span></span><br/>         | <span data-ttu-id="57245-117">CaseExact 字串</span><span class="sxs-lookup"><span data-stu-id="57245-117">CaseExact String</span></span><br/>                                         |
| <span data-ttu-id="57245-118">2.5.5.4</span><span class="sxs-lookup"><span data-stu-id="57245-118">2.5.5.4</span></span><br/>  | <span data-ttu-id="57245-119">略過 Case 字串</span><span class="sxs-lookup"><span data-stu-id="57245-119">Case Ignored String</span></span><br/>           | <span data-ttu-id="57245-120">CaseIgnore 字串</span><span class="sxs-lookup"><span data-stu-id="57245-120">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="57245-121">2.5.5.5</span><span class="sxs-lookup"><span data-stu-id="57245-121">2.5.5.5</span></span><br/>  | <span data-ttu-id="57245-122">列印案例字串</span><span class="sxs-lookup"><span data-stu-id="57245-122">Print Case String</span></span><br/>             | <span data-ttu-id="57245-123">可列印字串</span><span class="sxs-lookup"><span data-stu-id="57245-123">Printable String</span></span><br/>                                         |
| <span data-ttu-id="57245-124">2.5.5.6</span><span class="sxs-lookup"><span data-stu-id="57245-124">2.5.5.6</span></span><br/>  | <span data-ttu-id="57245-125">數值字串</span><span class="sxs-lookup"><span data-stu-id="57245-125">Numeric String</span></span><br/>                | <span data-ttu-id="57245-126">數值字串</span><span class="sxs-lookup"><span data-stu-id="57245-126">Numeric String</span></span><br/>                                           |
| <span data-ttu-id="57245-127">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="57245-127">2.5.5.7</span></span><br/>  | <span data-ttu-id="57245-128">**或** 名稱 DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="57245-128">**OR** Name DNWithOctetString</span></span><br/> | <span data-ttu-id="57245-129">不支援</span><span class="sxs-lookup"><span data-stu-id="57245-129">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="57245-130">2.5.5.8</span><span class="sxs-lookup"><span data-stu-id="57245-130">2.5.5.8</span></span><br/>  | <span data-ttu-id="57245-131">布林值</span><span class="sxs-lookup"><span data-stu-id="57245-131">Boolean</span></span><br/>                       | <span data-ttu-id="57245-132">布林值</span><span class="sxs-lookup"><span data-stu-id="57245-132">Boolean</span></span><br/>                                                  |
| <span data-ttu-id="57245-133">2.5.5.9</span><span class="sxs-lookup"><span data-stu-id="57245-133">2.5.5.9</span></span><br/>  | <span data-ttu-id="57245-134">整數</span><span class="sxs-lookup"><span data-stu-id="57245-134">Integer</span></span><br/>                       | <span data-ttu-id="57245-135">整數</span><span class="sxs-lookup"><span data-stu-id="57245-135">Integer</span></span><br/>                                                  |
| <span data-ttu-id="57245-136">2.5.5.10</span><span class="sxs-lookup"><span data-stu-id="57245-136">2.5.5.10</span></span><br/> | <span data-ttu-id="57245-137">八位字串</span><span class="sxs-lookup"><span data-stu-id="57245-137">Octet String</span></span><br/>                  | <span data-ttu-id="57245-138">八位字串</span><span class="sxs-lookup"><span data-stu-id="57245-138">Octet String</span></span><br/>                                             |
| <span data-ttu-id="57245-139">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="57245-139">2.5.5.11</span></span><br/> | <span data-ttu-id="57245-140">Time</span><span class="sxs-lookup"><span data-stu-id="57245-140">Time</span></span><br/>                          | <span data-ttu-id="57245-141">UTC 時間</span><span class="sxs-lookup"><span data-stu-id="57245-141">UTC Time</span></span><br/>                                                 |
| <span data-ttu-id="57245-142">2.5.5.12</span><span class="sxs-lookup"><span data-stu-id="57245-142">2.5.5.12</span></span><br/> | <span data-ttu-id="57245-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="57245-143">Unicode</span></span><br/>                       | <span data-ttu-id="57245-144">Case 忽略字串</span><span class="sxs-lookup"><span data-stu-id="57245-144">Case Ignore String</span></span><br/>                                       |
| <span data-ttu-id="57245-145">2.5.5.13</span><span class="sxs-lookup"><span data-stu-id="57245-145">2.5.5.13</span></span><br/> | <span data-ttu-id="57245-146">位址</span><span class="sxs-lookup"><span data-stu-id="57245-146">Address</span></span><br/>                       | <span data-ttu-id="57245-147">不支援</span><span class="sxs-lookup"><span data-stu-id="57245-147">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="57245-148">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="57245-148">2.5.5.14</span></span><br/> | <span data-ttu-id="57245-149">Distname-Address</span><span class="sxs-lookup"><span data-stu-id="57245-149">Distname-Address</span></span><br/>              |                                                                     |
| <span data-ttu-id="57245-150">2.5.5.15</span><span class="sxs-lookup"><span data-stu-id="57245-150">2.5.5.15</span></span><br/> | <span data-ttu-id="57245-151">NT 安全描述項</span><span class="sxs-lookup"><span data-stu-id="57245-151">NT Security Descriptor</span></span><br/>        | [<span data-ttu-id="57245-152">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="57245-152">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| <span data-ttu-id="57245-153">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="57245-153">2.5.5.16</span></span><br/> | <span data-ttu-id="57245-154">大型整數</span><span class="sxs-lookup"><span data-stu-id="57245-154">Large Integer</span></span><br/>                 | [<span data-ttu-id="57245-155">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="57245-155">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| <span data-ttu-id="57245-156">2.5.5.17</span><span class="sxs-lookup"><span data-stu-id="57245-156">2.5.5.17</span></span><br/> | <span data-ttu-id="57245-157">SID</span><span class="sxs-lookup"><span data-stu-id="57245-157">SID</span></span><br/>                           | <span data-ttu-id="57245-158">八位字串</span><span class="sxs-lookup"><span data-stu-id="57245-158">Octet String</span></span><br/>                                             |



 

 

 





