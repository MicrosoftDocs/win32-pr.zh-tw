---
title: DS-查詢-自我配額擴充許可權
description: 控制存取權限，可讓使用者查詢使用者自己的配額。
ms.assetid: 4cd1523b-8026-454e-9d10-e07d2fb24cea
ms.tgt_platform: multiple
keywords:
- DS-查詢-自我配額擴充的正確 AD 架構
topic_type:
- apiref
api_name:
- DS-Query-Self-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1bd8e0bcfe5de174b0725d7081df641841068f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108245"
---
# <a name="ds-query-self-quota-extended-right"></a><span data-ttu-id="ff562-104">DS-查詢-自我配額擴充許可權</span><span class="sxs-lookup"><span data-stu-id="ff562-104">DS-Query-Self-Quota extended right</span></span>

<span data-ttu-id="ff562-105">控制存取權限，可讓使用者查詢使用者自己的配額。</span><span class="sxs-lookup"><span data-stu-id="ff562-105">Control access right that allows a user to query the user's own quotas.</span></span>



| <span data-ttu-id="ff562-106">進入</span><span class="sxs-lookup"><span data-stu-id="ff562-106">Entry</span></span> | <span data-ttu-id="ff562-107">值</span><span class="sxs-lookup"><span data-stu-id="ff562-107">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="ff562-108">CN</span><span class="sxs-lookup"><span data-stu-id="ff562-108">CN</span></span>           | <span data-ttu-id="ff562-109">DS-查詢-自我配額</span><span class="sxs-lookup"><span data-stu-id="ff562-109">DS-Query-Self-Quota</span></span>                  |
| <span data-ttu-id="ff562-110">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ff562-110">Display-Name</span></span> | <span data-ttu-id="ff562-111">查詢自我配額</span><span class="sxs-lookup"><span data-stu-id="ff562-111">Query Self Quota</span></span>                     |
| <span data-ttu-id="ff562-112">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="ff562-112">Rights-GUID</span></span>  | <span data-ttu-id="ff562-113">4ecc03fe-ffc0-4947-b630-eb672a8a9dbc</span><span class="sxs-lookup"><span data-stu-id="ff562-113">4ecc03fe-ffc0-4947-b630-eb672a8a9dbc</span></span> |



## <a name="implementations"></a><span data-ttu-id="ff562-114">實作</span><span class="sxs-lookup"><span data-stu-id="ff562-114">Implementations</span></span>

-   [<span data-ttu-id="ff562-115">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff562-115">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff562-116">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ff562-116">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ff562-117">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff562-117">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff562-118">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff562-118">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff562-119">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff562-119">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff562-120">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff562-120">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ff562-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff562-121">Windows Server 2003</span></span>



| <span data-ttu-id="ff562-122">進入</span><span class="sxs-lookup"><span data-stu-id="ff562-122">Entry</span></span> | <span data-ttu-id="ff562-123">值</span><span class="sxs-lookup"><span data-stu-id="ff562-123">Value</span></span> |
|-------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff562-124">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ff562-124">Applies-To</span></span>              | [<span data-ttu-id="ff562-125">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="ff562-125">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |
| <span data-ttu-id="ff562-126">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="ff562-126">Localization-Display-ID</span></span> | <span data-ttu-id="ff562-127">71</span><span class="sxs-lookup"><span data-stu-id="ff562-127">71</span></span>                                                                |



## <a name="adam"></a><span data-ttu-id="ff562-128">亞當</span><span class="sxs-lookup"><span data-stu-id="ff562-128">ADAM</span></span>



| <span data-ttu-id="ff562-129">進入</span><span class="sxs-lookup"><span data-stu-id="ff562-129">Entry</span></span> | <span data-ttu-id="ff562-130">值</span><span class="sxs-lookup"><span data-stu-id="ff562-130">Value</span></span> |
|-------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff562-131">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ff562-131">Applies-To</span></span>              | [<span data-ttu-id="ff562-132">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="ff562-132">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |
| <span data-ttu-id="ff562-133">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="ff562-133">Localization-Display-ID</span></span> | <span data-ttu-id="ff562-134">71</span><span class="sxs-lookup"><span data-stu-id="ff562-134">71</span></span>                                                                |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff562-135">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff562-135">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff562-136">進入</span><span class="sxs-lookup"><span data-stu-id="ff562-136">Entry</span></span> | <span data-ttu-id="ff562-137">值</span><span class="sxs-lookup"><span data-stu-id="ff562-137">Value</span></span> |
|-------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff562-138">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ff562-138">Applies-To</span></span>              | [<span data-ttu-id="ff562-139">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="ff562-139">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |
| <span data-ttu-id="ff562-140">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="ff562-140">Localization-Display-ID</span></span> | <span data-ttu-id="ff562-141">71</span><span class="sxs-lookup"><span data-stu-id="ff562-141">71</span></span>                                                                |



## <a name="windows-server-2008"></a><span data-ttu-id="ff562-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff562-142">Windows Server 2008</span></span>



| <span data-ttu-id="ff562-143">進入</span><span class="sxs-lookup"><span data-stu-id="ff562-143">Entry</span></span> | <span data-ttu-id="ff562-144">值</span><span class="sxs-lookup"><span data-stu-id="ff562-144">Value</span></span> |
|-------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff562-145">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ff562-145">Applies-To</span></span>              | [<span data-ttu-id="ff562-146">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="ff562-146">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |
| <span data-ttu-id="ff562-147">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="ff562-147">Localization-Display-ID</span></span> | <span data-ttu-id="ff562-148">71</span><span class="sxs-lookup"><span data-stu-id="ff562-148">71</span></span>                                                                |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff562-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff562-149">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff562-150">進入</span><span class="sxs-lookup"><span data-stu-id="ff562-150">Entry</span></span> | <span data-ttu-id="ff562-151">值</span><span class="sxs-lookup"><span data-stu-id="ff562-151">Value</span></span> |
|-------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff562-152">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ff562-152">Applies-To</span></span>              | [<span data-ttu-id="ff562-153">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="ff562-153">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |
| <span data-ttu-id="ff562-154">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="ff562-154">Localization-Display-ID</span></span> | <span data-ttu-id="ff562-155">71</span><span class="sxs-lookup"><span data-stu-id="ff562-155">71</span></span>                                                                |



## <a name="windows-server-2012"></a><span data-ttu-id="ff562-156">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff562-156">Windows Server 2012</span></span>



| <span data-ttu-id="ff562-157">進入</span><span class="sxs-lookup"><span data-stu-id="ff562-157">Entry</span></span> | <span data-ttu-id="ff562-158">值</span><span class="sxs-lookup"><span data-stu-id="ff562-158">Value</span></span> |
|-------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff562-159">Applies-To</span><span class="sxs-lookup"><span data-stu-id="ff562-159">Applies-To</span></span>              | [<span data-ttu-id="ff562-160">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="ff562-160">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |
| <span data-ttu-id="ff562-161">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="ff562-161">Localization-Display-ID</span></span> | <span data-ttu-id="ff562-162">71</span><span class="sxs-lookup"><span data-stu-id="ff562-162">71</span></span>                                                                |



 

 





