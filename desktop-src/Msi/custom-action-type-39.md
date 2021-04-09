---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型39。
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: 自訂動作類型39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849975"
---
# <a name="custom-action-type-39"></a><span data-ttu-id="7e427-103">自訂動作類型39</span><span class="sxs-lookup"><span data-stu-id="7e427-103">Custom Action Type 39</span></span>

<span data-ttu-id="7e427-104">自訂動作類型39用於並行安裝。</span><span class="sxs-lookup"><span data-stu-id="7e427-104">The Custom Action Type 39 is used with concurrent installations.</span></span> <span data-ttu-id="7e427-105">不建議將並行安裝用於安裝應用程式，以供公開發行。</span><span class="sxs-lookup"><span data-stu-id="7e427-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="7e427-106">如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="7e427-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="7e427-107">類型39自訂動作會安裝已公告或已安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e427-107">Type 39 custom action installs an application that is advertised or already installed.</span></span> <span data-ttu-id="7e427-108">您可以使用這個自訂動作類型，重新安裝或移除目前產品安裝套件已安裝為並行安裝的產品。</span><span class="sxs-lookup"><span data-stu-id="7e427-108">This custom action type may be used to reinstall or remove a product that has been installed as a concurrent installation by the current product's installation package.</span></span> <span data-ttu-id="7e427-109">類型39自訂動作無法用來重新安裝或移除任何其他方法先前安裝的任何產品。</span><span class="sxs-lookup"><span data-stu-id="7e427-109">The Type 39 custom action cannot be used to reinstall or remove any product previously installed by any other means.</span></span> <span data-ttu-id="7e427-110">例如，如果在主要產品安裝期間使用類型39、類型23或類型7自訂動作安裝次要產品，則在卸載主要產品時，可能會使用類型39自訂動作來移除次要產品。</span><span class="sxs-lookup"><span data-stu-id="7e427-110">For example, if the secondary product is installed using a Type 39, Type 23, or Type 7 custom action during the installation of the primary product, a Type 39 custom action may be used to remove the secondary product when the primary product is uninstalled.</span></span>

## <a name="source"></a><span data-ttu-id="7e427-111">來源</span><span class="sxs-lookup"><span data-stu-id="7e427-111">Source</span></span>

<span data-ttu-id="7e427-112">[CustomAction 資料表](customaction-table.md)的 [來源] 欄位包含應用程式的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="7e427-112">The Source field of the [CustomAction table](customaction-table.md) contains the product code for the application.</span></span>

## <a name="numeric-type"></a><span data-ttu-id="7e427-113">數字類型</span><span class="sxs-lookup"><span data-stu-id="7e427-113">Numeric Type</span></span>



| <span data-ttu-id="7e427-114">類型名稱</span><span class="sxs-lookup"><span data-stu-id="7e427-114">Type name</span></span>                                                     | <span data-ttu-id="7e427-115">值</span><span class="sxs-lookup"><span data-stu-id="7e427-115">Value</span></span> |
|---------------------------------------------------------------|-------|
| <span data-ttu-id="7e427-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span><span class="sxs-lookup"><span data-stu-id="7e427-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span></span> | <span data-ttu-id="7e427-117">39</span><span class="sxs-lookup"><span data-stu-id="7e427-117">39</span></span>    |



 

## <a name="target"></a><span data-ttu-id="7e427-118">目標</span><span class="sxs-lookup"><span data-stu-id="7e427-118">Target</span></span>

<span data-ttu-id="7e427-119">[CustomAction 資料表](customaction-table.md)的 [目標] 欄位包含要傳遞至並行安裝的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="7e427-119">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="7e427-120">這些屬性設定可以指定功能。</span><span class="sxs-lookup"><span data-stu-id="7e427-120">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7e427-121">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="7e427-121">Return Processing Options</span></span>

<span data-ttu-id="7e427-122">如果未公告或未安裝應用程式，自訂動作類型39會失敗。</span><span class="sxs-lookup"><span data-stu-id="7e427-122">The custom action type 39 fails if the application is not advertised or installed.</span></span> <span data-ttu-id="7e427-123">若要避免這個錯誤，您必須設定 **msidbCustomActionTypeContinueflag**。</span><span class="sxs-lookup"><span data-stu-id="7e427-123">To avoid this failure, you must set the **msidbCustomActionTypeContinueflag**.</span></span>

<span data-ttu-id="7e427-124">並行安裝無法以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="7e427-124">A concurrent install cannot run asynchronously.</span></span>

<span data-ttu-id="7e427-125">請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="7e427-125">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7e427-126">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="7e427-126">Execution Scheduling Options</span></span>

<span data-ttu-id="7e427-127">選項旗標可用來控制自訂動作的潛在多次執行。</span><span class="sxs-lookup"><span data-stu-id="7e427-127">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="7e427-128">請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="7e427-128">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7e427-129">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="7e427-129">In-Script Execution Options</span></span>

<span data-ttu-id="7e427-130">自訂動作不會使用此選項。</span><span class="sxs-lookup"><span data-stu-id="7e427-130">The custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e427-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e427-131">Return Values</span></span>

<span data-ttu-id="7e427-132">從並行安裝的使用者結束、失敗、暫停或成功傳回狀態的處理方式，與其他任何動作的處理方式相同。</span><span class="sxs-lookup"><span data-stu-id="7e427-132">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="7e427-133">不過請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。</span><span class="sxs-lookup"><span data-stu-id="7e427-133">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="7e427-134">例如，如果動作傳回值在記錄檔中顯示為1，這表示動作傳回的錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="7e427-134">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="7e427-135">如需詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="7e427-135">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="7e427-136">請注意，如果同時安裝同時安裝了 **msidbCustomActionTypeContinue** ，則會傳回錯誤 \_ 安裝 \_ USEREXIT、錯誤 \_ 安裝 \_ 重新開機、錯誤安裝重新開機， \_ \_ \_ 或 \_ 需要錯誤成功 \_ 重新開機， \_ 以視為錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="7e427-136">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="7e427-137">這表示，如果您設定 **msidbCustomActionTypeContinue** ，且您的並行安裝需要重新開機，則會忽略重新開機的需求。</span><span class="sxs-lookup"><span data-stu-id="7e427-137">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="7e427-138">此外，也會忽略來自並行安裝自訂動作的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7e427-138">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="7e427-139">如果未設定 **msidbCustomActionTypeContinue** ，則會將下列傳回碼和錯誤 \_ 成功視為成功，並具有下列意義。</span><span class="sxs-lookup"><span data-stu-id="7e427-139">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="7e427-140">其他傳回碼會視為失敗。</span><span class="sxs-lookup"><span data-stu-id="7e427-140">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="7e427-141">訊息</span><span class="sxs-lookup"><span data-stu-id="7e427-141">Message</span></span>                          | <span data-ttu-id="7e427-142">意義</span><span class="sxs-lookup"><span data-stu-id="7e427-142">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e427-143">\_安裝 \_ 重新開機時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="7e427-143">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="7e427-144">重新開機旗標將會設定為在安裝結束時重新開機。</span><span class="sxs-lookup"><span data-stu-id="7e427-144">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="7e427-145">\_安裝 \_ 立即重新開機 \_ 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="7e427-145">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="7e427-146">需要重新開機，才能完成安裝。</span><span class="sxs-lookup"><span data-stu-id="7e427-146">A restart is required before completing the installation.</span></span> <span data-ttu-id="7e427-147">重新開機將會立即處理。</span><span class="sxs-lookup"><span data-stu-id="7e427-147">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="7e427-148">\_ \_ 需要重新開機 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="7e427-148">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="7e427-149">需要重新開機，但已隱藏。</span><span class="sxs-lookup"><span data-stu-id="7e427-149">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="7e427-150">備註</span><span class="sxs-lookup"><span data-stu-id="7e427-150">Remarks</span></span>

<span data-ttu-id="7e427-151">在安裝或移除相關聯的元件或功能時，必須要有條件運算式才能啟用並行安裝。</span><span class="sxs-lookup"><span data-stu-id="7e427-151">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e427-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e427-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e427-153">並行安裝</span><span class="sxs-lookup"><span data-stu-id="7e427-153">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="7e427-154">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="7e427-154">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="7e427-155">關於自訂動作</span><span class="sxs-lookup"><span data-stu-id="7e427-155">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="7e427-156">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="7e427-156">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



