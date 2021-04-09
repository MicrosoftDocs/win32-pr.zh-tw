---
title: 'EM_PASTESPECIAL 訊息 (Richedit .h) '
description: 在 rich edit 控制項中貼上特定的剪貼簿格式。
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843816"
---
# <a name="em_pastespecial-message"></a><span data-ttu-id="67c14-104">EM \_ PASTESPECIAL 訊息</span><span class="sxs-lookup"><span data-stu-id="67c14-104">EM\_PASTESPECIAL message</span></span>

<span data-ttu-id="67c14-105">在 rich edit 控制項中貼上特定的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="67c14-105">Pastes a specific clipboard format in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="67c14-106">參數</span><span class="sxs-lookup"><span data-stu-id="67c14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c14-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67c14-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67c14-108">指定 [剪貼簿格式](/windows/desktop/dataxchg/clipboard-formats)。</span><span class="sxs-lookup"><span data-stu-id="67c14-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats).</span></span>

</dd> <dt>

<span data-ttu-id="67c14-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67c14-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67c14-110">[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)結構的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="67c14-110">Pointer to a [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) structure or **NULL**.</span></span> <span data-ttu-id="67c14-111">如果要貼上物件，則會以所需的顯示外觀填入 **REPASTESPECIAL** 結構。</span><span class="sxs-lookup"><span data-stu-id="67c14-111">If an object is being pasted, the **REPASTESPECIAL** structure is filled in with the desired display aspect.</span></span> <span data-ttu-id="67c14-112">如果 *lParam* 為 **Null** 或 **dwAspect** 成員為零，則使用的顯示外觀將會是物件描述項的內容。</span><span class="sxs-lookup"><span data-stu-id="67c14-112">If *lParam* is **NULL** or the **dwAspect** member is zero, the display aspect used will be the contents of the object descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c14-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="67c14-113">Return value</span></span>

<span data-ttu-id="67c14-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="67c14-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c14-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="67c14-115">Requirements</span></span>



| <span data-ttu-id="67c14-116">需求</span><span class="sxs-lookup"><span data-stu-id="67c14-116">Requirement</span></span> | <span data-ttu-id="67c14-117">值</span><span class="sxs-lookup"><span data-stu-id="67c14-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67c14-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67c14-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67c14-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67c14-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67c14-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67c14-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67c14-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67c14-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67c14-122">標頭</span><span class="sxs-lookup"><span data-stu-id="67c14-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c14-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="67c14-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c14-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67c14-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c14-125">**REPASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="67c14-125">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

