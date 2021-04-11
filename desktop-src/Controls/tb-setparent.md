---
title: 'TB_SETPARENT 訊息 (Commctrl .h) '
description: 設定工具列控制項傳送通知訊息的視窗。
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844195"
---
# <a name="tb_setparent-message"></a><span data-ttu-id="bec63-104">TB \_ SETPARENT 訊息</span><span class="sxs-lookup"><span data-stu-id="bec63-104">TB\_SETPARENT message</span></span>

<span data-ttu-id="bec63-105">設定工具列控制項傳送通知訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="bec63-105">Sets the window to which the toolbar control sends notification messages.</span></span>

## <a name="parameters"></a><span data-ttu-id="bec63-106">參數</span><span class="sxs-lookup"><span data-stu-id="bec63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec63-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bec63-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bec63-108">接收通知訊息的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="bec63-108">Handle to the window to receive notification messages.</span></span>

</dd> <dt>

<span data-ttu-id="bec63-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bec63-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bec63-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bec63-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec63-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bec63-111">Return value</span></span>

<span data-ttu-id="bec63-112">傳回值是上一個通知視窗的控制碼; 如果沒有上一個通知視窗，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bec63-112">The return value is a handle to the previous notification window, or **NULL** if there is no previous notification window.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec63-113">備註</span><span class="sxs-lookup"><span data-stu-id="bec63-113">Remarks</span></span>

<span data-ttu-id="bec63-114">**TB 的 \_ SETPARENT** 訊息不會變更建立控制項時所指定的父視窗。</span><span class="sxs-lookup"><span data-stu-id="bec63-114">The **TB\_SETPARENT** message does not change the parent window that was specified when the control was created.</span></span> <span data-ttu-id="bec63-115">針對工具列控制項呼叫 [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) 函式會傳回實際的父視窗，而不是以 **TB \_ SETPARENT** 指定的視窗。</span><span class="sxs-lookup"><span data-stu-id="bec63-115">Calling the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function for a toolbar control will return the actual parent window, not the window specified in **TB\_SETPARENT**.</span></span> <span data-ttu-id="bec63-116">若要變更控制項的父視窗，請呼叫 [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) 函數。</span><span class="sxs-lookup"><span data-stu-id="bec63-116">To change the control's parent window, call the [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec63-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bec63-117">Requirements</span></span>



| <span data-ttu-id="bec63-118">需求</span><span class="sxs-lookup"><span data-stu-id="bec63-118">Requirement</span></span> | <span data-ttu-id="bec63-119">值</span><span class="sxs-lookup"><span data-stu-id="bec63-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bec63-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bec63-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bec63-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bec63-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bec63-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bec63-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bec63-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bec63-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bec63-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bec63-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bec63-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bec63-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

