---
title: 'TDN_CREATED (Commctrl 的通知碼) '
description: 在對話方塊建立之後以及顯示之前，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 TaskDialogIndirect 方法來註冊。
ms.assetid: cfe13db3-9c3c-425c-a6ef-17c5cb33eeb6
keywords:
- TDN_CREATED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_CREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25aa40af6b2cb002f2da7aab7c71fd68702ae65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935091"
---
# <a name="tdn_created-notification-code"></a><span data-ttu-id="f662c-105">TDN \_ 建立的通知碼</span><span class="sxs-lookup"><span data-stu-id="f662c-105">TDN\_CREATED notification code</span></span>

<span data-ttu-id="f662c-106">在對話方塊建立之後以及顯示之前，由工作對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="f662c-106">Sent by the task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="f662c-107">此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。</span><span class="sxs-lookup"><span data-stu-id="f662c-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_CREATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f662c-108">參數</span><span class="sxs-lookup"><span data-stu-id="f662c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f662c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f662c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f662c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f662c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f662c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f662c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f662c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f662c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f662c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f662c-113">Return value</span></span>

<span data-ttu-id="f662c-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f662c-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f662c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f662c-115">Requirements</span></span>



| <span data-ttu-id="f662c-116">需求</span><span class="sxs-lookup"><span data-stu-id="f662c-116">Requirement</span></span> | <span data-ttu-id="f662c-117">值</span><span class="sxs-lookup"><span data-stu-id="f662c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f662c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f662c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f662c-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f662c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f662c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f662c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f662c-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f662c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f662c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f662c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f662c-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f662c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





