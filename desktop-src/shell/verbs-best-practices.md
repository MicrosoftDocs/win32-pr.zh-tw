---
description: 本主題的組織方式如下：
title: 快速鍵功能表處理常式和多個動詞的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f8b47807c4647aec274e64dbcd137833d13e23cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973480"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a><span data-ttu-id="a703a-103">快速鍵功能表處理常式和多個動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a703a-103">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>

<span data-ttu-id="a703a-104">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="a703a-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a703a-105">最佳作法</span><span class="sxs-lookup"><span data-stu-id="a703a-105">Best Practices</span></span>](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [<span data-ttu-id="a703a-106">動詞實行的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a703a-106">Best Practices for Verb Implementations</span></span>](#best-practices-for-verb-implementations)
-   [<span data-ttu-id="a703a-107">多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a703a-107">Best Practices for Multiple Selection Verbs</span></span>](#best-practices-for-multiple-selection-verbs)
    -   [<span data-ttu-id="a703a-108">異類選取專案</span><span class="sxs-lookup"><span data-stu-id="a703a-108">Heterogenous Selections</span></span>](#heterogenous-selections)
-   [<span data-ttu-id="a703a-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="a703a-109">Related topics</span></span>](#related-topics)

## <a name="best-practices"></a><span data-ttu-id="a703a-110">最佳做法</span><span class="sxs-lookup"><span data-stu-id="a703a-110">Best Practices</span></span>

<span data-ttu-id="a703a-111">靜態動詞命令是要執行的最簡單動詞命令，並提供豐富的功能。</span><span class="sxs-lookup"><span data-stu-id="a703a-111">Static verb are simplest verbs to implement, and provide rich functionality.</span></span> <span data-ttu-id="a703a-112">強烈建議您使用其中一個靜態動詞方法來執行動詞。</span><span class="sxs-lookup"><span data-stu-id="a703a-112">We strongly encourage you to implement a verb using one of the static verb methods.</span></span>

### <a name="best-practices-for-verb-implementations"></a><span data-ttu-id="a703a-113">動詞實行的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a703a-113">Best Practices for Verb Implementations</span></span>

<span data-ttu-id="a703a-114">下列清單代表動詞實行的最佳作法：</span><span class="sxs-lookup"><span data-stu-id="a703a-114">The following list represents best practices for verb implementations:</span></span>

-   <span data-ttu-id="a703a-115">請一律選擇符合您需求的最簡單動詞方法。</span><span class="sxs-lookup"><span data-stu-id="a703a-115">Always chose the simplest verb method that meets your needs.</span></span>
-   <span data-ttu-id="a703a-116">盡可能使用靜態動詞方法。</span><span class="sxs-lookup"><span data-stu-id="a703a-116">Use a static verb method, if possible.</span></span>
-   <span data-ttu-id="a703a-117">請勿在 UI 執行緒上執行需要大量資源的作業或 i/o。</span><span class="sxs-lookup"><span data-stu-id="a703a-117">Do not perform resource-intensive operations or I/O on the UI thread.</span></span> <span data-ttu-id="a703a-118">[**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)和 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)在執行的工作中必須非常保守。</span><span class="sxs-lookup"><span data-stu-id="a703a-118">Both [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) and [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) need to be very conservative in the work they perform.</span></span> <span data-ttu-id="a703a-119">[**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 必須在另一個進程中執行，或者您必須建立新的執行緒，以避免封鎖呼叫者。</span><span class="sxs-lookup"><span data-stu-id="a703a-119">[**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) must be performed in another process, or you must create a new thread to avoid blocking the caller.</span></span>
-   <span data-ttu-id="a703a-120">與獨立軟體廠商 (ISV) 名稱的前置動詞，如下所示 `ISVName.verb` 。</span><span class="sxs-lookup"><span data-stu-id="a703a-120">Prefix verbs with the independent software vendor (ISV) name as follows, `ISVName.verb`.</span></span> <span data-ttu-id="a703a-121">使用不合格的名稱可能會與多個選擇相同動詞名稱的 Isv 產生衝突。</span><span class="sxs-lookup"><span data-stu-id="a703a-121">Using unqualified names can result in collisions with multiple ISVs that chose the same verb name.</span></span>
-   <span data-ttu-id="a703a-122">一律使用應用程式特定的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="a703a-122">Always use an application-specific ProgID.</span></span> <span data-ttu-id="a703a-123">由於某些專案類型不會使用此對應，因此需要廠商唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="a703a-123">Because some item types do not use this mapping, there is a need for vendor-unique names.</span></span>
-   <span data-ttu-id="a703a-124">相對於叫用的方法定位 UI，但不在啟動程式執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="a703a-124">Position the UI relative to the invoking method, but do not run on an invoker thread.</span></span>
-   <span data-ttu-id="a703a-125">針對傳遞給 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)方法的標準動詞，請不要接受傳回值 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="a703a-125">Do not accept the return value **S\_OK** for canonical verbs passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span> <span data-ttu-id="a703a-126">這麼做會導致叫用真正的動詞執行失敗，並傳回標準動詞的失敗碼。</span><span class="sxs-lookup"><span data-stu-id="a703a-126">Doing so causes a failure for the real verb implementation to be invoked, and returns a failure code for canonical verbs.</span></span> <span data-ttu-id="a703a-127">如果您不支援標準動詞，則在遇到非零 HIWORD (lpVerb) 值時，會傳回失敗。</span><span class="sxs-lookup"><span data-stu-id="a703a-127">If you do not support canonical verbs, then return failure when a nonzero HIWORD(lpVerb) value is encountered.</span></span>
-   <span data-ttu-id="a703a-128">請避免使用 **rundll32.exe** 作為動詞的主機。</span><span class="sxs-lookup"><span data-stu-id="a703a-128">Avoid the use of **rundll32.exe** as the host for your verb.</span></span>
-   <span data-ttu-id="a703a-129">在實 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 時，請務必使用 ResultFromShort 宏，透過 **HRESULT** 值傳回已新增至功能表的動詞數。</span><span class="sxs-lookup"><span data-stu-id="a703a-129">When implementing [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) be sure to return the number of verbs that have been added to the menu through the **HRESULT** value using the ResultFromShort macro.</span></span>
-   <span data-ttu-id="a703a-130">如果您在下列其中一個登錄機碼專案上註冊，請小心並務必在最特定的類型上註冊處理常式，以減少可能的非預期結果：</span><span class="sxs-lookup"><span data-stu-id="a703a-130">If you register on one of the following registry key entries, then exercise caution and be sure to register your handler on the most specific type to reduce the possibly unintended consequences:</span></span>
    -   <span data-ttu-id="a703a-131">\**HKEY \_類別 \_ \\ 根目錄 \** _</span><span class="sxs-lookup"><span data-stu-id="a703a-131">\**HKEY\_CLASSES\_ROOT\\\** _</span></span>
    -   <span data-ttu-id="a703a-132">_ *HKEY \_ 類別 \_ 根 \\ AllFileSystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="a703a-132">_ *HKEY\_CLASSES\_ROOT\\AllFileSystemObjects*\*</span></span>
    -   <span data-ttu-id="a703a-133">**HKEY \_ 類別 \_ 根 \\ 資料夾**</span><span class="sxs-lookup"><span data-stu-id="a703a-133">**HKEY\_CLASSES\_ROOT\\Folder**</span></span>
    -   <span data-ttu-id="a703a-134">**HKEY \_ 類別 \_ 根目錄 \\**</span><span class="sxs-lookup"><span data-stu-id="a703a-134">**HKEY\_CLASSES\_ROOT\\Directory**</span></span>
-   <span data-ttu-id="a703a-135">只有在您預期您可能需要變更快速鍵功能表中的預設動詞時，才設定 **MayChangeDefaultMenu** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a703a-135">Set the **MayChangeDefaultMenu** key only if you anticipate that you might need to change the default verb in the shortcut menu.</span></span> <span data-ttu-id="a703a-136">如果您的處理常式未變更預設的動詞命令，您就不應該設定此索引鍵，因為這樣做會導致系統不必要地載入您的 DLL。</span><span class="sxs-lookup"><span data-stu-id="a703a-136">If your handler does not change the default verb, then you should not set this key because doing so causes the system to load your DLL unnecessarily.</span></span>
-   <span data-ttu-id="a703a-137">將您在 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)中執行的工作降至最低。</span><span class="sxs-lookup"><span data-stu-id="a703a-137">Minimize the work you perform in [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize).</span></span> <span data-ttu-id="a703a-138">針對快速鍵功能表處理常式，請先捕捉傳遞給 **IShellExtInit：： Initialize** 的資料物件，然後在 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)或 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)中進行處理。</span><span class="sxs-lookup"><span data-stu-id="a703a-138">For shortcut menu handlers, capture the data object passed to **IShellExtInit::Initialize**, and then process it in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

## <a name="best-practices-for-multiple-selection-verbs"></a><span data-ttu-id="a703a-139">多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a703a-139">Best Practices for Multiple Selection Verbs</span></span>

<span data-ttu-id="a703a-140">因為多重選取動詞案例中的專案數可能很大，所以請務必考慮動詞執行的效能含意。</span><span class="sxs-lookup"><span data-stu-id="a703a-140">Because the number of items in a multi-selection verb scenario can be large, it is important that you consider the performance implications of your verb implementations.</span></span> <span data-ttu-id="a703a-141">例如，當使用者在 \* 包含大量專案的範圍上搜尋 ""，然後按一下 [ **全選** ] 和 [按一下滑鼠右鍵] 時，就會顯示該動詞中有上千個專案的選取專案。</span><span class="sxs-lookup"><span data-stu-id="a703a-141">For example, when a user searches for "\*" over a scope that includes large numbers of items, and then clicks **Select All** and right-clicks, the verb is presented with a selection that can have thousands of items in it.</span></span> <span data-ttu-id="a703a-142">因此，動詞應該只考慮選取專案中的第一個專案，以及整體專案計數。</span><span class="sxs-lookup"><span data-stu-id="a703a-142">As a result, verbs should only consider the first item in the selection, and the overall item count.</span></span> <span data-ttu-id="a703a-143">第一個專案定義為視圖頂端的專案，或使用者第一次以滑鼠右鍵按一下的專案。</span><span class="sxs-lookup"><span data-stu-id="a703a-143">The first item is defined as either the item at the top of the view, or the item that the user first right-clicked.</span></span>

<span data-ttu-id="a703a-144">在 Windows 7 和更新版本中，當查詢快捷方式功能表時，傳遞至動詞命令的專案數目限制為16。</span><span class="sxs-lookup"><span data-stu-id="a703a-144">In Windows 7 and later, the number of items passed to a verb is limited to 16 when a shortcut menu is queried.</span></span> <span data-ttu-id="a703a-145">然後會重新建立該動詞命令，並在叫用該動詞時，使用完整的選取專案重新初始化。</span><span class="sxs-lookup"><span data-stu-id="a703a-145">The verb is then re-created and re-initialized with the full selection when that verb is invoked.</span></span>

<span data-ttu-id="a703a-146">在某些情況下，請考慮少量的固定專案。</span><span class="sxs-lookup"><span data-stu-id="a703a-146">It is appropriate in some cases to consider a small number of fixed items.</span></span> <span data-ttu-id="a703a-147">例如，「差異」動詞適用于只考慮前兩個專案的「差異」動詞。</span><span class="sxs-lookup"><span data-stu-id="a703a-147">For example, it is appropriate for a "diff" verb to consider only the first two items.</span></span> <span data-ttu-id="a703a-148">一般而言，您不需要測試選取專案中的每個專案，以查看它是否為特定類型，或查詢選取專案中的每個專案是否有其屬性。</span><span class="sxs-lookup"><span data-stu-id="a703a-148">Generally, you need not test every item in the selection to see if it is a certain type, or query every item in the selection for its properties.</span></span> <span data-ttu-id="a703a-149">請查看第一個專案，並決定是否適合加入您的動詞。</span><span class="sxs-lookup"><span data-stu-id="a703a-149">Look rather at the first item and decide if it is appropriate to add your verb.</span></span>

### <a name="heterogenous-selections"></a><span data-ttu-id="a703a-150">異類選取專案</span><span class="sxs-lookup"><span data-stu-id="a703a-150">Heterogenous Selections</span></span>

<span data-ttu-id="a703a-151">在多重選取案例中，會自動加入開放式動詞，假設未檢查項目可以由動詞處理。</span><span class="sxs-lookup"><span data-stu-id="a703a-151">Optimistic verbs are automatically added in the multi-selection case, assuming that uninspected items can be handled by the verb.</span></span> <span data-ttu-id="a703a-152">相反地，當選取範圍包含未檢查項目時，不會加入封閉式動詞，而且只會在專案數目很小的情況下加入。</span><span class="sxs-lookup"><span data-stu-id="a703a-152">In contrast, pessimistic verbs are not added when the selection contains uninspected items, and are only added in cases where the number of items is small.</span></span>

<span data-ttu-id="a703a-153">播放機樣式動詞應該是開放式的，並且以無訊息方式略過未處理的專案。</span><span class="sxs-lookup"><span data-stu-id="a703a-153">Player style verbs should be optimistic, and silently skip the items that are not handled.</span></span> <span data-ttu-id="a703a-154">如果無法對專案採取動作，可能會導致資料遺失或混淆，則動詞應該警告使用者有關無法處理的專案。</span><span class="sxs-lookup"><span data-stu-id="a703a-154">If a failure to act on items can cause data loss or confusion, then the verb should warn users about items that cannot be processed.</span></span> <span data-ttu-id="a703a-155">例如，「備份」動詞應該表示某些專案無法備份。</span><span class="sxs-lookup"><span data-stu-id="a703a-155">For example a "backup" verb should indicate that some items could not be backed up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a703a-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="a703a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a703a-157">為快捷方式功能表選擇靜態或動態動詞</span><span class="sxs-lookup"><span data-stu-id="a703a-157">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="a703a-158">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="a703a-158">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="a703a-159">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="a703a-159">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="a703a-160">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="a703a-160">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="a703a-161">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="a703a-161">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="a703a-162">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="a703a-162">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 



