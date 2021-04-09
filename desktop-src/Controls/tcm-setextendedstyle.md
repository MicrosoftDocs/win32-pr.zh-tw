---
title: 'TCM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 設定索引標籤控制項將使用的擴充樣式。 您可以使用 TabCtrl SetExtendedStyle 宏明確地傳送此訊息 \_ 。
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025118"
---
# <a name="tcm_setextendedstyle-message"></a><span data-ttu-id="c6c45-105">TCM \_ SETEXTENDEDSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="c6c45-105">TCM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="c6c45-106">設定索引標籤控制項將使用的擴充樣式。</span><span class="sxs-lookup"><span data-stu-id="c6c45-106">Sets the extended styles that the tab control will use.</span></span> <span data-ttu-id="c6c45-107">您可以使用 [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6c45-107">You can send this message explicitly or by using the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6c45-108">參數</span><span class="sxs-lookup"><span data-stu-id="c6c45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6c45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c45-110">**DWORD** 值，指出要對 *lParam* 中的哪些樣式造成影響。</span><span class="sxs-lookup"><span data-stu-id="c6c45-110">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="c6c45-111">只有 *wParam* 中的擴充樣式會變更。</span><span class="sxs-lookup"><span data-stu-id="c6c45-111">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="c6c45-112">所有其他樣式都會維持不變。</span><span class="sxs-lookup"><span data-stu-id="c6c45-112">All other styles will be maintained as they are.</span></span> <span data-ttu-id="c6c45-113">如果此參數為零，則 *lParam* 中的所有樣式都會受到影響。</span><span class="sxs-lookup"><span data-stu-id="c6c45-113">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="c6c45-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6c45-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c45-115">指定擴充的索引標籤控制項樣式的值。</span><span class="sxs-lookup"><span data-stu-id="c6c45-115">Value specifying the extended tab control styles.</span></span> <span data-ttu-id="c6c45-116">此值為索引標籤控制項 [擴充樣式](tab-control-extended-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="c6c45-116">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c45-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6c45-117">Return value</span></span>

<span data-ttu-id="c6c45-118">傳回包含先前的索引標籤控制項擴充樣式的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="c6c45-118">Returns a **DWORD** value that contains the previous tab control extended styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c45-119">備註</span><span class="sxs-lookup"><span data-stu-id="c6c45-119">Remarks</span></span>

<span data-ttu-id="c6c45-120">*WParam* 參數可讓您修改一或多個擴充樣式，而不需要先取出現有的樣式。</span><span class="sxs-lookup"><span data-stu-id="c6c45-120">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="c6c45-121">例如，如果您傳遞 [**TCS 的 \_ \_ FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* 和0（ *lParam*），將會清除 **TCS \_ EX \_ FLATSEPARATORS** 樣式，但所有其他樣式都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="c6c45-121">For example, if you pass [**TCS\_EX\_FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **TCS\_EX\_FLATSEPARATORS** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="c6c45-122">基於回溯相容性的理由， [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) 宏尚未更新為使用 *dwExMask*。</span><span class="sxs-lookup"><span data-stu-id="c6c45-122">For backward compatibility reasons, the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro has not been updated to use *dwExMask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c45-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6c45-123">Requirements</span></span>



| <span data-ttu-id="c6c45-124">需求</span><span class="sxs-lookup"><span data-stu-id="c6c45-124">Requirement</span></span> | <span data-ttu-id="c6c45-125">值</span><span class="sxs-lookup"><span data-stu-id="c6c45-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c45-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6c45-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c45-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c45-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6c45-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6c45-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c45-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c45-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6c45-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c6c45-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c45-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c45-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c45-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6c45-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c45-133">**TCM \_ GETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="c6c45-133">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
</dt> </dl>

 

 





