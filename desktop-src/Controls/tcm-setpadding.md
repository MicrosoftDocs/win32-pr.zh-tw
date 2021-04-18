---
title: 'TCM_SETPADDING 訊息 (Commctrl .h) '
description: 設定在索引標籤控制項中每個索引標籤的圖示和標籤周圍的空間 (填補) 。 您可以使用 TabCtrl SetPadding 宏明確地傳送此訊息 \_ 。
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965693"
---
# <a name="tcm_setpadding-message"></a><span data-ttu-id="2f284-105">TCM \_ SETPADDING 訊息</span><span class="sxs-lookup"><span data-stu-id="2f284-105">TCM\_SETPADDING message</span></span>

<span data-ttu-id="2f284-106">設定在索引標籤控制項中每個索引標籤的圖示和標籤周圍的空間 (填補) 。</span><span class="sxs-lookup"><span data-stu-id="2f284-106">Sets the amount of space (padding) around each tab's icon and label in a tab control.</span></span> <span data-ttu-id="2f284-107">您可以使用 [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2f284-107">You can send this message explicitly or by using the [**TabCtrl\_SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f284-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f284-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f284-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f284-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f284-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **INT** 值，可指定水準填補量（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f284-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the amount of horizontal padding, in pixels.</span></span> <span data-ttu-id="2f284-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是 **INT** 值，可指定垂直填補量（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f284-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the amount of vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f284-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f284-112">Return value</span></span>

<span data-ttu-id="2f284-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2f284-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f284-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f284-114">Requirements</span></span>



| <span data-ttu-id="2f284-115">需求</span><span class="sxs-lookup"><span data-stu-id="2f284-115">Requirement</span></span> | <span data-ttu-id="2f284-116">值</span><span class="sxs-lookup"><span data-stu-id="2f284-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f284-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f284-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f284-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f284-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f284-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f284-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f284-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f284-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f284-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2f284-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f284-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f284-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

