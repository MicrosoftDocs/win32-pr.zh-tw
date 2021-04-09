---
title: 'BCM_GETSPLITINFO 訊息 (Commctrl .h) '
description: 取得分割按鈕控制項的資訊。 明確地傳送此訊息，或使用按鈕 \_ GetSplitInfo 宏。
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934452"
---
# <a name="bcm_getsplitinfo-message"></a><span data-ttu-id="805c7-105">BCM \_ GETSPLITINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="805c7-105">BCM\_GETSPLITINFO message</span></span>

<span data-ttu-id="805c7-106">取得分割按鈕控制項的資訊。</span><span class="sxs-lookup"><span data-stu-id="805c7-106">Gets information for a split button control.</span></span> <span data-ttu-id="805c7-107">明確地傳送此訊息，或使用 [**按鈕 \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) 宏。</span><span class="sxs-lookup"><span data-stu-id="805c7-107">Send this message explicitly or by using the [**Button\_GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="805c7-108">參數</span><span class="sxs-lookup"><span data-stu-id="805c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805c7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="805c7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="805c7-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="805c7-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="805c7-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="805c7-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="805c7-112">[**按鈕 \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo)結構的指標，用來接收按鈕的資訊。</span><span class="sxs-lookup"><span data-stu-id="805c7-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure to receive information on the button.</span></span> <span data-ttu-id="805c7-113">呼叫端負責配置結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="805c7-113">The caller is responsible for allocating the memory for the structure.</span></span> <span data-ttu-id="805c7-114">設定此結構的 **遮罩** 成員，以決定要接收的資訊。</span><span class="sxs-lookup"><span data-stu-id="805c7-114">Set the **mask** member of this structure to determine what information to receive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="805c7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="805c7-115">Return value</span></span>

<span data-ttu-id="805c7-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="805c7-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="805c7-117">備註</span><span class="sxs-lookup"><span data-stu-id="805c7-117">Remarks</span></span>

<span data-ttu-id="805c7-118">此訊息只能搭配 [**BS \_ SPLITBUTTON**](button-styles.md) 和 [**BS \_ DEFSPLITBUTTON**](button-styles.md) 按鈕樣式使用。</span><span class="sxs-lookup"><span data-stu-id="805c7-118">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="805c7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="805c7-119">Requirements</span></span>



| <span data-ttu-id="805c7-120">需求</span><span class="sxs-lookup"><span data-stu-id="805c7-120">Requirement</span></span> | <span data-ttu-id="805c7-121">值</span><span class="sxs-lookup"><span data-stu-id="805c7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="805c7-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="805c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="805c7-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="805c7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="805c7-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="805c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="805c7-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="805c7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="805c7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="805c7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="805c7-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="805c7-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805c7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="805c7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="805c7-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="805c7-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="805c7-130">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="805c7-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="805c7-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="805c7-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="805c7-132">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="805c7-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





