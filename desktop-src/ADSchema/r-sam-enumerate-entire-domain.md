---
title: SAM-列舉-整個定義域擴充許可權
description: 您可以使用這個 control 存取權限來限制誰可以使用舊版 API，例如 NetQueryDisplayInformation 和 NetUser/GroupEnum，以及列舉整個網域。
ms.assetid: d29e94f3-efaf-4a86-909c-88bd34abcf6c
ms.tgt_platform: multiple
keywords:
- SAM-列舉-整個網域擴充的正確 AD 架構
topic_type:
- apiref
api_name:
- SAM-Enumerate-Entire-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3683b6b6396295a88c66bfc333bf226aa42faa0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106985"
---
# <a name="sam-enumerate-entire-domain-extended-right"></a><span data-ttu-id="34f3a-104">SAM-列舉-整個定義域擴充許可權</span><span class="sxs-lookup"><span data-stu-id="34f3a-104">SAM-Enumerate-Entire-Domain extended right</span></span>

<span data-ttu-id="34f3a-105">您可以使用這個 control 存取權限來限制誰可以使用舊版 API，例如 NetQueryDisplayInformation 和 NetUser/GroupEnum，以及列舉整個網域。</span><span class="sxs-lookup"><span data-stu-id="34f3a-105">This control access right can be used to restrict who can be allowed to use a downlevel API, such as NetQueryDisplayInformation and NetUser/GroupEnum, and enumerate the entire domain.</span></span>



| <span data-ttu-id="34f3a-106">進入</span><span class="sxs-lookup"><span data-stu-id="34f3a-106">Entry</span></span> | <span data-ttu-id="34f3a-107">值</span><span class="sxs-lookup"><span data-stu-id="34f3a-107">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="34f3a-108">CN</span><span class="sxs-lookup"><span data-stu-id="34f3a-108">CN</span></span>           | <span data-ttu-id="34f3a-109">SAM-列舉-整個網域</span><span class="sxs-lookup"><span data-stu-id="34f3a-109">SAM-Enumerate-Entire-Domain</span></span>          |
| <span data-ttu-id="34f3a-110">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="34f3a-110">Display-Name</span></span> | <span data-ttu-id="34f3a-111">列舉整個 SAM 網域</span><span class="sxs-lookup"><span data-stu-id="34f3a-111">Enumerate Entire SAM Domain</span></span>          |
| <span data-ttu-id="34f3a-112">許可權-GUID</span><span class="sxs-lookup"><span data-stu-id="34f3a-112">Rights-GUID</span></span>  | <span data-ttu-id="34f3a-113">91d67418-0135-4acc-8d79-c08e857cfbec</span><span class="sxs-lookup"><span data-stu-id="34f3a-113">91d67418-0135-4acc-8d79-c08e857cfbec</span></span> |



## <a name="implementations"></a><span data-ttu-id="34f3a-114">實作</span><span class="sxs-lookup"><span data-stu-id="34f3a-114">Implementations</span></span>

-   [<span data-ttu-id="34f3a-115">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="34f3a-115">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="34f3a-116">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="34f3a-116">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="34f3a-117">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="34f3a-117">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="34f3a-118">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="34f3a-118">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="34f3a-119">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="34f3a-119">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="34f3a-120">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34f3a-120">Windows Server 2003</span></span>



| <span data-ttu-id="34f3a-121">進入</span><span class="sxs-lookup"><span data-stu-id="34f3a-121">Entry</span></span> | <span data-ttu-id="34f3a-122">值</span><span class="sxs-lookup"><span data-stu-id="34f3a-122">Value</span></span> |
|-------------------------|----------------------------------------------|
| <span data-ttu-id="34f3a-123">Applies-To</span><span class="sxs-lookup"><span data-stu-id="34f3a-123">Applies-To</span></span>              | [<span data-ttu-id="34f3a-124">**Sam-伺服器**</span><span class="sxs-lookup"><span data-stu-id="34f3a-124">**Sam-Server**</span></span>](c-samserver.md)<br/> |
| <span data-ttu-id="34f3a-125">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="34f3a-125">Localization-Display-ID</span></span> | <span data-ttu-id="34f3a-126">57</span><span class="sxs-lookup"><span data-stu-id="34f3a-126">57</span></span>                                           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="34f3a-127">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="34f3a-127">Windows Server 2003 R2</span></span>



| <span data-ttu-id="34f3a-128">進入</span><span class="sxs-lookup"><span data-stu-id="34f3a-128">Entry</span></span> | <span data-ttu-id="34f3a-129">值</span><span class="sxs-lookup"><span data-stu-id="34f3a-129">Value</span></span> |
|-------------------------|----------------------------------------------|
| <span data-ttu-id="34f3a-130">Applies-To</span><span class="sxs-lookup"><span data-stu-id="34f3a-130">Applies-To</span></span>              | [<span data-ttu-id="34f3a-131">**Sam-伺服器**</span><span class="sxs-lookup"><span data-stu-id="34f3a-131">**Sam-Server**</span></span>](c-samserver.md)<br/> |
| <span data-ttu-id="34f3a-132">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="34f3a-132">Localization-Display-ID</span></span> | <span data-ttu-id="34f3a-133">57</span><span class="sxs-lookup"><span data-stu-id="34f3a-133">57</span></span>                                           |



## <a name="windows-server-2008"></a><span data-ttu-id="34f3a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34f3a-134">Windows Server 2008</span></span>



| <span data-ttu-id="34f3a-135">進入</span><span class="sxs-lookup"><span data-stu-id="34f3a-135">Entry</span></span> | <span data-ttu-id="34f3a-136">值</span><span class="sxs-lookup"><span data-stu-id="34f3a-136">Value</span></span> |
|-------------------------|----------------------------------------------|
| <span data-ttu-id="34f3a-137">Applies-To</span><span class="sxs-lookup"><span data-stu-id="34f3a-137">Applies-To</span></span>              | [<span data-ttu-id="34f3a-138">**Sam-伺服器**</span><span class="sxs-lookup"><span data-stu-id="34f3a-138">**Sam-Server**</span></span>](c-samserver.md)<br/> |
| <span data-ttu-id="34f3a-139">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="34f3a-139">Localization-Display-ID</span></span> | <span data-ttu-id="34f3a-140">57</span><span class="sxs-lookup"><span data-stu-id="34f3a-140">57</span></span>                                           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="34f3a-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34f3a-141">Windows Server 2008 R2</span></span>



| <span data-ttu-id="34f3a-142">進入</span><span class="sxs-lookup"><span data-stu-id="34f3a-142">Entry</span></span> | <span data-ttu-id="34f3a-143">值</span><span class="sxs-lookup"><span data-stu-id="34f3a-143">Value</span></span> |
|-------------------------|----------------------------------------------|
| <span data-ttu-id="34f3a-144">Applies-To</span><span class="sxs-lookup"><span data-stu-id="34f3a-144">Applies-To</span></span>              | [<span data-ttu-id="34f3a-145">**Sam-伺服器**</span><span class="sxs-lookup"><span data-stu-id="34f3a-145">**Sam-Server**</span></span>](c-samserver.md)<br/> |
| <span data-ttu-id="34f3a-146">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="34f3a-146">Localization-Display-ID</span></span> | <span data-ttu-id="34f3a-147">57</span><span class="sxs-lookup"><span data-stu-id="34f3a-147">57</span></span>                                           |



## <a name="windows-server-2012"></a><span data-ttu-id="34f3a-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34f3a-148">Windows Server 2012</span></span>



| <span data-ttu-id="34f3a-149">進入</span><span class="sxs-lookup"><span data-stu-id="34f3a-149">Entry</span></span> | <span data-ttu-id="34f3a-150">值</span><span class="sxs-lookup"><span data-stu-id="34f3a-150">Value</span></span> |
|-------------------------|----------------------------------------------|
| <span data-ttu-id="34f3a-151">Applies-To</span><span class="sxs-lookup"><span data-stu-id="34f3a-151">Applies-To</span></span>              | [<span data-ttu-id="34f3a-152">**Sam-伺服器**</span><span class="sxs-lookup"><span data-stu-id="34f3a-152">**Sam-Server**</span></span>](c-samserver.md)<br/> |
| <span data-ttu-id="34f3a-153">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="34f3a-153">Localization-Display-ID</span></span> | <span data-ttu-id="34f3a-154">57</span><span class="sxs-lookup"><span data-stu-id="34f3a-154">57</span></span>                                           |



 

 





