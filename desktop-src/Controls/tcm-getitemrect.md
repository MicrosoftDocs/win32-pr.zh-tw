---
title: 'TCM_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中索引標籤的周框。 您可以使用 TabCtrl GetItemRect 宏明確地傳送此訊息 \_ 。
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- TCM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844180"
---
# <a name="tcm_getitemrect-message"></a><span data-ttu-id="f04a0-105">TCM \_ GETITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="f04a0-105">TCM\_GETITEMRECT message</span></span>

<span data-ttu-id="f04a0-106">抓取索引標籤控制項中索引標籤的周框。</span><span class="sxs-lookup"><span data-stu-id="f04a0-106">Retrieves the bounding rectangle for a tab in a tab control.</span></span> <span data-ttu-id="f04a0-107">您可以使用 [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f04a0-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f04a0-108">參數</span><span class="sxs-lookup"><span data-stu-id="f04a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f04a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f04a0-110">索引標籤的索引。</span><span class="sxs-lookup"><span data-stu-id="f04a0-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="f04a0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f04a0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f04a0-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收索引標籤的周框座標（以區座標表示）。</span><span class="sxs-lookup"><span data-stu-id="f04a0-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the tab, in viewport coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f04a0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f04a0-113">Return value</span></span>

<span data-ttu-id="f04a0-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f04a0-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04a0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f04a0-115">Requirements</span></span>



| <span data-ttu-id="f04a0-116">需求</span><span class="sxs-lookup"><span data-stu-id="f04a0-116">Requirement</span></span> | <span data-ttu-id="f04a0-117">值</span><span class="sxs-lookup"><span data-stu-id="f04a0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f04a0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f04a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f04a0-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f04a0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f04a0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f04a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f04a0-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f04a0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f04a0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f04a0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f04a0-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f04a0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

