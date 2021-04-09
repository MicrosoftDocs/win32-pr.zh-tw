---
title: 'TCM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 將工具提示控制項指派給索引標籤控制項。 您可以使用 TabCtrl SetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685500"
---
# <a name="tcm_settooltips-message"></a><span data-ttu-id="723e8-105">TCM \_ SETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="723e8-105">TCM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="723e8-106">將工具提示控制項指派給索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="723e8-106">Assigns a tooltip control to a tab control.</span></span> <span data-ttu-id="723e8-107">您可以使用 [**TabCtrl \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="723e8-107">You can send this message explicitly or by using the [**TabCtrl\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="723e8-108">參數</span><span class="sxs-lookup"><span data-stu-id="723e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="723e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="723e8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="723e8-110">工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="723e8-110">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="723e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="723e8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="723e8-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="723e8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="723e8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="723e8-113">Return value</span></span>

<span data-ttu-id="723e8-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="723e8-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="723e8-115">備註</span><span class="sxs-lookup"><span data-stu-id="723e8-115">Remarks</span></span>

<span data-ttu-id="723e8-116">您可以使用 [**TCM \_ GETTOOLTIPS**](tcm-gettooltips.md) 訊息來取得與索引標籤控制項相關聯的工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="723e8-116">You can retrieve the tooltip control associated with a tab control by using the [**TCM\_GETTOOLTIPS**](tcm-gettooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="723e8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="723e8-117">Requirements</span></span>



| <span data-ttu-id="723e8-118">需求</span><span class="sxs-lookup"><span data-stu-id="723e8-118">Requirement</span></span> | <span data-ttu-id="723e8-119">值</span><span class="sxs-lookup"><span data-stu-id="723e8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="723e8-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="723e8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="723e8-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="723e8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="723e8-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="723e8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="723e8-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="723e8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="723e8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="723e8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="723e8-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="723e8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





