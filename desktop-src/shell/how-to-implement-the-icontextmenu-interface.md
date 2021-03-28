---
description: ICoNtextMenu 是最強大的功能，但也是最複雜的介面來執行。
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: 如何執行 ICoNtextMenu 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944187"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a><span data-ttu-id="805ee-103">如何執行 ICoNtextMenu 介面</span><span class="sxs-lookup"><span data-stu-id="805ee-103">How to Implement the IContextMenu Interface</span></span>

<span data-ttu-id="805ee-104">[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 是最強大的功能，但也是最複雜的介面來執行。</span><span class="sxs-lookup"><span data-stu-id="805ee-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated interface to implement.</span></span> <span data-ttu-id="805ee-105">強烈建議您使用其中一個靜態動詞方法來執行動詞。</span><span class="sxs-lookup"><span data-stu-id="805ee-105">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="805ee-106">如需詳細資訊，請參閱 [選擇靜態或動態快捷方式功能表方法](shortcut-choose-method.md)。</span><span class="sxs-lookup"><span data-stu-id="805ee-106">For more information, see [Choosing a Static or Dynamic Shortcut Menu Method](shortcut-choose-method.md).</span></span> <span data-ttu-id="805ee-107">[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 有三種方法： [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring)、 [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)和 [**QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)，在這裡會詳細討論。</span><span class="sxs-lookup"><span data-stu-id="805ee-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which are discussed here in detail.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="805ee-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="805ee-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="805ee-109">技術</span><span class="sxs-lookup"><span data-stu-id="805ee-109">Technologies</span></span>

-   <span data-ttu-id="805ee-110">C++</span><span class="sxs-lookup"><span data-stu-id="805ee-110">C++</span></span>

### <a name="prerequisites"></a><span data-ttu-id="805ee-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="805ee-111">Prerequisites</span></span>

-   <span data-ttu-id="805ee-112">靜態動詞</span><span class="sxs-lookup"><span data-stu-id="805ee-112">Static Verb</span></span>
-   <span data-ttu-id="805ee-113">快速鍵功能表</span><span class="sxs-lookup"><span data-stu-id="805ee-113">Shortcut Menu</span></span>

## <a name="instructions"></a><span data-ttu-id="805ee-114">指示</span><span class="sxs-lookup"><span data-stu-id="805ee-114">Instructions</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="805ee-115">ICoNtextMenu：： GetCommandString 方法</span><span class="sxs-lookup"><span data-stu-id="805ee-115">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="805ee-116">處理常式的 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 方法是用來傳回動詞的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="805ee-116">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="805ee-117">這個方法是一個選擇項目。</span><span class="sxs-lookup"><span data-stu-id="805ee-117">This method is optional.</span></span> <span data-ttu-id="805ee-118">在 Windows XP 和舊版的 Windows 中，當 Windows 檔案總管有狀態列時，就會使用這個方法來取得顯示在功能表項目狀態列中的解說文字。</span><span class="sxs-lookup"><span data-stu-id="805ee-118">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="805ee-119">*IdCmd* 參數會保存呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)時所定義命令的識別碼位移。</span><span class="sxs-lookup"><span data-stu-id="805ee-119">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="805ee-120">如果要求了說明字串，則 *uFlags* 會設定為 **gc \_ HELPTEXTW**。</span><span class="sxs-lookup"><span data-stu-id="805ee-120">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="805ee-121">將說明字串複製到 *pszName* 緩衝區，並將其轉換成 **PWSTR**。</span><span class="sxs-lookup"><span data-stu-id="805ee-121">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="805ee-122">將 *uFlags* 設定為 **gc \_ VERBW**，即可要求動詞字串。</span><span class="sxs-lookup"><span data-stu-id="805ee-122">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="805ee-123">將適當的字串複製到 *pszName*，就像使用說明字串一樣。</span><span class="sxs-lookup"><span data-stu-id="805ee-123">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="805ee-124">快速鍵功能表處理常式不會使用 **gc \_ VALIDATEA** 和 **gc \_ VALIDATEW** 旗標。</span><span class="sxs-lookup"><span data-stu-id="805ee-124">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="805ee-125">下列範例顯示 [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring)的簡單執行，其對應至本主題的 [ICoNtextMenu：： QueryCoNtextMenu 方法](shortcut-menu-using-dynamic-verbs.md)一節中所提供的 [**QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)範例。</span><span class="sxs-lookup"><span data-stu-id="805ee-125">The following example shows a simple implementation of [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) section of this topic.</span></span> <span data-ttu-id="805ee-126">因為處理常式只會新增一個功能表項目，所以只能傳回一組字串。</span><span class="sxs-lookup"><span data-stu-id="805ee-126">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="805ee-127">方法會測試 *idCmd* 是否有效，如果是，則會傳回要求的字串。</span><span class="sxs-lookup"><span data-stu-id="805ee-127">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="805ee-128">[**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)函式可用來將要求的字串複製到 *pszName* ，以確保複製的字串不會超過 *cchName* 所指定的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="805ee-128">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="805ee-129">這個範例只會針對 *uFlags* 的 Unicode 值執行支援，因為只有在 Windows 2000 之後 Windows 檔案總管使用這些值。</span><span class="sxs-lookup"><span data-stu-id="805ee-129">This example implements support only for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="805ee-130">ICoNtextMenu：： InvokeCommand 方法</span><span class="sxs-lookup"><span data-stu-id="805ee-130">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="805ee-131">當使用者按一下功能表項目來指示處理常式執行相關聯的命令時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="805ee-131">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="805ee-132">*Pici* 參數指向包含執行命令所需資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="805ee-132">The *pici* parameter points to a structure that contains the information required to run the command.</span></span>

<span data-ttu-id="805ee-133">雖然 *pici* 是在 shlobj.h 中宣告為 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) 結構，但實際上它通常會指向 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構。</span><span class="sxs-lookup"><span data-stu-id="805ee-133">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="805ee-134">此結構是 **CMINVOKECOMMANDINFO** 的延伸版本，而且有數個額外的成員可以傳遞 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="805ee-134">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="805ee-135">檢查 *pici* 的 **cbSize** 成員，以判斷傳入的結構。</span><span class="sxs-lookup"><span data-stu-id="805ee-135">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="805ee-136">如果它是 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構，而且 **fMask** 成員已設定 **CMIC \_ MASK \_ UNICODE** 旗標，請將 *pici* 轉換成 **CMINVOKECOMMANDINFOEX**。</span><span class="sxs-lookup"><span data-stu-id="805ee-136">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="805ee-137">這可讓您的應用程式使用結構中最後五個成員所包含的 Unicode 資訊。</span><span class="sxs-lookup"><span data-stu-id="805ee-137">This enables your application to use the Unicode information that is contained in the last five members of the structure.</span></span>

<span data-ttu-id="805ee-138">結構的 **lpVerb** 或 **lpVerbW** 成員是用來識別要執行的命令。</span><span class="sxs-lookup"><span data-stu-id="805ee-138">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="805ee-139">您可以透過下列兩種方式之一來識別命令：</span><span class="sxs-lookup"><span data-stu-id="805ee-139">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="805ee-140">依命令的動詞字串</span><span class="sxs-lookup"><span data-stu-id="805ee-140">By the command's verb string</span></span>
-   <span data-ttu-id="805ee-141">依命令的識別碼位移</span><span class="sxs-lookup"><span data-stu-id="805ee-141">By the command's identifier offset</span></span>

<span data-ttu-id="805ee-142">若要區分這兩種情況，請檢查 **lpVerb** 的高序位單字是否有 Unicode 案例或 **lpVerbW** 。</span><span class="sxs-lookup"><span data-stu-id="805ee-142">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="805ee-143">如果高序位單字為非零值，則 **lpVerb** 或 **lpVerbW** 會保存動詞字串。</span><span class="sxs-lookup"><span data-stu-id="805ee-143">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="805ee-144">如果高序位字是零，命令位移就會是 **lpVerb** 的低序位字組。</span><span class="sxs-lookup"><span data-stu-id="805ee-144">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="805ee-145">下列範例示範 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 的簡單執行，其對應于在此區段之前和之後提供的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 和 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 範例。</span><span class="sxs-lookup"><span data-stu-id="805ee-145">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="805ee-146">方法會先決定要傳入的結構。</span><span class="sxs-lookup"><span data-stu-id="805ee-146">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="805ee-147">接著，它會判斷命令是否以其位移或其動詞來識別。</span><span class="sxs-lookup"><span data-stu-id="805ee-147">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="805ee-148">如果 **lpVerb** 或 **lpVerbW** 保存有效的動詞或位移，則方法會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="805ee-148">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="805ee-149">ICoNtextMenu：： QueryCoNtextMenu 方法</span><span class="sxs-lookup"><span data-stu-id="805ee-149">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="805ee-150">Shell 會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) ，以啟用快捷方式功能表處理常式，將其功能表項目加入功能表中。</span><span class="sxs-lookup"><span data-stu-id="805ee-150">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="805ee-151">它會傳入 *HMENU* 參數中的 **HMENU** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="805ee-151">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="805ee-152">*IndexMenu* 參數會設定為要用於要加入之第一個功能表項目的索引。</span><span class="sxs-lookup"><span data-stu-id="805ee-152">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="805ee-153">處理常式所加入的任何功能表項目都必須有介於 *idCmdFirst* 和 *idCmdLast* 參數值之間的識別碼。</span><span class="sxs-lookup"><span data-stu-id="805ee-153">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="805ee-154">一般來說，第一個命令識別碼會設定為 *idCmdFirst*，每個額外的命令 (1) 遞增一次。</span><span class="sxs-lookup"><span data-stu-id="805ee-154">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="805ee-155">這種做法可協助您避免超出 *idCmdLast* ，並在 Shell 呼叫多個處理常式時，將可用識別碼的數目最大化。</span><span class="sxs-lookup"><span data-stu-id="805ee-155">This practice helps you to avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="805ee-156">專案識別碼的 *命令位移* 是 *idCmdFirst* 中識別碼和值之間的差異。</span><span class="sxs-lookup"><span data-stu-id="805ee-156">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="805ee-157">將您的處理常式所加入之每個專案的位移儲存至快捷方式功能表，因為如果其後呼叫 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 或 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)，則 Shell 可能會使用位移來識別該專案。</span><span class="sxs-lookup"><span data-stu-id="805ee-157">Store the offset of each item that your handler adds to the shortcut menu, because the Shell might use the offset to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="805ee-158">您也應該將 [動詞](launch.md) 指派給您新增的每個命令。</span><span class="sxs-lookup"><span data-stu-id="805ee-158">You should also assign a [verb](launch.md) to each command that you add.</span></span> <span data-ttu-id="805ee-159">動詞是在呼叫 [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 時，可以用來代替位移來識別命令的字串。</span><span class="sxs-lookup"><span data-stu-id="805ee-159">A verb is a string that can be used instead of the offset to identify the command when [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="805ee-160">函式（例如 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ）也會用來執行快捷方式功能表命令。</span><span class="sxs-lookup"><span data-stu-id="805ee-160">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="805ee-161">有三個旗標可以透過與快捷方式功能表處理常式相關的 *uFlags* 參數傳入。</span><span class="sxs-lookup"><span data-stu-id="805ee-161">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="805ee-162">如下表中所述。</span><span class="sxs-lookup"><span data-stu-id="805ee-162">They are described in the following table.</span></span>



| <span data-ttu-id="805ee-163">旗標</span><span class="sxs-lookup"><span data-stu-id="805ee-163">Flag</span></span>             | <span data-ttu-id="805ee-164">描述</span><span class="sxs-lookup"><span data-stu-id="805ee-164">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805ee-165">CMF \_ DEFAULTONLY</span><span class="sxs-lookup"><span data-stu-id="805ee-165">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="805ee-166">使用者選取了預設的命令，通常是按兩下物件。</span><span class="sxs-lookup"><span data-stu-id="805ee-166">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="805ee-167">[**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 應該將控制權交還給 Shell，而不需修改功能表。</span><span class="sxs-lookup"><span data-stu-id="805ee-167">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="805ee-168">CMF \_ NODEFAULT</span><span class="sxs-lookup"><span data-stu-id="805ee-168">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="805ee-169">功能表中的專案都不應該是預設專案。</span><span class="sxs-lookup"><span data-stu-id="805ee-169">No item in the menu should be the default item.</span></span> <span data-ttu-id="805ee-170">方法應該將其命令新增至功能表。</span><span class="sxs-lookup"><span data-stu-id="805ee-170">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="805ee-171">CMF \_ 正常</span><span class="sxs-lookup"><span data-stu-id="805ee-171">CMF\_NORMAL</span></span>      | <span data-ttu-id="805ee-172">快捷方式功能表將會正常顯示。</span><span class="sxs-lookup"><span data-stu-id="805ee-172">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="805ee-173">方法應該將其命令新增至功能表。</span><span class="sxs-lookup"><span data-stu-id="805ee-173">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="805ee-174">您可以使用 [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) 或 [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) ，將功能表項目新增至清單。</span><span class="sxs-lookup"><span data-stu-id="805ee-174">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="805ee-175">然後傳回嚴重性值設定為「嚴重性成功」的 **HRESULT** 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="805ee-175">Then return an **HRESULT** value with the severity set to SEVERITY\_SUCCESS.</span></span> <span data-ttu-id="805ee-176">將 [程式碼] 值設定為已指派最大命令識別碼的位移，再加上一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="805ee-176">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="805ee-177">例如，假設 *idCmdFirst* 設為5，而您將三個專案新增至功能表，並將命令識別碼設定為5、7和8。</span><span class="sxs-lookup"><span data-stu-id="805ee-177">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="805ee-178">傳回值應設為 \_ HRESULT (嚴重性 \_ 成功、0、8 + 1) 。</span><span class="sxs-lookup"><span data-stu-id="805ee-178">The return value should be MAKE\_HRESULT(SEVERITY\_SUCCESS, 0, 8 + 1).</span></span>

<span data-ttu-id="805ee-179">下列範例顯示插入單一命令的 [**QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 簡單執行。</span><span class="sxs-lookup"><span data-stu-id="805ee-179">The following example shows a simple implementation of [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="805ee-180">此命令的識別碼位移是 IDM \_ 顯示，其設定為零。</span><span class="sxs-lookup"><span data-stu-id="805ee-180">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="805ee-181">**M \_ pszVerb** 和 **m \_ pwszVerb** 變數是私用變數，用來以 ANSI 和 Unicode 格式儲存相關聯的語言獨立動詞字串。</span><span class="sxs-lookup"><span data-stu-id="805ee-181">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables that are used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a><span data-ttu-id="805ee-182">備註</span><span class="sxs-lookup"><span data-stu-id="805ee-182">Remarks</span></span>

<span data-ttu-id="805ee-183">如需其他動詞的執行工作，請參閱 [建立快捷方式功能表處理常式](context-menu-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="805ee-183">For other verb implementation tasks, see [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

 

 
