---
description: 說明如何建立自訂圖示指派的處理常式。
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: 如何建立圖示處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973172"
---
# <a name="how-to-create-icon-handlers"></a><span data-ttu-id="6eeca-103">如何建立圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="6eeca-103">How to Create Icon Handlers</span></span>

<span data-ttu-id="6eeca-104">[檔案類型](fa-file-types.md)通常有與其相關聯的自訂圖示，可讓其成員在 Windows 檔案總管中容易辨識。</span><span class="sxs-lookup"><span data-stu-id="6eeca-104">A [file type](fa-file-types.md) often has a custom icon associated with it, to make its members easily recognizable in Windows Explorer.</span></span> <span data-ttu-id="6eeca-105">將自訂圖示指派給檔案類型最簡單的方式，就是註冊圖示的檔案。</span><span class="sxs-lookup"><span data-stu-id="6eeca-105">The simplest way to assign a custom icon to a file type is to register the icon's file.</span></span> <span data-ttu-id="6eeca-106">不過，以這種方式註冊的圖示在檔案類型的所有成員中都是相同的。</span><span class="sxs-lookup"><span data-stu-id="6eeca-106">However, an icon registered in this way will be the same for all members of the file type.</span></span> <span data-ttu-id="6eeca-107">您可以藉由執行 *圖示處理常式*，在將圖示指派給檔案類型的成員時，有更多的彈性。</span><span class="sxs-lookup"><span data-stu-id="6eeca-107">You can have much more flexibility in assigning icons to the members of the file type by implementing an *icon handler*.</span></span>

<span data-ttu-id="6eeca-108">圖示處理常式是一種 Shell 延伸模組處理常式，可讓您以動態方式將圖示指派給檔案類型的成員。</span><span class="sxs-lookup"><span data-stu-id="6eeca-108">An icon handler is a type of Shell extension handler that allows you to dynamically assign icons to the members of a file type.</span></span> <span data-ttu-id="6eeca-109">每次顯示類型的檔案時，Shell 會查詢適當圖示的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6eeca-109">Every time a file of the type is displayed, the Shell queries the handler for the appropriate icon.</span></span> <span data-ttu-id="6eeca-110">例如，圖示處理常式可以將不同的圖示指派給檔案類型的不同成員，或根據檔案的目前狀態來改變圖示。</span><span class="sxs-lookup"><span data-stu-id="6eeca-110">For instance, an icon handler can assign different icons to different members of the file type, or vary the icon based on the current state of the file.</span></span>

<span data-ttu-id="6eeca-111">[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。</span><span class="sxs-lookup"><span data-stu-id="6eeca-111">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="6eeca-112">本檔著重于圖示處理常式特定的執行層面。</span><span class="sxs-lookup"><span data-stu-id="6eeca-112">This document focuses on those aspects of implementation that are specific to icon handlers.</span></span>

-   [<span data-ttu-id="6eeca-113">執行圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="6eeca-113">Implementing Icon Handlers</span></span>](#step-1-implementing-icon-handlers)
-   [<span data-ttu-id="6eeca-114">執行 IExtractIcon 介面</span><span class="sxs-lookup"><span data-stu-id="6eeca-114">Implementing the IExtractIcon Interface</span></span>](#step-2-implementing-the-iextracticon-interface)
-   [<span data-ttu-id="6eeca-115">註冊圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="6eeca-115">Registering Icon Handlers</span></span>](#step-3-registering-icon-handlers)
-   [<span data-ttu-id="6eeca-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="6eeca-116">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="6eeca-117">指示</span><span class="sxs-lookup"><span data-stu-id="6eeca-117">Instructions</span></span>

### <a name="step-1-implementing-icon-handlers"></a><span data-ttu-id="6eeca-118">步驟1：執行圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="6eeca-118">Step 1: Implementing Icon Handlers</span></span>

<span data-ttu-id="6eeca-119">就像所有 Shell 擴充處理常式一樣，圖示處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="6eeca-119">Like all Shell extension handlers, icon handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="6eeca-120">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)之外，它們還必須匯出兩個介面。</span><span class="sxs-lookup"><span data-stu-id="6eeca-120">They must export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

<span data-ttu-id="6eeca-121">Shell 會透過其 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="6eeca-121">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="6eeca-122">它會使用此介面來要求 (CLSID) 的處理常式類別識別碼，並提供該檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6eeca-122">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="6eeca-123">其餘的作業會透過 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) 介面進行。</span><span class="sxs-lookup"><span data-stu-id="6eeca-123">The rest of the operation takes place through the [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) interface.</span></span> <span data-ttu-id="6eeca-124">如需如何執行 Shell 延伸模組處理常式（包括 **IPersistFile** 介面）的一般討論，請參閱 [建立 shell 擴充處理](handlers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="6eeca-124">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="6eeca-125">本檔的其餘部分將討論如何執行 **IExtractIcon** 介面。</span><span class="sxs-lookup"><span data-stu-id="6eeca-125">The remainder of this document discusses how to implement the **IExtractIcon** interface.</span></span>

### <a name="step-2-implementing-the-iextracticon-interface"></a><span data-ttu-id="6eeca-126">步驟2：執行 IExtractIcon 介面</span><span class="sxs-lookup"><span data-stu-id="6eeca-126">Step 2: Implementing the IExtractIcon Interface</span></span>

<span data-ttu-id="6eeca-127">初始化介面之後，Shell 會使用處理程式的 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) 介面來要求適當的圖示。</span><span class="sxs-lookup"><span data-stu-id="6eeca-127">After the interface is initialized, the Shell uses the handler's [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) interface to request the appropriate icon.</span></span> <span data-ttu-id="6eeca-128">介面有兩種方法： [**IExtractIcon：： GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) 和 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract)。</span><span class="sxs-lookup"><span data-stu-id="6eeca-128">The interface has two methods: [**IExtractIcon::GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) and [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).</span></span>

<span data-ttu-id="6eeca-129">圖示是由其在檔案系統中的位置來識別。</span><span class="sxs-lookup"><span data-stu-id="6eeca-129">Icons are identified by their location in the file system.</span></span> <span data-ttu-id="6eeca-130">呼叫 [**IExtractIcon：： GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) 方法以要求這項資訊。</span><span class="sxs-lookup"><span data-stu-id="6eeca-130">The [**IExtractIcon::GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) method is called to request this information.</span></span> <span data-ttu-id="6eeca-131">將 *szIconFile* 參數設定為檔案名。</span><span class="sxs-lookup"><span data-stu-id="6eeca-131">Set the *szIconFile* parameter to the file name.</span></span> <span data-ttu-id="6eeca-132">如果檔案中有一個以上的圖示，請將 *piIndex* 設定為圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="6eeca-132">If there is more than one icon in the file, set *piIndex* to the icon's index.</span></span> <span data-ttu-id="6eeca-133">為兩個旗標變數指派適當的值。</span><span class="sxs-lookup"><span data-stu-id="6eeca-133">Assign appropriate values to the two flag variables.</span></span> <span data-ttu-id="6eeca-134">如果您不想要指定檔案名，或不想要讓 Shell 將圖示解壓縮，請在 *pwFlags* 參數中設定 **GIL \_ NOTFILENAME** 旗標。</span><span class="sxs-lookup"><span data-stu-id="6eeca-134">If you do not want to specify a file name, or if you do not want the Shell to extract the icon, set the **GIL\_NOTFILENAME** flag in the *pwFlags* parameter.</span></span> <span data-ttu-id="6eeca-135">您不需要指派值給 *szIconFile*，不過當 Shell 呼叫 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract)時，處理常式必須提供圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="6eeca-135">You do not need to assign a value to *szIconFile*, but the handler must provide icon handles when the Shell calls [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).</span></span>

<span data-ttu-id="6eeca-136">如果您傳回檔案名，Shell 通常會嘗試從其快取載入圖示。</span><span class="sxs-lookup"><span data-stu-id="6eeca-136">If you return a file name, the Shell normally attempts to load the icon from its cache.</span></span> <span data-ttu-id="6eeca-137">若要防止載入快取的圖示，請在 *pwFlags* 參數中設定 **GIL \_ DONTCACHE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="6eeca-137">To prevent the loading of a cached icon, set the **GIL\_DONTCACHE** flag in the *pwFlags* parameter.</span></span> <span data-ttu-id="6eeca-138">如果未載入快取的圖示，則 Shell 會呼叫 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) 以要求圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="6eeca-138">If a cached icon is not loaded, the Shell then calls [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) to request the icon handle.</span></span>

<span data-ttu-id="6eeca-139">如果檔案和索引是由 [**IExtractIcon：： GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation)指定，它們會分別傳遞給 *pszFile* 和 *nIconIndex* 參數中的 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract)。</span><span class="sxs-lookup"><span data-stu-id="6eeca-139">If a file and index were specified by [**IExtractIcon::GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation), they are passed to [**IExtractIcon::Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) in the *pszFile* and *nIconIndex* parameters, respectively.</span></span> <span data-ttu-id="6eeca-140">如果有提供檔案名，您的處理常式可以傳回 \_ FALSE，讓 Shell 將圖示解壓縮。</span><span class="sxs-lookup"><span data-stu-id="6eeca-140">If a file name is provided, your handler can return S\_FALSE to have the Shell extract the icon.</span></span> <span data-ttu-id="6eeca-141">否則，您的處理常式必須解壓縮或產生大型和小型圖示，並將其 HICON 控制碼指派給 *phiconLarge* 和 *phiconSmall* 參數。</span><span class="sxs-lookup"><span data-stu-id="6eeca-141">Otherwise, your handler must extract or otherwise produce large and small icons, and assign their HICON handles to the *phiconLarge* and *phiconSmall* parameters.</span></span> <span data-ttu-id="6eeca-142">Shell 會將圖示新增至其快取，以加速後續呼叫處理常式。</span><span class="sxs-lookup"><span data-stu-id="6eeca-142">The Shell adds the icons to its cache to expedite subsequent calls to the handler.</span></span>

### <a name="step-3-registering-icon-handlers"></a><span data-ttu-id="6eeca-143">步驟3：註冊圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="6eeca-143">Step 3: Registering Icon Handlers</span></span>

<span data-ttu-id="6eeca-144">當您以 [靜態方式註冊](icon.md)[檔案類型](fa-file-types.md)的圖示時，會在檔案類型的 ProgID 底下建立 **DefaultIcon** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="6eeca-144">When you [statically register an icon](icon.md) for a [file type](fa-file-types.md), you create a **DefaultIcon** subkey under the ProgID for the file type.</span></span> <span data-ttu-id="6eeca-145">其預設值會設定為包含圖示的檔案。</span><span class="sxs-lookup"><span data-stu-id="6eeca-145">Its default value is set to the file that contains the icon.</span></span> <span data-ttu-id="6eeca-146">若要註冊圖示處理常式，您仍然必須有 **DefaultIcon** 子機碼，但其預設值必須設定為 "%1"。</span><span class="sxs-lookup"><span data-stu-id="6eeca-146">To register an icon handler, you must still have the **DefaultIcon** subkey, but its default value must be set to "%1".</span></span> <span data-ttu-id="6eeca-147">將 **IconHandler** 子機碼新增至 ProgID 子機碼的 **Shellex** 子機碼，並將其預設值設定為處理常式 CLSID GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="6eeca-147">Add an **IconHandler** subkey to the **Shellex** subkey of the ProgID subkey, and set its default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="6eeca-148">如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="6eeca-148">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="6eeca-149">下列範例會從 [自訂圖示](icon.md) 修改登錄專案，讓 myp 檔案類型現在使用快捷方式功能表處理常式，而不是靜態定義的圖示。</span><span class="sxs-lookup"><span data-stu-id="6eeca-149">The following example modifies the registry entry from [Customizing Icons](icon.md) so that the .myp file type now uses a shortcut menu handler instead of a statically defined icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = %1
      Shellex
         IconHandler
            (Default) = {The handler's CLSID GUID}
```

## <a name="related-topics"></a><span data-ttu-id="6eeca-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="6eeca-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eeca-151">建立 Shell 擴充功能處理常式</span><span class="sxs-lookup"><span data-stu-id="6eeca-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="6eeca-152">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="6eeca-152">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="6eeca-153">**IExtractIcon**</span><span class="sxs-lookup"><span data-stu-id="6eeca-153">**IExtractIcon**</span></span>](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)
</dt> </dl>

 

 
