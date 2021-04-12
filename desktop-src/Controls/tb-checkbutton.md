---
title: 'TB_CHECKBUTTON 訊息 (Commctrl .h) '
description: 檢查或取消核取工具列中的指定按鈕。
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- TB_CHECKBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025502"
---
# <a name="tb_checkbutton-message"></a><span data-ttu-id="5a9fd-104">TB \_ CHECKBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="5a9fd-104">TB\_CHECKBUTTON message</span></span>

<span data-ttu-id="5a9fd-105">檢查或取消核取工具列中的指定按鈕。</span><span class="sxs-lookup"><span data-stu-id="5a9fd-105">Checks or unchecks a given button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a9fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a9fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a9fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9fd-108">要檢查之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a9fd-108">Command identifier of the button to check.</span></span>

</dd> <dt>

<span data-ttu-id="5a9fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a9fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9fd-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指出是否要檢查或取消選取指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="5a9fd-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to check or uncheck the specified button.</span></span> <span data-ttu-id="5a9fd-111">若 **為 TRUE**，則會新增檢查。</span><span class="sxs-lookup"><span data-stu-id="5a9fd-111">If **TRUE**, the check is added.</span></span> <span data-ttu-id="5a9fd-112">如果 **為 FALSE**，則會移除檢查。</span><span class="sxs-lookup"><span data-stu-id="5a9fd-112">If **FALSE**, the check is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9fd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a9fd-113">Return value</span></span>

<span data-ttu-id="5a9fd-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5a9fd-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9fd-115">備註</span><span class="sxs-lookup"><span data-stu-id="5a9fd-115">Remarks</span></span>

<span data-ttu-id="5a9fd-116">核取按鈕時，會顯示為已按下的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a9fd-116">When a button is checked, it is displayed in the pressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9fd-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a9fd-117">Requirements</span></span>



| <span data-ttu-id="5a9fd-118">需求</span><span class="sxs-lookup"><span data-stu-id="5a9fd-118">Requirement</span></span> | <span data-ttu-id="5a9fd-119">值</span><span class="sxs-lookup"><span data-stu-id="5a9fd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9fd-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a9fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a9fd-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a9fd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a9fd-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a9fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a9fd-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a9fd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a9fd-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5a9fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a9fd-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a9fd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

