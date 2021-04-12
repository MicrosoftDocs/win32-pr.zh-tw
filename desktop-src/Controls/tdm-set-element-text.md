---
title: 'TDM_SET_ELEMENT_TEXT 訊息 (Commctrl .h) '
description: 更新工作對話方塊中的文字專案。
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025433"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="f226a-104">TDM \_ 設定 \_ 元素 \_ 文字訊息</span><span class="sxs-lookup"><span data-stu-id="f226a-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="f226a-105">更新工作對話方塊中的文字專案。</span><span class="sxs-lookup"><span data-stu-id="f226a-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="f226a-106">參數</span><span class="sxs-lookup"><span data-stu-id="f226a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f226a-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f226a-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f226a-108">表示要更新的元素。</span><span class="sxs-lookup"><span data-stu-id="f226a-108">Indicates the element to update.</span></span> <span data-ttu-id="f226a-109"> (圖的詳細資訊，請參閱 [關於工作對話方塊](task-dialogs-overview.md)。 ) 此參數必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="f226a-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="f226a-110">值</span><span class="sxs-lookup"><span data-stu-id="f226a-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="f226a-111">意義</span><span class="sxs-lookup"><span data-stu-id="f226a-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="f226a-112"><dt>**TDE \_ 內容**</dt></span><span class="sxs-lookup"><span data-stu-id="f226a-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="f226a-113">內容。</span><span class="sxs-lookup"><span data-stu-id="f226a-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="f226a-114"><dt>**TDE \_ 展開的 \_ 資訊**</dt></span><span class="sxs-lookup"><span data-stu-id="f226a-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="f226a-115">展開的資訊。</span><span class="sxs-lookup"><span data-stu-id="f226a-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="f226a-116"><dt>**TDE \_ 頁尾**</dt></span><span class="sxs-lookup"><span data-stu-id="f226a-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="f226a-117">頁尾文字。</span><span class="sxs-lookup"><span data-stu-id="f226a-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="f226a-118"><dt>**TDE \_ 主要 \_ 指示**</dt></span><span class="sxs-lookup"><span data-stu-id="f226a-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="f226a-119">Main 指令。</span><span class="sxs-lookup"><span data-stu-id="f226a-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="f226a-120">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f226a-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f226a-121">要使用的新文字。</span><span class="sxs-lookup"><span data-stu-id="f226a-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f226a-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="f226a-122">Return value</span></span>

<span data-ttu-id="f226a-123">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f226a-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f226a-124">備註</span><span class="sxs-lookup"><span data-stu-id="f226a-124">Remarks</span></span>

<span data-ttu-id="f226a-125">工作對話方塊的大小或配置可能會變更，以容納新的文字。</span><span class="sxs-lookup"><span data-stu-id="f226a-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="f226a-126">範例</span><span class="sxs-lookup"><span data-stu-id="f226a-126">Examples</span></span>

<span data-ttu-id="f226a-127">下列範例程式碼示範如何設定 *hwnd* 所代表之工作對話方塊中的頁尾文字。</span><span class="sxs-lookup"><span data-stu-id="f226a-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="f226a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="f226a-128">Requirements</span></span>



| <span data-ttu-id="f226a-129">需求</span><span class="sxs-lookup"><span data-stu-id="f226a-129">Requirement</span></span> | <span data-ttu-id="f226a-130">值</span><span class="sxs-lookup"><span data-stu-id="f226a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f226a-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f226a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f226a-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f226a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f226a-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f226a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f226a-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f226a-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f226a-135">標頭</span><span class="sxs-lookup"><span data-stu-id="f226a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f226a-136"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f226a-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f226a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f226a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f226a-138">**TDM \_ UPDATE \_ 元素 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="f226a-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





