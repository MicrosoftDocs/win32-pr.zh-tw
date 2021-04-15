---
title: 'TBM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 將工具提示控制項指派給 [對等] 控制項。
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- TBM_SETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464769"
---
# <a name="tbm_settooltips-message"></a><span data-ttu-id="dc850-104">TBM \_ SETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="dc850-104">TBM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="dc850-105">將工具提示控制項指派給 [對等] 控制項。</span><span class="sxs-lookup"><span data-stu-id="dc850-105">Assigns a tooltip control to a trackbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc850-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc850-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc850-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc850-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc850-108">現有工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dc850-108">Handle to an existing tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="dc850-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc850-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dc850-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="dc850-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc850-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc850-111">Return value</span></span>

<span data-ttu-id="dc850-112">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="dc850-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc850-113">備註</span><span class="sxs-lookup"><span data-stu-id="dc850-113">Remarks</span></span>

<span data-ttu-id="dc850-114">當使用 [ [**tb] \_ 工具提示**](trackbar-control-styles.md) 樣式建立的 [顯示] 控制項時，它會建立一個預設的工具提示控制項，顯示在滑杆旁邊，顯示滑杆的目前位置。</span><span class="sxs-lookup"><span data-stu-id="dc850-114">When a trackbar control is created with the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc850-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc850-115">Requirements</span></span>



| <span data-ttu-id="dc850-116">需求</span><span class="sxs-lookup"><span data-stu-id="dc850-116">Requirement</span></span> | <span data-ttu-id="dc850-117">值</span><span class="sxs-lookup"><span data-stu-id="dc850-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc850-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc850-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc850-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc850-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc850-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc850-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc850-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc850-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc850-122">標頭</span><span class="sxs-lookup"><span data-stu-id="dc850-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc850-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc850-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





