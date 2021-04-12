---
title: 'TDN_NAVIGATED (Commctrl 的通知碼) '
description: 在流覽發生時由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 TaskDialogIndirect 方法來註冊。
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- TDN_NAVIGATED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9d8e9244889d7e55aad2b89f8ca4bb1c0bb1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509423"
---
# <a name="tdn_navigated-notification-code"></a><span data-ttu-id="7b89f-105">TDN \_ 流覽的通知碼</span><span class="sxs-lookup"><span data-stu-id="7b89f-105">TDN\_NAVIGATED notification code</span></span>

<span data-ttu-id="7b89f-106">在流覽發生時由工作對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="7b89f-106">Sent by a task dialog when navigation has occurred.</span></span> <span data-ttu-id="7b89f-107">此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。</span><span class="sxs-lookup"><span data-stu-id="7b89f-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_NAVIGATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="7b89f-108">參數</span><span class="sxs-lookup"><span data-stu-id="7b89f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b89f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b89f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b89f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7b89f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7b89f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b89f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b89f-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7b89f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b89f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b89f-113">Return value</span></span>

<span data-ttu-id="7b89f-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7b89f-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b89f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b89f-115">Requirements</span></span>



| <span data-ttu-id="7b89f-116">需求</span><span class="sxs-lookup"><span data-stu-id="7b89f-116">Requirement</span></span> | <span data-ttu-id="7b89f-117">值</span><span class="sxs-lookup"><span data-stu-id="7b89f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b89f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b89f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b89f-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b89f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b89f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b89f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b89f-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b89f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b89f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7b89f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b89f-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b89f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





