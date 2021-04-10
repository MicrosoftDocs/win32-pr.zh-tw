---
title: 'TB_SETBUTTONWIDTH 訊息 (Commctrl .h) '
description: 設定工具列控制項中的最小和最大按鈕寬度。
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103758"
---
# <a name="tb_setbuttonwidth-message"></a><span data-ttu-id="688be-104">TB \_ SETBUTTONWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="688be-104">TB\_SETBUTTONWIDTH message</span></span>

<span data-ttu-id="688be-105">設定工具列控制項中的最小和最大按鈕寬度。</span><span class="sxs-lookup"><span data-stu-id="688be-105">Sets the minimum and maximum button widths in the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="688be-106">參數</span><span class="sxs-lookup"><span data-stu-id="688be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="688be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="688be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="688be-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="688be-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="688be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="688be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="688be-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最小按鈕寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="688be-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum button width, in pixels.</span></span> <span data-ttu-id="688be-111">工具列按鈕絕不會比這個值窄。</span><span class="sxs-lookup"><span data-stu-id="688be-111">Toolbar buttons will never be narrower than this value.</span></span>

<span data-ttu-id="688be-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大按鈕寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="688be-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum button width, in pixels.</span></span> <span data-ttu-id="688be-113">如果按鈕文字太寬，控制項會以省略號點顯示。</span><span class="sxs-lookup"><span data-stu-id="688be-113">If button text is too wide, the control displays it with ellipsis points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="688be-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="688be-114">Return value</span></span>

<span data-ttu-id="688be-115">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="688be-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="688be-116">備註</span><span class="sxs-lookup"><span data-stu-id="688be-116">Remarks</span></span>

<span data-ttu-id="688be-117">使用 [ **TB] \_ SETBUTTONWIDTH** 可設定按鈕在新增之前允許的最大寬度和最小值。</span><span class="sxs-lookup"><span data-stu-id="688be-117">Use **TB\_SETBUTTONWIDTH** to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="688be-118">使用 [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) 來設定按鈕的實際大小。</span><span class="sxs-lookup"><span data-stu-id="688be-118">Use [**TB\_SETBUTTONSIZE**](tb-setbuttonsize.md) to set the actual size of buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="688be-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="688be-119">Requirements</span></span>



| <span data-ttu-id="688be-120">需求</span><span class="sxs-lookup"><span data-stu-id="688be-120">Requirement</span></span> | <span data-ttu-id="688be-121">值</span><span class="sxs-lookup"><span data-stu-id="688be-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="688be-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="688be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="688be-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="688be-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="688be-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="688be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="688be-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="688be-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="688be-126">標頭</span><span class="sxs-lookup"><span data-stu-id="688be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="688be-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="688be-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

