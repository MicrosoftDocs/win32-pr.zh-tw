---
title: 'EM_GETAUTOCORRECTPROC 訊息 (Richedit .h) '
description: 取得應用程式定義之 AutoCorrectProc 函數的指標。
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- EM_GETAUTOCORRECTPROC message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465573"
---
# <a name="em_getautocorrectproc-message"></a><span data-ttu-id="469d2-104">EM \_ GETAUTOCORRECTPROC 訊息</span><span class="sxs-lookup"><span data-stu-id="469d2-104">EM\_GETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="469d2-105">取得應用程式定義之 [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) 函數的指標。</span><span class="sxs-lookup"><span data-stu-id="469d2-105">Gets a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="469d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="469d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="469d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="469d2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="469d2-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="469d2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="469d2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="469d2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="469d2-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="469d2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="469d2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="469d2-111">Return value</span></span>

<span data-ttu-id="469d2-112">傳回應用程式定義 [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) 函式的指標。</span><span class="sxs-lookup"><span data-stu-id="469d2-112">Returns a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="469d2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="469d2-113">Requirements</span></span>



| <span data-ttu-id="469d2-114">需求</span><span class="sxs-lookup"><span data-stu-id="469d2-114">Requirement</span></span> | <span data-ttu-id="469d2-115">值</span><span class="sxs-lookup"><span data-stu-id="469d2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="469d2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="469d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="469d2-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="469d2-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="469d2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="469d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="469d2-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="469d2-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="469d2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="469d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="469d2-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="469d2-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="469d2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="469d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469d2-123">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="469d2-123">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="469d2-124">**EM \_ CALLAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="469d2-124">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="469d2-125">**EM \_ SETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="469d2-125">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





