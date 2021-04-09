---
title: 'EM_SETWORDBREAKPROCEX 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的擴充字組分隔程式。
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- EM_SETWORDBREAKPROCEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934206"
---
# <a name="em_setwordbreakprocex-message"></a><span data-ttu-id="ef151-104">EM \_ SETWORDBREAKPROCEX 訊息</span><span class="sxs-lookup"><span data-stu-id="ef151-104">EM\_SETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="ef151-105">設定 rich edit 控制項的擴充字組分隔程式。</span><span class="sxs-lookup"><span data-stu-id="ef151-105">Sets the extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef151-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef151-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef151-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef151-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef151-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="ef151-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ef151-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef151-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef151-110">[*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)函式的指標，或為 **Null** 以使用預設程式。</span><span class="sxs-lookup"><span data-stu-id="ef151-110">Pointer to an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function, or **NULL** to use the default procedure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef151-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef151-111">Return value</span></span>

<span data-ttu-id="ef151-112">此訊息會傳回先前擴充的斷詞程式位址。</span><span class="sxs-lookup"><span data-stu-id="ef151-112">This message returns the address of the previous extended word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef151-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef151-113">Requirements</span></span>



| <span data-ttu-id="ef151-114">需求</span><span class="sxs-lookup"><span data-stu-id="ef151-114">Requirement</span></span> | <span data-ttu-id="ef151-115">值</span><span class="sxs-lookup"><span data-stu-id="ef151-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef151-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef151-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef151-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef151-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef151-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef151-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef151-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef151-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef151-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ef151-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef151-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef151-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef151-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef151-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef151-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="ef151-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ef151-124">**EditWordBreakProcEx**</span><span class="sxs-lookup"><span data-stu-id="ef151-124">**EditWordBreakProcEx**</span></span>](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[<span data-ttu-id="ef151-125">**EM \_ GETWORDBREAKPROCEX**</span><span class="sxs-lookup"><span data-stu-id="ef151-125">**EM\_GETWORDBREAKPROCEX**</span></span>](em-getwordbreakprocex.md)
</dt> </dl>

 

 





