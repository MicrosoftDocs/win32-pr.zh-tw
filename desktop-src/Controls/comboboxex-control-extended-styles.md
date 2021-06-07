---
title: 'ComboBoxEx 控制項擴充樣式 (CommCtrl .h) '
description: 支援本節中所列的延伸樣式，以及大部分標準的下拉式方塊控制項樣式。
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966d259cf427bcc83e9a8b2fb65670a2a05b9458
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387654"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="57d64-103">ComboBoxEx 控制項擴充樣式</span><span class="sxs-lookup"><span data-stu-id="57d64-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="57d64-104">支援本節中所列的延伸樣式，以及大部分標準的下拉式方塊控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="57d64-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="57d64-105">常數</span><span class="sxs-lookup"><span data-stu-id="57d64-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="57d64-106">描述</span><span class="sxs-lookup"><span data-stu-id="57d64-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="57d64-107"><dt>**CBES \_ EX \_ CASESENSITIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="57d64-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="57d64-108">清單中的 **BSTR** 搜尋會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="57d64-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="57d64-109">這包括在編輯方塊中輸入文字的結果，以及 CB FINDSTRINGEXACT 訊息中的搜尋結果 \_ 。</span><span class="sxs-lookup"><span data-stu-id="57d64-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="57d64-110"><dt>**CBES \_ EX \_ NOEDITIMAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="57d64-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="57d64-111">編輯方塊和下拉式清單不會顯示專案影像。</span><span class="sxs-lookup"><span data-stu-id="57d64-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="57d64-112"><dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt></span><span class="sxs-lookup"><span data-stu-id="57d64-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="57d64-113">編輯方塊和下拉式清單不會顯示專案影像。</span><span class="sxs-lookup"><span data-stu-id="57d64-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="57d64-114"><dt>**CBES \_ EX \_ NOSIZELIMIT**</dt></span><span class="sxs-lookup"><span data-stu-id="57d64-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="57d64-115">允許 ComboBoxEx 控制項的垂直大小小於其包含的下拉式方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="57d64-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="57d64-116">如果 ComboBoxEx 的大小小於下拉式方塊，則會裁剪下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="57d64-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="57d64-117"><dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt></span><span class="sxs-lookup"><span data-stu-id="57d64-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="57d64-118">僅 Windows NT。</span><span class="sxs-lookup"><span data-stu-id="57d64-118">Windows NT only.</span></span> <span data-ttu-id="57d64-119">編輯方塊會使用斜線 (/) 、反斜線 (\\) 和句號 (. ) 字元作為文字分隔符號。</span><span class="sxs-lookup"><span data-stu-id="57d64-119">The edit box will use the slash (/), backslash (\\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="57d64-120">這可讓鍵盤快速鍵在路徑名稱和 Url 中有效地移動單字游標。</span><span class="sxs-lookup"><span data-stu-id="57d64-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="57d64-121"><dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="57d64-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="57d64-122">**Windows Vista （含）以後版本。**</span><span class="sxs-lookup"><span data-stu-id="57d64-122">**Windows Vista and later.**</span></span> <span data-ttu-id="57d64-123">當編輯方塊為唯讀時，會導致下拉式清單和編輯方塊中的專案 () 要以省略號 ( "... ) " 來截斷，而不是只由控制項邊緣裁剪。</span><span class="sxs-lookup"><span data-stu-id="57d64-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="57d64-124">當控制項必須設定為固定寬度，但清單中的專案可能很長時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="57d64-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="57d64-125">備註</span><span class="sxs-lookup"><span data-stu-id="57d64-125">Remarks</span></span>

<span data-ttu-id="57d64-126">您可以使用 [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) 和 [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) 訊息來設定和取出 combobox 擴充樣式。</span><span class="sxs-lookup"><span data-stu-id="57d64-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="57d64-127">如果您嘗試為以 [**CBS \_ 簡單**](combo-box-styles.md) 樣式建立的 ComboBoxEx 控制項設定擴充樣式，則可能無法正確地重新繪製。</span><span class="sxs-lookup"><span data-stu-id="57d64-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="57d64-128">**CBS \_ 簡單** 樣式也無法與 CBES \_ EX \_ PATHWORDBREAKPROC 擴充樣式一起正常運作。</span><span class="sxs-lookup"><span data-stu-id="57d64-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57d64-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="57d64-129">Requirements</span></span>



| <span data-ttu-id="57d64-130">需求</span><span class="sxs-lookup"><span data-stu-id="57d64-130">Requirement</span></span> | <span data-ttu-id="57d64-131">值</span><span class="sxs-lookup"><span data-stu-id="57d64-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57d64-132">標頭</span><span class="sxs-lookup"><span data-stu-id="57d64-132">Header</span></span><br/> | <dl> <span data-ttu-id="57d64-133"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="57d64-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





