---
title: 'EM_GETIMECOMPTEXT 訊息 (Richedit .h) '
description: 抓取輸入方法編輯器 (IME) 組合文字。
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934733"
---
# <a name="em_getimecomptext-message"></a><span data-ttu-id="3a234-104">EM \_ GETIMECOMPTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="3a234-104">EM\_GETIMECOMPTEXT message</span></span>

<span data-ttu-id="3a234-105">抓取輸入方法編輯器 (IME) 組合文字。</span><span class="sxs-lookup"><span data-stu-id="3a234-105">Retrieves the Input Method Editor (IME) composition text.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a234-106">參數</span><span class="sxs-lookup"><span data-stu-id="3a234-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a234-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a234-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-108">[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)結構。</span><span class="sxs-lookup"><span data-stu-id="3a234-108">The [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3a234-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a234-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-110">接收組合文字的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3a234-110">The buffer that receives the composition text.</span></span> <span data-ttu-id="3a234-111">這個緩衝區的大小是包含在 *wParam* 結構的 **cb** 成員中。</span><span class="sxs-lookup"><span data-stu-id="3a234-111">The size of this buffer is contained in the **cb** member of the *wParam* structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a234-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a234-112">Return value</span></span>

<span data-ttu-id="3a234-113">如果成功，傳回值就是複製到緩衝區的 Unicode 字元數。</span><span class="sxs-lookup"><span data-stu-id="3a234-113">If successful, the return value is the number of Unicode characters copied to the buffer.</span></span> <span data-ttu-id="3a234-114">否則，它是零。</span><span class="sxs-lookup"><span data-stu-id="3a234-114">Otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a234-115">備註</span><span class="sxs-lookup"><span data-stu-id="3a234-115">Remarks</span></span>

<span data-ttu-id="3a234-116">此訊息只會採用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="3a234-116">This message only takes Unicode strings.</span></span>

<span data-ttu-id="3a234-117">**安全性警告：** 請確定有足夠的緩衝區來滿足輸入的大小。</span><span class="sxs-lookup"><span data-stu-id="3a234-117">**Security Warning:** Be sure to have a buffer sufficient for the size of the input.</span></span> <span data-ttu-id="3a234-118">若未這麼做，可能會導致您的應用程式發生問題。</span><span class="sxs-lookup"><span data-stu-id="3a234-118">Failure to do so could cause problems for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a234-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a234-119">Requirements</span></span>



| <span data-ttu-id="3a234-120">需求</span><span class="sxs-lookup"><span data-stu-id="3a234-120">Requirement</span></span> | <span data-ttu-id="3a234-121">值</span><span class="sxs-lookup"><span data-stu-id="3a234-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a234-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a234-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a234-123">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a234-123">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a234-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a234-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a234-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a234-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a234-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3a234-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a234-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a234-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a234-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a234-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a234-129">**IMECOMPTEXT**</span><span class="sxs-lookup"><span data-stu-id="3a234-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





