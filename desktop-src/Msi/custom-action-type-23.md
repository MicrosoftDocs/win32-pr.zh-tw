---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型23。
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: 自訂動作類型23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853136"
---
# <a name="custom-action-type-23"></a><span data-ttu-id="ebb71-103">自訂動作類型23</span><span class="sxs-lookup"><span data-stu-id="ebb71-103">Custom Action Type 23</span></span>

<span data-ttu-id="ebb71-104">自訂動作類型23用於並行安裝。</span><span class="sxs-lookup"><span data-stu-id="ebb71-104">The Custom Action Type 23 is used with concurrent installations.</span></span> <span data-ttu-id="ebb71-105">不建議將並行安裝用於安裝應用程式，以供公開發行。</span><span class="sxs-lookup"><span data-stu-id="ebb71-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="ebb71-106">如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="ebb71-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="ebb71-107">此自訂動作會安裝位於應用程式來源樹狀結構中的另一個安裝程式套件。</span><span class="sxs-lookup"><span data-stu-id="ebb71-107">This custom action installs another installer package that resides in the application's source tree.</span></span>

## <a name="source"></a><span data-ttu-id="ebb71-108">來源</span><span class="sxs-lookup"><span data-stu-id="ebb71-108">Source</span></span>

<span data-ttu-id="ebb71-109">並行安裝封裝的位置會指定為相對於 [CustomAction 資料表](customaction-table.md)之 [來源] 欄位中所顯示來源位置的根目錄。</span><span class="sxs-lookup"><span data-stu-id="ebb71-109">The location of the concurrent installation package is specified relative to the root of the source location shown in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="ebb71-110">數字類型</span><span class="sxs-lookup"><span data-stu-id="ebb71-110">Numeric Type</span></span>



| <span data-ttu-id="ebb71-111">類型名稱</span><span class="sxs-lookup"><span data-stu-id="ebb71-111">Type name</span></span>                                                      | <span data-ttu-id="ebb71-112">值</span><span class="sxs-lookup"><span data-stu-id="ebb71-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="ebb71-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span><span class="sxs-lookup"><span data-stu-id="ebb71-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span></span> | <span data-ttu-id="ebb71-114">23</span><span class="sxs-lookup"><span data-stu-id="ebb71-114">23</span></span>    |



 

## <a name="target"></a><span data-ttu-id="ebb71-115">目標</span><span class="sxs-lookup"><span data-stu-id="ebb71-115">Target</span></span>

<span data-ttu-id="ebb71-116">[CustomAction 資料表](customaction-table.md)的 [目標] 欄位包含要傳遞至並行安裝的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="ebb71-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="ebb71-117">這些屬性設定可以指定功能。</span><span class="sxs-lookup"><span data-stu-id="ebb71-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="ebb71-118">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="ebb71-118">Return Processing Options</span></span>

<span data-ttu-id="ebb71-119">並行安裝會話會以另一個執行緒的形式在目前的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="ebb71-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="ebb71-120">並行安裝無法以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="ebb71-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="ebb71-121">如需詳細資訊，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="ebb71-121">For more information, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="ebb71-122">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="ebb71-122">Execution Scheduling Options</span></span>

<span data-ttu-id="ebb71-123">選項旗標可用來控制自訂動作的潛在多次執行。</span><span class="sxs-lookup"><span data-stu-id="ebb71-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="ebb71-124">如需詳細資訊，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="ebb71-124">For more information, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="ebb71-125">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="ebb71-125">In-Script Execution Options</span></span>

<span data-ttu-id="ebb71-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="ebb71-126">Not used.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebb71-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebb71-127">Return Values</span></span>

<span data-ttu-id="ebb71-128">從並行安裝的使用者結束、失敗、暫停或成功傳回狀態的處理方式，與其他任何動作的處理方式相同。</span><span class="sxs-lookup"><span data-stu-id="ebb71-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="ebb71-129">不過請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。</span><span class="sxs-lookup"><span data-stu-id="ebb71-129">Note however, that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="ebb71-130">例如，如果動作傳回值在記錄檔中顯示為1，這表示動作傳回的錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="ebb71-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="ebb71-131">如需詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="ebb71-131">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="ebb71-132">請注意，如果同時安裝同時安裝了 **msidbCustomActionTypeContinue** ，則會傳回錯誤 \_ 安裝 \_ USEREXIT、錯誤 \_ 安裝 \_ 重新開機、錯誤安裝重新開機， \_ \_ \_ 或 \_ 需要錯誤成功 \_ 重新開機， \_ 以視為錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="ebb71-132">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="ebb71-133">這表示，如果您設定 **msidbCustomActionTypeContinue** ，且您的並行安裝需要重新開機，則會忽略重新開機的需求。</span><span class="sxs-lookup"><span data-stu-id="ebb71-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="ebb71-134">此外，也會忽略來自並行安裝自訂動作的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ebb71-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="ebb71-135">如果未設定 **msidbCustomActionTypeContinue** ，則會將下列傳回碼和錯誤 \_ 成功視為成功，並具有下列意義。</span><span class="sxs-lookup"><span data-stu-id="ebb71-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="ebb71-136">其他傳回碼會視為失敗。</span><span class="sxs-lookup"><span data-stu-id="ebb71-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="ebb71-137">訊息</span><span class="sxs-lookup"><span data-stu-id="ebb71-137">Message</span></span>                          | <span data-ttu-id="ebb71-138">意義</span><span class="sxs-lookup"><span data-stu-id="ebb71-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb71-139">\_安裝 \_ 重新開機時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="ebb71-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="ebb71-140">重新開機旗標將會設定為在安裝結束時重新開機。</span><span class="sxs-lookup"><span data-stu-id="ebb71-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="ebb71-141">\_安裝 \_ 立即重新開機 \_ 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="ebb71-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="ebb71-142">需要重新開機，才能完成安裝。</span><span class="sxs-lookup"><span data-stu-id="ebb71-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="ebb71-143">重新開機將會立即處理。</span><span class="sxs-lookup"><span data-stu-id="ebb71-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="ebb71-144">\_ \_ 需要重新開機 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="ebb71-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="ebb71-145">需要重新開機，但已隱藏。</span><span class="sxs-lookup"><span data-stu-id="ebb71-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="ebb71-146">備註</span><span class="sxs-lookup"><span data-stu-id="ebb71-146">Remarks</span></span>

<span data-ttu-id="ebb71-147">在安裝或移除相關聯的元件或功能時，必須要有條件運算式才能啟用並行安裝。</span><span class="sxs-lookup"><span data-stu-id="ebb71-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebb71-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebb71-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebb71-149">並行安裝</span><span class="sxs-lookup"><span data-stu-id="ebb71-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="ebb71-150">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="ebb71-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="ebb71-151">關於自訂動作</span><span class="sxs-lookup"><span data-stu-id="ebb71-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="ebb71-152">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="ebb71-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="ebb71-153">自訂動作傳回值</span><span class="sxs-lookup"><span data-stu-id="ebb71-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



