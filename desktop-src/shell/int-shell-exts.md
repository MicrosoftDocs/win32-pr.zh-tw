---
description: Shell 擴充處理常式物件的大部分執行都是由其型別所決定。 不過，有一些常見的元素。 本主題討論所有 Shell 延伸模組處理常式所共用的執行層面。
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: 初始化 Shell 擴充處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973761"
---
# <a name="initializing-shell-extension-handlers"></a><span data-ttu-id="f7c26-105">初始化 Shell 擴充處理常式</span><span class="sxs-lookup"><span data-stu-id="f7c26-105">Initializing Shell Extension Handlers</span></span>

<span data-ttu-id="f7c26-106">Shell 擴充處理常式物件的大部分執行都是由其型別所決定。</span><span class="sxs-lookup"><span data-stu-id="f7c26-106">Much of the implementation of a Shell extension handler object is dictated by its type.</span></span> <span data-ttu-id="f7c26-107">不過，有一些常見的元素。</span><span class="sxs-lookup"><span data-stu-id="f7c26-107">There are, however, some common elements.</span></span> <span data-ttu-id="f7c26-108">本主題討論所有 Shell 延伸模組處理常式所共用的執行層面。</span><span class="sxs-lookup"><span data-stu-id="f7c26-108">This topic discusses those aspects of implementation that are shared by all Shell extension handlers.</span></span>

<span data-ttu-id="f7c26-109">所有 Shell 擴充處理常式都是 (COM) 物件的同進程元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="f7c26-109">All Shell extension handlers are in-process Component Object Model (COM) objects.</span></span> <span data-ttu-id="f7c26-110">您必須將 GUID 指派給它們，如 [註冊 Shell 擴充處理常式](handlers.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="f7c26-110">They must be assigned a GUID and registered as described in [Registering Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="f7c26-111">它們會實作為 Dll，而且必須匯出下列標準函式：</span><span class="sxs-lookup"><span data-stu-id="f7c26-111">They are implemented as DLLs and must export the following standard functions:</span></span>

-   <span data-ttu-id="f7c26-112">[**DllMain**](../dlls/dllmain.md)。</span><span class="sxs-lookup"><span data-stu-id="f7c26-112">[**DllMain**](../dlls/dllmain.md).</span></span> <span data-ttu-id="f7c26-113">DLL 的標準進入點。</span><span class="sxs-lookup"><span data-stu-id="f7c26-113">The standard entry point to the DLL.</span></span>
-   <span data-ttu-id="f7c26-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)。</span><span class="sxs-lookup"><span data-stu-id="f7c26-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span></span> <span data-ttu-id="f7c26-115">公開物件的 class factory。</span><span class="sxs-lookup"><span data-stu-id="f7c26-115">Exposes the object's class factory.</span></span>
-   <span data-ttu-id="f7c26-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)。</span><span class="sxs-lookup"><span data-stu-id="f7c26-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span></span> <span data-ttu-id="f7c26-117">COM 會呼叫這個函式，以判斷物件是否為任何用戶端提供服務。</span><span class="sxs-lookup"><span data-stu-id="f7c26-117">COM calls this function to determine whether the object is serving any clients.</span></span> <span data-ttu-id="f7c26-118">如果不是，則系統可以卸載 DLL 並釋放相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f7c26-118">If not, the system can unload the DLL and free the associated memory.</span></span>

<span data-ttu-id="f7c26-119">Shell 擴充處理常式和所有 COM 物件一樣，都必須執行 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面和 [class factory](../com/implementing-iclassfactory.md)。</span><span class="sxs-lookup"><span data-stu-id="f7c26-119">Like all COM objects, Shell extension handlers must implement an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a [class factory](../com/implementing-iclassfactory.md).</span></span> <span data-ttu-id="f7c26-120">大部分也必須在 Windows XP 或更早版本中執行 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 或 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面。</span><span class="sxs-lookup"><span data-stu-id="f7c26-120">Most must also implement either an [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface in Windows XP or earlier.</span></span> <span data-ttu-id="f7c26-121">這些已由 Windows Vista 中的 [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)、 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) 和 [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) 取代。</span><span class="sxs-lookup"><span data-stu-id="f7c26-121">These were replaced by [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) and [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span></span> <span data-ttu-id="f7c26-122">Shell 會使用這些介面來初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="f7c26-122">The Shell uses these interfaces to initialize the handler.</span></span>

<span data-ttu-id="f7c26-123">[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面必須由下列各項執行：</span><span class="sxs-lookup"><span data-stu-id="f7c26-123">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="f7c26-124">圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="f7c26-124">Icon handlers</span></span>
-   <span data-ttu-id="f7c26-125">資料處理程式</span><span class="sxs-lookup"><span data-stu-id="f7c26-125">Data handlers</span></span>
-   <span data-ttu-id="f7c26-126">捨棄處理常式</span><span class="sxs-lookup"><span data-stu-id="f7c26-126">Drop handlers</span></span>

<span data-ttu-id="f7c26-127">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)介面必須由下列各項執行：</span><span class="sxs-lookup"><span data-stu-id="f7c26-127">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="f7c26-128">快速鍵功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="f7c26-128">Shortcut menu handlers</span></span>
-   <span data-ttu-id="f7c26-129">拖放處理常式</span><span class="sxs-lookup"><span data-stu-id="f7c26-129">Drag-and-drop handlers</span></span>
-   <span data-ttu-id="f7c26-130">屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="f7c26-130">Property sheet handlers</span></span>

<span data-ttu-id="f7c26-131">本主題的其餘部分將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="f7c26-131">The following subjects are discussed in the remainder of this topic:</span></span>

-   [<span data-ttu-id="f7c26-132">執行 IPersistFile</span><span class="sxs-lookup"><span data-stu-id="f7c26-132">Implementing IPersistFile</span></span>](#implementing-ipersistfile)
-   [<span data-ttu-id="f7c26-133">執行 IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="f7c26-133">Implementing IShellExtInit</span></span>](#implementing-ishellextinit)
-   [<span data-ttu-id="f7c26-134">提示自訂</span><span class="sxs-lookup"><span data-stu-id="f7c26-134">Infotip Customization</span></span>](#infotip-customization)
-   [<span data-ttu-id="f7c26-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7c26-135">Related topics</span></span>](#related-topics)

## <a name="implementing-ipersistfile"></a><span data-ttu-id="f7c26-136">執行 IPersistFile</span><span class="sxs-lookup"><span data-stu-id="f7c26-136">Implementing IPersistFile</span></span>

<span data-ttu-id="f7c26-137">[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面是設計來允許將物件載入或儲存到磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="f7c26-137">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is designed to permit an object to be loaded from or saved to a disk file.</span></span> <span data-ttu-id="f7c26-138">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、其本身的五個方法，以及它繼承自 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)的 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)方法之外，它還有六個方法。</span><span class="sxs-lookup"><span data-stu-id="f7c26-138">It has six methods in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), five of its own, and the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) method that it inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span></span> <span data-ttu-id="f7c26-139">使用 Shell 擴充功能時， **IPersist** 只會用來初始化 Shell 擴充處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="f7c26-139">With Shell extensions, **IPersist** is used only to initialize a Shell extension handler object.</span></span> <span data-ttu-id="f7c26-140">因為通常不需要讀取或寫入磁片，所以只有 **GetClassID** 和 [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 方法需要 nontoken 執行。</span><span class="sxs-lookup"><span data-stu-id="f7c26-140">Because there is typically no need to read from or write to the disk, only the **GetClassID** and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods require a nontoken implementation.</span></span>

<span data-ttu-id="f7c26-141">Shell 會先呼叫 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) ，函式會傳回擴充處理常式物件 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7c26-141">The Shell calls [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) first, and the function returns the class identifier (CLSID) of the extension handler object.</span></span> <span data-ttu-id="f7c26-142">然後，Shell 會呼叫 [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 並以兩個值傳遞。</span><span class="sxs-lookup"><span data-stu-id="f7c26-142">The Shell then calls [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) and passes in two values.</span></span> <span data-ttu-id="f7c26-143">第一個 *pszFile* 是 Unicode 字串，其中包含 Shell 即將操作的檔案或資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7c26-143">The first, *pszFile*, is a Unicode string with the name of the file or folder that Shell is about to operate on.</span></span> <span data-ttu-id="f7c26-144">第二個是 *dwMode*，表示檔案存取模式。</span><span class="sxs-lookup"><span data-stu-id="f7c26-144">The second is *dwMode*, which indicates the file access mode.</span></span> <span data-ttu-id="f7c26-145">因為通常不需要存取檔案， *dwMode* 通常是零。</span><span class="sxs-lookup"><span data-stu-id="f7c26-145">Because there is normally no need to access files, *dwMode* is typically zero.</span></span> <span data-ttu-id="f7c26-146">方法會視需要儲存這些值以供稍後參考。</span><span class="sxs-lookup"><span data-stu-id="f7c26-146">The method stores these values as needed for later reference.</span></span>

<span data-ttu-id="f7c26-147">下列程式碼片段說明一般 Shell 擴充處理常式如何執行 [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) 和 [**載入**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) 方法。</span><span class="sxs-lookup"><span data-stu-id="f7c26-147">The following code fragment illustrates how a typical Shell extension handler implements the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods.</span></span> <span data-ttu-id="f7c26-148">它是設計來處理 ANSI 或 Unicode。</span><span class="sxs-lookup"><span data-stu-id="f7c26-148">It is designed to handle either ANSI or Unicode.</span></span> <span data-ttu-id="f7c26-149">CLSID \_ SampleExtHandler 是延伸模組處理常式物件的 GUID，而 CSampleShellExtension 是用來執行介面的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f7c26-149">CLSID\_SampleExtHandler is the extension handler object's GUID, and CSampleShellExtension is the name of the class used to implement the interface.</span></span> <span data-ttu-id="f7c26-150">**M \_ szFileName** 和 **m \_ dwMode** 變數是私用變數，用來儲存檔案的名稱和存取旗標。</span><span class="sxs-lookup"><span data-stu-id="f7c26-150">The **m\_szFileName** and **m\_dwMode** variables are private variables that are used to store the file's name and access flags.</span></span>


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a><span data-ttu-id="f7c26-151">執行 IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="f7c26-151">Implementing IShellExtInit</span></span>

<span data-ttu-id="f7c26-152">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)介面除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)之外，只有一個方法 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)。</span><span class="sxs-lookup"><span data-stu-id="f7c26-152">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface has only one method, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="f7c26-153">方法有三個參數，可供 Shell 用來傳入各種類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="f7c26-153">The method has three parameters that the Shell can use to pass in various types of information.</span></span> <span data-ttu-id="f7c26-154">傳入的值取決於處理常式的類型，而部分可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7c26-154">The values passed in depend on the type of handler, and some can be set to **NULL**.</span></span>

-   <span data-ttu-id="f7c26-155">*pidlFolder* 會保留資料夾的 (PIDL) 專案識別碼清單的指標。</span><span class="sxs-lookup"><span data-stu-id="f7c26-155">*pidlFolder* holds a folder's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="f7c26-156">這是絕對 PIDL。</span><span class="sxs-lookup"><span data-stu-id="f7c26-156">This is an absolute PIDL.</span></span> <span data-ttu-id="f7c26-157">若為屬性工作表延伸，此值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7c26-157">For property sheet extensions, this value is **NULL**.</span></span> <span data-ttu-id="f7c26-158">如果是快捷方式功能表延伸，則是包含要顯示其快捷方式功能表之專案的資料夾 PIDL。</span><span class="sxs-lookup"><span data-stu-id="f7c26-158">For shortcut menu extensions, it is the PIDL of the folder that contains the item whose shortcut menu is being displayed.</span></span> <span data-ttu-id="f7c26-159">若是非預設的拖放處理常式，則為目的檔案夾的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="f7c26-159">For nondefault drag-and-drop handlers, it is the PIDL of the target folder.</span></span>
-   <span data-ttu-id="f7c26-160">*pDataObject* 會保留資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f7c26-160">*pDataObject* holds a pointer to a data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="f7c26-161">資料物件會以 [CF \_ HDROP](dragdrop.md) 格式保存一或多個檔案名。</span><span class="sxs-lookup"><span data-stu-id="f7c26-161">The data object holds one or more file names in [CF\_HDROP](dragdrop.md) format.</span></span>
-   <span data-ttu-id="f7c26-162">*hRegKey* 會保留檔案物件或資料夾類型的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="f7c26-162">*hRegKey* holds a registry key for the file object or folder type.</span></span>

<span data-ttu-id="f7c26-163">[**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法會視需要儲存檔案名、 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標和登錄機碼，以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="f7c26-163">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method stores the file name, [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer, and registry key as needed for later use.</span></span> <span data-ttu-id="f7c26-164">下列程式碼片段說明 **IShellExtInit：： Initialize** 的實作為。</span><span class="sxs-lookup"><span data-stu-id="f7c26-164">The following code fragment illustrates an implementation of **IShellExtInit::Initialize**.</span></span> <span data-ttu-id="f7c26-165">為了簡單起見，此範例假設資料物件只包含單一檔案。</span><span class="sxs-lookup"><span data-stu-id="f7c26-165">For simplicity, this example assumes that the data object contains only a single file.</span></span> <span data-ttu-id="f7c26-166">一般而言，資料物件可能包含多個檔案，每個檔案都需要解壓縮。</span><span class="sxs-lookup"><span data-stu-id="f7c26-166">In general, the data object might contain multiple files, each of which will need to be extracted.</span></span>


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a><span data-ttu-id="f7c26-167">提示自訂</span><span class="sxs-lookup"><span data-stu-id="f7c26-167">Infotip Customization</span></span>

<span data-ttu-id="f7c26-168">有兩種方式可以自訂提示。</span><span class="sxs-lookup"><span data-stu-id="f7c26-168">There are two ways to customize infotips.</span></span> <span data-ttu-id="f7c26-169">其中一種方式是執行支援 [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) 的物件，然後在登錄中的適當子機碼下註冊物件 (請參閱下面的) 。</span><span class="sxs-lookup"><span data-stu-id="f7c26-169">One way is to implement an object that supports [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) and then register the object under the proper subkey in the registry (see below).</span></span> <span data-ttu-id="f7c26-170">或者，您可以指定要顯示的固定字串或特定檔案屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="f7c26-170">Alternatively, you can specify either a fixed string or a list of certain file properties to be displayed.</span></span>

<span data-ttu-id="f7c26-171">若要顯示命名空間延伸的固定字串，請在命名空間延伸模組的 CLSID 機 **碼底下建立** 名為 [提示] 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="f7c26-171">To display a fixed string for a namespace extension, create a subkey called **InfoTip** beneath the CLSID key of your namespace extension.</span></span> <span data-ttu-id="f7c26-172">將該子機碼的資料設定為您想要顯示的字串。</span><span class="sxs-lookup"><span data-stu-id="f7c26-172">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

<span data-ttu-id="f7c26-173">若要顯示檔案類型的固定字串，請在您要提供提示的檔案類型的 **ProgID** 索引 **鍵下方，** 建立名為 [提示] 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="f7c26-173">To display a fixed string for a file type, create a subkey called **InfoTip** beneath the **ProgID** key of the file type for which you want to supply infotips.</span></span> <span data-ttu-id="f7c26-174">將該子機碼的資料設定為您想要顯示的字串。</span><span class="sxs-lookup"><span data-stu-id="f7c26-174">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

<span data-ttu-id="f7c26-175">如果您想要讓 Shell 在特定檔案類型的提示中顯示特定的檔案屬性，請在該檔案類型的 **ProgID** **金鑰下方建立** 名為 [提示] 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="f7c26-175">If you want the Shell to show certain file properties in the infotip for a specific file type, create a subkey called **InfoTip** beneath the **ProgID** key of that file type.</span></span> <span data-ttu-id="f7c26-176">將該子機碼的資料設定為以分號分隔的標準屬性名稱清單或 {fmtid}、pid 組，其中 *propname* 是標準的屬性名稱，而 *{fmtid}，pid* 是 [**fmtid/pid**](./objects.md)組。</span><span class="sxs-lookup"><span data-stu-id="f7c26-176">Set the data of that subkey to be a semicolon-delineated list of canonical property names or {fmtid}, pid pairs where *propname* is a canonical property name and *{fmtid},pid* is a [**FMTID/PID pair**](./objects.md).</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

<span data-ttu-id="f7c26-177">您可以使用下列屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="f7c26-177">The following property names can be used.</span></span>



| <span data-ttu-id="f7c26-178">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="f7c26-178">Property Name</span></span>    | <span data-ttu-id="f7c26-179">描述</span><span class="sxs-lookup"><span data-stu-id="f7c26-179">Description</span></span>                   | <span data-ttu-id="f7c26-180">取出來源</span><span class="sxs-lookup"><span data-stu-id="f7c26-180">Retrieved From</span></span>                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c26-181">作者</span><span class="sxs-lookup"><span data-stu-id="f7c26-181">Author</span></span>           | <span data-ttu-id="f7c26-182">檔作者</span><span class="sxs-lookup"><span data-stu-id="f7c26-182">Author of the document</span></span>        | [<span data-ttu-id="f7c26-183">**PIDSI \_ 作者**</span><span class="sxs-lookup"><span data-stu-id="f7c26-183">**PIDSI\_AUTHOR**</span></span>](../stg/the-summary-information-property-set.md)                             |
| <span data-ttu-id="f7c26-184">標題</span><span class="sxs-lookup"><span data-stu-id="f7c26-184">Title</span></span>            | <span data-ttu-id="f7c26-185">檔的標題</span><span class="sxs-lookup"><span data-stu-id="f7c26-185">Title of the document</span></span>         | [<span data-ttu-id="f7c26-186">**PIDSI \_ 標題**</span><span class="sxs-lookup"><span data-stu-id="f7c26-186">**PIDSI\_TITLE**</span></span>](../stg/the-summary-information-property-set.md)                              |
| <span data-ttu-id="f7c26-187">主體</span><span class="sxs-lookup"><span data-stu-id="f7c26-187">Subject</span></span>          | <span data-ttu-id="f7c26-188">主題摘要</span><span class="sxs-lookup"><span data-stu-id="f7c26-188">Subject summary</span></span>               | [<span data-ttu-id="f7c26-189">**PIDSI \_ 主旨**</span><span class="sxs-lookup"><span data-stu-id="f7c26-189">**PIDSI\_SUBJECT**</span></span>](../stg/the-summary-information-property-set.md)                            |
| <span data-ttu-id="f7c26-190">註解</span><span class="sxs-lookup"><span data-stu-id="f7c26-190">Comment</span></span>          | <span data-ttu-id="f7c26-191">檔批註</span><span class="sxs-lookup"><span data-stu-id="f7c26-191">Document comments</span></span>             | <span data-ttu-id="f7c26-192">[**PIDSI \_批註**](../stg/the-summary-information-property-set.md) 或資料夾/磁片磁碟機屬性</span><span class="sxs-lookup"><span data-stu-id="f7c26-192">[**PIDSI\_COMMENT**](../stg/the-summary-information-property-set.md) or folder/drive properties</span></span> |
| <span data-ttu-id="f7c26-193">PageCount</span><span class="sxs-lookup"><span data-stu-id="f7c26-193">PageCount</span></span>        | <span data-ttu-id="f7c26-194">頁面數目</span><span class="sxs-lookup"><span data-stu-id="f7c26-194">Number of pages</span></span>               | [<span data-ttu-id="f7c26-195">**PIDSI \_ PAGECOUNT**</span><span class="sxs-lookup"><span data-stu-id="f7c26-195">**PIDSI\_PAGECOUNT**</span></span>](../stg/the-summary-information-property-set.md)                          |
| <span data-ttu-id="f7c26-196">Name</span><span class="sxs-lookup"><span data-stu-id="f7c26-196">Name</span></span>             | <span data-ttu-id="f7c26-197">易記名稱</span><span class="sxs-lookup"><span data-stu-id="f7c26-197">Friendly name</span></span>                 | <span data-ttu-id="f7c26-198">標準資料夾檢視</span><span class="sxs-lookup"><span data-stu-id="f7c26-198">Standard folder view</span></span>                                                                      |
| <span data-ttu-id="f7c26-199">OriginalLocation</span><span class="sxs-lookup"><span data-stu-id="f7c26-199">OriginalLocation</span></span> | <span data-ttu-id="f7c26-200">原始檔案的位置</span><span class="sxs-lookup"><span data-stu-id="f7c26-200">Location of original file</span></span>     | <span data-ttu-id="f7c26-201">[公事包] 資料夾和資源回收筒資料夾</span><span class="sxs-lookup"><span data-stu-id="f7c26-201">Briefcase folder and Recycle Bin folder</span></span>                                                   |
| <span data-ttu-id="f7c26-202">DateDeleted</span><span class="sxs-lookup"><span data-stu-id="f7c26-202">DateDeleted</span></span>      | <span data-ttu-id="f7c26-203">資料檔案已刪除</span><span class="sxs-lookup"><span data-stu-id="f7c26-203">Date file was deleted</span></span>         | <span data-ttu-id="f7c26-204">資源回收筒資料夾</span><span class="sxs-lookup"><span data-stu-id="f7c26-204">Recycle Bin folder</span></span>                                                                        |
| <span data-ttu-id="f7c26-205">類型</span><span class="sxs-lookup"><span data-stu-id="f7c26-205">Type</span></span>             | <span data-ttu-id="f7c26-206">檔案類型</span><span class="sxs-lookup"><span data-stu-id="f7c26-206">Type of file</span></span>                  | <span data-ttu-id="f7c26-207">標準資料夾詳細資料檢視</span><span class="sxs-lookup"><span data-stu-id="f7c26-207">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="f7c26-208">大小</span><span class="sxs-lookup"><span data-stu-id="f7c26-208">Size</span></span>             | <span data-ttu-id="f7c26-209">檔案大小</span><span class="sxs-lookup"><span data-stu-id="f7c26-209">Size of file</span></span>                  | <span data-ttu-id="f7c26-210">標準資料夾詳細資料檢視</span><span class="sxs-lookup"><span data-stu-id="f7c26-210">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="f7c26-211">SyncCopyIn</span><span class="sxs-lookup"><span data-stu-id="f7c26-211">SyncCopyIn</span></span>       | <span data-ttu-id="f7c26-212">與 OriginalLocation 相同</span><span class="sxs-lookup"><span data-stu-id="f7c26-212">Same as OriginalLocation</span></span>      | <span data-ttu-id="f7c26-213">與 OriginalLocation 相同</span><span class="sxs-lookup"><span data-stu-id="f7c26-213">Same as OriginalLocation</span></span>                                                                  |
| <span data-ttu-id="f7c26-214">修改日期</span><span class="sxs-lookup"><span data-stu-id="f7c26-214">Modified</span></span>         | <span data-ttu-id="f7c26-215">上次修改日期</span><span class="sxs-lookup"><span data-stu-id="f7c26-215">Date last modified</span></span>            | <span data-ttu-id="f7c26-216">標準資料夾詳細資料檢視</span><span class="sxs-lookup"><span data-stu-id="f7c26-216">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="f7c26-217">建立時間</span><span class="sxs-lookup"><span data-stu-id="f7c26-217">Created</span></span>          | <span data-ttu-id="f7c26-218">建立日期</span><span class="sxs-lookup"><span data-stu-id="f7c26-218">Date created</span></span>                  | <span data-ttu-id="f7c26-219">標準資料夾詳細資料檢視</span><span class="sxs-lookup"><span data-stu-id="f7c26-219">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="f7c26-220">訪問</span><span class="sxs-lookup"><span data-stu-id="f7c26-220">Accessed</span></span>         | <span data-ttu-id="f7c26-221">上次存取日期</span><span class="sxs-lookup"><span data-stu-id="f7c26-221">Date last accessed</span></span>            | <span data-ttu-id="f7c26-222">標準資料夾詳細資料檢視</span><span class="sxs-lookup"><span data-stu-id="f7c26-222">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="f7c26-223">InFolder</span><span class="sxs-lookup"><span data-stu-id="f7c26-223">InFolder</span></span>         | <span data-ttu-id="f7c26-224">包含檔案的目錄</span><span class="sxs-lookup"><span data-stu-id="f7c26-224">Directory containing the file</span></span> | <span data-ttu-id="f7c26-225">檔搜尋結果</span><span class="sxs-lookup"><span data-stu-id="f7c26-225">Document search results</span></span>                                                                   |
| <span data-ttu-id="f7c26-226">排名</span><span class="sxs-lookup"><span data-stu-id="f7c26-226">Rank</span></span>             | <span data-ttu-id="f7c26-227">搜尋符合品質</span><span class="sxs-lookup"><span data-stu-id="f7c26-227">Quality of search match</span></span>       | <span data-ttu-id="f7c26-228">檔搜尋結果</span><span class="sxs-lookup"><span data-stu-id="f7c26-228">Document search results</span></span>                                                                   |
| <span data-ttu-id="f7c26-229">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="f7c26-229">FreeSpace</span></span>        | <span data-ttu-id="f7c26-230">可用的儲存空間</span><span class="sxs-lookup"><span data-stu-id="f7c26-230">Available storage space</span></span>       | <span data-ttu-id="f7c26-231">磁碟機</span><span class="sxs-lookup"><span data-stu-id="f7c26-231">Disk drives</span></span>                                                                               |
| <span data-ttu-id="f7c26-232">NumberOfVisits</span><span class="sxs-lookup"><span data-stu-id="f7c26-232">NumberOfVisits</span></span>   | <span data-ttu-id="f7c26-233">瀏覽次數</span><span class="sxs-lookup"><span data-stu-id="f7c26-233">Number of visits</span></span>              | <span data-ttu-id="f7c26-234">我的最愛資料夾</span><span class="sxs-lookup"><span data-stu-id="f7c26-234">Favorites folder</span></span>                                                                          |
| <span data-ttu-id="f7c26-235">屬性</span><span class="sxs-lookup"><span data-stu-id="f7c26-235">Attributes</span></span>       | <span data-ttu-id="f7c26-236">檔案屬性</span><span class="sxs-lookup"><span data-stu-id="f7c26-236">File Attributes</span></span>               | <span data-ttu-id="f7c26-237">標準資料夾詳細資料檢視</span><span class="sxs-lookup"><span data-stu-id="f7c26-237">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="f7c26-238">公司</span><span class="sxs-lookup"><span data-stu-id="f7c26-238">Company</span></span>          | <span data-ttu-id="f7c26-239">公司名稱</span><span class="sxs-lookup"><span data-stu-id="f7c26-239">Company name</span></span>                  | [<span data-ttu-id="f7c26-240">**PIDDSI \_ 公司**</span><span class="sxs-lookup"><span data-stu-id="f7c26-240">**PIDDSI\_COMPANY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| <span data-ttu-id="f7c26-241">類別</span><span class="sxs-lookup"><span data-stu-id="f7c26-241">Category</span></span>         | <span data-ttu-id="f7c26-242">檔類別</span><span class="sxs-lookup"><span data-stu-id="f7c26-242">Document category</span></span>             | [<span data-ttu-id="f7c26-243">**PIDDSI \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="f7c26-243">**PIDDSI\_CATEGORY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| <span data-ttu-id="f7c26-244">著作權</span><span class="sxs-lookup"><span data-stu-id="f7c26-244">Copyright</span></span>        | <span data-ttu-id="f7c26-245">媒體著作權</span><span class="sxs-lookup"><span data-stu-id="f7c26-245">Media copyright</span></span>               | [<span data-ttu-id="f7c26-246">**PIDMSI \_ 著作權**</span><span class="sxs-lookup"><span data-stu-id="f7c26-246">**PIDMSI\_COPYRIGHT**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| <span data-ttu-id="f7c26-247">HTMLInfoTipFile</span><span class="sxs-lookup"><span data-stu-id="f7c26-247">HTMLInfoTipFile</span></span>  | <span data-ttu-id="f7c26-248">HTML 提示檔</span><span class="sxs-lookup"><span data-stu-id="f7c26-248">HTML InfoTip file</span></span>             | <span data-ttu-id="f7c26-249">資料夾的 Desktop.ini 檔案</span><span class="sxs-lookup"><span data-stu-id="f7c26-249">Desktop.ini file for folder</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="f7c26-250">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7c26-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7c26-251">註冊 Shell 延伸模組處理常式</span><span class="sxs-lookup"><span data-stu-id="f7c26-251">Registering Shell Extension Handlers</span></span>](reg-shell-exts.md)
</dt> </dl>

 

 
