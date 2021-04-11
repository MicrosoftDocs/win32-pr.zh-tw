---
title: 'TB_INSERTBUTTON 訊息 (Commctrl .h) '
description: 在工具列中插入按鈕。
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094291"
---
# <a name="tb_insertbutton-message"></a><span data-ttu-id="f56b8-104">TB \_ INSERTBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="f56b8-104">TB\_INSERTBUTTON message</span></span>

<span data-ttu-id="f56b8-105">在工具列中插入按鈕。</span><span class="sxs-lookup"><span data-stu-id="f56b8-105">Inserts a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f56b8-106">參數</span><span class="sxs-lookup"><span data-stu-id="f56b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f56b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f56b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f56b8-108">以零為基底的按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="f56b8-108">Zero-based index of a button.</span></span> <span data-ttu-id="f56b8-109">訊息會將新按鈕插入此按鈕的左邊。</span><span class="sxs-lookup"><span data-stu-id="f56b8-109">The message inserts the new button to the left of this button.</span></span>

</dd> <dt>

<span data-ttu-id="f56b8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f56b8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f56b8-111">[**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的指標，其中包含要插入之按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f56b8-111">Pointer to a [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure containing information about the button to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f56b8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f56b8-112">Return value</span></span>

<span data-ttu-id="f56b8-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f56b8-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f56b8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f56b8-114">Requirements</span></span>



| <span data-ttu-id="f56b8-115">需求</span><span class="sxs-lookup"><span data-stu-id="f56b8-115">Requirement</span></span> | <span data-ttu-id="f56b8-116">值</span><span class="sxs-lookup"><span data-stu-id="f56b8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f56b8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f56b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f56b8-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f56b8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f56b8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f56b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f56b8-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f56b8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f56b8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f56b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f56b8-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f56b8-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f56b8-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f56b8-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f56b8-124">**TB \_INSERTBUTTONW** (Unicode) 和 **TB \_ INSERTBUTTONA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f56b8-124">**TB\_INSERTBUTTONW** (Unicode) and **TB\_INSERTBUTTONA** (ANSI)</span></span><br/>           |



 

 





