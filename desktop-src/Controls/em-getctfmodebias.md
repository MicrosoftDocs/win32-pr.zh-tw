---
title: 'EM_GETCTFMODEBIAS 訊息 (Richedit .h) '
description: 取得 Microsoft Rich Edit 控制項的文字服務架構模式偏差值。
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104040"
---
# <a name="em_getctfmodebias-message"></a><span data-ttu-id="96806-104">EM \_ GETCTFMODEBIAS 訊息</span><span class="sxs-lookup"><span data-stu-id="96806-104">EM\_GETCTFMODEBIAS message</span></span>

<span data-ttu-id="96806-105">取得 Microsoft Rich Edit 控制項的文字服務架構模式偏差值。</span><span class="sxs-lookup"><span data-stu-id="96806-105">Gets the Text Services Framework mode bias values for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="96806-106">參數</span><span class="sxs-lookup"><span data-stu-id="96806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96806-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96806-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96806-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="96806-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="96806-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96806-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96806-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="96806-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96806-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="96806-111">Return value</span></span>

<span data-ttu-id="96806-112">目前的文字服務架構模式偏差值。</span><span class="sxs-lookup"><span data-stu-id="96806-112">The current Text Services Framework mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96806-113">備註</span><span class="sxs-lookup"><span data-stu-id="96806-113">Remarks</span></span>

<span data-ttu-id="96806-114">若要取得 IME 模式偏差，請呼叫 [**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)。</span><span class="sxs-lookup"><span data-stu-id="96806-114">To get the IME mode bias, call [**EM\_GETIMEMODEBIAS**](em-getimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96806-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="96806-115">Requirements</span></span>



| <span data-ttu-id="96806-116">需求</span><span class="sxs-lookup"><span data-stu-id="96806-116">Requirement</span></span> | <span data-ttu-id="96806-117">值</span><span class="sxs-lookup"><span data-stu-id="96806-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96806-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96806-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96806-119">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96806-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96806-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96806-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96806-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96806-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96806-122">標頭</span><span class="sxs-lookup"><span data-stu-id="96806-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96806-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="96806-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96806-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96806-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="96806-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="96806-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96806-126">**EM \_ SETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="96806-126">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="96806-127">**EM \_ GETIMEMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="96806-127">**EM\_GETIMEMODEBIAS**</span></span>](em-getimemodebias.md)
</dt> </dl>

 

 





