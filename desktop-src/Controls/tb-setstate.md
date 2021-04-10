---
title: 'TB_SETSTATE 訊息 (Commctrl .h) '
description: 在工具列中設定指定之按鈕的狀態。
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106589"
---
# <a name="tb_setstate-message"></a><span data-ttu-id="27936-104">TB \_ SETSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="27936-104">TB\_SETSTATE message</span></span>

<span data-ttu-id="27936-105">在工具列中設定指定之按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="27936-105">Sets the state for the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="27936-106">參數</span><span class="sxs-lookup"><span data-stu-id="27936-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27936-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27936-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27936-108">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="27936-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="27936-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27936-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27936-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是列在 [工具列按鈕狀態](toolbar-button-states.md)中的值組合。</span><span class="sxs-lookup"><span data-stu-id="27936-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a combination of values listed in [Toolbar Button States](toolbar-button-states.md).</span></span> <span data-ttu-id="27936-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。</span><span class="sxs-lookup"><span data-stu-id="27936-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27936-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="27936-112">Return value</span></span>

<span data-ttu-id="27936-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="27936-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="27936-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="27936-114">Requirements</span></span>



| <span data-ttu-id="27936-115">需求</span><span class="sxs-lookup"><span data-stu-id="27936-115">Requirement</span></span> | <span data-ttu-id="27936-116">值</span><span class="sxs-lookup"><span data-stu-id="27936-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27936-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27936-117">Minimum supported client</span></span><br/> | <span data-ttu-id="27936-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27936-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27936-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27936-119">Minimum supported server</span></span><br/> | <span data-ttu-id="27936-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27936-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27936-121">標頭</span><span class="sxs-lookup"><span data-stu-id="27936-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="27936-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="27936-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

