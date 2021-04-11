---
title: DS-執行-意圖-編寫擴充許可權
description: 必須授與資料分割容器的 Control 存取權限，以允許在網域重新命名中使用 Rendom.exe 或準備作業。
ms.assetid: 39e9e76c-55c5-4514-ad4d-102844bcbc5a
ms.tgt_platform: multiple
keywords:
- DS-執行意圖-編寫擴充的正確 AD 架構
topic_type:
- apiref
api_name:
- DS-Execute-Intentions-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b34765db2063688ccc8fced0a1e25cac23b98ded
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108249"
---
# <a name="ds-execute-intentions-script-extended-right"></a><span data-ttu-id="8e6b0-104">DS-執行-意圖-編寫擴充許可權</span><span class="sxs-lookup"><span data-stu-id="8e6b0-104">DS-Execute-Intentions-Script extended right</span></span>

<span data-ttu-id="8e6b0-105">必須授與資料分割容器的 Control 存取權限，以允許在網域重新命名中使用 Rendom.exe 或準備作業。</span><span class="sxs-lookup"><span data-stu-id="8e6b0-105">Control access right, which should be granted to the partitions container, that allows the Rendom.exe or prepare operation to be used in a domain rename.</span></span> <span data-ttu-id="8e6b0-106">此控制項存取權也會在執行 Rendom.exe 或執行步驟作業時，顯示為僅限審核許可權。</span><span class="sxs-lookup"><span data-stu-id="8e6b0-106">This control access right also appears as an audit-only right when the Rendom.exe or execute step operation is performed.</span></span>



| <span data-ttu-id="8e6b0-107">進入</span><span class="sxs-lookup"><span data-stu-id="8e6b0-107">Entry</span></span> | <span data-ttu-id="8e6b0-108">值</span><span class="sxs-lookup"><span data-stu-id="8e6b0-108">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="8e6b0-109">CN</span><span class="sxs-lookup"><span data-stu-id="8e6b0-109">CN</span></span>           | <span data-ttu-id="8e6b0-110">DS-執行-意圖-腳本</span><span class="sxs-lookup"><span data-stu-id="8e6b0-110">DS-Execute-Intentions-Script</span></span>         |
| <span data-ttu-id="8e6b0-111">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8e6b0-111">Display-Name</span></span> | <span data-ttu-id="8e6b0-112">執行樹系更新腳本</span><span class="sxs-lookup"><span data-stu-id="8e6b0-112">Execute Forest Update Script</span></span>         |
| <span data-ttu-id="8e6b0-113">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="8e6b0-113">Rights-GUID</span></span>  | <span data-ttu-id="8e6b0-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span><span class="sxs-lookup"><span data-stu-id="8e6b0-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span></span> |



## <a name="implementations"></a><span data-ttu-id="8e6b0-115">實作</span><span class="sxs-lookup"><span data-stu-id="8e6b0-115">Implementations</span></span>

-   [<span data-ttu-id="8e6b0-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e6b0-117">**亞當**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8e6b0-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e6b0-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e6b0-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e6b0-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8e6b0-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e6b0-122">Windows Server 2003</span></span>



| <span data-ttu-id="8e6b0-123">進入</span><span class="sxs-lookup"><span data-stu-id="8e6b0-123">Entry</span></span> | <span data-ttu-id="8e6b0-124">值</span><span class="sxs-lookup"><span data-stu-id="8e6b0-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e6b0-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e6b0-125">Applies-To</span></span>              | [<span data-ttu-id="8e6b0-126">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-126">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8e6b0-127">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8e6b0-127">Localization-Display-ID</span></span> | <span data-ttu-id="8e6b0-128">66</span><span class="sxs-lookup"><span data-stu-id="8e6b0-128">66</span></span>                                                            |



## <a name="adam"></a><span data-ttu-id="8e6b0-129">亞當</span><span class="sxs-lookup"><span data-stu-id="8e6b0-129">ADAM</span></span>



| <span data-ttu-id="8e6b0-130">進入</span><span class="sxs-lookup"><span data-stu-id="8e6b0-130">Entry</span></span> | <span data-ttu-id="8e6b0-131">值</span><span class="sxs-lookup"><span data-stu-id="8e6b0-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e6b0-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e6b0-132">Applies-To</span></span>              | [<span data-ttu-id="8e6b0-133">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-133">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8e6b0-134">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8e6b0-134">Localization-Display-ID</span></span> | <span data-ttu-id="8e6b0-135">66</span><span class="sxs-lookup"><span data-stu-id="8e6b0-135">66</span></span>                                                            |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e6b0-136">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e6b0-136">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e6b0-137">進入</span><span class="sxs-lookup"><span data-stu-id="8e6b0-137">Entry</span></span> | <span data-ttu-id="8e6b0-138">值</span><span class="sxs-lookup"><span data-stu-id="8e6b0-138">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e6b0-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e6b0-139">Applies-To</span></span>              | [<span data-ttu-id="8e6b0-140">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-140">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8e6b0-141">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8e6b0-141">Localization-Display-ID</span></span> | <span data-ttu-id="8e6b0-142">66</span><span class="sxs-lookup"><span data-stu-id="8e6b0-142">66</span></span>                                                            |



## <a name="windows-server-2008"></a><span data-ttu-id="8e6b0-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e6b0-143">Windows Server 2008</span></span>



| <span data-ttu-id="8e6b0-144">進入</span><span class="sxs-lookup"><span data-stu-id="8e6b0-144">Entry</span></span> | <span data-ttu-id="8e6b0-145">值</span><span class="sxs-lookup"><span data-stu-id="8e6b0-145">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e6b0-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e6b0-146">Applies-To</span></span>              | [<span data-ttu-id="8e6b0-147">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-147">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8e6b0-148">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8e6b0-148">Localization-Display-ID</span></span> | <span data-ttu-id="8e6b0-149">66</span><span class="sxs-lookup"><span data-stu-id="8e6b0-149">66</span></span>                                                            |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e6b0-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e6b0-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e6b0-151">進入</span><span class="sxs-lookup"><span data-stu-id="8e6b0-151">Entry</span></span> | <span data-ttu-id="8e6b0-152">值</span><span class="sxs-lookup"><span data-stu-id="8e6b0-152">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e6b0-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e6b0-153">Applies-To</span></span>              | [<span data-ttu-id="8e6b0-154">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8e6b0-155">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8e6b0-155">Localization-Display-ID</span></span> | <span data-ttu-id="8e6b0-156">66</span><span class="sxs-lookup"><span data-stu-id="8e6b0-156">66</span></span>                                                            |



## <a name="windows-server-2012"></a><span data-ttu-id="8e6b0-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e6b0-157">Windows Server 2012</span></span>



| <span data-ttu-id="8e6b0-158">進入</span><span class="sxs-lookup"><span data-stu-id="8e6b0-158">Entry</span></span> | <span data-ttu-id="8e6b0-159">值</span><span class="sxs-lookup"><span data-stu-id="8e6b0-159">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e6b0-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="8e6b0-160">Applies-To</span></span>              | [<span data-ttu-id="8e6b0-161">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="8e6b0-161">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="8e6b0-162">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="8e6b0-162">Localization-Display-ID</span></span> | <span data-ttu-id="8e6b0-163">66</span><span class="sxs-lookup"><span data-stu-id="8e6b0-163">66</span></span>                                                            |



 

 





