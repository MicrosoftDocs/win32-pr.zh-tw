---
title: 'TDN_VERIFICATION_CLICKED (Commctrl 的通知碼) '
description: 當使用者按一下工作對話方塊驗證核取方塊時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 TaskDialogIndirect 方法來註冊。
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935085"
---
# <a name="tdn_verification_clicked-notification-code"></a><span data-ttu-id="c25a3-105">TDN \_ 驗證已 \_ 按一下通知碼</span><span class="sxs-lookup"><span data-stu-id="c25a3-105">TDN\_VERIFICATION\_CLICKED notification code</span></span>

<span data-ttu-id="c25a3-106">當使用者按一下工作對話方塊驗證核取方塊時，由工作對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="c25a3-106">Sent by a task dialog when the user clicks the task dialog verification check box.</span></span> <span data-ttu-id="c25a3-107">此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。</span><span class="sxs-lookup"><span data-stu-id="c25a3-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="c25a3-108">參數</span><span class="sxs-lookup"><span data-stu-id="c25a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c25a3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c25a3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c25a3-110">指定驗證核取方塊狀態的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="c25a3-110">A **BOOL** that specifies the status of the verification checkbox.</span></span> <span data-ttu-id="c25a3-111">如果已核取 [驗證] 核取方塊，則為 **TRUE** ; 如果未核取，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c25a3-111">It is **TRUE** if the verification checkbox is checked, or **FALSE** if it is unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="c25a3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c25a3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c25a3-113">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c25a3-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c25a3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c25a3-114">Return value</span></span>

<span data-ttu-id="c25a3-115">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c25a3-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c25a3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c25a3-116">Requirements</span></span>



| <span data-ttu-id="c25a3-117">需求</span><span class="sxs-lookup"><span data-stu-id="c25a3-117">Requirement</span></span> | <span data-ttu-id="c25a3-118">值</span><span class="sxs-lookup"><span data-stu-id="c25a3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c25a3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c25a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c25a3-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c25a3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c25a3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c25a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c25a3-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c25a3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c25a3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c25a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c25a3-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c25a3-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c25a3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c25a3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c25a3-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="c25a3-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c25a3-127">*TaskDialogCallbackProc*</span><span class="sxs-lookup"><span data-stu-id="c25a3-127">*TaskDialogCallbackProc*</span></span>](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

