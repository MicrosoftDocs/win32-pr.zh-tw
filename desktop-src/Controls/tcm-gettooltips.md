---
title: 'TCM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取與索引標籤控制項相關聯的工具提示控制項控點。 您可以使用 TabCtrl GetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- TCM_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105737"
---
# <a name="tcm_gettooltips-message"></a><span data-ttu-id="a2ec2-105">TCM \_ GETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="a2ec2-105">TCM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="a2ec2-106">抓取與索引標籤控制項相關聯的工具提示控制項控點。</span><span class="sxs-lookup"><span data-stu-id="a2ec2-106">Retrieves the handle to the tooltip control associated with a tab control.</span></span> <span data-ttu-id="a2ec2-107">您可以使用 [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a2ec2-107">You can send this message explicitly or by using the [**TabCtrl\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2ec2-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2ec2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ec2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2ec2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a2ec2-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a2ec2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a2ec2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2ec2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a2ec2-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a2ec2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ec2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2ec2-113">Return value</span></span>

<span data-ttu-id="a2ec2-114">如果成功，則傳回工具提示控制項的控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a2ec2-114">Returns the handle to the tooltip control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ec2-115">備註</span><span class="sxs-lookup"><span data-stu-id="a2ec2-115">Remarks</span></span>

<span data-ttu-id="a2ec2-116">如果工具提示控制項有 [**TCS \_ 工具提示**](tab-control-styles.md) 樣式，則會建立工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="a2ec2-116">A tab control creates a tooltip control if it has the [**TCS\_TOOLTIPS**](tab-control-styles.md) style.</span></span> <span data-ttu-id="a2ec2-117">您也可以使用 [**TCM \_ SETTOOLTIPS**](tcm-settooltips.md) 訊息，將工具提示控制項指派給索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="a2ec2-117">You can also assign a tooltip control to a tab control by using the [**TCM\_SETTOOLTIPS**](tcm-settooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ec2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2ec2-118">Requirements</span></span>



| <span data-ttu-id="a2ec2-119">需求</span><span class="sxs-lookup"><span data-stu-id="a2ec2-119">Requirement</span></span> | <span data-ttu-id="a2ec2-120">值</span><span class="sxs-lookup"><span data-stu-id="a2ec2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ec2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2ec2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ec2-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2ec2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2ec2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2ec2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ec2-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2ec2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2ec2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a2ec2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ec2-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ec2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





