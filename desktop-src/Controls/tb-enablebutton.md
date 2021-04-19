---
title: 'TB_ENABLEBUTTON 訊息 (Commctrl .h) '
description: 在工具列中啟用或停用指定的按鈕。
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- TB_ENABLEBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970465"
---
# <a name="tb_enablebutton-message"></a><span data-ttu-id="18449-104">TB \_ ENABLEBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="18449-104">TB\_ENABLEBUTTON message</span></span>

<span data-ttu-id="18449-105">在工具列中啟用或停用指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="18449-105">Enables or disables the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="18449-106">參數</span><span class="sxs-lookup"><span data-stu-id="18449-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18449-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18449-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18449-108">要啟用或停用之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="18449-108">Command identifier of the button to enable or disable.</span></span>

</dd> <dt>

<span data-ttu-id="18449-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18449-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18449-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指出是否要啟用或停用指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="18449-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to enable or disable the specified button.</span></span> <span data-ttu-id="18449-111">若 **為 TRUE**，則會啟用按鈕。</span><span class="sxs-lookup"><span data-stu-id="18449-111">If **TRUE**, the button is enabled.</span></span> <span data-ttu-id="18449-112">如果 **為 FALSE**，則表示按鈕已停用。</span><span class="sxs-lookup"><span data-stu-id="18449-112">If **FALSE**, the button is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18449-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="18449-113">Return value</span></span>

<span data-ttu-id="18449-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="18449-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="18449-115">備註</span><span class="sxs-lookup"><span data-stu-id="18449-115">Remarks</span></span>

<span data-ttu-id="18449-116">啟用按鈕之後，您可以按下並核取按鈕。</span><span class="sxs-lookup"><span data-stu-id="18449-116">When a button has been enabled, it can be pressed and checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="18449-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="18449-117">Requirements</span></span>



| <span data-ttu-id="18449-118">需求</span><span class="sxs-lookup"><span data-stu-id="18449-118">Requirement</span></span> | <span data-ttu-id="18449-119">值</span><span class="sxs-lookup"><span data-stu-id="18449-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18449-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18449-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18449-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18449-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18449-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18449-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18449-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18449-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18449-124">標頭</span><span class="sxs-lookup"><span data-stu-id="18449-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18449-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="18449-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

