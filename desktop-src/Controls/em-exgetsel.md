---
title: 'EM_EXGETSEL 訊息 (Richedit .h) '
description: 在 rich edit 控制項中，抓取選取範圍的開始和結束字元位置。
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- EM_EXGETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465893"
---
# <a name="em_exgetsel-message"></a><span data-ttu-id="092fe-104">EM \_ EXGETSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="092fe-104">EM\_EXGETSEL message</span></span>

<span data-ttu-id="092fe-105">在 rich edit 控制項中，抓取選取範圍的開始和結束字元位置。</span><span class="sxs-lookup"><span data-stu-id="092fe-105">Retrieves the starting and ending character positions of the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="092fe-106">參數</span><span class="sxs-lookup"><span data-stu-id="092fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="092fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="092fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="092fe-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="092fe-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="092fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="092fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="092fe-110">接收選取範圍的 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) 結構。</span><span class="sxs-lookup"><span data-stu-id="092fe-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that receives the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="092fe-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="092fe-111">Return value</span></span>

<span data-ttu-id="092fe-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="092fe-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="092fe-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="092fe-113">Requirements</span></span>



| <span data-ttu-id="092fe-114">需求</span><span class="sxs-lookup"><span data-stu-id="092fe-114">Requirement</span></span> | <span data-ttu-id="092fe-115">值</span><span class="sxs-lookup"><span data-stu-id="092fe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="092fe-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="092fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="092fe-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="092fe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="092fe-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="092fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="092fe-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="092fe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="092fe-120">標頭</span><span class="sxs-lookup"><span data-stu-id="092fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="092fe-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="092fe-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="092fe-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="092fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="092fe-123">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="092fe-123">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





