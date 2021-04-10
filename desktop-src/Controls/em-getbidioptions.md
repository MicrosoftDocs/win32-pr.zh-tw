---
title: 'EM_GETBIDIOPTIONS 訊息 (Richedit .h) '
description: 指出 rich edit 控制項中雙向選項的目前狀態。
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104046"
---
# <a name="em_getbidioptions-message"></a><span data-ttu-id="4fd42-104">EM \_ GETBIDIOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="4fd42-104">EM\_GETBIDIOPTIONS message</span></span>

<span data-ttu-id="4fd42-105">指出 rich edit 控制項中雙向選項的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4fd42-105">Indicates the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4fd42-106">參數</span><span class="sxs-lookup"><span data-stu-id="4fd42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd42-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fd42-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd42-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="4fd42-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4fd42-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fd42-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd42-110">[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)結構，此結構會接收 rich edit 控制項中雙向選項的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4fd42-110">A [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that receives the current state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fd42-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fd42-111">Return value</span></span>

<span data-ttu-id="4fd42-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4fd42-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd42-113">備註</span><span class="sxs-lookup"><span data-stu-id="4fd42-113">Remarks</span></span>

<span data-ttu-id="4fd42-114">這則訊息會將 **wMask** 和 **wEffects** 成員的值設定為 rich edit 控制項中雙向選項目前狀態的值。</span><span class="sxs-lookup"><span data-stu-id="4fd42-114">This message sets the values of the **wMask** and **wEffects** members to the value of the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fd42-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fd42-115">Requirements</span></span>



| <span data-ttu-id="4fd42-116">需求</span><span class="sxs-lookup"><span data-stu-id="4fd42-116">Requirement</span></span> | <span data-ttu-id="4fd42-117">值</span><span class="sxs-lookup"><span data-stu-id="4fd42-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd42-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fd42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd42-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fd42-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4fd42-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fd42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd42-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fd42-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4fd42-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4fd42-122">Redistributable</span></span><br/>          | <span data-ttu-id="4fd42-123">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="4fd42-123">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="4fd42-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4fd42-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fd42-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4fd42-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fd42-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fd42-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="4fd42-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="4fd42-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4fd42-128">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="4fd42-128">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="4fd42-129">**EM \_ SETBIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="4fd42-129">**EM\_SETBIDIOPTIONS**</span></span>](em-setbidioptions.md)
</dt> </dl>

 

 





