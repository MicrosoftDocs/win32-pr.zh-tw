---
title: 虛擬化實例生命週期
description: ProjFS 虛擬化實例的生命週期總覽。
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507959"
---
# <a name="virtualization-instance-lifecycle"></a><span data-ttu-id="6cb2c-103">虛擬化實例生命週期</span><span class="sxs-lookup"><span data-stu-id="6cb2c-103">Virtualization Instance Lifecycle</span></span>

<span data-ttu-id="6cb2c-104">提供者應用程式會維護一或多個虛擬化實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-104">The provider application maintains one or more virtualization instances.</span></span>  <span data-ttu-id="6cb2c-105">每個虛擬化實例在其生命週期中都會經歷四個階段：</span><span class="sxs-lookup"><span data-stu-id="6cb2c-105">Each virtualization instance goes through four stages in its lifecycle:</span></span>

1. <span data-ttu-id="6cb2c-106">建立</span><span class="sxs-lookup"><span data-stu-id="6cb2c-106">Creation</span></span>
2. <span data-ttu-id="6cb2c-107">啟動</span><span class="sxs-lookup"><span data-stu-id="6cb2c-107">Startup</span></span>
3. <span data-ttu-id="6cb2c-108">執行階段</span><span class="sxs-lookup"><span data-stu-id="6cb2c-108">Runtime</span></span>
4. <span data-ttu-id="6cb2c-109">關機</span><span class="sxs-lookup"><span data-stu-id="6cb2c-109">Shutdown</span></span>

<span data-ttu-id="6cb2c-110">請注意，關閉虛擬化實例之後，提供者不需要重新建立它來重複使用它。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-110">Note that after shutting down a virtualization instance the provider does not need to re-create it to reuse it.</span></span>  <span data-ttu-id="6cb2c-111">只要重新開機就可以了。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-111">It can simply start it up again.</span></span>

> <span data-ttu-id="6cb2c-112">**注意**：本節說明 ProjFS api 的範例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-112">**Note**: This section shows examples of ProjFS APIs.</span></span>  <span data-ttu-id="6cb2c-113">每個範例都旨在說明基本的 API 使用方式。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-113">Each example is meant to illustrate basic API usage.</span></span>  <span data-ttu-id="6cb2c-114">如需這些範例中未使用之選項的檔，請參閱 [PROJFS API 參考](/windows/desktop/api/_projfs)。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-114">For documentation of options unused in these examples please consult the [ProjFS API reference](/windows/desktop/api/_projfs).</span></span>

## <a name="creating-a-virtualization-root"></a><span data-ttu-id="6cb2c-115">建立虛擬化根</span><span class="sxs-lookup"><span data-stu-id="6cb2c-115">Creating a virtualization root</span></span>

<span data-ttu-id="6cb2c-116">在提供者可以啟動將專案投射到本機檔案系統中的虛擬化實例之前，必須先建立虛擬化根。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-116">Before a provider can start up the virtualization instance that will project items into the local file system, it must create the virtualization root.</span></span>  <span data-ttu-id="6cb2c-117">虛擬化根是提供者用來投射目錄和檔案樹狀結構的目錄。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-117">The virtualization root is the directory under which the provider projects a tree of directories and files.</span></span>

<span data-ttu-id="6cb2c-118">若要建立虛擬化根，提供者必須：</span><span class="sxs-lookup"><span data-stu-id="6cb2c-118">To create a virtualization root the provider must:</span></span>

1. <span data-ttu-id="6cb2c-119">建立做為虛擬化根的目錄。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-119">Create a directory to serve as the virtualization root.</span></span>

    <span data-ttu-id="6cb2c-120">提供者會使用 **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)** 來建立作為虛擬化根的目錄，例如：</span><span class="sxs-lookup"><span data-stu-id="6cb2c-120">The provider creates a directory to serve as the virtualization root using, for example **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span></span>

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="6cb2c-121">建立虛擬化實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-121">Create a virtualization instance ID.</span></span>

    <span data-ttu-id="6cb2c-122">每個虛擬化實例都有一個稱為 _虛擬化實例識別碼_ 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-122">Every virtualization instance has a unique ID called the _virtualization instance ID_.</span></span>  <span data-ttu-id="6cb2c-123">系統會使用此值來識別與其內容相關聯的虛擬化實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-123">The system uses this value to identify which virtualization instance its contents are associated to.</span></span>

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="6cb2c-124">將新目錄標示為虛擬化根。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-124">Mark the new directory as the virtualization root.</span></span>

    <span data-ttu-id="6cb2c-125">提供者會呼叫 **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** ，將新目錄標示為虛擬化根，並將其指派給虛擬化實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-125">The provider calls **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** to mark the new directory as the virtualization root and assign it to the virtualization instance.</span></span>

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

<span data-ttu-id="6cb2c-126">提供者只需要針對每個虛擬化實例建立虛擬化根。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-126">The provider only needs to create the virtualization root once for each virtualization instance.</span></span>  <span data-ttu-id="6cb2c-127">建立根目錄之後，就可以重複啟動和停止其相關聯的實例，而不需要重新建立根。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-127">Once a root has been created, its associated instance can be repeatedly started and stopped without recreating the root.</span></span>

## <a name="starting-a-virtualization-instance"></a><span data-ttu-id="6cb2c-128">啟動虛擬化實例</span><span class="sxs-lookup"><span data-stu-id="6cb2c-128">Starting a virtualization instance</span></span>

<span data-ttu-id="6cb2c-129">建立虛擬化根之後，提供者必須啟動虛擬化實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-129">Once the virtualization root has been created the provider must start the virtualization instance.</span></span>  <span data-ttu-id="6cb2c-130">這會通知 ProjFS 提供者已準備好接收回呼並提供資料。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-130">This signals ProjFS that the provider is ready to receive callbacks and provide data.</span></span>

<span data-ttu-id="6cb2c-131">若要啟動虛擬化實例，提供者必須：</span><span class="sxs-lookup"><span data-stu-id="6cb2c-131">To start the virtualization instance the provider must:</span></span>

1. <span data-ttu-id="6cb2c-132">設定回呼資料表。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-132">Set up the callback table.</span></span>

    <span data-ttu-id="6cb2c-133">ProjFS 藉由叫用提供者所執行的回呼常式來與提供者通訊。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-133">ProjFS communicates with the provider by invoking callback routines implemented by the provider.</span></span>  <span data-ttu-id="6cb2c-134">提供者會在 [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) 結構中填入其回呼常式的指標。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-134">The provider populates a [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct with pointers to its callback routines.</span></span>

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. <span data-ttu-id="6cb2c-135">啟動實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-135">Start the instance.</span></span>

    <span data-ttu-id="6cb2c-136">提供者會呼叫 **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** 來啟動虛擬化實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-136">The provider calls **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** to start the virtualization instance.</span></span>

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    <span data-ttu-id="6cb2c-137">**PrjStartVirtualizing** 的 _instanceHandle_ 參數會傳回虛擬化實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-137">**PrjStartVirtualizing**'s _instanceHandle_ parameter returns a handle to the virtualization instance.</span></span>  <span data-ttu-id="6cb2c-138">在呼叫其他 ProjFS Api 時，提供者會使用此控制碼。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-138">The provider uses this handle when calling other ProjFS APIs.</span></span>

## <a name="virtualization-instance-runtime"></a><span data-ttu-id="6cb2c-139">虛擬化實例執行時間</span><span class="sxs-lookup"><span data-stu-id="6cb2c-139">Virtualization instance runtime</span></span>

<span data-ttu-id="6cb2c-140">一旦呼叫 **PrjStartVirtualizing** 傳回，ProjFS 將會叫用提供者的回呼常式，以回應虛擬化實例中的檔案系統作業。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-140">Once the call to **PrjStartVirtualizing** returns, ProjFS will invoke the provider's callback routines in response to file system operations in the virtualization instance.</span></span>  <span data-ttu-id="6cb2c-141">如需提供者如何處理各種檔案系統作業的相關資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="6cb2c-141">For information on how the provider can handle various file system operations, refer to the following sections:</span></span>

* [<span data-ttu-id="6cb2c-142">列舉檔案和目錄</span><span class="sxs-lookup"><span data-stu-id="6cb2c-142">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)
* [<span data-ttu-id="6cb2c-143">提供檔案資料</span><span class="sxs-lookup"><span data-stu-id="6cb2c-143">Providing File Data</span></span>](providing-file-data.md)
* [<span data-ttu-id="6cb2c-144">檔案系統作業通知</span><span class="sxs-lookup"><span data-stu-id="6cb2c-144">File System Operation Notifications</span></span>](file-system-operation-notifications.md)
* [<span data-ttu-id="6cb2c-145">處理視圖變更</span><span class="sxs-lookup"><span data-stu-id="6cb2c-145">Handling View Changes</span></span>](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a><span data-ttu-id="6cb2c-146">關閉虛擬化實例</span><span class="sxs-lookup"><span data-stu-id="6cb2c-146">Shutting down a virtualization instance</span></span>

<span data-ttu-id="6cb2c-147">為了告知 ProjFS 提供者想要停止接收回呼並提供資料，提供者必須停止虛擬化實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-147">To signal ProjFS that the provider wants to stop receiving callbacks and providing data, the provider must stop the virtualization instance.</span></span>  <span data-ttu-id="6cb2c-148">若要這樣做，提供者會呼叫 **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**，並將控制碼傳遞給它從 **PrjStartVirtualizing** 呼叫所接收到的虛擬化實例。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-148">To do this the provider calls **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passing it the handle to the virtualization instance that it received from the call to **PrjStartVirtualizing**.</span></span>

```C++
PrjStopVirtualizing(instanceHandle);
```

<span data-ttu-id="6cb2c-149">請注意，在此呼叫傳回之前，ProjFS 可能會繼續叫用提供者的回呼常式。</span><span class="sxs-lookup"><span data-stu-id="6cb2c-149">Note that until this call returns, ProjFS may continue to invoke the provider's callback routines.</span></span>