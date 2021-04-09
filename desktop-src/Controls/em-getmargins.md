---
title: 'EM_GETMARGINS 訊息 (Winuser .h) '
description: 取得編輯控制項左邊界和右邊界的寬度。
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- EM_GETMARGINS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685607"
---
# <a name="em_getmargins-message"></a><span data-ttu-id="7df86-104">EM \_ GETMARGINS 訊息</span><span class="sxs-lookup"><span data-stu-id="7df86-104">EM\_GETMARGINS message</span></span>

<span data-ttu-id="7df86-105">取得編輯控制項左邊界和右邊界的寬度。</span><span class="sxs-lookup"><span data-stu-id="7df86-105">Gets the widths of the left and right margins for an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7df86-106">參數</span><span class="sxs-lookup"><span data-stu-id="7df86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df86-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7df86-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7df86-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="7df86-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7df86-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7df86-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7df86-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="7df86-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df86-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7df86-111">Return value</span></span>

<span data-ttu-id="7df86-112">傳回 LOWORD 中左邊界的寬度，以及 HIWORD 中右邊界的寬度。</span><span class="sxs-lookup"><span data-stu-id="7df86-112">Returns the width of the left margin in the LOWORD, and the width of the right margin in the HIWORD.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df86-113">備註</span><span class="sxs-lookup"><span data-stu-id="7df86-113">Remarks</span></span>

<span data-ttu-id="7df86-114">**Rich Edit：** 不支援 **EM \_ GETMARGINS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="7df86-114">**Rich Edit:** The **EM\_GETMARGINS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df86-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7df86-115">Requirements</span></span>



| <span data-ttu-id="7df86-116">需求</span><span class="sxs-lookup"><span data-stu-id="7df86-116">Requirement</span></span> | <span data-ttu-id="7df86-117">值</span><span class="sxs-lookup"><span data-stu-id="7df86-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df86-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7df86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7df86-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7df86-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7df86-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7df86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7df86-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7df86-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7df86-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7df86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7df86-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7df86-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df86-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7df86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df86-125">**EM \_ SETMARGINS**</span><span class="sxs-lookup"><span data-stu-id="7df86-125">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
</dt> </dl>

 

 





