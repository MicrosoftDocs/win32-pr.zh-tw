---
description: 當使用者以滑鼠右鍵按一下檔案類型的成員來顯示 [屬性] 屬性工作表時，Shell 會呼叫已註冊檔案類型的屬性工作表處理常式。 每個處理常式都可以在預設的屬性工作表中加入一個自訂頁面。
title: 如何註冊及執行檔案類型的屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991555"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="707bf-104">如何註冊及執行檔案類型的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="707bf-104">How to Register and Implement a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="707bf-105">當使用者以滑鼠右鍵按一下檔案類型的成員來顯示 [屬性] 屬性工作表時，Shell 會呼叫已註冊檔案類型的屬性工作表處理常式。</span><span class="sxs-lookup"><span data-stu-id="707bf-105">When the user right-clicks a member of a file type to display the Properties property sheet, the Shell calls the property sheet handlers that are registered for the file type.</span></span> <span data-ttu-id="707bf-106">每個處理常式都可以在預設的屬性工作表中加入一個自訂頁面。</span><span class="sxs-lookup"><span data-stu-id="707bf-106">Each handler can add one custom page to the default property sheet.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="707bf-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="707bf-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="707bf-108">技術</span><span class="sxs-lookup"><span data-stu-id="707bf-108">Technologies</span></span>

-   <span data-ttu-id="707bf-109">殼層</span><span class="sxs-lookup"><span data-stu-id="707bf-109">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="707bf-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="707bf-110">Prerequisites</span></span>

-   <span data-ttu-id="707bf-111">對快速鍵功能表的瞭解</span><span class="sxs-lookup"><span data-stu-id="707bf-111">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="707bf-112">指示</span><span class="sxs-lookup"><span data-stu-id="707bf-112">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="707bf-113">步驟1：註冊檔案類型的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="707bf-113">Step 1: Registering a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="707bf-114">除了 (COM) 註冊的一般元件物件模型之外，還請將 **PropertySheetHandlers** 子機碼新增至與檔案類型相關聯之應用程式 ProgID 索引鍵的 **shellex** 子機碼中。</span><span class="sxs-lookup"><span data-stu-id="707bf-114">In addition to normal Component Object Model (COM) registration, add a **PropertySheetHandlers** subkey to the **shellex** subkey of the ProgID key of the application associated with the file type.</span></span> <span data-ttu-id="707bf-115">使用處理程式的名稱建立 **PropertySheetHandlers** 的子機碼，並將預設值設定為屬性工作表處理常式之類別識別碼的字串格式， (CLSID) GUID。</span><span class="sxs-lookup"><span data-stu-id="707bf-115">Create a subkey of **PropertySheetHandlers** with the handler's name, and set the default value to the string form of the property sheet handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="707bf-116">若要在屬性工作表中加入多個頁面，請為每個頁面註冊處理常式。</span><span class="sxs-lookup"><span data-stu-id="707bf-116">To add more than one page to the property sheet, register a handler for each page.</span></span> <span data-ttu-id="707bf-117">屬性工作表可以支援的最大頁面數目是32。</span><span class="sxs-lookup"><span data-stu-id="707bf-117">The maximum number of pages that a property sheet can support is 32.</span></span> <span data-ttu-id="707bf-118">若要註冊多個處理常式，請在每個處理常式的 **shellex** 索引鍵下建立金鑰，並將預設值設定為處理常式的 CLSID GUID。</span><span class="sxs-lookup"><span data-stu-id="707bf-118">To register multiple handlers, create a key under the **shellex** key for each handler, with the default value set to the handler's CLSID GUID.</span></span> <span data-ttu-id="707bf-119">不需要為每個處理常式建立相異物件，這表示多個處理常式可以有相同的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="707bf-119">It is not necessary to create a distinct object for each handler, which means that multiple handlers can all have the same GUID value.</span></span> <span data-ttu-id="707bf-120">頁面將會依其索引鍵列在 [ **shellex**] 底下的順序顯示。</span><span class="sxs-lookup"><span data-stu-id="707bf-120">The pages will be displayed in the order that their keys are listed under **shellex**.</span></span>

<span data-ttu-id="707bf-121">下列範例說明的登錄專案，可啟用 myp 檔案類型的兩個屬性工作表延伸模組處理常式。</span><span class="sxs-lookup"><span data-stu-id="707bf-121">The following example illustrates a registry entry that enables two property sheet extension handlers for an example .myp file type.</span></span> <span data-ttu-id="707bf-122">在此範例中，會針對每個頁面使用個別的物件，但是單一物件也可用於兩者。</span><span class="sxs-lookup"><span data-stu-id="707bf-122">In this example, a separate object is used for each page, but a single object could also be used for both.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="707bf-123">步驟2：為檔案類型執行屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="707bf-123">Step 2: Implementing a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="707bf-124">除了 [屬性工作表處理常式如何運作](propsheet-handlers.md)的一般執行之外，檔案類型的屬性工作表處理常式也必須有適當的 [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) 介面執行。</span><span class="sxs-lookup"><span data-stu-id="707bf-124">In addition to the general implementation discussed in [How Property Sheet Handlers Work](propsheet-handlers.md), a property sheet handler for a file type must also have an appropriate implementation of the [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="707bf-125">只有 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 方法需要 nontoken 執行。</span><span class="sxs-lookup"><span data-stu-id="707bf-125">Only the [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method needs a nontoken implementation.</span></span> <span data-ttu-id="707bf-126">Shell 不會呼叫 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage)。</span><span class="sxs-lookup"><span data-stu-id="707bf-126">The Shell does not call [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span></span>

<span data-ttu-id="707bf-127">[**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)方法可讓屬性工作表處理常式將頁面加入至屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="707bf-127">The [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method allows a property sheet handler to add a page to a property sheet.</span></span> <span data-ttu-id="707bf-128">方法有兩個輸入參數。</span><span class="sxs-lookup"><span data-stu-id="707bf-128">The method has two input parameters.</span></span> <span data-ttu-id="707bf-129">第一個 *lpfnAddPage* 是 [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) 回呼函式的指標，它是用來為 Shell 提供將頁面加入至屬性工作表所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="707bf-129">The first, *lpfnAddPage*, is a pointer to an [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) callback function that is used to provide the Shell with the information needed to add the page to the property sheet.</span></span> <span data-ttu-id="707bf-130">第二個 *lParam* 是 Shell 定義的值，不是由處理常式處理。</span><span class="sxs-lookup"><span data-stu-id="707bf-130">The second, *lParam*, is a Shell-defined value that is not processed by the handler.</span></span> <span data-ttu-id="707bf-131">呼叫回呼函式時，它只會傳回給 Shell。</span><span class="sxs-lookup"><span data-stu-id="707bf-131">It is simply passed back to the Shell when the callback function is called.</span></span>

<span data-ttu-id="707bf-132">執行 [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 的一般程式如下所示。</span><span class="sxs-lookup"><span data-stu-id="707bf-132">The general procedure for implementing [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) is as follows.</span></span>

<span data-ttu-id="707bf-133">**執行 AddPages 方法**</span><span class="sxs-lookup"><span data-stu-id="707bf-133">**Implementing the AddPages Method**</span></span>

1.  <span data-ttu-id="707bf-134">將適當的值指派給 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="707bf-134">Assign appropriate values to the members of a [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span> <span data-ttu-id="707bf-135">尤其是：</span><span class="sxs-lookup"><span data-stu-id="707bf-135">In particular:</span></span>
    -   <span data-ttu-id="707bf-136">將保存處理常式參考計數的變數指派給 **pcRefParent** 成員。</span><span class="sxs-lookup"><span data-stu-id="707bf-136">Assign the variable that holds the handler's reference count to the **pcRefParent** member.</span></span> <span data-ttu-id="707bf-137">這種做法可防止在屬性工作表仍在顯示時卸載處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="707bf-137">This practice prevents the handler object from being unloaded while the property sheet is still being displayed.</span></span>
    -   <span data-ttu-id="707bf-138">您也可以執行 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 回呼函式，並將其指標指派給 **pfnCallback** 成員。</span><span class="sxs-lookup"><span data-stu-id="707bf-138">You can also implement a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function and assign its pointer to a **pfnCallback** member.</span></span> <span data-ttu-id="707bf-139">這個函式會在頁面建立時以及即將終結時呼叫。</span><span class="sxs-lookup"><span data-stu-id="707bf-139">This function is called when the page is created and when it is about to be destroyed.</span></span>
2.  <span data-ttu-id="707bf-140">藉由將 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) 結構傳遞至 [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 函式，建立頁面的 HPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="707bf-140">Create the page's HPAGE handle by passing the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure to the [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span>
3.  <span data-ttu-id="707bf-141">呼叫 *lpfnAddPage* 所指向的函式。</span><span class="sxs-lookup"><span data-stu-id="707bf-141">Call the function that is pointed to by *lpfnAddPage*.</span></span> <span data-ttu-id="707bf-142">將其第一個參數設定為上一個步驟中所建立的 HPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="707bf-142">Set its first parameter to the HPAGE handle that was created in the previous step.</span></span> <span data-ttu-id="707bf-143">將其第二個參數設定為由 Shell 傳遞給 [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)的 *lParam* 值。</span><span class="sxs-lookup"><span data-stu-id="707bf-143">Set its second parameter to the *lParam* value that was passed in to [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) by the Shell.</span></span>
4.  <span data-ttu-id="707bf-144">任何與頁面相關聯的訊息都會傳遞至已指派給 [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3)結構之 **pfnDlgProc** 成員的對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="707bf-144">Any messages associated with the page will be passed to the dialog box procedure that was assigned to the **pfnDlgProc** member of the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span>
5.  <span data-ttu-id="707bf-145">如果您將 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 回呼函式指派給 **pfnCallback**，則會在頁面即將終結時呼叫它。</span><span class="sxs-lookup"><span data-stu-id="707bf-145">If you assigned a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function to **pfnCallback**, it will be called when the page is about to be destroyed.</span></span> <span data-ttu-id="707bf-146">然後，您的處理常式可以執行任何所需的清除作業，例如釋出它所保留的任何參考。</span><span class="sxs-lookup"><span data-stu-id="707bf-146">Your handler can then perform any needed cleanup operations, such as releasing any references that it holds.</span></span>

<span data-ttu-id="707bf-147">下列程式碼範例說明簡單的 [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) 執行。</span><span class="sxs-lookup"><span data-stu-id="707bf-147">The following code sample illustrates a simple [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) implementation.</span></span>


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



<span data-ttu-id="707bf-148">**G \_ hInst** 變數是 DLL 的實例控制碼，而 IDD \_ PAGEDLG 是頁面之對話方塊範本的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="707bf-148">The **g\_hInst** variable is the instance handle to the DLL, and IDD\_PAGEDLG is the resource ID of the page's dialog box template.</span></span> <span data-ttu-id="707bf-149">**PageDlgProc** 函數是處理頁面訊息的對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="707bf-149">The **PageDlgProc** function is the dialog box procedure that handles the page's messages.</span></span> <span data-ttu-id="707bf-150">**G \_ DllRefCount** 變數會保存物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="707bf-150">The **g\_DllRefCount** variable holds the object's reference count.</span></span> <span data-ttu-id="707bf-151">[**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)方法會呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)來遞增計數。</span><span class="sxs-lookup"><span data-stu-id="707bf-151">The [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method calls [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) to increment the count.</span></span> <span data-ttu-id="707bf-152">不過，當頁面即將終結時， **PageCallbackProc** 回呼函數會釋放參考計數。</span><span class="sxs-lookup"><span data-stu-id="707bf-152">However, the reference count is released by the callback function, **PageCallbackProc**, when the page is about to be destroyed.</span></span>

## <a name="remarks"></a><span data-ttu-id="707bf-153">備註</span><span class="sxs-lookup"><span data-stu-id="707bf-153">Remarks</span></span>

<span data-ttu-id="707bf-154">如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="707bf-154">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="707bf-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="707bf-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="707bf-156">**IShellPropSheetExt**</span><span class="sxs-lookup"><span data-stu-id="707bf-156">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
