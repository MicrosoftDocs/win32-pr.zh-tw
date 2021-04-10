---
title: 'BCM_SETNOTE 訊息 (Commctrl .h) '
description: 設定與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用按鈕 \_ SetNote 宏。
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934364"
---
# <a name="bcm_setnote-message"></a><span data-ttu-id="929e7-105">BCM \_ SETNOTE 訊息</span><span class="sxs-lookup"><span data-stu-id="929e7-105">BCM\_SETNOTE message</span></span>

<span data-ttu-id="929e7-106">設定與命令連結按鈕相關聯的備註文字。</span><span class="sxs-lookup"><span data-stu-id="929e7-106">Sets the text of the note associated with a command link button.</span></span> <span data-ttu-id="929e7-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) 宏。</span><span class="sxs-lookup"><span data-stu-id="929e7-107">You can send this message explicitly or use the [**Button\_SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="929e7-108">參數</span><span class="sxs-lookup"><span data-stu-id="929e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="929e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="929e7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="929e7-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="929e7-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="929e7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="929e7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="929e7-112">包含附注之以 null 終止的 **WCHAR** 字串指標。</span><span class="sxs-lookup"><span data-stu-id="929e7-112">A pointer to a null-terminated **WCHAR** string that contains the note.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="929e7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="929e7-113">Return value</span></span>

<span data-ttu-id="929e7-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="929e7-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="929e7-115">備註</span><span class="sxs-lookup"><span data-stu-id="929e7-115">Remarks</span></span>

<span data-ttu-id="929e7-116">從 comctl32.dll DLL 6.01 版開始，命令連結按鈕可能具有附注。</span><span class="sxs-lookup"><span data-stu-id="929e7-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span>

<span data-ttu-id="929e7-117">[ **BCM \_ SETNOTE** ] 訊息只適用于 [ [**BS \_ COMMANDLINK**](button-styles.md) ] 和 [ [**BS \_ DEFCOMMANDLINK**](button-styles.md) ] 按鈕樣式。</span><span class="sxs-lookup"><span data-stu-id="929e7-117">The **BCM\_SETNOTE** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="929e7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="929e7-118">Requirements</span></span>



| <span data-ttu-id="929e7-119">需求</span><span class="sxs-lookup"><span data-stu-id="929e7-119">Requirement</span></span> | <span data-ttu-id="929e7-120">值</span><span class="sxs-lookup"><span data-stu-id="929e7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="929e7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="929e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="929e7-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="929e7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="929e7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="929e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="929e7-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="929e7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="929e7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="929e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="929e7-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="929e7-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="929e7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="929e7-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="929e7-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="929e7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="929e7-129">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="929e7-129">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="929e7-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="929e7-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="929e7-131">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="929e7-131">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





