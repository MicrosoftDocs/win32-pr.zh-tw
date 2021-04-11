---
title: 'TDN_DESTROYED (Commctrl 的通知碼) '
description: 當工作對話方塊終結時傳送，而且其視窗控制碼不再有效。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 TaskDialogIndirect 方法來註冊。
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- TDN_DESTROYED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844335"
---
# <a name="tdn_destroyed-notification-code"></a><span data-ttu-id="f3369-105">TDN \_ 損毀的通知碼</span><span class="sxs-lookup"><span data-stu-id="f3369-105">TDN\_DESTROYED notification code</span></span>

<span data-ttu-id="f3369-106">當工作對話方塊終結時傳送，而且其視窗控制碼不再有效。</span><span class="sxs-lookup"><span data-stu-id="f3369-106">Sent by a task dialog when it is destroyed and its window handle is no longer valid.</span></span> <span data-ttu-id="f3369-107">此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。</span><span class="sxs-lookup"><span data-stu-id="f3369-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f3369-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3369-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3369-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3369-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3369-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f3369-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3369-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3369-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3369-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f3369-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3369-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3369-113">Return value</span></span>

<span data-ttu-id="f3369-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f3369-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3369-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3369-115">Requirements</span></span>



| <span data-ttu-id="f3369-116">需求</span><span class="sxs-lookup"><span data-stu-id="f3369-116">Requirement</span></span> | <span data-ttu-id="f3369-117">值</span><span class="sxs-lookup"><span data-stu-id="f3369-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3369-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3369-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f3369-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3369-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3369-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3369-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f3369-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3369-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3369-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f3369-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3369-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3369-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





