---
title: 'BCM_SETSPLITINFO 訊息 (Commctrl .h) '
description: 設定分割按鈕控制項的資訊。 明確地傳送此訊息，或使用按鈕 \_ SetSplitInfo 宏。
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965089"
---
# <a name="bcm_setsplitinfo-message"></a><span data-ttu-id="40dd5-105">BCM \_ SETSPLITINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="40dd5-105">BCM\_SETSPLITINFO message</span></span>

<span data-ttu-id="40dd5-106">設定分割按鈕控制項的資訊。</span><span class="sxs-lookup"><span data-stu-id="40dd5-106">Sets information for a split button control.</span></span> <span data-ttu-id="40dd5-107">明確地傳送此訊息，或使用 [**按鈕 \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) 宏。</span><span class="sxs-lookup"><span data-stu-id="40dd5-107">Send this message explicitly or by using the [**Button\_SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="40dd5-108">參數</span><span class="sxs-lookup"><span data-stu-id="40dd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40dd5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40dd5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40dd5-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="40dd5-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="40dd5-111">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40dd5-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40dd5-112">[**按鈕 \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo)結構的指標，其中包含分割按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="40dd5-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure containing information about the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40dd5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="40dd5-113">Return value</span></span>

<span data-ttu-id="40dd5-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="40dd5-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="40dd5-115">備註</span><span class="sxs-lookup"><span data-stu-id="40dd5-115">Remarks</span></span>

<span data-ttu-id="40dd5-116">此訊息只能搭配 [**BS \_ SPLITBUTTON**](button-styles.md) 和 [**BS \_ DEFSPLITBUTTON**](button-styles.md) 按鈕樣式使用。</span><span class="sxs-lookup"><span data-stu-id="40dd5-116">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="40dd5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="40dd5-117">Requirements</span></span>



| <span data-ttu-id="40dd5-118">需求</span><span class="sxs-lookup"><span data-stu-id="40dd5-118">Requirement</span></span> | <span data-ttu-id="40dd5-119">值</span><span class="sxs-lookup"><span data-stu-id="40dd5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40dd5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40dd5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="40dd5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40dd5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40dd5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40dd5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="40dd5-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40dd5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40dd5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="40dd5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="40dd5-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="40dd5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40dd5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40dd5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="40dd5-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="40dd5-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="40dd5-128">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="40dd5-128">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="40dd5-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="40dd5-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="40dd5-130">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="40dd5-130">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





