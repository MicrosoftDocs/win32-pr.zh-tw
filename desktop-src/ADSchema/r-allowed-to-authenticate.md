---
title: 允許驗證擴充許可權
description: Control 存取權限可控制誰可以驗證特定的電腦或服務。
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- 允許驗證擴充的正確 AD 架構
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467372"
---
# <a name="allowed-to-authenticate-extended-right"></a><span data-ttu-id="8a99a-104">允許驗證擴充許可權</span><span class="sxs-lookup"><span data-stu-id="8a99a-104">Allowed-To-Authenticate extended right</span></span>

<span data-ttu-id="8a99a-105">Control 存取權限可控制誰可以驗證特定的電腦或服務。</span><span class="sxs-lookup"><span data-stu-id="8a99a-105">The control access right controls who can authenticate to a particular computer or service.</span></span> <span data-ttu-id="8a99a-106">基本上是在電腦、使用者和 InetOrgPerson 物件上。</span><span class="sxs-lookup"><span data-stu-id="8a99a-106">It basically lives on computer, user, and InetOrgPerson objects.</span></span> <span data-ttu-id="8a99a-107">如果整個網域允許存取，它也適用于網域物件。</span><span class="sxs-lookup"><span data-stu-id="8a99a-107">It is also applicable on the domain object if access is allowed for the entire domain.</span></span> <span data-ttu-id="8a99a-108">它可以套用至 Ou，讓使用者能夠在包含一組使用者或電腦物件的 Ou 上設定可繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="8a99a-108">It can be applied to OUs to permit users to be able to set inheritable ACEs on OUs that contain a set of user or computer objects.</span></span>



| <span data-ttu-id="8a99a-109">進入</span><span class="sxs-lookup"><span data-stu-id="8a99a-109">Entry</span></span> | <span data-ttu-id="8a99a-110">值</span><span class="sxs-lookup"><span data-stu-id="8a99a-110">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="8a99a-111">CN</span><span class="sxs-lookup"><span data-stu-id="8a99a-111">CN</span></span>           | <span data-ttu-id="8a99a-112">允許驗證</span><span class="sxs-lookup"><span data-stu-id="8a99a-112">Allowed-To-Authenticate</span></span>              |
| <span data-ttu-id="8a99a-113">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8a99a-113">Display-Name</span></span> | <span data-ttu-id="8a99a-114">允許驗證</span><span class="sxs-lookup"><span data-stu-id="8a99a-114">Allowed to Authenticate</span></span>              |
| <span data-ttu-id="8a99a-115">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="8a99a-115">Rights-GUID</span></span>  | <span data-ttu-id="8a99a-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span><span class="sxs-lookup"><span data-stu-id="8a99a-116">68b1d179-0d15-4d4f-ab71-46152e79a7bc</span></span> |



## <a name="implementations"></a><span data-ttu-id="8a99a-117">實作</span><span class="sxs-lookup"><span data-stu-id="8a99a-117">Implementations</span></span>

-   [<span data-ttu-id="8a99a-118">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a99a-118">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a99a-119">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a99a-119">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a99a-120">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a99a-120">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a99a-121">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a99a-121">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a99a-122">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a99a-122">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8a99a-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a99a-123">Windows Server 2003</span></span>



| <span data-ttu-id="8a99a-124">進入</span><span class="sxs-lookup"><span data-stu-id="8a99a-124">Entry</span></span> | <span data-ttu-id="8a99a-125">值</span><span class="sxs-lookup"><span data-stu-id="8a99a-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a99a-126">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8a99a-126">Applies-To</span></span>              | [<span data-ttu-id="8a99a-127">**電腦**</span><span class="sxs-lookup"><span data-stu-id="8a99a-127">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8a99a-128">**User**</span><span class="sxs-lookup"><span data-stu-id="8a99a-128">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="8a99a-129">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="8a99a-129">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="8a99a-130">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8a99a-130">Localization-Display-ID</span></span> | <span data-ttu-id="8a99a-131">65</span><span class="sxs-lookup"><span data-stu-id="8a99a-131">65</span></span>                                                                                                                              |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a99a-132">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a99a-132">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a99a-133">進入</span><span class="sxs-lookup"><span data-stu-id="8a99a-133">Entry</span></span> | <span data-ttu-id="8a99a-134">值</span><span class="sxs-lookup"><span data-stu-id="8a99a-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a99a-135">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8a99a-135">Applies-To</span></span>              | [<span data-ttu-id="8a99a-136">**電腦**</span><span class="sxs-lookup"><span data-stu-id="8a99a-136">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8a99a-137">**User**</span><span class="sxs-lookup"><span data-stu-id="8a99a-137">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="8a99a-138">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="8a99a-138">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="8a99a-139">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8a99a-139">Localization-Display-ID</span></span> | <span data-ttu-id="8a99a-140">65</span><span class="sxs-lookup"><span data-stu-id="8a99a-140">65</span></span>                                                                                                                              |



## <a name="windows-server-2008"></a><span data-ttu-id="8a99a-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a99a-141">Windows Server 2008</span></span>



| <span data-ttu-id="8a99a-142">進入</span><span class="sxs-lookup"><span data-stu-id="8a99a-142">Entry</span></span> | <span data-ttu-id="8a99a-143">值</span><span class="sxs-lookup"><span data-stu-id="8a99a-143">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a99a-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8a99a-144">Applies-To</span></span>              | [<span data-ttu-id="8a99a-145">**電腦**</span><span class="sxs-lookup"><span data-stu-id="8a99a-145">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8a99a-146">**User**</span><span class="sxs-lookup"><span data-stu-id="8a99a-146">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="8a99a-147">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="8a99a-147">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="8a99a-148">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8a99a-148">Localization-Display-ID</span></span> | <span data-ttu-id="8a99a-149">65</span><span class="sxs-lookup"><span data-stu-id="8a99a-149">65</span></span>                                                                                                                              |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a99a-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a99a-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a99a-151">進入</span><span class="sxs-lookup"><span data-stu-id="8a99a-151">Entry</span></span> | <span data-ttu-id="8a99a-152">值</span><span class="sxs-lookup"><span data-stu-id="8a99a-152">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a99a-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8a99a-153">Applies-To</span></span>              | [<span data-ttu-id="8a99a-154">**電腦**</span><span class="sxs-lookup"><span data-stu-id="8a99a-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8a99a-155">**ms DS 管理-服務-帳戶**</span><span class="sxs-lookup"><span data-stu-id="8a99a-155">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="8a99a-156">**User**</span><span class="sxs-lookup"><span data-stu-id="8a99a-156">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="8a99a-157">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="8a99a-157">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="8a99a-158">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8a99a-158">Localization-Display-ID</span></span> | <span data-ttu-id="8a99a-159">65</span><span class="sxs-lookup"><span data-stu-id="8a99a-159">65</span></span>                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a><span data-ttu-id="8a99a-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a99a-160">Windows Server 2012</span></span>



| <span data-ttu-id="8a99a-161">進入</span><span class="sxs-lookup"><span data-stu-id="8a99a-161">Entry</span></span> | <span data-ttu-id="8a99a-162">值</span><span class="sxs-lookup"><span data-stu-id="8a99a-162">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a99a-163">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8a99a-163">Applies-To</span></span>              | [<span data-ttu-id="8a99a-164">**電腦**</span><span class="sxs-lookup"><span data-stu-id="8a99a-164">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8a99a-165">**ms DS 管理-服務-帳戶**</span><span class="sxs-lookup"><span data-stu-id="8a99a-165">**ms-DS-Managed-Service-Account**</span></span>](c-msds-managedserviceaccount.md)<br/> [<span data-ttu-id="8a99a-166">**User**</span><span class="sxs-lookup"><span data-stu-id="8a99a-166">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="8a99a-167">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="8a99a-167">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> |
| <span data-ttu-id="8a99a-168">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8a99a-168">Localization-Display-ID</span></span> | <span data-ttu-id="8a99a-169">65</span><span class="sxs-lookup"><span data-stu-id="8a99a-169">65</span></span>                                                                                                                                                                                                               |



 

 





