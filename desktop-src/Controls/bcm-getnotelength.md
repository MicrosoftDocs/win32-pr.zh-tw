---
title: 'BCM_GETNOTELENGTH 訊息 (Commctrl .h) '
description: 取得可在 [命令連結] 按鈕的 [描述] 中顯示的附注文字長度。 明確地傳送此訊息，或使用按鈕 \_ GetNoteLength 宏。
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024999"
---
# <a name="bcm_getnotelength-message"></a><span data-ttu-id="6df22-105">BCM \_ GETNOTELENGTH 訊息</span><span class="sxs-lookup"><span data-stu-id="6df22-105">BCM\_GETNOTELENGTH message</span></span>

<span data-ttu-id="6df22-106">取得可在 [命令連結] 按鈕的 [描述] 中顯示的附注文字長度。</span><span class="sxs-lookup"><span data-stu-id="6df22-106">Gets the length of the note text that may be displayed in the description for a command link button.</span></span> <span data-ttu-id="6df22-107">明確地傳送此訊息，或使用 [**按鈕 \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) 宏。</span><span class="sxs-lookup"><span data-stu-id="6df22-107">Send this message explicitly or by using the [**Button\_GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6df22-108">參數</span><span class="sxs-lookup"><span data-stu-id="6df22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df22-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6df22-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6df22-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6df22-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6df22-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6df22-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6df22-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6df22-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df22-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6df22-113">Return value</span></span>

<span data-ttu-id="6df22-114">傳回 **WCHARs** 中的附注文字長度，不包括任何結束的 **Null**，或如果沒有附注文字，則為零。</span><span class="sxs-lookup"><span data-stu-id="6df22-114">Returns the length of the note text in **WCHARs**, not including any terminating **NULL**, or zero if there is no note text.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df22-115">備註</span><span class="sxs-lookup"><span data-stu-id="6df22-115">Remarks</span></span>

<span data-ttu-id="6df22-116">從 comctl32.dll DLL 6.01 版開始，命令連結按鈕可能具有附注。</span><span class="sxs-lookup"><span data-stu-id="6df22-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span> <span data-ttu-id="6df22-117">如需 DLL 版本的詳細資訊，請參閱 [通用控制項版本](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="6df22-117">For information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="6df22-118">[ **BCM \_ GETNOTELENGTH** ] 訊息只適用于 [ [**BS \_ COMMANDLINK**](button-styles.md) ] 和 [ [**BS \_ DEFCOMMANDLINK**](button-styles.md) ] 按鈕樣式。</span><span class="sxs-lookup"><span data-stu-id="6df22-118">The **BCM\_GETNOTELENGTH** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df22-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6df22-119">Requirements</span></span>



| <span data-ttu-id="6df22-120">需求</span><span class="sxs-lookup"><span data-stu-id="6df22-120">Requirement</span></span> | <span data-ttu-id="6df22-121">值</span><span class="sxs-lookup"><span data-stu-id="6df22-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6df22-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6df22-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6df22-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6df22-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6df22-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6df22-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6df22-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6df22-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6df22-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6df22-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df22-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6df22-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df22-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6df22-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6df22-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="6df22-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6df22-130">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="6df22-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="6df22-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="6df22-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6df22-132">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="6df22-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





