---
title: 'PROPSHEETPAGE 結構 (Prsht.idl .h) '
description: 定義屬性工作表中的頁面。
keywords:
- PROPSHEETPAGE 結構 Windows 控制項
topic_type:
- apiref
api_name:
- PROPSHEETPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 78e1d1e4e6b4b2067083443bdb5dc4db5df59558
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550343"
---
# <a name="propsheetpage-structure"></a><span data-ttu-id="51644-104">PROPSHEETPAGE 結構</span><span class="sxs-lookup"><span data-stu-id="51644-104">PROPSHEETPAGE structure</span></span>

<span data-ttu-id="51644-105">定義屬性工作表中的頁面。</span><span class="sxs-lookup"><span data-stu-id="51644-105">Defines a page in a property sheet.</span></span>

## <a name="syntax"></a><span data-ttu-id="51644-106">語法</span><span class="sxs-lookup"><span data-stu-id="51644-106">Syntax</span></span>

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HINSTANCE  hInstance;
    union {
        LPCSTR                 pszTemplate;
        PROPSHEETPAGE_RESOURCE pResource;
    };
    union {
        HICON  hIcon;
        LPCSTR pszIcon;
    };
    LPCSTR          pszTitle;
    DLGPROC         pfnDlgProc;
    LPARAM          lParam;
    LPFNPSPCALLBACK pfnCallback;
    UINT            *pcRefParent;
    LPCTSTR         pszHeaderTitle;
    LPCTSTR         pszHeaderSubTitle;
    HANDLE          hActCtx;
    union 
    {
        HBITMAP     hbmHeader;
        LPCSTR      pszbmHeader;
    }
} PROPSHEETPAGE, *LPPROPSHEETPAGE;
```

## <a name="members"></a><span data-ttu-id="51644-107">成員</span><span class="sxs-lookup"><span data-stu-id="51644-107">Members</span></span>

<span data-ttu-id="51644-108">*dwSize*</span><span class="sxs-lookup"><span data-stu-id="51644-108">*dwSize*</span></span> 

<span data-ttu-id="51644-109">類型： [DWORD](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-109">Type: [DWORD](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-110">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="51644-110">Size, in bytes, of this structure.</span></span>

<span data-ttu-id="51644-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="51644-111">*dwFlags*</span></span> 

<span data-ttu-id="51644-112">類型： [DWORD](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-112">Type: [DWORD](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-113">旗標，指出建立屬性工作表頁面時要使用的選項。</span><span class="sxs-lookup"><span data-stu-id="51644-113">Flags that indicate which options to use when creating the property sheet page.</span></span> <span data-ttu-id="51644-114">這個成員可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="51644-114">This member can be a combination of the following values.</span></span>

| <span data-ttu-id="51644-115">值</span><span class="sxs-lookup"><span data-stu-id="51644-115">Value</span></span> | <span data-ttu-id="51644-116">意義</span><span class="sxs-lookup"><span data-stu-id="51644-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="51644-117">PSP_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="51644-117">PSP_DEFAULT</span></span> | <span data-ttu-id="51644-118">使用所有結構成員的預設意義。</span><span class="sxs-lookup"><span data-stu-id="51644-118">Uses the default meaning for all structure members.</span></span> <span data-ttu-id="51644-119">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-119">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span> |
| <span data-ttu-id="51644-120">PSP_DLGINDIRECT</span><span class="sxs-lookup"><span data-stu-id="51644-120">PSP_DLGINDIRECT</span></span> | <span data-ttu-id="51644-121">從 *pResource* 成員所指向之記憶體中的對話方塊範本建立頁面。</span><span class="sxs-lookup"><span data-stu-id="51644-121">Creates the page from the dialog box template in memory pointed to by the *pResource* member.</span></span> <span data-ttu-id="51644-122">[PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta)函式會假設記憶體中的範本未寫入保護。</span><span class="sxs-lookup"><span data-stu-id="51644-122">The [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) function assumes that the template that is in memory is not write-protected.</span></span> <span data-ttu-id="51644-123">唯讀範本會在某些版本的 Windows 中造成例外狀況。</span><span class="sxs-lookup"><span data-stu-id="51644-123">A read-only template will cause an exception in some versions of Windows.</span></span> |
| <span data-ttu-id="51644-124">PSP_HASHELP</span><span class="sxs-lookup"><span data-stu-id="51644-124">PSP_HASHELP</span></span> | <span data-ttu-id="51644-125">當頁面為使用中狀態時，啟用 **屬性工作表說明** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="51644-125">Enables the property sheet **Help** button when the page is active.</span></span> <span data-ttu-id="51644-126">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-126">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span> |
| <span data-ttu-id="51644-127">PSP_HIDEHEADER</span><span class="sxs-lookup"><span data-stu-id="51644-127">PSP_HIDEHEADER</span></span> | <span data-ttu-id="51644-128">[5.80 版](common-control-versions.md) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-128">[Version 5.80](common-control-versions.md) and later.</span></span> <span data-ttu-id="51644-129">當選取頁面時，讓 wizard 屬性工作表隱藏頁首區域。</span><span class="sxs-lookup"><span data-stu-id="51644-129">Causes the wizard property sheet to hide the header area when the page is selected.</span></span> <span data-ttu-id="51644-130">如果已提供浮水印，則會在頁面的左側繪製。</span><span class="sxs-lookup"><span data-stu-id="51644-130">If a watermark has been provided, it will be painted on the left side of the page.</span></span> <span data-ttu-id="51644-131">此旗標應針對 [歡迎使用] 和 [完成] 頁面設定，並針對內部頁面省略。</span><span class="sxs-lookup"><span data-stu-id="51644-131">This flag should be set for welcome and completion pages, and omitted for interior pages.</span></span> <span data-ttu-id="51644-132">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-132">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span> |
| <span data-ttu-id="51644-133">PSP_PREMATURE</span><span class="sxs-lookup"><span data-stu-id="51644-133">PSP_PREMATURE</span></span> | <span data-ttu-id="51644-134">[4.71 版](common-control-versions.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-134">[Version 4.71](common-control-versions.md) or later.</span></span> <span data-ttu-id="51644-135">當建立屬性工作表時，會建立頁面。</span><span class="sxs-lookup"><span data-stu-id="51644-135">Causes the page to be created when the property sheet is created.</span></span> <span data-ttu-id="51644-136">如果未指定此旗標，則在第一次選取該頁面之前，將不會建立該頁面。</span><span class="sxs-lookup"><span data-stu-id="51644-136">If this flag is not specified, the page will not be created until it is selected the first time.</span></span> <span data-ttu-id="51644-137">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-137">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span> |
| <span data-ttu-id="51644-138">PSP_RTLREADING</span><span class="sxs-lookup"><span data-stu-id="51644-138">PSP_RTLREADING</span></span> | <span data-ttu-id="51644-139">反轉顯示 *pszTitle* 的方向。</span><span class="sxs-lookup"><span data-stu-id="51644-139">Reverses the direction in which *pszTitle* is displayed.</span></span> <span data-ttu-id="51644-140">一般視窗會顯示所有文字，包括 *pszTitle*、由左至右 (LTR) 。</span><span class="sxs-lookup"><span data-stu-id="51644-140">Normal windows display all text, including *pszTitle*, left-to-right (LTR).</span></span> <span data-ttu-id="51644-141">針對從右至左 (RTL) 的希伯來文或阿拉伯文等語言，可以將視窗鏡像，所有文字都會以 RTL 顯示。</span><span class="sxs-lookup"><span data-stu-id="51644-141">For languages such as Hebrew or Arabic that read right-to-left (RTL), a window can be mirrored and all text will be displayed RTL.</span></span> <span data-ttu-id="51644-142">如果設定了 PSP_RTLREADING， *pszTitle* 會改為在一般父視窗中讀取 RTL，並在鏡像父視窗中 LTR。</span><span class="sxs-lookup"><span data-stu-id="51644-142">If PSP_RTLREADING is set, *pszTitle* will instead read RTL in a normal parent window, and LTR in a mirrored parent window.</span></span> |
| <span data-ttu-id="51644-143">PSP_USECALLBACK</span><span class="sxs-lookup"><span data-stu-id="51644-143">PSP_USECALLBACK</span></span> | <span data-ttu-id="51644-144">當建立或終結此結構所定義的屬性工作表頁面時，呼叫 *pfnCallback* 成員所指定的函式。</span><span class="sxs-lookup"><span data-stu-id="51644-144">Calls the function specified by the *pfnCallback* member when creating or destroying the property sheet page defined by this structure.</span></span> |
| <span data-ttu-id="51644-145">PSP_USEFUSIONCONTEXT</span><span class="sxs-lookup"><span data-stu-id="51644-145">PSP_USEFUSIONCONTEXT</span></span> | <span data-ttu-id="51644-146">[6.0 版](common-control-versions.md) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-146">[Version 6.0](common-control-versions.md) and later.</span></span> <span data-ttu-id="51644-147">使用啟用內容。</span><span class="sxs-lookup"><span data-stu-id="51644-147">Use an activation context.</span></span> <span data-ttu-id="51644-148">若要使用啟用內容，您必須設定這個旗標，並將啟用內容控制碼指派給 *hActCtx*。</span><span class="sxs-lookup"><span data-stu-id="51644-148">To use an activation context, you must set this flag and assign the activation context handle to *hActCtx*.</span></span> <span data-ttu-id="51644-149">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="51644-149">See the Remarks.</span></span> |
| <span data-ttu-id="51644-150">PSP_USEHEADERSUBTITLE</span><span class="sxs-lookup"><span data-stu-id="51644-150">PSP_USEHEADERSUBTITLE</span></span> | <span data-ttu-id="51644-151">[5.80 版](common-control-versions.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-151">[Version 5.80](common-control-versions.md) or later.</span></span> <span data-ttu-id="51644-152">顯示 *pszHeaderSubTitle* 成員指向的字串，做為 Wizard97 頁面標頭區域的子標題。</span><span class="sxs-lookup"><span data-stu-id="51644-152">Displays the string pointed to by the *pszHeaderSubTitle* member as the subtitle of the header area of a Wizard97 page.</span></span> <span data-ttu-id="51644-153">若要使用此旗標，您也必須在相關聯的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-153">To use this flag, you must also set the PSH_WIZARD97 flag in the *dwFlags* member of the associated [PROPSHEETHEADER](pss-propsheetheader.md) structure.</span></span> <span data-ttu-id="51644-154">如果已設定 PSP_HIDEHEADER，則會忽略 PSP_USEHEADERSUBTITLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-154">The PSP_USEHEADERSUBTITLE flag is ignored if PSP_HIDEHEADER is set.</span></span> <span data-ttu-id="51644-155">在 Aero 樣式的嚮導中，標題會出現在工作區頂端附近。</span><span class="sxs-lookup"><span data-stu-id="51644-155">In Aero-style wizards, the title appears near the top of the client area.</span></span> |
| <span data-ttu-id="51644-156">PSP_USEHEADERTITLE</span><span class="sxs-lookup"><span data-stu-id="51644-156">PSP_USEHEADERTITLE</span></span> | <span data-ttu-id="51644-157">[5.80 版](common-control-versions.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-157">[Version 5.80](common-control-versions.md) or later.</span></span> <span data-ttu-id="51644-158">顯示 *pszHeaderTitle* 成員所指向的字串，做為 Wizard97 內部頁面標頭中的標題。</span><span class="sxs-lookup"><span data-stu-id="51644-158">Displays the string pointed to by the *pszHeaderTitle* member as the title in the header of a Wizard97 interior page.</span></span> <span data-ttu-id="51644-159">您也必須在相關聯的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-159">You must also set the PSH_WIZARD97 flag in the *dwFlags* member of the associated [PROPSHEETHEADER](pss-propsheetheader.md) structure.</span></span> <span data-ttu-id="51644-160">如果已設定 PSP_HIDEHEADER，則會忽略 PSP_USEHEADERTITLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-160">The PSP_USEHEADERTITLE flag is ignored if PSP_HIDEHEADER is set.</span></span> <span data-ttu-id="51644-161">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-161">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span> |
| <span data-ttu-id="51644-162">PSP_USEHICON</span><span class="sxs-lookup"><span data-stu-id="51644-162">PSP_USEHICON</span></span> | <span data-ttu-id="51644-163">使用 *hIcon* 做為頁面索引標籤上的小圖示。</span><span class="sxs-lookup"><span data-stu-id="51644-163">Uses *hIcon* as the small icon on the tab for the page.</span></span> <span data-ttu-id="51644-164">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-164">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span>  |
| <span data-ttu-id="51644-165">PSP_USEICONID</span><span class="sxs-lookup"><span data-stu-id="51644-165">PSP_USEICONID</span></span> | <span data-ttu-id="51644-166">使用 *pszIcon* 做為要載入的圖示資源名稱，並作為頁面索引標籤上的小圖示使用。</span><span class="sxs-lookup"><span data-stu-id="51644-166">Uses *pszIcon* as the name of the icon resource to load and use as the small icon on the tab for the page.</span></span> <span data-ttu-id="51644-167">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-167">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span> |
| <span data-ttu-id="51644-168">PSP_USEREFPARENT</span><span class="sxs-lookup"><span data-stu-id="51644-168">PSP_USEREFPARENT</span></span> | <span data-ttu-id="51644-169">針對從此結構建立的屬性工作表頁面存留期，維護 *pcRefParent* 成員所指定的參考計數。</span><span class="sxs-lookup"><span data-stu-id="51644-169">Maintains the reference count specified by the *pcRefParent* member for the lifetime of the property sheet page created from this structure.</span></span> |
| <span data-ttu-id="51644-170">PSP_USETITLE</span><span class="sxs-lookup"><span data-stu-id="51644-170">PSP_USETITLE</span></span> | <span data-ttu-id="51644-171">使用 *pszTitle* 成員做為屬性工作表對話方塊的標題，而不是儲存在對話方塊範本中的標題。</span><span class="sxs-lookup"><span data-stu-id="51644-171">Uses the *pszTitle* member as the title of the property sheet dialog box instead of the title stored in the dialog box template.</span></span> <span data-ttu-id="51644-172">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)) 時，不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-172">This flag is not supported when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md)).</span></span> |

<span data-ttu-id="51644-173">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="51644-173">*hInstance*</span></span> 

<span data-ttu-id="51644-174">類型： [HINSTANCE](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-174">Type: [HINSTANCE](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-175">要從其中載入圖示或字串資源的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="51644-175">Handle to the instance from which to load an icon or string resource.</span></span> <span data-ttu-id="51644-176">如果 *pszIcon*、 *pszTitle*、 *pszHeaderTitle* 或 *pszHeaderSubTitle* 成員識別要載入的資源，則必須指定 *hInstance* 。</span><span class="sxs-lookup"><span data-stu-id="51644-176">If the *pszIcon*, *pszTitle*, *pszHeaderTitle*, or *pszHeaderSubTitle* member identifies a resource to load, *hInstance* must be specified.</span></span>

<span data-ttu-id="51644-177">*pszTemplate*</span><span class="sxs-lookup"><span data-stu-id="51644-177">*pszTemplate*</span></span> 

<span data-ttu-id="51644-178">類型： [LPCSTR](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-178">Type: [LPCSTR](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-179">用來建立頁面的對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="51644-179">Dialog box template to use to create the page.</span></span> <span data-ttu-id="51644-180">這個成員可以指定範本的資源識別碼，或指定範本名稱的字串位址。</span><span class="sxs-lookup"><span data-stu-id="51644-180">This member can specify either the resource identifier of the template or the address of a string that specifies the name of the template.</span></span> <span data-ttu-id="51644-181">如果已設定 *dwFlags* 成員中的 PSP_DLGINDIRECT 旗標，則會忽略 *pszTemplate* 。</span><span class="sxs-lookup"><span data-stu-id="51644-181">If the PSP_DLGINDIRECT flag in the *dwFlags* member is set, *pszTemplate* is ignored.</span></span> <span data-ttu-id="51644-182">這個成員會宣告為具有 *pResource* 的聯集。</span><span class="sxs-lookup"><span data-stu-id="51644-182">This member is declared as a union with *pResource*.</span></span>

<span data-ttu-id="51644-183">*pResource*</span><span class="sxs-lookup"><span data-stu-id="51644-183">*pResource*</span></span> 

<span data-ttu-id="51644-184">類型： **LPCDLGTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="51644-184">Type: **LPCDLGTEMPLATE**</span></span>

<span data-ttu-id="51644-185">記憶體中對話方塊範本的指標。</span><span class="sxs-lookup"><span data-stu-id="51644-185">Pointer to a dialog box template in memory.</span></span> <span data-ttu-id="51644-186">[PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta)函式會假設範本未受寫入保護。</span><span class="sxs-lookup"><span data-stu-id="51644-186">The [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) function assumes that the template is not write-protected.</span></span> <span data-ttu-id="51644-187">唯讀範本會在某些版本的 Windows 中造成例外狀況。</span><span class="sxs-lookup"><span data-stu-id="51644-187">A read-only template will cause an exception in some versions of Windows.</span></span> <span data-ttu-id="51644-188">若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_DLGINDIRECT 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-188">To use this member, you must set the PSP_DLGINDIRECT flag in the *dwFlags* member.</span></span> <span data-ttu-id="51644-189">這個成員會宣告為具有 *pszTemplate* 的聯集。</span><span class="sxs-lookup"><span data-stu-id="51644-189">This member is declared as a union with *pszTemplate*.</span></span>

<span data-ttu-id="51644-190">*hIcon*</span><span class="sxs-lookup"><span data-stu-id="51644-190">*hIcon*</span></span> 

<span data-ttu-id="51644-191">類型： [HICON](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-191">Type: [HICON](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-192">圖示的控制碼，用來做為頁面索引標籤中的圖示。</span><span class="sxs-lookup"><span data-stu-id="51644-192">Handle to the icon to use as the icon in the tab of the page.</span></span> <span data-ttu-id="51644-193">如果 *dwFlags* 成員不包含 PSP_USEHICON，則會忽略這個成員。</span><span class="sxs-lookup"><span data-stu-id="51644-193">If the *dwFlags* member does not include PSP_USEHICON, this member is ignored.</span></span> <span data-ttu-id="51644-194">這個成員會宣告為具有 *pszIcon* 的聯集。</span><span class="sxs-lookup"><span data-stu-id="51644-194">This member is declared as a union with *pszIcon*.</span></span>

<span data-ttu-id="51644-195">*pszIcon*</span><span class="sxs-lookup"><span data-stu-id="51644-195">*pszIcon*</span></span> 

<span data-ttu-id="51644-196">類型： [LPCSTR](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-196">Type: [LPCSTR](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-197">圖示資源，用來做為頁面索引標籤中的圖示。</span><span class="sxs-lookup"><span data-stu-id="51644-197">Icon resource to use as the icon in the tab of the page.</span></span> <span data-ttu-id="51644-198">這個成員可以指定圖示資源的識別碼，或指定圖示資源名稱的字串位址。</span><span class="sxs-lookup"><span data-stu-id="51644-198">This member can specify either the identifier of the icon resource or the address of the string that specifies the name of the icon resource.</span></span> <span data-ttu-id="51644-199">若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USEICONID 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-199">To use this member, you must set the PSP_USEICONID flag in the *dwFlags* member.</span></span> <span data-ttu-id="51644-200">這個成員會宣告為具有 *hIcon* 的聯集。</span><span class="sxs-lookup"><span data-stu-id="51644-200">This member is declared as a union with *hIcon*.</span></span>

<span data-ttu-id="51644-201">*pszTitle*</span><span class="sxs-lookup"><span data-stu-id="51644-201">*pszTitle*</span></span> 

<span data-ttu-id="51644-202">類型： [LPCSTR](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-202">Type: [LPCSTR](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-203">[屬性工作表] 對話方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="51644-203">Title of the property sheet dialog box.</span></span> <span data-ttu-id="51644-204">此標題會覆寫對話方塊範本中指定的標題。</span><span class="sxs-lookup"><span data-stu-id="51644-204">This title overrides the title specified in the dialog box template.</span></span> <span data-ttu-id="51644-205">這個成員可以指定字串資源的識別碼或指定標題之字串的位址。</span><span class="sxs-lookup"><span data-stu-id="51644-205">This member can specify either the identifier of a string resource or the address of a string that specifies the title.</span></span> <span data-ttu-id="51644-206">若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USETITLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-206">To use this member, you must set the PSP_USETITLE flag in the *dwFlags* member.</span></span>

<span data-ttu-id="51644-207">*pfnDlgProc*</span><span class="sxs-lookup"><span data-stu-id="51644-207">*pfnDlgProc*</span></span> 

<span data-ttu-id="51644-208">類型： **DLGPROC**</span><span class="sxs-lookup"><span data-stu-id="51644-208">Type: **DLGPROC**</span></span>

<span data-ttu-id="51644-209">頁面的對話方塊程式指標。</span><span class="sxs-lookup"><span data-stu-id="51644-209">Pointer to the dialog box procedure for the page.</span></span> <span data-ttu-id="51644-210">因為頁面是建立為非強制回應對話方塊，所以對話方塊程式不能呼叫 [EndDialog](/windows/win32/api/winuser/nf-winuser-enddialog) 函數。</span><span class="sxs-lookup"><span data-stu-id="51644-210">Because the pages are created as modeless dialog boxes, the dialog box procedure must not call the [EndDialog](/windows/win32/api/winuser/nf-winuser-enddialog) function.</span></span>

<span data-ttu-id="51644-211">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51644-211">*lParam*</span></span> 

<span data-ttu-id="51644-212">類型： [LPARAM](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-212">Type: [LPARAM](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-213">當建立頁面時，會將頁面的 **PROPSHEETPAGE** 結構複本傳遞至對話方塊程式，並提供 [WM_INITDIALOG](../dlgbox/wm-initdialog.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="51644-213">When the page is created, a copy of the page's **PROPSHEETPAGE** structure is passed to the dialog box procedure with a [WM_INITDIALOG](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="51644-214">系統會提供 *lParam* 成員，讓您將應用程式特定的資訊傳遞給對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="51644-214">The *lParam* member is provided to allow you to pass application-specific information to the dialog box procedure.</span></span> <span data-ttu-id="51644-215">它不會對頁面本身產生任何影響。</span><span class="sxs-lookup"><span data-stu-id="51644-215">It has no effect on the page itself.</span></span>

<span data-ttu-id="51644-216">*pfnCallback*</span><span class="sxs-lookup"><span data-stu-id="51644-216">*pfnCallback*</span></span> 

<span data-ttu-id="51644-217">類型： **LPFNPSPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="51644-217">Type: **LPFNPSPCALLBACK**</span></span>

<span data-ttu-id="51644-218">應用程式定義回呼函式的指標，該函式會在頁面建立時以及即將終結時呼叫。</span><span class="sxs-lookup"><span data-stu-id="51644-218">Pointer to an application-defined callback function that is called when the page is created and when it is about to be destroyed.</span></span> <span data-ttu-id="51644-219">如需回呼函數的詳細資訊，請參閱 [LPFNPSPCALLBACKA 回呼函數](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)。</span><span class="sxs-lookup"><span data-stu-id="51644-219">For more information about the callback function, see [LPFNPSPCALLBACKA callback function](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka).</span></span> <span data-ttu-id="51644-220">若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USECALLBACK 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-220">To use this member, you must set the PSP_USECALLBACK flag in the *dwFlags* member.</span></span>

<span data-ttu-id="51644-221">*pcRefParent*</span><span class="sxs-lookup"><span data-stu-id="51644-221">*pcRefParent*</span></span> 

<span data-ttu-id="51644-222">類型： [UINT \*](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-222">Type: [UINT\*](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-223">參考計數值的指標。</span><span class="sxs-lookup"><span data-stu-id="51644-223">Pointer to the reference count value.</span></span> <span data-ttu-id="51644-224">若要使用這個成員，您必須在 *dwFlags* 成員中設定 PSP_USEREFPARENT 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-224">To use this member, you must set the PSP_USEREFPARENT flag in the *dwFlags* member.</span></span>

> [!NOTE]
> <span data-ttu-id="51644-225">建立屬性工作表頁面時， *pcRefParent* 所指向的值會遞增。</span><span class="sxs-lookup"><span data-stu-id="51644-225">When a property sheet page is created, the value pointed to by *pcRefParent* is incremented.</span></span> <span data-ttu-id="51644-226">您可以在 [PROPSHEETHEADER](pss-propsheetheader.md)的 *dwFlags* 成員中設定 PSH_PROPSHEETPAGE 旗標，並呼叫 [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta)函式，以隱含方式建立屬性工作表頁面。</span><span class="sxs-lookup"><span data-stu-id="51644-226">You create a property sheet page implicitly by setting the PSH_PROPSHEETPAGE flag in the *dwFlags* member of [PROPSHEETHEADER](pss-propsheetheader.md) and calling the [PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) function.</span></span> <span data-ttu-id="51644-227">您可以使用 [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) 函式來明確地進行。</span><span class="sxs-lookup"><span data-stu-id="51644-227">You can do it explicitly by using the [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span> <span data-ttu-id="51644-228">當屬性工作表頁面損毀時， *pcRefParent* 成員指向的值會遞減。</span><span class="sxs-lookup"><span data-stu-id="51644-228">When a property sheet page is destroyed, the value pointed to by the *pcRefParent* member is decremented.</span></span> <span data-ttu-id="51644-229">當屬性工作表損毀時，就會自動發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="51644-229">This takes place automatically when the property sheet is destroyed.</span></span> <span data-ttu-id="51644-230">您可以使用 [DestroyPropertySheetPage](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage) 函式來明確終結屬性工作表頁面。</span><span class="sxs-lookup"><span data-stu-id="51644-230">You can explicitly destroy a property sheet page by using the [DestroyPropertySheetPage](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage) function.</span></span>

<span data-ttu-id="51644-231">*pszHeaderTitle*</span><span class="sxs-lookup"><span data-stu-id="51644-231">*pszHeaderTitle*</span></span> 

<span data-ttu-id="51644-232">類型： [LPCTSTR](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-232">Type: [LPCTSTR](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-233">[5.80 版](common-control-versions.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-233">[Version 5.80](common-control-versions.md) or later.</span></span> <span data-ttu-id="51644-234">標題區域的標題。</span><span class="sxs-lookup"><span data-stu-id="51644-234">Title of the header area.</span></span> <span data-ttu-id="51644-235">若要在 Wizard97 樣式的 wizard 下使用這個成員，您也必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="51644-235">To use this member under the Wizard97-style wizard, you must also do the following:</span></span>

* <span data-ttu-id="51644-236">在 *dwFlags* 成員中設定 PSP_USEHEADERTITLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-236">Set the PSP_USEHEADERTITLE flag in the *dwFlags* member.</span></span>
* <span data-ttu-id="51644-237">在頁面的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-237">Set the PSH_WIZARD97 flag in the *dwFlags* member of the page's [PROPSHEETHEADER](pss-propsheetheader.md) structure.</span></span>
* <span data-ttu-id="51644-238">請確定未設定 *dwFlags* 成員中的 PSP_HIDEHEADER 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-238">Make sure that the PSP_HIDEHEADER flag in the *dwFlags* member is not set.</span></span>

<span data-ttu-id="51644-239">*pszHeaderSubTitle*</span><span class="sxs-lookup"><span data-stu-id="51644-239">*pszHeaderSubTitle*</span></span> 

<span data-ttu-id="51644-240">類型： [LPCTSTR](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-240">Type: [LPCTSTR](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-241">[5.80 版](common-control-versions.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-241">[Version 5.80](common-control-versions.md) or later.</span></span> <span data-ttu-id="51644-242">標題區域的子標題。</span><span class="sxs-lookup"><span data-stu-id="51644-242">Subtitle of the header area.</span></span> <span data-ttu-id="51644-243">若要使用這個成員，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="51644-243">To use this member, you must do the following:</span></span>

* <span data-ttu-id="51644-244">在 *dwFlags* 成員中設定 PSP_USEHEADERSUBTITLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-244">Set the PSP_USEHEADERSUBTITLE flag in the *dwFlags* member.</span></span>
* <span data-ttu-id="51644-245">在頁面的 [PROPSHEETHEADER](pss-propsheetheader.md)結構的 *dwFlags* 成員中設定 PSH_WIZARD97 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-245">Set the PSH_WIZARD97 flag in the *dwFlags* member of the page's [PROPSHEETHEADER](pss-propsheetheader.md) structure.</span></span>
* <span data-ttu-id="51644-246">請確定未設定 *dwFlags* 成員中的 PSP_HIDEHEADER 旗標。</span><span class="sxs-lookup"><span data-stu-id="51644-246">Make sure that the PSP_HIDEHEADER flag in the *dwFlags* member is not set.</span></span>

> [!NOTE]
> <span data-ttu-id="51644-247">使用 Aero 樣式的 wizard ([PSH_AEROWIZARD](pss-propsheetheader.md) 時，會忽略這個成員) </span><span class="sxs-lookup"><span data-stu-id="51644-247">This member is ignored when using the Aero-style wizard ([PSH_AEROWIZARD](pss-propsheetheader.md))</span></span>

<span data-ttu-id="51644-248">*hActCtx*</span><span class="sxs-lookup"><span data-stu-id="51644-248">*hActCtx*</span></span> 

<span data-ttu-id="51644-249">類型： [控制碼](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-249">Type: [HANDLE](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-250">[6.0 版](common-control-versions.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="51644-250">[Version 6.0](common-control-versions.md) or later.</span></span> <span data-ttu-id="51644-251">啟用內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="51644-251">An activation context handle.</span></span> <span data-ttu-id="51644-252">將這個成員設定為當您使用 [CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa)建立啟用內容時所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="51644-252">Set this member to the handle that is returned when you create the activation context with [CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa).</span></span> <span data-ttu-id="51644-253">系統會先啟動此內容，再建立對話方塊。</span><span class="sxs-lookup"><span data-stu-id="51644-253">The system will activate this context before creating the dialog box.</span></span> <span data-ttu-id="51644-254">如果您使用全域資訊清單，就不需要使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="51644-254">You do not need to use this member if you use a global manifest.</span></span>

<span data-ttu-id="51644-255">*hbmHeader*</span><span class="sxs-lookup"><span data-stu-id="51644-255">*hbmHeader*</span></span> 

<span data-ttu-id="51644-256">類型： [HBITMAP](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-256">Type: [HBITMAP](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-257">這個成員會宣告為具有 *pszbmHeader* 的聯集。</span><span class="sxs-lookup"><span data-stu-id="51644-257">This member is declared as a union with *pszbmHeader*.</span></span>

<span data-ttu-id="51644-258">*pszbmHeader*</span><span class="sxs-lookup"><span data-stu-id="51644-258">*pszbmHeader*</span></span>

<span data-ttu-id="51644-259">類型： [LPCSTR](../winprog/windows-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="51644-259">Type: [LPCSTR](../winprog/windows-data-types.md)</span></span>

<span data-ttu-id="51644-260">這個成員會宣告為具有 *hbmHeader* 的聯集。</span><span class="sxs-lookup"><span data-stu-id="51644-260">This member is declared as a union with *hbmHeader*.</span></span>

## <a name="remarks"></a><span data-ttu-id="51644-261">備註</span><span class="sxs-lookup"><span data-stu-id="51644-261">Remarks</span></span>

<span data-ttu-id="51644-262">Comctl32.dll 版6和更新版本不能轉散發。</span><span class="sxs-lookup"><span data-stu-id="51644-262">Comctl32.dll version 6 and later are not redistributable.</span></span> <span data-ttu-id="51644-263">若要使用 Comctl32.dll 6 版或更新版本，請在資訊清單中指定 .dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="51644-263">To use Comctl32.dll version 6 or later, specify the .dll file in a manifest.</span></span> <span data-ttu-id="51644-264">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="51644-264">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51644-265">規格需求</span><span class="sxs-lookup"><span data-stu-id="51644-265">Requirements</span></span>

| <span data-ttu-id="51644-266">需求</span><span class="sxs-lookup"><span data-stu-id="51644-266">Requirement</span></span> | <span data-ttu-id="51644-267">值</span><span class="sxs-lookup"><span data-stu-id="51644-267">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51644-268">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51644-268">Minimum supported client</span></span> | <span data-ttu-id="51644-269">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51644-269">Windows Vista \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="51644-270">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51644-270">Minimum supported server</span></span> | <span data-ttu-id="51644-271">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51644-271">Windows Server 2003 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="51644-272">標頭</span><span class="sxs-lookup"><span data-stu-id="51644-272">Header</span></span>                   | <span data-ttu-id="51644-273">Prsht.idl。h</span><span class="sxs-lookup"><span data-stu-id="51644-273">Prsht.h</span></span> |
| <span data-ttu-id="51644-274">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="51644-274">Unicode and ANSI names</span></span>                   | <span data-ttu-id="51644-275">**PROPSHEETHEADERW** (Unicode) 和 **PROPSHEETHEADERA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="51644-275">**PROPSHEETHEADERW** (Unicode) and **PROPSHEETHEADERA** (ANSI)</span></span> |