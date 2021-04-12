---
title: 'TDN_HELP (Commctrl 的通知碼) '
description: 當使用者在對話方塊具有焦點時按下鍵盤上的 F1 時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 TaskDialogIndirect 方法來註冊。
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- TDN_HELP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d5e08342094aec5adc3da42621307d1577cd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106236"
---
# <a name="tdn_help-notification-code"></a><span data-ttu-id="e35e0-105">TDN 說明 \_ 通知碼</span><span class="sxs-lookup"><span data-stu-id="e35e0-105">TDN\_HELP notification code</span></span>

<span data-ttu-id="e35e0-106">當使用者在對話方塊具有焦點時按下鍵盤上的 F1 時，由工作對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="e35e0-106">Sent by a task dialog when the user presses F1 on the keyboard while the dialog has focus.</span></span> <span data-ttu-id="e35e0-107">此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。</span><span class="sxs-lookup"><span data-stu-id="e35e0-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HELP
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e35e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="e35e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e35e0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e35e0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e35e0-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e35e0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e35e0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e35e0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e35e0-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e35e0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e35e0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e35e0-113">Return value</span></span>

<span data-ttu-id="e35e0-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e35e0-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e35e0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e35e0-115">Requirements</span></span>



| <span data-ttu-id="e35e0-116">需求</span><span class="sxs-lookup"><span data-stu-id="e35e0-116">Requirement</span></span> | <span data-ttu-id="e35e0-117">值</span><span class="sxs-lookup"><span data-stu-id="e35e0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e35e0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e35e0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e35e0-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e35e0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e35e0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e35e0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e35e0-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e35e0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e35e0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e35e0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e35e0-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e35e0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





