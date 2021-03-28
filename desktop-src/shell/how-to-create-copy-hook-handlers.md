---
description: 使用 Shell 擴充功能來執行複製勾點處理常式。
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: 如何建立複製勾點處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192689"
---
# <a name="how-to-create-copy-hook-handlers"></a><span data-ttu-id="c0a03-103">如何建立複製勾點處理常式</span><span class="sxs-lookup"><span data-stu-id="c0a03-103">How to Create Copy Hook Handlers</span></span>

<span data-ttu-id="c0a03-104">[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。</span><span class="sxs-lookup"><span data-stu-id="c0a03-104">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="c0a03-105">本檔著重于複製攔截處理常式特定的執行層面。</span><span class="sxs-lookup"><span data-stu-id="c0a03-105">This document focuses on those aspects of implementation that are specific to copy hook handlers.</span></span>

-   [<span data-ttu-id="c0a03-106">執行複製勾點處理常式</span><span class="sxs-lookup"><span data-stu-id="c0a03-106">Implementing Copy Hook Handlers</span></span>](#step-1-implementing-copy-hook-handlers)
-   [<span data-ttu-id="c0a03-107">註冊複製勾點處理常式</span><span class="sxs-lookup"><span data-stu-id="c0a03-107">Registering Copy Hook Handlers</span></span>](#step-2-registering-copy-hook-handlers)
-   [<span data-ttu-id="c0a03-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0a03-108">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="c0a03-109">指示</span><span class="sxs-lookup"><span data-stu-id="c0a03-109">Instructions</span></span>

### <a name="step-1-implementing-copy-hook-handlers"></a><span data-ttu-id="c0a03-110">步驟1：執行複製勾點處理常式</span><span class="sxs-lookup"><span data-stu-id="c0a03-110">Step 1: Implementing Copy Hook Handlers</span></span>

<span data-ttu-id="c0a03-111">如同所有 Shell 延伸模組處理常式，複製攔截處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="c0a03-111">Like all Shell extension handlers, copy hook handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="c0a03-112">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))之外，也會匯出一個介面。</span><span class="sxs-lookup"><span data-stu-id="c0a03-112">They export one interface in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span></span> <span data-ttu-id="c0a03-113">Shell 會直接初始化處理常式，因此不需要初始化介面（例如 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)）。</span><span class="sxs-lookup"><span data-stu-id="c0a03-113">The Shell initializes the handler directly, so there is no need for an initialization interface such as [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span></span>

<span data-ttu-id="c0a03-114">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))介面具有單一方法 [**ICopyHook：： CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c0a03-114">The [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) interface has a single method, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span></span> <span data-ttu-id="c0a03-115">當即將移動資料夾時，Shell 會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c0a03-115">When a folder is about to be moved, the Shell calls this method.</span></span> <span data-ttu-id="c0a03-116">它會傳入各種資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="c0a03-116">It passes in a variety of information, including:</span></span>

-   <span data-ttu-id="c0a03-117">資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0a03-117">The folder's name.</span></span>
-   <span data-ttu-id="c0a03-118">資料夾的目的地或新名稱。</span><span class="sxs-lookup"><span data-stu-id="c0a03-118">The folder's destination or new name.</span></span>
-   <span data-ttu-id="c0a03-119">正在嘗試的作業。</span><span class="sxs-lookup"><span data-stu-id="c0a03-119">The operation that is being attempted.</span></span>
-   <span data-ttu-id="c0a03-120">來源和目的資料夾的屬性。</span><span class="sxs-lookup"><span data-stu-id="c0a03-120">The attributes of the source and destination folders.</span></span>
-   <span data-ttu-id="c0a03-121">可以用來顯示使用者介面的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="c0a03-121">A window handle that can be used to display a user interface.</span></span>

<span data-ttu-id="c0a03-122">呼叫處理常式的 [**ICopyHook：： CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) 方法時，它會傳回下列三個值的其中一個，以指示 Shell 應如何繼續進行。</span><span class="sxs-lookup"><span data-stu-id="c0a03-122">When your handler's [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) method is called, it returns one of the three following values to indicate to the Shell how it should proceed.</span></span>



| <span data-ttu-id="c0a03-123">值</span><span class="sxs-lookup"><span data-stu-id="c0a03-123">Value</span></span>    | <span data-ttu-id="c0a03-124">描述</span><span class="sxs-lookup"><span data-stu-id="c0a03-124">Description</span></span>                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a03-125">IDYES</span><span class="sxs-lookup"><span data-stu-id="c0a03-125">IDYES</span></span>    | <span data-ttu-id="c0a03-126">允許操作。</span><span class="sxs-lookup"><span data-stu-id="c0a03-126">Allows the operation.</span></span>                                                                                                                            |
| <span data-ttu-id="c0a03-127">IDNO</span><span class="sxs-lookup"><span data-stu-id="c0a03-127">IDNO</span></span>     | <span data-ttu-id="c0a03-128">防止此資料夾上的操作。</span><span class="sxs-lookup"><span data-stu-id="c0a03-128">Prevents the operation on this folder.</span></span> <span data-ttu-id="c0a03-129">Shell 可以繼續執行任何其他已核准的作業，例如批次複製作業。</span><span class="sxs-lookup"><span data-stu-id="c0a03-129">The Shell can continue with any other operations that have been approved, such as a batch copy operation.</span></span> |
| <span data-ttu-id="c0a03-130">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="c0a03-130">IDCANCEL</span></span> | <span data-ttu-id="c0a03-131">防止目前的作業，並取消任何暫止的作業。</span><span class="sxs-lookup"><span data-stu-id="c0a03-131">Prevents the current operation and cancels any pending operations.</span></span>                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a><span data-ttu-id="c0a03-132">步驟2：註冊複製勾點處理常式</span><span class="sxs-lookup"><span data-stu-id="c0a03-132">Step 2: Registering Copy Hook Handlers</span></span>

<span data-ttu-id="c0a03-133">資料夾的複製勾點處理常式會在 **HKEY \_ 類別的 \_ 根目錄** \\  \\ **shellex** \\ **CopyHookHandlers** 子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="c0a03-133">Copy hook handlers for folders are registered under the **HKEY\_CLASSES\_ROOT**\\**Directory**\\**shellex**\\**CopyHookHandlers** subkey.</span></span> <span data-ttu-id="c0a03-134">針對處理常式建立名為 **CopyHookHandlers** 的子機碼，並將子機碼的預設值設定為處理常式之類別識別碼的字串格式， (CLSID) GUID。</span><span class="sxs-lookup"><span data-stu-id="c0a03-134">Create a subkey of **CopyHookHandlers** named for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="c0a03-135">下列範例會將 **MyCopyHandler** 子機碼新增至 Shell 的複製攔截處理常式清單。</span><span class="sxs-lookup"><span data-stu-id="c0a03-135">The following example adds the **MyCopyHandler** subkey to the Shell's list of copy hook handlers.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

<span data-ttu-id="c0a03-136">印表機物件的複製勾點處理常式基本上是以相同方式註冊。</span><span class="sxs-lookup"><span data-stu-id="c0a03-136">Copy hook handlers for printer objects are registered in essentially the same way.</span></span> <span data-ttu-id="c0a03-137">唯一的差別在於您必須在 **HKEY \_ 類別的 \_ 根** 印表機子機碼下註冊它們 \\  。</span><span class="sxs-lookup"><span data-stu-id="c0a03-137">The only difference is that you must register them under the **HKEY\_CLASSES\_ROOT**\\**Printers** subkey.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0a03-138">備註</span><span class="sxs-lookup"><span data-stu-id="c0a03-138">Remarks</span></span>

<span data-ttu-id="c0a03-139">一般情況下，使用者和應用程式可以複製、移動、刪除或重新命名資料夾，但有一些限制。</span><span class="sxs-lookup"><span data-stu-id="c0a03-139">Normally, users and applications can copy, move, delete, or rename folders with few restrictions.</span></span> <span data-ttu-id="c0a03-140">藉由執行複製勾點處理常式，您可以控制是否進行這些作業。</span><span class="sxs-lookup"><span data-stu-id="c0a03-140">By implementing a copy hook handler, you can control whether these operations take place.</span></span> <span data-ttu-id="c0a03-141">例如，執行這類處理常式可讓您防止重要的資料夾重新命名或刪除。</span><span class="sxs-lookup"><span data-stu-id="c0a03-141">For instance, implementing such a handler allows you to prevent critical folders from being renamed or deleted.</span></span> <span data-ttu-id="c0a03-142">也可以針對印表機物件來執行複製勾點處理常式。</span><span class="sxs-lookup"><span data-stu-id="c0a03-142">Copy hook handlers can also be implemented for printer objects.</span></span>

<span data-ttu-id="c0a03-143">複製勾點處理常式是全域的。</span><span class="sxs-lookup"><span data-stu-id="c0a03-143">Copy hook handlers are global.</span></span> <span data-ttu-id="c0a03-144">Shell 會在每次應用程式或使用者嘗試複製、移動、刪除或重新命名資料夾或印表機物件時，呼叫所有已註冊的處理常式。</span><span class="sxs-lookup"><span data-stu-id="c0a03-144">The Shell calls all registered handlers every time an application or user attempts to copy, move, delete, or rename a folder or printer object.</span></span> <span data-ttu-id="c0a03-145">處理常式不會執行作業本身。</span><span class="sxs-lookup"><span data-stu-id="c0a03-145">The handler does not perform the operation itself.</span></span> <span data-ttu-id="c0a03-146">只核准或 vetoes。</span><span class="sxs-lookup"><span data-stu-id="c0a03-146">It only approves or vetoes it.</span></span> <span data-ttu-id="c0a03-147">如果所有處理常式都已核准，則 Shell 會執行作業。</span><span class="sxs-lookup"><span data-stu-id="c0a03-147">If all handlers approve, the Shell does the operation.</span></span> <span data-ttu-id="c0a03-148">如果有任何處理程式 vetoes 作業，就會取消它，而不會呼叫剩餘的處理常式。</span><span class="sxs-lookup"><span data-stu-id="c0a03-148">If any handler vetoes the operation, it is canceled and the remaining handlers are not called.</span></span> <span data-ttu-id="c0a03-149">複製攔截處理常式不會收到作業成功或失敗的通知，因此不能用來監視檔案作業。</span><span class="sxs-lookup"><span data-stu-id="c0a03-149">Copy hook handlers are not informed of the success or failure of the operation, so they cannot be used to monitor file operations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0a03-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0a03-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0a03-151">建立 Shell 擴充功能處理常式</span><span class="sxs-lookup"><span data-stu-id="c0a03-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

<span data-ttu-id="c0a03-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0a03-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span></span>
</dt> </dl>

 

 
