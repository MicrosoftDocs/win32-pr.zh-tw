---
title: 'EM_GETTYPOGRAPHYOPTIONS 訊息 (Richedit .h) '
description: 傳回 rich edit 控制項之印刷樣式選項的目前狀態。
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105107"
---
# <a name="em_gettypographyoptions-message"></a><span data-ttu-id="aab5c-104">EM \_ GETTYPOGRAPHYOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="aab5c-104">EM\_GETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="aab5c-105">傳回 rich edit 控制項之印刷樣式選項的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="aab5c-105">Returns the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="aab5c-106">參數</span><span class="sxs-lookup"><span data-stu-id="aab5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab5c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aab5c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aab5c-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="aab5c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aab5c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aab5c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aab5c-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="aab5c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab5c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aab5c-111">Return value</span></span>

<span data-ttu-id="aab5c-112">傳回目前的印刷樣式選項。</span><span class="sxs-lookup"><span data-stu-id="aab5c-112">Returns the current typography options.</span></span> <span data-ttu-id="aab5c-113">如需選項的清單，請參閱 [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)。</span><span class="sxs-lookup"><span data-stu-id="aab5c-113">For a list of options, see [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aab5c-114">備註</span><span class="sxs-lookup"><span data-stu-id="aab5c-114">Remarks</span></span>

<span data-ttu-id="aab5c-115">您可以藉由傳送 [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) 訊息來開啟 advanced line。</span><span class="sxs-lookup"><span data-stu-id="aab5c-115">You can turn on advanced line breaking by sending the [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) message.</span></span> <span data-ttu-id="aab5c-116">Rich edit 控制項（如果特定語言需要的話）也會自動開啟 Advanced 和 normal 分行符號。</span><span class="sxs-lookup"><span data-stu-id="aab5c-116">Advanced and normal line breaking may also be turned on automatically by the rich edit control if it is needed for certain languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab5c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="aab5c-117">Requirements</span></span>



| <span data-ttu-id="aab5c-118">需求</span><span class="sxs-lookup"><span data-stu-id="aab5c-118">Requirement</span></span> | <span data-ttu-id="aab5c-119">值</span><span class="sxs-lookup"><span data-stu-id="aab5c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aab5c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aab5c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aab5c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aab5c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aab5c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aab5c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aab5c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aab5c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aab5c-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="aab5c-124">Redistributable</span></span><br/>          | <span data-ttu-id="aab5c-125">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="aab5c-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="aab5c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="aab5c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab5c-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="aab5c-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab5c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aab5c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="aab5c-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="aab5c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aab5c-130">**EM \_ SETTYPOGRAPHYOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="aab5c-130">**EM\_SETTYPOGRAPHYOPTIONS**</span></span>](em-settypographyoptions.md)
</dt> <dt>

<span data-ttu-id="aab5c-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="aab5c-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aab5c-132">關於 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="aab5c-132">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





