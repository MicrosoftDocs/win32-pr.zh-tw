---
title: 'HDM_LAYOUT 訊息 (Commctrl .h) '
description: 抓取用來在父視窗的目標矩形內設定標題控制項大小和位置的資訊。 您可以明確地傳送此訊息，或使用標頭 \_ 版面配置宏。
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025126"
---
# <a name="hdm_layout-message"></a><span data-ttu-id="af325-105">HDM \_ 版面配置訊息</span><span class="sxs-lookup"><span data-stu-id="af325-105">HDM\_LAYOUT message</span></span>

<span data-ttu-id="af325-106">抓取用來在父視窗的目標矩形內設定標題控制項大小和位置的資訊。</span><span class="sxs-lookup"><span data-stu-id="af325-106">Retrieves information used to set the size and position of the header control within the target rectangle of the parent window.</span></span> <span data-ttu-id="af325-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ 版面**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) 配置宏。</span><span class="sxs-lookup"><span data-stu-id="af325-107">You can send this message explicitly or use the [**Header\_Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af325-108">參數</span><span class="sxs-lookup"><span data-stu-id="af325-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af325-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af325-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="af325-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="af325-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="af325-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af325-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af325-112">[**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="af325-112">A pointer to an [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) structure.</span></span> <span data-ttu-id="af325-113">**Prc** 成員會指定矩形的座標，而 **pwpos** 成員會收到矩形內標題控制項的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="af325-113">The **prc** member specifies the coordinates of a rectangle, and the **pwpos** member receives the size and position for the header control within the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af325-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="af325-114">Return value</span></span>

<span data-ttu-id="af325-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="af325-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af325-116">備註</span><span class="sxs-lookup"><span data-stu-id="af325-116">Remarks</span></span>

<span data-ttu-id="af325-117">*LParam* 結構的 **pwpos** 成員會收到適當的大小和位置值，以便將控制項放在指定矩形的上方。</span><span class="sxs-lookup"><span data-stu-id="af325-117">The **pwpos** member of the *lParam* structure receives size and position values appropriate for positioning the control along the top of the specified rectangle.</span></span> <span data-ttu-id="af325-118">高度值是控制項的水準框線高度，以及目前在控制項裝置內容中所選取之字型的平均高度。</span><span class="sxs-lookup"><span data-stu-id="af325-118">The height value is the sum of the heights of the control's horizontal borders and the average height of characters in the font currently selected into the control's device context.</span></span>

<span data-ttu-id="af325-119">若要使用 **HDM \_ 版面** 配置來設定標題控制項的初始大小和位置，請設定控制項的初始可見度狀態，使其隱藏。</span><span class="sxs-lookup"><span data-stu-id="af325-119">To use **HDM\_LAYOUT** to set the initial size and position of a header control, set the initial visibility state of the control so that it is hidden.</span></span> <span data-ttu-id="af325-120">傳送 HDM 配置以抓取大小和位置值之後，請使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)函式來設定新的大小、位置和可見度狀態。 **\_**</span><span class="sxs-lookup"><span data-stu-id="af325-120">After sending **HDM\_LAYOUT** to retrieve the size and position values, use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to set the new size, position, and visibility state.</span></span>

## <a name="requirements"></a><span data-ttu-id="af325-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="af325-121">Requirements</span></span>



| <span data-ttu-id="af325-122">需求</span><span class="sxs-lookup"><span data-stu-id="af325-122">Requirement</span></span> | <span data-ttu-id="af325-123">值</span><span class="sxs-lookup"><span data-stu-id="af325-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af325-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af325-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af325-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af325-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af325-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af325-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af325-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af325-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af325-128">標頭</span><span class="sxs-lookup"><span data-stu-id="af325-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af325-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="af325-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

