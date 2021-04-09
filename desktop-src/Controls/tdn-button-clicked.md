---
title: 'TDN_BUTTON_CLICKED (Commctrl 的通知碼) '
description: 當使用者選取工作對話方塊中的按鈕或命令連結時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 TaskDialogIndirect 方法來註冊。
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935090"
---
# <a name="tdn_button_clicked-notification-code"></a><span data-ttu-id="0ddc5-105">TDN 按鈕已按下 \_ \_ 通知碼</span><span class="sxs-lookup"><span data-stu-id="0ddc5-105">TDN\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="0ddc5-106">當使用者選取工作對話方塊中的按鈕或命令連結時，由工作對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="0ddc5-106">Sent by a task dialog when the user selects a button or command link in the task dialog.</span></span> <span data-ttu-id="0ddc5-107">此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。</span><span class="sxs-lookup"><span data-stu-id="0ddc5-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0ddc5-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ddc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ddc5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ddc5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ddc5-110">**Int** ，指定所選取之按鈕或命令連結的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ddc5-110">An **int** that specifies the ID of the button or comand link that was selected.</span></span>

</dd> <dt>

<span data-ttu-id="0ddc5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ddc5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ddc5-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0ddc5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ddc5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ddc5-113">Return value</span></span>

<span data-ttu-id="0ddc5-114">若要防止工作對話方塊關閉，應用程式必須傳回 **\_ FALSE**，否則工作對話方塊會關閉，而按鈕識別碼會透過原始應用程式呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="0ddc5-114">To prevent the task dialog from closing, the application must return **S\_FALSE**, otherwise the task dialog is closed and the button ID is returned via the original application call.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddc5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ddc5-115">Requirements</span></span>



| <span data-ttu-id="0ddc5-116">需求</span><span class="sxs-lookup"><span data-stu-id="0ddc5-116">Requirement</span></span> | <span data-ttu-id="0ddc5-117">值</span><span class="sxs-lookup"><span data-stu-id="0ddc5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddc5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ddc5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddc5-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddc5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ddc5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ddc5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddc5-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddc5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ddc5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0ddc5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ddc5-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddc5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





