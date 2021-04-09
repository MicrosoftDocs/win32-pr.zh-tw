---
title: 判斷電腦上的位版本
description: 若要判斷用戶端電腦上的位版本，請檢查 QMgr.dll 的版本。
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671440"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a><span data-ttu-id="1e912-103">判斷電腦上的位版本</span><span class="sxs-lookup"><span data-stu-id="1e912-103">Determining the Version of BITS on a Computer</span></span>

<span data-ttu-id="1e912-104">若要判斷用戶端電腦上的位版本，請檢查 QMgr.dll 的版本。</span><span class="sxs-lookup"><span data-stu-id="1e912-104">To determine the version of BITS on the client computer, check the version of QMgr.dll.</span></span> <span data-ttu-id="1e912-105">若要尋找 DLL 的版本號碼：</span><span class="sxs-lookup"><span data-stu-id="1e912-105">To find the version number of the DLL:</span></span>

-   <span data-ttu-id="1e912-106">在% windir% System32 中找出 QMgr.dll \\ 。</span><span class="sxs-lookup"><span data-stu-id="1e912-106">Locate QMgr.dll in %windir%\\System32.</span></span>
-   <span data-ttu-id="1e912-107">以滑鼠右鍵按一下 QMgr.dll，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="1e912-107">Right-click QMgr.dll and click **Properties**.</span></span>
-   <span data-ttu-id="1e912-108">按一下 [ **版本** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="1e912-108">Click the **Version** tab.</span></span>
-   <span data-ttu-id="1e912-109">記下版本號碼。</span><span class="sxs-lookup"><span data-stu-id="1e912-109">Note the version number.</span></span>

<span data-ttu-id="1e912-110">您也可以使用下列 PowerShell 程式碼來判斷您系統上的 .dll 版本：</span><span class="sxs-lookup"><span data-stu-id="1e912-110">You can also use the following PowerShell code to determine the version of the .dll on your system:</span></span>

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

<span data-ttu-id="1e912-111">如果 DLL 也存在於% windir% \\ System32 \\ 位中，請重複上述步驟。</span><span class="sxs-lookup"><span data-stu-id="1e912-111">If the DLL also exists in %windir%\\System32\\Bits, repeat the previous steps.</span></span> <span data-ttu-id="1e912-112">BITS 使用具有較高版本號碼的 DLL。</span><span class="sxs-lookup"><span data-stu-id="1e912-112">BITS uses the DLL with the higher version number.</span></span>

<span data-ttu-id="1e912-113">下表列出 BITS 的版本及其對應的 QMgr.dll 檔案版本號碼。</span><span class="sxs-lookup"><span data-stu-id="1e912-113">The following table lists the versions of BITS and their corresponding QMgr.dll file version numbers.</span></span>



| <span data-ttu-id="1e912-114">BITS 版本</span><span class="sxs-lookup"><span data-stu-id="1e912-114">BITS version</span></span> | <span data-ttu-id="1e912-115">QMgr.dll 檔案版本號碼</span><span class="sxs-lookup"><span data-stu-id="1e912-115">QMgr.dll file version number</span></span> |
|--------------|------------------------------|
| <span data-ttu-id="1e912-116">BITS 10。1</span><span class="sxs-lookup"><span data-stu-id="1e912-116">BITS 10.1</span></span>    | <span data-ttu-id="1e912-117">7.8. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-117">7.8.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-118">BITS 5。0</span><span class="sxs-lookup"><span data-stu-id="1e912-118">BITS 5.0</span></span>     | <span data-ttu-id="1e912-119">7.7. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-119">7.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-120">BITS 4。0</span><span class="sxs-lookup"><span data-stu-id="1e912-120">BITS 4.0</span></span>     | <span data-ttu-id="1e912-121">7.5. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-121">7.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-122">BITS 3。0</span><span class="sxs-lookup"><span data-stu-id="1e912-122">BITS 3.0</span></span>     | <span data-ttu-id="1e912-123">7.0. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-123">7.0.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-124">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="1e912-124">BITS 2.5</span></span>     | <span data-ttu-id="1e912-125">6.7. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-125">6.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-126">BITS 2。0</span><span class="sxs-lookup"><span data-stu-id="1e912-126">BITS 2.0</span></span>     | <span data-ttu-id="1e912-127">6.6. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-127">6.6.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-128">BITS 1。5</span><span class="sxs-lookup"><span data-stu-id="1e912-128">BITS 1.5</span></span>     | <span data-ttu-id="1e912-129">6.5. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-129">6.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-130">BITS 1。2</span><span class="sxs-lookup"><span data-stu-id="1e912-130">BITS 1.2</span></span>     | <span data-ttu-id="1e912-131">6.2. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-131">6.2.xxxx.xxxx</span></span>                |
| <span data-ttu-id="1e912-132">BITS 1。0</span><span class="sxs-lookup"><span data-stu-id="1e912-132">BITS 1.0</span></span>     | <span data-ttu-id="1e912-133">6.0. xxxx</span><span class="sxs-lookup"><span data-stu-id="1e912-133">6.0.xxxx.xxxx</span></span>                |



 

<span data-ttu-id="1e912-134">您也可以使用符號類別識別碼來判斷電腦上已註冊的位版本。</span><span class="sxs-lookup"><span data-stu-id="1e912-134">You can also use the symbolic class identifiers to determine the version of BITS that is registered on the computer.</span></span> <span data-ttu-id="1e912-135">下表列出 BITS 的版本及其對應的符號類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e912-135">The following table lists the versions of BITS and their corresponding symbolic class identifiers.</span></span> <span data-ttu-id="1e912-136">如果未註冊類別， **CoCreateInstance** 函數會傳回 **REGDB \_ E \_ CLASSNOTREG** 。</span><span class="sxs-lookup"><span data-stu-id="1e912-136">The **CoCreateInstance** function returns **REGDB\_E\_CLASSNOTREG** if the class is not registered.</span></span>



| <span data-ttu-id="1e912-137">BITS 版本</span><span class="sxs-lookup"><span data-stu-id="1e912-137">BITS version</span></span>  | <span data-ttu-id="1e912-138">符號類別識別碼</span><span class="sxs-lookup"><span data-stu-id="1e912-138">Symbolic class identifier</span></span>         |
|---------------|-----------------------------------|
| <span data-ttu-id="1e912-139">BITS 10。1</span><span class="sxs-lookup"><span data-stu-id="1e912-139">BITS 10.1</span></span>     | <span data-ttu-id="1e912-140">CLSID \_ BackgroundCopyManager10 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1e912-140">CLSID\_BackgroundCopyManager10\_1</span></span> |
| <span data-ttu-id="1e912-141">BITS 5。0</span><span class="sxs-lookup"><span data-stu-id="1e912-141">BITS 5.0</span></span>      | <span data-ttu-id="1e912-142">CLSID \_ BackgroundCopyManager5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1e912-142">CLSID\_BackgroundCopyManager5\_0</span></span>  |
| <span data-ttu-id="1e912-143">BITS 4。0</span><span class="sxs-lookup"><span data-stu-id="1e912-143">BITS 4.0</span></span>      | <span data-ttu-id="1e912-144">CLSID \_ BackgroundCopyManager4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1e912-144">CLSID\_BackgroundCopyManager4\_0</span></span>  |
| <span data-ttu-id="1e912-145">BITS 3。0</span><span class="sxs-lookup"><span data-stu-id="1e912-145">BITS 3.0</span></span>      | <span data-ttu-id="1e912-146">CLSID \_ BackgroundCopyManager3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1e912-146">CLSID\_BackgroundCopyManager3\_0</span></span>  |
| <span data-ttu-id="1e912-147">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="1e912-147">BITS 2.5</span></span>      | <span data-ttu-id="1e912-148">CLSID \_ BackgroundCopyManager2 \_ 5</span><span class="sxs-lookup"><span data-stu-id="1e912-148">CLSID\_BackgroundCopyManager2\_5</span></span>  |
| <span data-ttu-id="1e912-149">BITS 2。0</span><span class="sxs-lookup"><span data-stu-id="1e912-149">BITS 2.0</span></span>      | <span data-ttu-id="1e912-150">CLSID \_ BackgroundCopyManager2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1e912-150">CLSID\_BackgroundCopyManager2\_0</span></span>  |
| <span data-ttu-id="1e912-151">BITS 1。5</span><span class="sxs-lookup"><span data-stu-id="1e912-151">BITS 1.5</span></span>      | <span data-ttu-id="1e912-152">CLSID \_ BackgroundCopyManager1 \_ 5</span><span class="sxs-lookup"><span data-stu-id="1e912-152">CLSID\_BackgroundCopyManager1\_5</span></span>  |
| <span data-ttu-id="1e912-153">位1.2、1。0</span><span class="sxs-lookup"><span data-stu-id="1e912-153">BITS 1.2, 1.0</span></span> | <span data-ttu-id="1e912-154">CLSID \_ BackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="1e912-154">CLSID\_BackgroundCopyManager</span></span>      |



 

 

 




