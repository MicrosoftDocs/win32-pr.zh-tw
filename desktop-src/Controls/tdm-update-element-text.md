---
title: 'TDM_UPDATE_ELEMENT_TEXT 訊息 (Commctrl .h) '
description: 更新工作對話方塊中的文字專案。
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106247"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="d94b6-104">TDM \_ UPDATE \_ 元素 \_ 文字訊息</span><span class="sxs-lookup"><span data-stu-id="d94b6-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="d94b6-105">更新工作對話方塊中的文字專案。</span><span class="sxs-lookup"><span data-stu-id="d94b6-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="d94b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="d94b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94b6-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d94b6-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94b6-108">表示要更新的元素。</span><span class="sxs-lookup"><span data-stu-id="d94b6-108">Indicates the element to update.</span></span> <span data-ttu-id="d94b6-109"> (如需元素的圖例，請參閱 [關於工作對話方塊](task-dialogs-overview.md)。 ) 此參數必須是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="d94b6-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="d94b6-110">值</span><span class="sxs-lookup"><span data-stu-id="d94b6-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="d94b6-111">意義</span><span class="sxs-lookup"><span data-stu-id="d94b6-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="d94b6-112"><dt>**TDE \_ 內容**</dt></span><span class="sxs-lookup"><span data-stu-id="d94b6-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="d94b6-113">內容。</span><span class="sxs-lookup"><span data-stu-id="d94b6-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="d94b6-114"><dt>**TDE \_ 展開的 \_ 資訊**</dt></span><span class="sxs-lookup"><span data-stu-id="d94b6-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="d94b6-115">展開的資訊。</span><span class="sxs-lookup"><span data-stu-id="d94b6-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="d94b6-116"><dt>**TDE \_ 頁尾**</dt></span><span class="sxs-lookup"><span data-stu-id="d94b6-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="d94b6-117">頁尾文字。</span><span class="sxs-lookup"><span data-stu-id="d94b6-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="d94b6-118"><dt>**TDE \_ 主要 \_ 指示**</dt></span><span class="sxs-lookup"><span data-stu-id="d94b6-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="d94b6-119">Main 指令。</span><span class="sxs-lookup"><span data-stu-id="d94b6-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="d94b6-120">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d94b6-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94b6-121">包含新文字的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="d94b6-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94b6-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="d94b6-122">Return value</span></span>

<span data-ttu-id="d94b6-123">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d94b6-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d94b6-124">備註</span><span class="sxs-lookup"><span data-stu-id="d94b6-124">Remarks</span></span>

<span data-ttu-id="d94b6-125">若要避免裁剪，新的文字必須不超過現有文字。</span><span class="sxs-lookup"><span data-stu-id="d94b6-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="d94b6-126">將文字設定為較短的字串並不會讓對話方塊調整大小。</span><span class="sxs-lookup"><span data-stu-id="d94b6-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="d94b6-127">如果用來建立工作對話方塊的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **PszExpandedInformation** 成員為 **Null**，而且您傳送了具有 TDE 擴充資訊的 **TDM \_ UPDATE \_ 元素 \_ 文字** 訊息 \_ ，則 \_ 不會發生任何事。</span><span class="sxs-lookup"><span data-stu-id="d94b6-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="d94b6-128">上述也適用于頁尾和 TDE 頁尾 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d94b6-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94b6-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d94b6-129">Requirements</span></span>



| <span data-ttu-id="d94b6-130">需求</span><span class="sxs-lookup"><span data-stu-id="d94b6-130">Requirement</span></span> | <span data-ttu-id="d94b6-131">值</span><span class="sxs-lookup"><span data-stu-id="d94b6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d94b6-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d94b6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d94b6-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d94b6-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d94b6-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d94b6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d94b6-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d94b6-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d94b6-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d94b6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d94b6-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d94b6-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94b6-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d94b6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94b6-139">**TDM \_ 設定 \_ 元素 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="d94b6-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





