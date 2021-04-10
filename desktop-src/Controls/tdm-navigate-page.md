---
title: 'TDM_NAVIGATE_PAGE 訊息 (Commctrl .h) '
description: 以新的內容重新建立工作對話方塊，模擬多頁 wizard 的功能。
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935005"
---
# <a name="tdm_navigate_page-message"></a><span data-ttu-id="f1f96-104">TDM \_ 導覽 \_ 頁面訊息</span><span class="sxs-lookup"><span data-stu-id="f1f96-104">TDM\_NAVIGATE\_PAGE message</span></span>

<span data-ttu-id="f1f96-105">以新的內容重新建立工作對話方塊，模擬多頁 wizard 的功能。</span><span class="sxs-lookup"><span data-stu-id="f1f96-105">Recreates a task dialog with new contents, simulating the functionality of a multi-page wizard.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1f96-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1f96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f96-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1f96-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f96-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="f1f96-108">Not used.</span></span> <span data-ttu-id="f1f96-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f1f96-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f1f96-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1f96-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f96-111">描述要建立之工作對話方塊的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="f1f96-111">A pointer to a [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that describes the task dialog to create.</span></span> <span data-ttu-id="f1f96-112">呼叫的應用程式必須配置此結構並設定其成員。</span><span class="sxs-lookup"><span data-stu-id="f1f96-112">The calling application must allocate this structure and set its members.</span></span> <span data-ttu-id="f1f96-113">成員的值會根據使用者流覽至的頁面類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f1f96-113">The values of the members vary depending on the kind of page the user navigates to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f96-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1f96-114">Return value</span></span>

<span data-ttu-id="f1f96-115">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f1f96-115">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f96-116">備註</span><span class="sxs-lookup"><span data-stu-id="f1f96-116">Remarks</span></span>

<span data-ttu-id="f1f96-117">若要啟動嚮導工作對話方塊，請使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 函式。</span><span class="sxs-lookup"><span data-stu-id="f1f96-117">To launch a wizard task dialog, use the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="f1f96-118">當使用者使用嚮導流覽時，請將此訊息傳送至工作對話方塊以顯示下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="f1f96-118">As the user navigates using the wizard, send this message to the task dialog to display the next page.</span></span> <span data-ttu-id="f1f96-119">新的工作對話方塊 (看起來就像新的頁面) 是使用 *lParam* 所指向的結構中指定的元素所建立。</span><span class="sxs-lookup"><span data-stu-id="f1f96-119">A new task dialog (looks like a new page) is created with the elements specified in the structure pointed to by *lParam*.</span></span> <span data-ttu-id="f1f96-120">建立時，會終結並重建對話方塊框架的整個內容。</span><span class="sxs-lookup"><span data-stu-id="f1f96-120">At creation, the entire contents of the dialog frame are destroyed and reconstructed.</span></span> <span data-ttu-id="f1f96-121">如此一來，控制項所持有的任何狀態資訊 (例如，會遺失對話方塊中的進度列、expando 按鈕或驗證核取方塊) 。</span><span class="sxs-lookup"><span data-stu-id="f1f96-121">As a result, any state information held by controls (for example, a progress bar, expando button, or verification checkbox) in the dialog is lost.</span></span>

<span data-ttu-id="f1f96-122">工作對話方塊的版面配置可能會失敗，而且不會反映在傳回值中。</span><span class="sxs-lookup"><span data-stu-id="f1f96-122">The layout of the task dialog may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="f1f96-123">\_[確定] 的傳回值只會反映工作對話方塊收到的訊息，並嘗試進行處理。</span><span class="sxs-lookup"><span data-stu-id="f1f96-123">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="f1f96-124">如果工作對話方塊的配置失敗 (工作對話方塊無法顯示) ，對話方塊將會關閉，並且會在註冊的回呼函式傳回 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="f1f96-124">If the layout of the task dialog fails (the task dialog cannot be displayed), the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="f1f96-125">如需回呼函數語法的詳細資訊，請參閱 [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)。</span><span class="sxs-lookup"><span data-stu-id="f1f96-125">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f96-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1f96-126">Requirements</span></span>



| <span data-ttu-id="f1f96-127">需求</span><span class="sxs-lookup"><span data-stu-id="f1f96-127">Requirement</span></span> | <span data-ttu-id="f1f96-128">值</span><span class="sxs-lookup"><span data-stu-id="f1f96-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f96-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1f96-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f96-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1f96-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1f96-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1f96-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f96-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1f96-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1f96-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f1f96-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1f96-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f96-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

