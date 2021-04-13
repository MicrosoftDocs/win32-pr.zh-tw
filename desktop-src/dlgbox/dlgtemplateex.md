---
title: DLGTEMPLATEEX 結構
description: 擴充的對話方塊範本以描述對話方塊的 DLGTEMPLATEEX 標頭開頭，並在對話方塊中指定控制項數目。
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- DLGTEMPLATEEX 結構對話方塊
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508959"
---
# <a name="dlgtemplateex-structure"></a><span data-ttu-id="29f0a-104">DLGTEMPLATEEX 結構</span><span class="sxs-lookup"><span data-stu-id="29f0a-104">DLGTEMPLATEEX structure</span></span>

<span data-ttu-id="29f0a-105">擴充的對話方塊範本以描述對話方塊的 **DLGTEMPLATEEX** 標頭開頭，並在對話方塊中指定控制項數目。</span><span class="sxs-lookup"><span data-stu-id="29f0a-105">An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box.</span></span> <span data-ttu-id="29f0a-106">針對對話方塊中的每個控制項，擴充的對話方塊範本都有一個使用 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 格式來描述控制項的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="29f0a-106">For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control.</span></span>

<span data-ttu-id="29f0a-107">**DLGTEMPLATEEX** 結構未定義于任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="29f0a-107">The **DLGTEMPLATEEX** structure is not defined in any standard header file.</span></span> <span data-ttu-id="29f0a-108">此處提供結構定義，以說明對話方塊的延伸範本格式。</span><span class="sxs-lookup"><span data-stu-id="29f0a-108">The structure definition is provided here to explain the format of an extended template for a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="29f0a-109">語法</span><span class="sxs-lookup"><span data-stu-id="29f0a-109">Syntax</span></span>


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="29f0a-110">成員</span><span class="sxs-lookup"><span data-stu-id="29f0a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="29f0a-111">**dlgVer**</span><span class="sxs-lookup"><span data-stu-id="29f0a-111">**dlgVer**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-112">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-112">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-113">延伸對話方塊範本的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="29f0a-113">The version number of the extended dialog box template.</span></span> <span data-ttu-id="29f0a-114">此成員必須設定為1。</span><span class="sxs-lookup"><span data-stu-id="29f0a-114">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-115">**簽章**</span><span class="sxs-lookup"><span data-stu-id="29f0a-115">**signature**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-116">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-117">指出範本是否為擴充的對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="29f0a-117">Indicates whether a template is an extended dialog box template.</span></span> <span data-ttu-id="29f0a-118">如果 **signature** 是0xffff，這就是延伸的對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="29f0a-118">If **signature** is 0xFFFF, this is an extended dialog box template.</span></span> <span data-ttu-id="29f0a-119">在此情況下， **dlgVer** 成員會指定範本版本號碼。</span><span class="sxs-lookup"><span data-stu-id="29f0a-119">In this case, the **dlgVer** member specifies the template version number.</span></span> <span data-ttu-id="29f0a-120">如果 **signature** 是0xffff 以外的任何值，則這是使用 [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) 和 [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) 結構的標準對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="29f0a-120">If **signature** is any value other than 0xFFFF, this is a standard dialog box template that uses the [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) and [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-121">**h**</span><span class="sxs-lookup"><span data-stu-id="29f0a-121">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-122">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-123">對話方塊視窗的說明內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="29f0a-123">The help context identifier for the dialog box window.</span></span> <span data-ttu-id="29f0a-124">當系統傳送 WM 說明 [**訊息 \_**](../shell/wm-help.md)時，它會在 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的 **wCoNtextId** 成員中傳遞此值。</span><span class="sxs-lookup"><span data-stu-id="29f0a-124">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes this value in the **wContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-125">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="29f0a-125">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-126">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-127">擴充的 windows 樣式。</span><span class="sxs-lookup"><span data-stu-id="29f0a-127">The extended windows styles.</span></span> <span data-ttu-id="29f0a-128">建立對話方塊時不會使用這個成員，但是使用對話方塊範本的應用程式可以使用它來建立其他類型的視窗。</span><span class="sxs-lookup"><span data-stu-id="29f0a-128">This member is not used when creating dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="29f0a-129">如需值清單，請參閱 [**擴充的視窗樣式**](/windows/desktop/winmsg/extended-window-styles)。</span><span class="sxs-lookup"><span data-stu-id="29f0a-129">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-130">**style**</span><span class="sxs-lookup"><span data-stu-id="29f0a-130">**style**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-131">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-132">對話方塊的樣式。</span><span class="sxs-lookup"><span data-stu-id="29f0a-132">The style of the dialog box.</span></span> <span data-ttu-id="29f0a-133">這個成員可以是 [視窗樣式值](/windows/desktop/winmsg/window-styles) 和 [對話方塊樣式值](dialog-box-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="29f0a-133">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) and [dialog box style values](dialog-box-styles.md).</span></span>

<span data-ttu-id="29f0a-134">如果 [ **樣式** ] 包含 [ **ds \_ SETFONT** ] 或 [ **ds \_ SHELLFONT** ] 對話方塊樣式，則延伸對話方塊範本的 **DLGTEMPLATEEX** 標頭會包含四個額外的成員 ( [ **dialog**]、[ **權數**]、[ **斜體**] 和 [ **字型** ]) ，其中描述要用於工作區中的文字和對話方塊控制項的字型。</span><span class="sxs-lookup"><span data-stu-id="29f0a-134">If **style** includes the **DS\_SETFONT** or **DS\_SHELLFONT** dialog box style, the **DLGTEMPLATEEX** header of the extended dialog box template contains four additional members ( **pointsize**, **weight**, **italic**, and **typeface**) that describe the font to use for the text in the client area and controls of the dialog box.</span></span> <span data-ttu-id="29f0a-135">可能的話，系統會根據這些成員中指定的值來建立字型。</span><span class="sxs-lookup"><span data-stu-id="29f0a-135">If possible, the system creates a font according to the values specified in these members.</span></span> <span data-ttu-id="29f0a-136">然後系統會將 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息傳送至對話方塊，並傳送至每個控制項，以提供字型的控制碼。</span><span class="sxs-lookup"><span data-stu-id="29f0a-136">Then the system sends a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to the dialog box and to each control to provide a handle to the font.</span></span>

<span data-ttu-id="29f0a-137">如需詳細資訊，請參閱 [對話方塊](about-dialog-boxes.md)字型。</span><span class="sxs-lookup"><span data-stu-id="29f0a-137">For more information, see [Dialog Box Fonts](about-dialog-boxes.md).</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-138">**cDlgItems**</span><span class="sxs-lookup"><span data-stu-id="29f0a-138">**cDlgItems**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-139">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-140">對話方塊中的控制項數目。</span><span class="sxs-lookup"><span data-stu-id="29f0a-140">The number of controls in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-141">**x**</span><span class="sxs-lookup"><span data-stu-id="29f0a-141">**x**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-142">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="29f0a-142">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-143">對話方塊左上角的 x 座標（以對話方塊單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="29f0a-143">The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-144">**y**</span><span class="sxs-lookup"><span data-stu-id="29f0a-144">**y**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-145">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="29f0a-145">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-146">對話方塊左上角的 y 座標（以對話方塊單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="29f0a-146">The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-147">**殘雪**</span><span class="sxs-lookup"><span data-stu-id="29f0a-147">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-148">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="29f0a-148">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-149">對話方塊的寬度（以對話方塊單位）。</span><span class="sxs-lookup"><span data-stu-id="29f0a-149">The width, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-150">**cy**</span><span class="sxs-lookup"><span data-stu-id="29f0a-150">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-151">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="29f0a-151">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-152">對話方塊的高度（以對話方塊單位）。</span><span class="sxs-lookup"><span data-stu-id="29f0a-152">The height, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-153">**功能表**</span><span class="sxs-lookup"><span data-stu-id="29f0a-153">**menu**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-154">類型： **sz \_ 或 \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="29f0a-154">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-155">變數長度的16位元素陣列，識別對話方塊的功能表資源。</span><span class="sxs-lookup"><span data-stu-id="29f0a-155">A variable-length array of 16-bit elements that identifies a menu resource for the dialog box.</span></span> <span data-ttu-id="29f0a-156">如果這個陣列的第一個元素是0x0000，則對話方塊沒有功能表，且陣列沒有其他元素。</span><span class="sxs-lookup"><span data-stu-id="29f0a-156">If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements.</span></span> <span data-ttu-id="29f0a-157">如果第一個元素是0xFFFF，陣列有一個額外的元素，可在可執行檔中指定功能表資源的序數值。</span><span class="sxs-lookup"><span data-stu-id="29f0a-157">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file.</span></span> <span data-ttu-id="29f0a-158">如果第一個元素有任何其他值，系統會將陣列視為以 null 終止的 Unicode 字串，在可執行檔中指定功能表資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="29f0a-158">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-159">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="29f0a-159">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-160">類型： **sz \_ 或 \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="29f0a-160">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-161">變數長度的16位元素陣列，識別對話方塊的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="29f0a-161">A variable-length array of 16-bit elements that identifies the window class of the dialog box.</span></span> <span data-ttu-id="29f0a-162">如果陣列的第一個元素是0x0000，系統就會使用對話方塊的預先定義對話方塊類別，而陣列沒有其他元素。</span><span class="sxs-lookup"><span data-stu-id="29f0a-162">If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements.</span></span> <span data-ttu-id="29f0a-163">如果第一個元素是0xFFFF，陣列有一個額外的元素，可指定預先定義之系統視窗類別的序數值。</span><span class="sxs-lookup"><span data-stu-id="29f0a-163">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class.</span></span> <span data-ttu-id="29f0a-164">如果第一個元素有任何其他值，系統會將陣列視為以 null 終止的 Unicode 字串，以指定已註冊視窗類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="29f0a-164">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-165">**title**</span><span class="sxs-lookup"><span data-stu-id="29f0a-165">**title**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-166">類型： **WCHAR \[ titleLen \]**</span><span class="sxs-lookup"><span data-stu-id="29f0a-166">Type: **WCHAR\[titleLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-167">對話方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="29f0a-167">The title of the dialog box.</span></span> <span data-ttu-id="29f0a-168">如果這個陣列的第一個元素是0x0000，則對話方塊沒有標題，而且陣列沒有其他元素。</span><span class="sxs-lookup"><span data-stu-id="29f0a-168">If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-169">**dialog**</span><span class="sxs-lookup"><span data-stu-id="29f0a-169">**pointsize**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-170">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-170">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-171">要用於對話方塊和其控制項中文字的字型點大小。</span><span class="sxs-lookup"><span data-stu-id="29f0a-171">The point size of the font to use for the text in the dialog box and its controls.</span></span>

<span data-ttu-id="29f0a-172">只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。</span><span class="sxs-lookup"><span data-stu-id="29f0a-172">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-173">**weight**</span><span class="sxs-lookup"><span data-stu-id="29f0a-173">**weight**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-174">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="29f0a-174">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-175">字型的粗細。</span><span class="sxs-lookup"><span data-stu-id="29f0a-175">The weight of the font.</span></span> <span data-ttu-id="29f0a-176">請注意，雖然這可以是 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfWeight** 成員所列出的任何值，但使用的任何值都會自動變更為 **FW \_ NORMAL**。</span><span class="sxs-lookup"><span data-stu-id="29f0a-176">Note that, although this can be any of the values listed for the **lfWeight** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure, any value that is used will be automatically changed to **FW\_NORMAL**.</span></span>

<span data-ttu-id="29f0a-177">只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。</span><span class="sxs-lookup"><span data-stu-id="29f0a-177">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-178">**斜體**</span><span class="sxs-lookup"><span data-stu-id="29f0a-178">**italic**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-179">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="29f0a-179">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-180">指出字型是否為斜體。</span><span class="sxs-lookup"><span data-stu-id="29f0a-180">Indicates whether the font is italic.</span></span> <span data-ttu-id="29f0a-181">如果這個值為 **TRUE**，表示字型為斜體。</span><span class="sxs-lookup"><span data-stu-id="29f0a-181">If this value is **TRUE**, the font is italic.</span></span>

<span data-ttu-id="29f0a-182">只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。</span><span class="sxs-lookup"><span data-stu-id="29f0a-182">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-183">**字元集**</span><span class="sxs-lookup"><span data-stu-id="29f0a-183">**charset**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-184">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="29f0a-184">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-185">要使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="29f0a-185">The character set to be used.</span></span> <span data-ttu-id="29f0a-186">如需詳細資訊，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)的 **lfcharset** 成員。</span><span class="sxs-lookup"><span data-stu-id="29f0a-186">For more information, see the **lfcharset** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span></span>

<span data-ttu-id="29f0a-187">只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。</span><span class="sxs-lookup"><span data-stu-id="29f0a-187">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="29f0a-188">**字體**</span><span class="sxs-lookup"><span data-stu-id="29f0a-188">**typeface**</span></span>
</dt> <dd>

<span data-ttu-id="29f0a-189">類型： **WCHAR \[ stringLen \]**</span><span class="sxs-lookup"><span data-stu-id="29f0a-189">Type: **WCHAR\[stringLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="29f0a-190">字型的字型名稱。</span><span class="sxs-lookup"><span data-stu-id="29f0a-190">The name of the typeface for the font.</span></span>

<span data-ttu-id="29f0a-191">只有當 **style** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 時，才會出現這個成員。</span><span class="sxs-lookup"><span data-stu-id="29f0a-191">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29f0a-192">備註</span><span class="sxs-lookup"><span data-stu-id="29f0a-192">Remarks</span></span>

<span data-ttu-id="29f0a-193">您可以使用擴充的對話方塊範本，而不是 [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)、 [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)、 [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)和 [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) 函數中的標準對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="29f0a-193">You can use an extended dialog box template instead of a standard dialog box template in the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta), and [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) functions.</span></span>

<span data-ttu-id="29f0a-194">在擴充對話方塊範本中的 **DLGTEMPLATEEX** 標頭之後，就是一或多個描述對話方塊控制項的 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="29f0a-194">Following the **DLGTEMPLATEEX** header in an extended dialog box template is one or more [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structures that describe the controls of the dialog box.</span></span> <span data-ttu-id="29f0a-195">**DLGITEMTEMPLATEEX** 結構的 **cDlgItems** 成員會指定範本中遵循的 **DLGITEMTEMPLATEEX** 結構數目。</span><span class="sxs-lookup"><span data-stu-id="29f0a-195">The **cDlgItems** member of the **DLGITEMTEMPLATEEX** structure specifies the number of **DLGITEMTEMPLATEEX** structures that follow in the template.</span></span>

<span data-ttu-id="29f0a-196">範本中的每個 [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) 結構都必須對齊 **DWORD** 界限。</span><span class="sxs-lookup"><span data-stu-id="29f0a-196">Each [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structure in the template must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="29f0a-197">如果 **樣式** 成員指定 **Ds \_ SETFONT** 或 **ds \_ SHELLFONT** 樣式，則第一個 **DLGITEMTEMPLATEEX** 結構會在 **字型** 字串之後的第一個 **DWORD** 界限上開始。</span><span class="sxs-lookup"><span data-stu-id="29f0a-197">If the **style** member specifies the **DS\_SETFONT** or **DS\_SHELLFONT** style, the first **DLGITEMTEMPLATEEX** structure begins on the first **DWORD** boundary after the **typeface** string.</span></span> <span data-ttu-id="29f0a-198">如果未指定這些樣式，則第一個結構會在 **標題** 字串之後的第一個 **DWORD** 界限上開始。</span><span class="sxs-lookup"><span data-stu-id="29f0a-198">If these styles are not specified, the first structure begins on the first **DWORD** boundary after the **title** string.</span></span>

<span data-ttu-id="29f0a-199">**Menu**、 **windowClass**、 **title** 和 **字樣** 陣列必須對齊 **字** 組邊界。</span><span class="sxs-lookup"><span data-stu-id="29f0a-199">The **menu**, **windowClass**, **title**, and **typeface** arrays must be aligned on **WORD** boundaries.</span></span>

<span data-ttu-id="29f0a-200">如果您在 **功能表**、 **windowClass**、 **title** 和 **字樣** 陣列中指定字元字串，就必須使用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="29f0a-200">If you specify character strings in the **menu**, **windowClass**, **title**, and **typeface** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="29f0a-201">您可以使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函數，從 ANSI 字串產生這些 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="29f0a-201">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="29f0a-202">**X**、 **y**、 **cx** 和 **cy** 成員會在對話方塊單位中指定值。</span><span class="sxs-lookup"><span data-stu-id="29f0a-202">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="29f0a-203">您可以使用 [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) 函式，將這些值轉換為螢幕單位 (圖元) 。</span><span class="sxs-lookup"><span data-stu-id="29f0a-203">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="29f0a-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="29f0a-204">Requirements</span></span>



| <span data-ttu-id="29f0a-205">需求</span><span class="sxs-lookup"><span data-stu-id="29f0a-205">Requirement</span></span> | <span data-ttu-id="29f0a-206">值</span><span class="sxs-lookup"><span data-stu-id="29f0a-206">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="29f0a-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29f0a-207">Minimum supported client</span></span><br/> | <span data-ttu-id="29f0a-208">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29f0a-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="29f0a-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29f0a-209">Minimum supported server</span></span><br/> | <span data-ttu-id="29f0a-210">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29f0a-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="29f0a-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29f0a-211">See also</span></span>

<dl> <dt>

<span data-ttu-id="29f0a-212">**參考**</span><span class="sxs-lookup"><span data-stu-id="29f0a-212">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29f0a-213">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="29f0a-213">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="29f0a-214">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="29f0a-214">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="29f0a-215">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="29f0a-215">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="29f0a-216">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="29f0a-216">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="29f0a-217">**DLGITEMTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="29f0a-217">**DLGITEMTEMPLATEEX**</span></span>](dlgitemtemplateex.md)
</dt> <dt>

[<span data-ttu-id="29f0a-218">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="29f0a-218">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="29f0a-219">**WM \_ SETFONT**</span><span class="sxs-lookup"><span data-stu-id="29f0a-219">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

<span data-ttu-id="29f0a-220">**概念**</span><span class="sxs-lookup"><span data-stu-id="29f0a-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29f0a-221">對話方塊</span><span class="sxs-lookup"><span data-stu-id="29f0a-221">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="29f0a-222">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="29f0a-222">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="29f0a-223">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="29f0a-223">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="29f0a-224">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="29f0a-224">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

