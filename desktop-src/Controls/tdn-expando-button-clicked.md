---
title: 'TDN_EXPANDO_BUTTON_CLICKED (Commctrl 的通知碼) '
description: 當使用者按一下對話方塊的 expando 按鈕時，由工作對話方塊傳送。 只有透過工作對話方塊回呼函式（可使用 TaskDialogIndirect 方法來註冊）才會收到此通知。
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- TDN_EXPANDO_BUTTON_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968998"
---
# <a name="tdn_expando_button_clicked-notification-code"></a><span data-ttu-id="bb4aa-105">TDN \_ EXPANDO \_ 按鈕已 \_ 按一下通知碼</span><span class="sxs-lookup"><span data-stu-id="bb4aa-105">TDN\_EXPANDO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="bb4aa-106">當使用者按一下對話方塊的 expando 按鈕時，由工作對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="bb4aa-106">Sent by the task dialog when the user clicks on the dialog's expando button.</span></span> <span data-ttu-id="bb4aa-107">只有透過工作對話方塊回呼函式（可使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊）才會收到此通知。</span><span class="sxs-lookup"><span data-stu-id="bb4aa-107">This notification is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="bb4aa-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb4aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb4aa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb4aa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb4aa-110">如果展開對話方塊，則 **布林\*\*\*\*值為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bb4aa-110">A **BOOL** that is **TRUE** if the dialog is expanded, or **FALSE** if not.</span></span>

</dd> <dt>

<span data-ttu-id="bb4aa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb4aa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb4aa-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bb4aa-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb4aa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb4aa-113">Return value</span></span>

<span data-ttu-id="bb4aa-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="bb4aa-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb4aa-115">備註</span><span class="sxs-lookup"><span data-stu-id="bb4aa-115">Remarks</span></span>

<span data-ttu-id="bb4aa-116">語法區段中的範例會顯示在傳送通知之前轉換成 wParam。</span><span class="sxs-lookup"><span data-stu-id="bb4aa-116">The example in the Syntax section shows the cast to wParam before sending the notification.</span></span> <span data-ttu-id="bb4aa-117">**LPARAM** 不會使用，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="bb4aa-117">**LPARAM** is not used and must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb4aa-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb4aa-118">Requirements</span></span>



| <span data-ttu-id="bb4aa-119">需求</span><span class="sxs-lookup"><span data-stu-id="bb4aa-119">Requirement</span></span> | <span data-ttu-id="bb4aa-120">值</span><span class="sxs-lookup"><span data-stu-id="bb4aa-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4aa-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb4aa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb4aa-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb4aa-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb4aa-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb4aa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb4aa-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb4aa-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb4aa-125">標頭</span><span class="sxs-lookup"><span data-stu-id="bb4aa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb4aa-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb4aa-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





