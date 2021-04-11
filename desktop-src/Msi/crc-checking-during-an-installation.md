---
description: Windows Installer 會提供) 檔案 (CRC 的迴圈重複檢查。
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: 安裝期間的 CRC 檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193922"
---
# <a name="crc-checking-during-an-installation"></a><span data-ttu-id="4c889-103">安裝期間的 CRC 檢查</span><span class="sxs-lookup"><span data-stu-id="4c889-103">CRC Checking During an Installation</span></span>

<span data-ttu-id="4c889-104">Windows Installer 會提供) 檔案 (CRC 的迴圈重複檢查。</span><span class="sxs-lookup"><span data-stu-id="4c889-104">A Cyclic Redundancy Check (CRC) of files is available with Windows Installer.</span></span> <span data-ttu-id="4c889-105">CRC 檢查是類似于總和檢查碼的錯誤檢查機制，可讓應用程式判斷檔案中的資訊是否已修改。</span><span class="sxs-lookup"><span data-stu-id="4c889-105">CRC checking is an error-checking mechanism, similar to a checksum, that enables an application to determine whether the information in a file has been modified.</span></span> <span data-ttu-id="4c889-106">在 Windows Installer 完成複製檔案之後，它會從來源和目的地檔案取得 CRC 值。</span><span class="sxs-lookup"><span data-stu-id="4c889-106">After the Windows Installer finishes copying a file, it gets a CRC value from both the source and destination files.</span></span> <span data-ttu-id="4c889-107">安裝程式會將原始的 CRC 戳記簽入檔案中，並將其與從複本計算出來的 CRC 進行比較。</span><span class="sxs-lookup"><span data-stu-id="4c889-107">The installer checks the original CRC stamped into the file and compares this to the CRC calculated from the copy.</span></span> <span data-ttu-id="4c889-108">如果原始 CRC 值為非 null，且與複製上計算的 CRC 不同，CRC 檢查就會失敗。</span><span class="sxs-lookup"><span data-stu-id="4c889-108">The CRC check fails if the original CRC value is non-null and is different from the CRC calculated on the copy.</span></span> <span data-ttu-id="4c889-109">如果原始 CRC 為 null，則不會執行任何檢查。</span><span class="sxs-lookup"><span data-stu-id="4c889-109">If the original CRC is null, no check occurs.</span></span>

<span data-ttu-id="4c889-110">在下列情況下，Windows Installer 會對檔案執行 CRC 檢查：</span><span class="sxs-lookup"><span data-stu-id="4c889-110">The Windows Installer does a CRC check on a file in the following cases:</span></span>

-   <span data-ttu-id="4c889-111">如果已設定 [MSICHECKCRCS 屬性](msicheckcrcs.md) ，而且 **msidbFileAttributesChecksum** 包含在檔案 [資料表](file-table.md)中檔案記錄的 [屬性] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="4c889-111">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md).</span></span> <span data-ttu-id="4c889-112">安裝、複製或移動檔案之後，安裝程式會進行 CRC 檢查一次。</span><span class="sxs-lookup"><span data-stu-id="4c889-112">The installer does the CRC check once after installing, duplicating, or moving the file.</span></span>
-   <span data-ttu-id="4c889-113">如果 [ [MSICHECKCRCS] 屬性](msicheckcrcs.md) 已設定，而且 **msidbFileAttributesChecksum** 包含在檔案的記錄的 [屬性] 欄位中 [，則](file-table.md)安裝程式會在修補檔案之後進行 CRC 檢查。</span><span class="sxs-lookup"><span data-stu-id="4c889-113">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check after patching the file.</span></span>
-   <span data-ttu-id="4c889-114">如果 **msidbFileAttributesChecksum** 包含在檔案的記錄檔中的 [屬性] 欄位 [中，則](file-table.md)安裝程式會先進行 CRC 檢查，再系結影像。</span><span class="sxs-lookup"><span data-stu-id="4c889-114">If the **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check before binding images.</span></span>

<span data-ttu-id="4c889-115">如果檢查在系結映射之前失敗，安裝程式會報告記錄檔中的下列兩個錯誤，並繼續安裝，而不會系結檔案。</span><span class="sxs-lookup"><span data-stu-id="4c889-115">If the check fails before binding an image, the installer reports the following two errors in the log file and continues the installation without binding the file.</span></span>



| <span data-ttu-id="4c889-116">程式碼</span><span class="sxs-lookup"><span data-stu-id="4c889-116">Code</span></span> | <span data-ttu-id="4c889-117">訊息</span><span class="sxs-lookup"><span data-stu-id="4c889-117">Message</span></span>                                               |
|------|-------------------------------------------------------|
| <span data-ttu-id="4c889-118">2941</span><span class="sxs-lookup"><span data-stu-id="4c889-118">2941</span></span> | <span data-ttu-id="4c889-119">無法計算檔2的 CRC \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="4c889-119">Unable to compute the CRC for file \[2\].</span></span>             |
| <span data-ttu-id="4c889-120">2942</span><span class="sxs-lookup"><span data-stu-id="4c889-120">2942</span></span> | <span data-ttu-id="4c889-121">未在2個檔案上執行 BindImage 動作 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="4c889-121">BindImage action has not been executed on \[2\] file.</span></span> |



 

<span data-ttu-id="4c889-122">如果在複製、複製或修補未壓縮檔案後檢查失敗，安裝程式會報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c889-122">If the check fails after an uncompressed file had been copied, duplicated, or patched, the installer reports the following error.</span></span> <span data-ttu-id="4c889-123">如果複製壓縮檔案之後的檢查失敗，也會報告此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c889-123">This error is also reported if the check fails after a compressed file is copied.</span></span> <span data-ttu-id="4c889-124">如果檔案具有 **msidbFileAttributesVital** 屬性，則會將該檔案視為重要的安裝，而且使用者會取得重試或取消安裝的選項。</span><span class="sxs-lookup"><span data-stu-id="4c889-124">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the user gets the option to retry or cancel the installation.</span></span> <span data-ttu-id="4c889-125">如果檔案在檔案 [資料表](file-table.md)的 [屬性] 資料行中標示為 nonvital，使用者可能會忽略錯誤並繼續、重試或取消安裝。</span><span class="sxs-lookup"><span data-stu-id="4c889-125">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user may ignore the error and continue, retry, or cancel the installation.</span></span>



| <span data-ttu-id="4c889-126">程式碼</span><span class="sxs-lookup"><span data-stu-id="4c889-126">Code</span></span> | <span data-ttu-id="4c889-127">訊息</span><span class="sxs-lookup"><span data-stu-id="4c889-127">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="4c889-128">1331</span><span class="sxs-lookup"><span data-stu-id="4c889-128">1331</span></span> | <span data-ttu-id="4c889-129">無法正確複製2個檔案 \[ \] ： CRC 錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c889-129">Failed to correctly copy \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="4c889-130">請注意，只會移動未壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="4c889-130">Note that only uncompressed files are moved.</span></span> <span data-ttu-id="4c889-131">如果在移動未壓縮檔案後檢查失敗，安裝程式會顯示下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c889-131">If the check fails after an uncompressed file is moved, the installer displays the following error.</span></span> <span data-ttu-id="4c889-132">如果檔案具有 **msidbFileAttributesVital** 屬性，則會將該檔案視為對安裝很重要，且安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="4c889-132">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="4c889-133">如果檔案 [資料表](file-table.md)的 [屬性] 資料行中的檔案標示為 nonvital，使用者會取得取消或忽略錯誤的選項，並繼續進行安裝。</span><span class="sxs-lookup"><span data-stu-id="4c889-133">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="4c889-134">程式碼</span><span class="sxs-lookup"><span data-stu-id="4c889-134">Code</span></span> | <span data-ttu-id="4c889-135">訊息</span><span class="sxs-lookup"><span data-stu-id="4c889-135">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="4c889-136">1332</span><span class="sxs-lookup"><span data-stu-id="4c889-136">1332</span></span> | <span data-ttu-id="4c889-137">無法正確地移動 \[ 2 個檔案 \] ： CRC 錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c889-137">Failed to correctly move \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="4c889-138">如果在修補未壓縮檔案之後檢查失敗，安裝程式會顯示下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c889-138">If the check fails after an uncompressed file is patched, the installer displays the following error.</span></span> <span data-ttu-id="4c889-139">如果檔案具有 **msidbFileAttributesVital** 屬性，則會將該檔案視為對安裝很重要，且安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="4c889-139">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="4c889-140">如果檔案 [資料表](file-table.md)的 [屬性] 資料行中的檔案標示為 nonvital，使用者會取得取消或忽略錯誤的選項，並繼續進行安裝。</span><span class="sxs-lookup"><span data-stu-id="4c889-140">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="4c889-141">程式碼</span><span class="sxs-lookup"><span data-stu-id="4c889-141">Code</span></span> | <span data-ttu-id="4c889-142">訊息</span><span class="sxs-lookup"><span data-stu-id="4c889-142">Message</span></span>                                          |
|------|--------------------------------------------------|
| <span data-ttu-id="4c889-143">1333</span><span class="sxs-lookup"><span data-stu-id="4c889-143">1333</span></span> | <span data-ttu-id="4c889-144">無法正確修補2個檔案 \[ \] ： CRC 錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c889-144">Failed to correctly patch \[2\] file: CRC error.</span></span> |



 

 

 



