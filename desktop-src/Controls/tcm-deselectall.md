---
title: 'TCM_DESELECTALL 訊息 (Commctrl .h) '
description: 重設索引標籤控制項中的專案，清除任何已設定為 TCIS \_ BUTTONPRESSED 狀態的專案。 您可以使用 TabCtrl DeselectAll 宏明確地傳送此訊息 \_ 。
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- TCM_DESELECTALL message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105749"
---
# <a name="tcm_deselectall-message"></a><span data-ttu-id="23d65-105">TCM \_ DESELECTALL 訊息</span><span class="sxs-lookup"><span data-stu-id="23d65-105">TCM\_DESELECTALL message</span></span>

<span data-ttu-id="23d65-106">重設索引標籤控制項中的專案，清除任何已設定為 [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) 狀態的專案。</span><span class="sxs-lookup"><span data-stu-id="23d65-106">Resets items in a tab control, clearing any that were set to the [**TCIS\_BUTTONPRESSED**](tab-control-item-states.md) state.</span></span> <span data-ttu-id="23d65-107">您可以使用 [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="23d65-107">You can send this message explicitly or by using the [**TabCtrl\_DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="23d65-108">參數</span><span class="sxs-lookup"><span data-stu-id="23d65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d65-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23d65-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23d65-110">指定專案 deselection 範圍的旗標。</span><span class="sxs-lookup"><span data-stu-id="23d65-110">Flag that specifies the scope of the item deselection.</span></span> <span data-ttu-id="23d65-111">如果此參數設定為 **FALSE**，則會重設所有索引標籤專案。</span><span class="sxs-lookup"><span data-stu-id="23d65-111">If this parameter is set to **FALSE**, all tab items will be reset.</span></span> <span data-ttu-id="23d65-112">如果設定為 **TRUE**，則會重設目前選取專案以外的所有索引標籤專案。</span><span class="sxs-lookup"><span data-stu-id="23d65-112">If it is set to **TRUE**, then all tab items except for the one currently selected will be reset.</span></span>

</dd> <dt>

<span data-ttu-id="23d65-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23d65-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="23d65-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="23d65-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23d65-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="23d65-115">Return value</span></span>

<span data-ttu-id="23d65-116">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="23d65-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="23d65-117">備註</span><span class="sxs-lookup"><span data-stu-id="23d65-117">Remarks</span></span>

<span data-ttu-id="23d65-118">只有在已設定 [**TCS \_ 按鈕**](tab-control-styles.md) 樣式旗標的情況下，此訊息才有意義。</span><span class="sxs-lookup"><span data-stu-id="23d65-118">This message is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span>

## <a name="requirements"></a><span data-ttu-id="23d65-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="23d65-119">Requirements</span></span>



| <span data-ttu-id="23d65-120">需求</span><span class="sxs-lookup"><span data-stu-id="23d65-120">Requirement</span></span> | <span data-ttu-id="23d65-121">值</span><span class="sxs-lookup"><span data-stu-id="23d65-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23d65-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23d65-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23d65-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23d65-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23d65-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23d65-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23d65-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23d65-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23d65-126">標頭</span><span class="sxs-lookup"><span data-stu-id="23d65-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="23d65-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="23d65-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





