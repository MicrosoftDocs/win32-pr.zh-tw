---
title: 'EM_SETAUTOCORRECTPROC 訊息 (Richedit .h) '
description: 定義目前的自動校正回呼程式。
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- EM_SETAUTOCORRECTPROC message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466557"
---
# <a name="em_setautocorrectproc-message"></a><span data-ttu-id="c7f7b-104">EM \_ SETAUTOCORRECTPROC 訊息</span><span class="sxs-lookup"><span data-stu-id="c7f7b-104">EM\_SETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="c7f7b-105">定義目前的自動校正回呼程式。</span><span class="sxs-lookup"><span data-stu-id="c7f7b-105">Defines the current autocorrect callback procedure.</span></span>


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a><span data-ttu-id="c7f7b-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7f7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f7b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7f7b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7f7b-108">[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c7f7b-108">The [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c7f7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7f7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7f7b-110">未使用;必須為零</span><span class="sxs-lookup"><span data-stu-id="c7f7b-110">Not used; must be zero</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7f7b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7f7b-111">Return value</span></span>

<span data-ttu-id="c7f7b-112">如果作業成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="c7f7b-112">If the operation succeeds, the return value is zero.</span></span> <span data-ttu-id="c7f7b-113">如果作業失敗，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="c7f7b-113">If the operation fails, the return value is a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7f7b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7f7b-114">Requirements</span></span>



| <span data-ttu-id="c7f7b-115">需求</span><span class="sxs-lookup"><span data-stu-id="c7f7b-115">Requirement</span></span> | <span data-ttu-id="c7f7b-116">值</span><span class="sxs-lookup"><span data-stu-id="c7f7b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f7b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7f7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f7b-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7f7b-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c7f7b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7f7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f7b-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7f7b-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7f7b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c7f7b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7f7b-122"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7f7b-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f7b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7f7b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f7b-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="c7f7b-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="c7f7b-125">**EM \_ CALLAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="c7f7b-125">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="c7f7b-126">**EM \_ GETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="c7f7b-126">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> </dl>

 

 





