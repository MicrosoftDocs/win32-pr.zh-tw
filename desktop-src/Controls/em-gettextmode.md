---
title: 'EM_GETTEXTMODE 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的目前文字模式和復原層級。
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- EM_GETTEXTMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466240"
---
# <a name="em_gettextmode-message"></a><span data-ttu-id="dce36-104">EM \_ GETTEXTMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="dce36-104">EM\_GETTEXTMODE message</span></span>

<span data-ttu-id="dce36-105">取得 rich edit 控制項的目前文字模式和復原層級。</span><span class="sxs-lookup"><span data-stu-id="dce36-105">Gets the current text mode and undo level of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dce36-106">參數</span><span class="sxs-lookup"><span data-stu-id="dce36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce36-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dce36-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dce36-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="dce36-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dce36-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dce36-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dce36-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="dce36-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce36-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dce36-111">Return value</span></span>

<span data-ttu-id="dce36-112">傳回值是 [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) 列舉型別中的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="dce36-112">The return value is one or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="dce36-113">這些值表示控制項目前的文字模式和復原層級。</span><span class="sxs-lookup"><span data-stu-id="dce36-113">The values indicate the current text mode and undo level of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce36-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="dce36-114">Requirements</span></span>



| <span data-ttu-id="dce36-115">需求</span><span class="sxs-lookup"><span data-stu-id="dce36-115">Requirement</span></span> | <span data-ttu-id="dce36-116">值</span><span class="sxs-lookup"><span data-stu-id="dce36-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dce36-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dce36-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dce36-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce36-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dce36-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dce36-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dce36-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce36-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dce36-121">標頭</span><span class="sxs-lookup"><span data-stu-id="dce36-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce36-122"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="dce36-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce36-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dce36-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="dce36-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="dce36-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dce36-125">**EM \_ SETTEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="dce36-125">**EM\_SETTEXTMODE**</span></span>](em-settextmode.md)
</dt> <dt>

[<span data-ttu-id="dce36-126">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="dce36-126">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





