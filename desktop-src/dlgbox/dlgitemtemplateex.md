---
title: DLGITEMTEMPLATEEX 結構
description: 延伸對話方塊範本用來描述延伸對話方塊的文字區塊。 如需延伸對話方塊範本格式的描述，請參閱 DLGTEMPLATEEX。
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- DLGITEMTEMPLATEEX 結構對話方塊
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385214"
---
# <a name="dlgitemtemplateex-structure"></a><span data-ttu-id="77c53-105">DLGITEMTEMPLATEEX 結構</span><span class="sxs-lookup"><span data-stu-id="77c53-105">DLGITEMTEMPLATEEX structure</span></span>

<span data-ttu-id="77c53-106">延伸對話方塊範本用來描述延伸對話方塊的文字區塊。</span><span class="sxs-lookup"><span data-stu-id="77c53-106">A block of text used by an extended dialog box template to describe the extended dialog box.</span></span> <span data-ttu-id="77c53-107">如需延伸對話方塊範本格式的描述，請參閱 [**DLGTEMPLATEEX**](dlgtemplateex.md)。</span><span class="sxs-lookup"><span data-stu-id="77c53-107">For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="77c53-108">語法</span><span class="sxs-lookup"><span data-stu-id="77c53-108">Syntax</span></span>


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="77c53-109">成員</span><span class="sxs-lookup"><span data-stu-id="77c53-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="77c53-110">**h**</span><span class="sxs-lookup"><span data-stu-id="77c53-110">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="77c53-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-112">控制項的說明內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="77c53-112">The help context identifier for the control.</span></span> <span data-ttu-id="77c53-113">當系統傳送 WM 說明 [**\_**](../shell/wm-help.md)訊息時，它會在 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的 **dwCoNtextId** 成員中傳遞 **h** 值。</span><span class="sxs-lookup"><span data-stu-id="77c53-113">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes the **helpID** value in the **dwContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="77c53-114">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="77c53-114">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-115">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="77c53-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-116">視窗的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="77c53-116">The extended styles for a window.</span></span> <span data-ttu-id="77c53-117">此成員不會用來在對話方塊中建立控制項，但使用對話方塊範本的應用程式可以使用它來建立其他類型的視窗。</span><span class="sxs-lookup"><span data-stu-id="77c53-117">This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="77c53-118">如需值清單，請參閱 [**擴充的視窗樣式**](/windows/desktop/winmsg/extended-window-styles)。</span><span class="sxs-lookup"><span data-stu-id="77c53-118">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="77c53-119">**style**</span><span class="sxs-lookup"><span data-stu-id="77c53-119">**style**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-120">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="77c53-120">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-121">控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="77c53-121">The style of the control.</span></span> <span data-ttu-id="77c53-122">這個成員可以是 [視窗樣式值](/windows/desktop/winmsg/window-styles) 的組合 (例如 **WS \_ 框線**) ，以及一或多個 [控制項樣式值](/windows/desktop/Controls/common-control-styles) (例如 **BS \_ 按鈕** 和 **ES \_ 左方**) 。</span><span class="sxs-lookup"><span data-stu-id="77c53-122">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) (such as **WS\_BORDER**) and one or more of the [control style values](/windows/desktop/Controls/common-control-styles) (such as **BS\_PUSHBUTTON** and **ES\_LEFT**).</span></span>

</dd> <dt>

<span data-ttu-id="77c53-123">**x**</span><span class="sxs-lookup"><span data-stu-id="77c53-123">**x**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-124">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="77c53-124">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-125">控制項左上角的 x 座標（以對話方塊單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="77c53-125">The x-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="77c53-126">此座標一律相對於對話方塊工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="77c53-126">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="77c53-127">**y**</span><span class="sxs-lookup"><span data-stu-id="77c53-127">**y**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-128">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="77c53-128">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-129">控制項左上角的 y 座標（以對話方塊單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="77c53-129">The y-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="77c53-130">此座標一律相對於對話方塊工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="77c53-130">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="77c53-131">**殘雪**</span><span class="sxs-lookup"><span data-stu-id="77c53-131">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-132">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="77c53-132">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-133">控制項的寬度（以對話方塊單位）。</span><span class="sxs-lookup"><span data-stu-id="77c53-133">The width, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="77c53-134">**cy**</span><span class="sxs-lookup"><span data-stu-id="77c53-134">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-135">類型： **short**</span><span class="sxs-lookup"><span data-stu-id="77c53-135">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-136">控制項之對話方塊單位中的高度。</span><span class="sxs-lookup"><span data-stu-id="77c53-136">The height, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="77c53-137">**id**</span><span class="sxs-lookup"><span data-stu-id="77c53-137">**id**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-138">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="77c53-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-139">控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="77c53-139">The control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="77c53-140">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="77c53-140">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-141">類型： **sz \_ 或 \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="77c53-141">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-142">變數長度的16位元素陣列，指定控制項的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="77c53-142">A variable-length array of 16-bit elements that specifies the window class of the control.</span></span> <span data-ttu-id="77c53-143">如果這個陣列的第一個元素是0xFFFF 以外的任何值，系統會將陣列視為以 null 終止的 Unicode 字串，以指定已註冊視窗類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="77c53-143">If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

<span data-ttu-id="77c53-144">如果第一個元素是0xFFFF，陣列有一個額外的元素，可指定預先定義之系統類別的序數值。</span><span class="sxs-lookup"><span data-stu-id="77c53-144">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class.</span></span> <span data-ttu-id="77c53-145">序數可以是下列其中一個 atom 值。</span><span class="sxs-lookup"><span data-stu-id="77c53-145">The ordinal can be one of the following atom values.</span></span>



| <span data-ttu-id="77c53-146">值</span><span class="sxs-lookup"><span data-stu-id="77c53-146">Value</span></span>                                                                             | <span data-ttu-id="77c53-147">意義</span><span class="sxs-lookup"><span data-stu-id="77c53-147">Meaning</span></span>               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="77c53-148"><dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="77c53-148"><dt>0x0080</dt></span></span> </dl> | <span data-ttu-id="77c53-149">按鈕</span><span class="sxs-lookup"><span data-stu-id="77c53-149">Button</span></span><br/>     |
| <dl> <span data-ttu-id="77c53-150"><dt>0x0081</dt></span><span class="sxs-lookup"><span data-stu-id="77c53-150"><dt>0x0081</dt></span></span> </dl> | <span data-ttu-id="77c53-151">編輯</span><span class="sxs-lookup"><span data-stu-id="77c53-151">Edit</span></span><br/>       |
| <dl> <span data-ttu-id="77c53-152"><dt>0x0082</dt></span><span class="sxs-lookup"><span data-stu-id="77c53-152"><dt>0x0082</dt></span></span> </dl> | <span data-ttu-id="77c53-153">Static</span><span class="sxs-lookup"><span data-stu-id="77c53-153">Static</span></span><br/>     |
| <dl> <span data-ttu-id="77c53-154"><dt>0x0083</dt></span><span class="sxs-lookup"><span data-stu-id="77c53-154"><dt>0x0083</dt></span></span> </dl> | <span data-ttu-id="77c53-155">清單方塊</span><span class="sxs-lookup"><span data-stu-id="77c53-155">List box</span></span><br/>   |
| <dl> <span data-ttu-id="77c53-156"><dt>0x0084</dt></span><span class="sxs-lookup"><span data-stu-id="77c53-156"><dt>0x0084</dt></span></span> </dl> | <span data-ttu-id="77c53-157">捲軸</span><span class="sxs-lookup"><span data-stu-id="77c53-157">Scroll bar</span></span><br/> |
| <dl> <span data-ttu-id="77c53-158"><dt>0x0085</dt></span><span class="sxs-lookup"><span data-stu-id="77c53-158"><dt>0x0085</dt></span></span> </dl> | <span data-ttu-id="77c53-159">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="77c53-159">Combo box</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="77c53-160">**title**</span><span class="sxs-lookup"><span data-stu-id="77c53-160">**title**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-161">類型： **sz \_ 或 \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="77c53-161">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-162">16位元素的可變長度陣列，包含控制項的初始文字或資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="77c53-162">A variable-length array of 16-bit elements that contains the initial text or resource identifier of the control.</span></span> <span data-ttu-id="77c53-163">如果這個陣列的第一個元素是0xFFFF，則陣列有一個額外的元素，可在可執行檔中指定資源的序數值（例如圖示）。</span><span class="sxs-lookup"><span data-stu-id="77c53-163">If the first element of this array is 0xFFFF, the array has one additional element that specifies the ordinal value of a resource, such as an icon, in an executable file.</span></span> <span data-ttu-id="77c53-164">您可以針對控制項（例如靜態圖示控制項）使用資源識別碼來載入和顯示圖示或其他資源，而不是文字。</span><span class="sxs-lookup"><span data-stu-id="77c53-164">You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text.</span></span> <span data-ttu-id="77c53-165">如果第一個元素是0xFFFF 以外的任何值，系統會將陣列視為以 null 終止的 Unicode 字串，以指定初始文字。</span><span class="sxs-lookup"><span data-stu-id="77c53-165">If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text.</span></span>

</dd> <dt>

<span data-ttu-id="77c53-166">**extraCount**</span><span class="sxs-lookup"><span data-stu-id="77c53-166">**extraCount**</span></span>
</dt> <dd>

<span data-ttu-id="77c53-167">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="77c53-167">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="77c53-168">遵循這個成員的建立資料位元組數目。</span><span class="sxs-lookup"><span data-stu-id="77c53-168">The number of bytes of creation data that follow this member.</span></span> <span data-ttu-id="77c53-169">如果這個值大於零，則建立的資料會從下一個 **字** 邊界開始。</span><span class="sxs-lookup"><span data-stu-id="77c53-169">If this value is greater than zero, the creation data begins at the next **WORD** boundary.</span></span> <span data-ttu-id="77c53-170">此建立資料可以是任何大小和格式。</span><span class="sxs-lookup"><span data-stu-id="77c53-170">This creation data can be of any size and format.</span></span> <span data-ttu-id="77c53-171">控制項的視窗程式必須能夠解讀資料。</span><span class="sxs-lookup"><span data-stu-id="77c53-171">The control's window procedure must be able to interpret the data.</span></span> <span data-ttu-id="77c53-172">當系統建立控制項時，它會在傳送至控制項之 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息的 *lParam* 參數中，傳遞此資料的指標。</span><span class="sxs-lookup"><span data-stu-id="77c53-172">When the system creates the control, it passes a pointer to this data in the *lParam* parameter of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message that it sends to the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77c53-173">備註</span><span class="sxs-lookup"><span data-stu-id="77c53-173">Remarks</span></span>

<span data-ttu-id="77c53-174">對話方塊的延伸範本包含 [**DLGTEMPLATEEX**](dlgtemplateex.md) 標頭，後面接著對話方塊中每個控制項的 **DLGITEMTEMPLATEEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="77c53-174">An extended template for a dialog box consists of a [**DLGTEMPLATEEX**](dlgtemplateex.md) header followed by a **DLGITEMTEMPLATEEX** structure for each control in the dialog box.</span></span>

<span data-ttu-id="77c53-175">每個 **DLGITEMTEMPLATEEX** 結構都必須對齊 **DWORD** 界限。</span><span class="sxs-lookup"><span data-stu-id="77c53-175">Each **DLGITEMTEMPLATEEX** structure must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="77c53-176">可變長度的 **windowClass** 和 **標題** 陣列必須對齊 **字** 組邊界。</span><span class="sxs-lookup"><span data-stu-id="77c53-176">The variable-length **windowClass** and **title** arrays must be aligned on **WORD** boundaries.</span></span> <span data-ttu-id="77c53-177">建立資料陣列（如果有的話）必須對齊 **字** 邊界。</span><span class="sxs-lookup"><span data-stu-id="77c53-177">The creation data array, if any, must be aligned on a **WORD** boundary.</span></span>

<span data-ttu-id="77c53-178">如果您在 **windowClass** 和 **標題** 陣列中指定字元字串，就必須使用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="77c53-178">If you specify character strings in the **windowClass** and **title** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="77c53-179">您可以使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函數，從 ANSI 字串產生 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="77c53-179">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="77c53-180">**X**、 **y**、 **cx** 和 **cy** 成員會在對話方塊單位中指定值。</span><span class="sxs-lookup"><span data-stu-id="77c53-180">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="77c53-181">您可以使用 [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) 函式，將這些值轉換為螢幕單位 (圖元) 。</span><span class="sxs-lookup"><span data-stu-id="77c53-181">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="77c53-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="77c53-182">Requirements</span></span>



| <span data-ttu-id="77c53-183">需求</span><span class="sxs-lookup"><span data-stu-id="77c53-183">Requirement</span></span> | <span data-ttu-id="77c53-184">值</span><span class="sxs-lookup"><span data-stu-id="77c53-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="77c53-185">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77c53-185">Minimum supported client</span></span><br/> | <span data-ttu-id="77c53-186">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77c53-186">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="77c53-187">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77c53-187">Minimum supported server</span></span><br/> | <span data-ttu-id="77c53-188">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77c53-188">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="77c53-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77c53-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="77c53-190">**參考**</span><span class="sxs-lookup"><span data-stu-id="77c53-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="77c53-191">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="77c53-191">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="77c53-192">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="77c53-192">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="77c53-193">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="77c53-193">**CreateWindowEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="77c53-194">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="77c53-194">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="77c53-195">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="77c53-195">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="77c53-196">**DLGTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="77c53-196">**DLGTEMPLATEEX**</span></span>](dlgtemplateex.md)
</dt> <dt>

[<span data-ttu-id="77c53-197">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="77c53-197">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="77c53-198">**WM \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="77c53-198">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)
</dt> <dt>

<span data-ttu-id="77c53-199">**概念**</span><span class="sxs-lookup"><span data-stu-id="77c53-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="77c53-200">對話方塊</span><span class="sxs-lookup"><span data-stu-id="77c53-200">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="77c53-201">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="77c53-201">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="77c53-202">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="77c53-202">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[<span data-ttu-id="77c53-203">**WM \_ 說明**</span><span class="sxs-lookup"><span data-stu-id="77c53-203">**WM\_HELP**</span></span>](../shell/wm-help.md)
</dt> </dl>

 

