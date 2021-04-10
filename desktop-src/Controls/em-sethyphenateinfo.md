---
title: 'EM_SETHYPHENATEINFO 訊息 (Richedit .h) '
description: 設定 rich edit 控制項進行斷字的方式。
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844128"
---
# <a name="em_sethyphenateinfo-message"></a><span data-ttu-id="87686-104">EM \_ SETHYPHENATEINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="87686-104">EM\_SETHYPHENATEINFO message</span></span>

<span data-ttu-id="87686-105">設定 rich edit 控制項進行斷字的方式。</span><span class="sxs-lookup"><span data-stu-id="87686-105">Sets the way a rich edit control does hyphenation.</span></span>

## <a name="parameters"></a><span data-ttu-id="87686-106">參數</span><span class="sxs-lookup"><span data-stu-id="87686-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87686-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87686-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87686-108">[**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="87686-108">Pointer to a [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="87686-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87686-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87686-110">未使用，必須為零。</span><span class="sxs-lookup"><span data-stu-id="87686-110">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87686-111">備註</span><span class="sxs-lookup"><span data-stu-id="87686-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87686-112">若要啟用斷字功能，用戶端必須呼叫 [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)，並指定 \_ ADVANCEDTYPOGRAPHY。</span><span class="sxs-lookup"><span data-stu-id="87686-112">To enable hyphenation, the client must call [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specifying TO\_ADVANCEDTYPOGRAPHY.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87686-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="87686-113">Requirements</span></span>



| <span data-ttu-id="87686-114">需求</span><span class="sxs-lookup"><span data-stu-id="87686-114">Requirement</span></span> | <span data-ttu-id="87686-115">值</span><span class="sxs-lookup"><span data-stu-id="87686-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87686-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87686-116">Minimum supported client</span></span><br/> | <span data-ttu-id="87686-117">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87686-117">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87686-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87686-118">Minimum supported server</span></span><br/> | <span data-ttu-id="87686-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87686-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87686-120">標頭</span><span class="sxs-lookup"><span data-stu-id="87686-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="87686-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="87686-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87686-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87686-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87686-123">**EM \_ GETHYPHENATEINFO**</span><span class="sxs-lookup"><span data-stu-id="87686-123">**EM\_GETHYPHENATEINFO**</span></span>](em-gethyphenateinfo.md)
</dt> </dl>

 

 





