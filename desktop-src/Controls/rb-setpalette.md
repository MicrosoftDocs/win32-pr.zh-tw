---
title: 'RB_SETPALETTE 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的目前調色板。
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934705"
---
# <a name="rb_setpalette-message"></a><span data-ttu-id="9c163-104">RB \_ SETPALETTE 訊息</span><span class="sxs-lookup"><span data-stu-id="9c163-104">RB\_SETPALETTE message</span></span>

<span data-ttu-id="9c163-105">設定 Rebar 控制項的目前調色板。</span><span class="sxs-lookup"><span data-stu-id="9c163-105">Sets the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c163-106">參數</span><span class="sxs-lookup"><span data-stu-id="9c163-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c163-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c163-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c163-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9c163-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9c163-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c163-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c163-110">**HPALETTE** ，指定 Rebar 控制項將使用的新調色板。</span><span class="sxs-lookup"><span data-stu-id="9c163-110">An **HPALETTE** that specifies the new palette that the rebar control will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c163-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c163-111">Return value</span></span>

<span data-ttu-id="9c163-112">傳回 **HPALETTE** ，指定 Rebar 控制項先前的調色板。</span><span class="sxs-lookup"><span data-stu-id="9c163-112">Returns an **HPALETTE** that specifies the rebar control's previous palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c163-113">備註</span><span class="sxs-lookup"><span data-stu-id="9c163-113">Remarks</span></span>

<span data-ttu-id="9c163-114">傳送此訊息的應用程式必須負責刪除此訊息中傳遞的 **HPALETTE** (請參閱 [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)) 。</span><span class="sxs-lookup"><span data-stu-id="9c163-114">It is the responsibility of the application sending this message to delete the **HPALETTE** passed in this message (see [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span></span> <span data-ttu-id="9c163-115">Rebar 控制項不會刪除包含此訊息的 **HPALETTE** 集。</span><span class="sxs-lookup"><span data-stu-id="9c163-115">The rebar control will not delete an **HPALETTE** set with this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c163-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c163-116">Requirements</span></span>



| <span data-ttu-id="9c163-117">需求</span><span class="sxs-lookup"><span data-stu-id="9c163-117">Requirement</span></span> | <span data-ttu-id="9c163-118">值</span><span class="sxs-lookup"><span data-stu-id="9c163-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c163-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c163-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c163-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c163-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c163-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c163-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c163-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c163-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c163-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9c163-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c163-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c163-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c163-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c163-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c163-126">**RB \_ GETPALETTE**</span><span class="sxs-lookup"><span data-stu-id="9c163-126">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
</dt> </dl>

 

