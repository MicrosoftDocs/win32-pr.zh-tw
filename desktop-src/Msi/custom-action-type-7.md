---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型7。
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: 自訂動作類型7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026885"
---
# <a name="custom-action-type-7"></a><span data-ttu-id="827f6-103">自訂動作類型7</span><span class="sxs-lookup"><span data-stu-id="827f6-103">Custom Action Type 7</span></span>

<span data-ttu-id="827f6-104">自訂動作類型7會搭配並行安裝使用。</span><span class="sxs-lookup"><span data-stu-id="827f6-104">The Custom Action Type 7 is used with concurrent installations.</span></span> <span data-ttu-id="827f6-105">不建議將並行安裝用於安裝應用程式，以供公開發行。</span><span class="sxs-lookup"><span data-stu-id="827f6-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="827f6-106">如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="827f6-106">For more information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="827f6-107">此自訂動作會安裝另一個內嵌于第一個封裝內的安裝程式套件。</span><span class="sxs-lookup"><span data-stu-id="827f6-107">This custom action installs another installer package that is nested inside of the first package.</span></span>

## <a name="source"></a><span data-ttu-id="827f6-108">來源</span><span class="sxs-lookup"><span data-stu-id="827f6-108">Source</span></span>

<span data-ttu-id="827f6-109">並行應用程式的資料庫會儲存為封裝的 substorage，而 substorage 的名稱則是在 [CustomAction 資料表](customaction-table.md)的 [來源] 欄位中指定。</span><span class="sxs-lookup"><span data-stu-id="827f6-109">The database of the concurrent application is stored as a substorage of the package, and the name of the substorage is designated in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="827f6-110">數字類型</span><span class="sxs-lookup"><span data-stu-id="827f6-110">Numeric Type</span></span>



| <span data-ttu-id="827f6-111">類型名稱</span><span class="sxs-lookup"><span data-stu-id="827f6-111">Type name</span></span>                                                      | <span data-ttu-id="827f6-112">值</span><span class="sxs-lookup"><span data-stu-id="827f6-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="827f6-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span><span class="sxs-lookup"><span data-stu-id="827f6-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span></span> | <span data-ttu-id="827f6-114">7</span><span class="sxs-lookup"><span data-stu-id="827f6-114">7</span></span>     |



 

## <a name="target"></a><span data-ttu-id="827f6-115">目標</span><span class="sxs-lookup"><span data-stu-id="827f6-115">Target</span></span>

<span data-ttu-id="827f6-116">[CustomAction 資料表](customaction-table.md)的目標欄位包含要傳遞至並行安裝的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="827f6-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings to be passed to the concurrent installation.</span></span> <span data-ttu-id="827f6-117">這些屬性設定可以指定功能。</span><span class="sxs-lookup"><span data-stu-id="827f6-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="827f6-118">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="827f6-118">Return Processing Options</span></span>

<span data-ttu-id="827f6-119">並行安裝會話會以另一個執行緒的形式在目前的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="827f6-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="827f6-120">並行安裝無法以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="827f6-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="827f6-121">請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="827f6-121">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="827f6-122">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="827f6-122">Execution Scheduling Options</span></span>

<span data-ttu-id="827f6-123">選項旗標可用來控制自訂動作的潛在多次執行。</span><span class="sxs-lookup"><span data-stu-id="827f6-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="827f6-124">請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="827f6-124">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="827f6-125">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="827f6-125">In-Script Execution Options</span></span>

<span data-ttu-id="827f6-126">此自訂動作不會使用此選項。</span><span class="sxs-lookup"><span data-stu-id="827f6-126">This custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="827f6-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="827f6-127">Return Values</span></span>

<span data-ttu-id="827f6-128">從並行安裝的使用者結束、失敗、暫停或成功傳回狀態的處理方式，與其他任何動作的處理方式相同。</span><span class="sxs-lookup"><span data-stu-id="827f6-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="827f6-129">不過請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。</span><span class="sxs-lookup"><span data-stu-id="827f6-129">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="827f6-130">例如，如果動作傳回值在記錄檔中顯示為1，這表示動作傳回的錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="827f6-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="827f6-131">如需此轉譯的詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="827f6-131">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="827f6-132">請注意，如果同時安裝同時安裝了 **msidbCustomActionTypeContinue** ，則會傳回錯誤 \_ 安裝 \_ USEREXIT、錯誤 \_ 安裝 \_ 重新開機、錯誤安裝重新開機， \_ \_ \_ 或 \_ 需要錯誤成功 \_ 重新開機， \_ 以視為錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="827f6-132">Note that if a concurrent install has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="827f6-133">這表示，如果您設定 **msidbCustomActionTypeContinue** ，且您的並行安裝需要重新開機，則會忽略重新開機的需求。</span><span class="sxs-lookup"><span data-stu-id="827f6-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="827f6-134">此外，也會忽略來自並行安裝自訂動作的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="827f6-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="827f6-135">如果未設定 **msidbCustomActionTypeContinue** ，則會將下列傳回碼和錯誤 \_ 成功視為成功，並具有下列意義。</span><span class="sxs-lookup"><span data-stu-id="827f6-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="827f6-136">其他傳回碼會視為失敗。</span><span class="sxs-lookup"><span data-stu-id="827f6-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="827f6-137">訊息</span><span class="sxs-lookup"><span data-stu-id="827f6-137">Message</span></span>                          | <span data-ttu-id="827f6-138">意義</span><span class="sxs-lookup"><span data-stu-id="827f6-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="827f6-139">\_安裝 \_ 重新開機時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="827f6-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="827f6-140">重新開機旗標將會設定為在安裝結束時重新開機。</span><span class="sxs-lookup"><span data-stu-id="827f6-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="827f6-141">\_安裝 \_ 立即重新開機 \_ 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="827f6-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="827f6-142">需要重新開機，才能完成安裝。</span><span class="sxs-lookup"><span data-stu-id="827f6-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="827f6-143">重新開機將會立即處理。</span><span class="sxs-lookup"><span data-stu-id="827f6-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="827f6-144">\_ \_ 需要重新開機 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="827f6-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="827f6-145">需要重新開機，但已隱藏。</span><span class="sxs-lookup"><span data-stu-id="827f6-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="827f6-146">備註</span><span class="sxs-lookup"><span data-stu-id="827f6-146">Remarks</span></span>

<span data-ttu-id="827f6-147">在安裝或移除相關聯的元件或功能時，必須要有條件運算式才能啟用並行安裝。</span><span class="sxs-lookup"><span data-stu-id="827f6-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="827f6-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="827f6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="827f6-149">並行安裝</span><span class="sxs-lookup"><span data-stu-id="827f6-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="827f6-150">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="827f6-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="827f6-151">關於自訂動作</span><span class="sxs-lookup"><span data-stu-id="827f6-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="827f6-152">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="827f6-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="827f6-153">自訂動作傳回值</span><span class="sxs-lookup"><span data-stu-id="827f6-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



